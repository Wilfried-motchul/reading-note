# Heroku Deployment

Error pages are not what typically appear on your screen when you're surfing the web, but when it happens it's so annoying! To see how servers work from within, we will build a simple web server by ourselves. We will use Node.js as a server part technology for that task. Then we'll use Heroku cloud application platform to turn this local server into a world wide server.

## Why should I?

Hi, everyone! Don't know how about you, but my weekend was great!

Friday evening. I came home from work, fed my cat, grabbed some pizza, and wanted to have some fun. What could be funnier than good old movies? Nothing, right? So, I went to "IMDB Top 500" to choose one. Then this happened:

And I had to choose my evening movie randomly. It was "Sharknado". Should I say that my Friday was ruined?

To be honest, this is not what typically happens when you are surfing the web. But when it does... Man, it's so annoying! It's annoying, but we're curious, aren't we? And, for our curiosity to be satisfied, we will build a simple web server by ourselves. It will help us to see how it works (or how it won’t work) from within.

Pretty simple, but it's a server!
First of all, we need to create a JavaScript file. Let's name it server.js:

server.js

```
var http = require("http");

http.createServer(function(request, response) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  response.write("It's alive!");
  response.end();
}).listen(3000);
```

Create your project directory. And then create the server.js file inside of it.

First of all, let's declare some variables:

```
var http = require("http"); 
var fs = require("fs");
var path = require("path");
var mime = require("mime");

```
The first one will give you the key to Node's HTTP functionality. The second one is for possibility to interact with the file system. The third one allows you to handle file paths. The last one allows you to determine a file's MIME-type. And it's not a part of Node.js, so we need to install third-party dependencies before using it. We need to create the package.json file for that purpose. It will contain project related information, such as name, version, description, and so on. For our project we will use MIME-types recognition, because it's not enough to just send the contents of a file when you use HTTP. You also need to set the Content-Type header with proper MIME-type. That's why we need this plug-in.

Create the package.json file and fill it with proper information. Here's mine:

package.json
```
{
  "name" : "blog",
  "version" : "0.0.1",
  "description" : "My minimalistic blog",
  "dependencies" : {
    "mime" : "~1.2.7"
  }
}
```
There are "name", "version", "description", and "dependencies" fields in it. The syntax is simple, as you can see. We added our "mime" plug-in and now it's time to download it. We'll use built-in Node Package Manager. Just run:

`npm install`

It will create node_modules folder and place all the files inside of it. So, we resolve our dependencies and can return to our code.

We will now create send404() function. It will handle the sending of 404 error, which usually appears when requested file doesn't exist:

```
function send404(response) {
  response.writeHead(404, {"Content-type" : "text/plain"});
  response.write("Error 404: resource not found");
  response.end();
}

```
Nothing sophisticated with this one. It returns plain text when server can't find a page.

Now we will define sendPage() function. It first writes the header and then sends the contents of the file:

```
function sendPage(response, filePath, fileContents) {
  response.writeHead(200, {"Content-type" : mime.lookup(path.basename(filePath))});
  response.end(fileContents);
}

```
Notice the way we handle the MIME-types.

Now we'll define how our server will handle responses. This function will return the content of the requested file or the 404 error otherwise:

```
handler.js
function serverWorking(response, absPath) {
  fs.exists(absPath, function(exists) {
    if (exists) {
      fs.readFile(absPath, function(err, data) {
        if (err) {
          send404(response)
        } else {
          sendPage(response, absPath, data);
        }
      });
    } else {
      send404(response);
    }
  });
}
And now it's time to create the HTTP server:

create-server.js
var server = http.createServer(function(request, response) {
  var filePath = false;

  if (request.url == '/') {
    filePath = "public/index.html";
  } else {
    filePath = "public" + request.url;
  }

  var absPath = "./" + filePath;
  serverWorking(response, absPath);
});
```

Now we need to start our server. And here's the tricky part. Do you remember how we told the server to listen to the 3000th port in our first example? No? I'll remind you:

``
http.createServer(<some code here>).listen(3000)
``

We can do it when we run our server locally. But Heroku sets a dynamically assigned port number to your app. That's why we need to handle all this mess with ports as it’s shown below:

``
var port_number = server.listen(process.env.PORT || 3000);
``

You can use the port_number variable later. For example, in console.log() function to tell the user, which port is used. This is your homework for tomorrow.

That's all we need to run our simple web server. Now it's time to create some content. We'll create the public folder and two folders inside of it: stylesheets and images. We'll put all our HTML files into the public folder.The stylesheets folder is for CSS files. And the images one is for pictures.

We need to create the index.html file. It will determine our blog's exterior. Here's the code:

index.html
```
<!DOCTYPE html>
<html>
    <head>
        <title>Blog</title>
        <link rel="stylesheet" type="text/css" href="stylesheets/style.css">
    </head>
    <body>
        <div id="header">
            <span>My Simple Blog</span>
            <ul id="menu">
                <li>ABOUT</li>
                <li>ARTICLES</li>
                <li>VIDEOS</li>
                <li>SUBSCRIBE</li>
            </ul>
        </div>
        <div id="content">
            <h2><a href="ui_libraries_comparison.html">JavaScript UI libraries comparison</a></h2>
            <p>It seems to be pretty easy to create a good-looking web page. Even your neighbor has one or two of them. It's for sure! For approximately two decades of World Wide Web existence hordes of web developers are trying to improve the way of how you interact with the Global Network. And how it interacts with you through different technologies such as JavaScript, for example... <a class="article" href="ui_libraries_comparison.html">Read more</a></p>
            <h2><a href="">Node.js for beginners. Building your own web server</a></h2>
            <p>We will use Node.js for our project. Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run within the Node.js runtime on any platform. First of all, of course, you need to install it... <a class="article" href="hode.html">Read more</a></p>
        </div>
    </body>
</html>
```