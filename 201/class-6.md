# OBJECTS LITERALS

## What is an object?
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.

#### In an object: variable Become known as properties

If a variable is part of an object, it is called a property.

#### In an object: Function become known as methods
If a function is part of an object, it is called a method.


#### Sample of an abject
this object will have 5 propreties and 1 method: 

```
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  gym: true,
  roomTypes: ['twin', 'double', 'suite'],
  checkAvailability: fuction(){
    return this.rooms - this.booked;
  }
};
```

as we can see, an objcet can have propreties and each of those propreties as a key and a value 


### Creating objects using literal notation

This example starts by creating an object using literal notation.
This object is called hotel which represents a hotel called Quay with 40 rooms (25 of which have been booked).
Next, the content of the page
is updated with data from this object. It shows the name of the hotel by accessing the object's name property and the number of vacant rooms using the `checkAvailability()` method.
To access a property of this object, the object name is followed by a dot (the period symbol) and the name of the property that you want.
Similarly, to use the method, you can use the object name followed by the method name. `hotel.checkAvailability()`
If the method needs parameters, you can supply them in the parentheses (just like you can pass arguments to a function).

#### sample

```
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  gym: true,
  roomTypes: ['twin', 'double', 'suite'],
  checkAvailability: fuction(){
    return this.rooms - this.booked;
  }
};

var elName = document.getElementById('hotel Name');
elName.textContent = hotel.name;

var elRooms = document.getElementById('rooms');
elRooms.textContent = hotel.checkAvailability();
```


# Document Object Mode

The Document Object Model (DOM) specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the contents of a web page while it is in the browser window.


The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas:

#### MAKING A MODEL OF THE HTML PAGE
When the browser loads a web page, it creates a model of the page in memory.

The DOM specifies the way in which the browser should structure this model using a DOM tree.

The DOM is called an object model because the model (the DOM tree) is made of objects.

Each object represents a different part of the page loaded in the browser window.


#### ACCESSING AND CHANGING THE HTML PAGE

The DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser.

You will hear people call the DOM an 1 Application Programming Interface (API).
User interfaces let humans interact with
programs; APls let programs (and scripts)
talk to each other. The DOM states what your script can "ask the browser about the current page, and how to tell the browser to update what is being shown to the user.

### THE DOM TREE IS A MODEL OF A WEB PAGE

As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes.

#### BODY OF HTML PAGE

```

<html>
  <body>
    <div id="page">
      <hl id="header">List</hl> 
      <h2>Buy groceries</h2>
      <ul>
        <li id="one" class="hot"><em>fresh</em> figs</li> 
        <li id="two" class="hot">pine nuts</li>
        <li id="three" class="hot">honey</li>
        <li id="four">balsamic vinegar</li>
      </ ul >
      <script src="js/list.js"></script> 
    </ div>
  </ body> 
</ html >

```