# IMAGES

## Adding images

### `<img>`
To add an image into the page you need to use an `<img>` element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:

#### src

This tells the browser where
it can find the image file. This will usually be a relative URL pointing to an image on your own site. (Here you can see that the images are in a child folder called images — relative URLs

#### alt
This provides a text description of the image which describes the image if you cannot see it.

#### title
You can also use the title attribute with the `<img>` element to provide additional information about the image. Most browsers will display the content of this attribute in a tootip when the user hovers over the image.

#### Sample
```
<img src="images/quokka.jpg" alt="A family of quokka" title="The quokka is an Australian marsupial that is similar in size to the domestic cat." />
```


## Height & width of the images

You will also often see an `<img>` element use two other attributes that specify its size:

#### height
This specifies the height of the image in pixels.

#### width

This specifies the width of the image in pixels.

#### Sample

```
<img src="images/quokka.jpg" alt="A family of quokka" width="600" height="450" />
```


## Aligning images horizontally

#### align 
The align attribute was commonly used to indicate how the other parts of a page should flow around an image. It has been removed from HTML5
and new websites should use CSS to control the alignment of images.

The align attribute can take these horizontal values:

#### left
This aligns the image to the left (allowing text to flow around its right-hand side).

#### right 

This aligns the image to the right (allowing text to flow around its left-hand side).


#### Sample
```
<p><img src="images/bird.gif" alt="Bird" width="100" height="100" align="left" />There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="right" />There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform 
```


### Aligning images vertucally

There are three values that the align attribute can take that control how the image should align vertically with the text that surrounds it:

#### top
This aligns the first line of the surrounding text with the top of the image.

#### middle 
This aligns the first line of the surrounding text with the middle of the image.

#### bottom
This aligns the first line of the surrounding text with the bottom of the image.tom


#### Sample

```
<p><img src="images/bird.gif" alt="Bird" width="100" height="100" align="top" />There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="middle" />There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="bottom" />There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
```




# COLOR


### FORGROUND COLOR  (color)

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

#### rgb values

These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)

#### hex Codes
These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80

#### Color names
There are 147 predefined color names that are recognized
by browsers. For example: DarkCyan

#### Sample

```
/* color name */
h1 {
  color: DarkCyan;}
/* hex code */
h2 {
  color: #ee3e80;}
/* rgb value */
p{
color: rgb(100,100,90);}
```


 Above each CSS rule in this example you can see how CSS allows you to add comments to your CSS files. Anything between the /* symbols and the */ symbols will not be interpreted by the browser. They are shown in grey above.


 ### FORGROUND COLOR (backgound-color)

 CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.


 #### Sample
 
```
body {
background-color: rgb(200,200,200);}
h1 {
background-color: DarkCyan;}
h2 {
background-color: #ee3e80;}
p{
background-color: white;}
 ```

### OPACITY

CSS3 introduces the opacity property which allows you to specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0 (so a value of 0.5
is 50% opacity and 0.15 is 15% opacity).

#### Sample 

```
p.one {
background-color: rgb(0,0,0); opacity: 0.5;}
p.two {
background-color: rgb(0,0,0); background-color: rgba(0,0,0,0.5);}
```

### HSL & HSLA (hsl, hsla)


The hsl color property has been introduced in CSS3 as an alternative way to specify colors. The value of the property starts with the letters hsl, followed
by individual values inside parentheses for:

#### HUE

This is expressed as an angle (between 0 and 360 degrees).

#### SATURATION 
This is expressed as a percentage.

#### LIGHTNESS
This is expressed as a percentage with 0% being white, 50% being normal, and 100% being black.

The hsla color property allows you to specify color properties using hue, saturation, and lightness as above, and adds a fourth value which represents transparency (just like the rgba property). The a stands for:

#### ALPHA 

This is expressed as a number between 0 and 1.0. For example, 0.5 represents 50% transparency, and 0.75 represents 75% transparency.


#### Sample

```
body {
background-color: #C8C8C8; background-color: hsl(0,0%,78%);}
p{
background-color: #ffffff; background-color: hsla(0,100%,100%,0.5);}
```


# TEXT

### font-family

The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.
The value of this property is the name of the typeface you want to use.

#### Sample 

```
<!DOCTYPE html>
<html>
<head>
<title>Font Family</title> <style type="text/css">
body {
font-family: Georgia, Times, serif;}
h1, h2 {
font-family: Arial, Verdana, sans-serif;}
.credits {
font-family: "Courier New", Courier,
monospace;}
    </style>
  </head>
<body>
<h1>Briards</h1>
<p class="credits">by Ivy Duckett</p> <p class="intro">The <a class="breed"
href="http://en.wikipedia.org/wiki/ Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep...</p>
  </body>
</html>
```