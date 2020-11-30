# IMAGES

## caortnItcrloellIng sIzes of Images In css

You can control the size of an image using the width and height properties in CSS, just like you can for any other box.

Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.

You might think that your site
is likely to have images of all different sizes, but a lot of sites use the same sized image across many of their pages.

For example, an e-commerce site tends to show product photos
at the same size. Or, if your site is designed on a grid, then you might have a selection of image sizes that are commonly used on all pages, such as:

* Small portrait: 220 x 360 
* Small landscape: 330 x 210 
* Feature photo: 620 x 400

Whenever you use consistently sized images across a site,
you can use CSS to control
the dimensions of the
images, instead of putting the dimensions in the HTML.

### Smaple
```
(HTML)
<img src="images/magnolia-large.jpg" 
  class="large" alt="Magnolia" />
<img src="images/magnolia-medium.jpg" 
  class="medium" alt="Magnolia" />
<img src="images/magnolia-small.jpg" 
  class="small" alt="Magnolia" />

(CSS)
img.large {
   width: 500px; height: 500px;}
img.medium { 
  width: 250px; height: 250px;}
img.small { 
  width: 100px; height: 100px;}

```

First you need to determine the sizes of images that will be used commonly throughout the site, then give each size a name.

For example: <br>
> * small 
> * medium 
> * large

Where the `<img>` elements appear in the HTML, rather than using width and height attributes you can use these names as values for the class attribute.

In the CSS, you add selectors for each of the class names, then use the CSS width and height properties to control the image dimensions.


## alrItgIcnlIneg Images UsIng css

We saw how the float property can be used to move an element to the left or the right of its containing block, allowing text to flow around it.

Rather than using the `<img>` element's align attribute, web page authors are increasingly using the float property to align images. There are two ways that this is commonly achieved:

1: The float property is added to the class that was created to represent the size of the image (such as the small class in our example).

2: New classes are created with names such as align-left or align-right to align the images to the left or right of the page. These class names are used in addition to classes that indicate the size of the image.

In this example you can see the align-left and align-right classes used to align the image.

It is also common to add a margin to the image to ensure that the text does not touch their edges.

### Sample

```
(HTML)
<p><img src="images/magnolia-medium.jpg"
  alt="Magnolia" class="align-left medium" /> <b><i>Magnolia</i></b> is a large genus that contains over 200 flowering plant species...
</p>
<p><img src="images/magnolia-medium.jpg" 
  alt="Magnolia" class="align-right medium"/> 
  Some magnolias, such as <i>Magnolia stellata</i> and <i>Magnolia soulangeana</i>, flower quite early in the spring before the leaves open...
</p>

(CSS)
img.align-left { 
  float: left; 
  margin-right: 10px;}
img.align-right { 
  float: right; 
  margin-left: 10px;}
img.medium { 
  width: 250px; 
  height: 250px;}

```
## centerIngaImrtaIgceles UsIng css

By default, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a block- level element using the display property with a value of block.

Once it has been made into a block-level element, there are two common ways in which you can horizontally center an image:

1: On the containing element, you can use the text-align property with a value of center.

2: On the image itself, you can use the use the margin property and set the values of the left and right margins to auto.

You can specify class names that allow any element to be centered, in the same way that you can for the dimensions or alignment of images.

The techniques for specifying image size and alignment of images can also be used with the HTML5 `<figure>` element.

### Sample

```
(HTML)
<p><img src="images/magnolia-medium.jpg"
   alt="Magnolia" class="align-center medium" />
  <b><i>Magnolia</i></b> is a large genus that contains over 200 flowering plant species. It
  is named after French botanist Pierre Magnol and, having evolved before bees appeared, the
  flowers were developed to encourage pollination by beetle.</p>

(CSS)
img.align-center { 
  display: block; 
  margin: 0px auto;}
img.medium { 
  width: 250px; 
  height: 250px;}

``` 
<br>


# PRACTICAL INFORMATION

## search engine oPtimization (seo)

SEO is a huge topic and several books have been written on the subject. The following pages will help you understand the key concepts so you can improve your website's visibility on search engines.

### The Basics
Search engine optimization (or SEO) is the practice of trying

to help your site appear nearer the top of search engine results when people look for the topics that your website covers.

At the heart of SEO is the idea of working out which terms people are likely to enter into a search engine to find your site and then using these terms in the right places on your site to increase the chances that search engines will show a link to your site in their results.

In order to determine who comes first in the search results, search engines do not only look at what appears on your site. They also consider how many sites link
to you (and how relevant those links are). For this reason, SEO
is often split into two areas: on-page techniques and off-page technique

### On-Page techniques

On-page techniques are the methods you can use on your web pages to improve their rating in search engines.

The main component of this is looking at keywords that people are likely to enter into a search engine if they wanted to find your site, and then including these in the text and HTML code for your site in order to help the search engines know that your site covers these topics.

Search engines rely very heavily on the text that is in your pages so it is important that the terms people are going to search for are in text. There are seven essential places where you want your keywords to appear.

Ensuring that any images have appropriate text in the value of their alt attribute also helps search engines understand the content of images.

### Off-Page techniques

Getting other sites to link to you is just as important as on-page techniques. Search engines help determine how to rank your
site by looking at the number of other sites that link to yours.

They are particularly interested in sites whose content is related to yours. For example, if you were running a website that sold fish bait, then a link from
a hairdresser is not likely to be considered as relevant as one from an angling community.

Search engines also look at the words between the opening `<a>` tag and closing `</a>` tag
in the link. If the text in the link contains keywords (rather than just click here or your website address) it may be considered more relevant.

The words that appear in links to your site should also appear in the text of the page that the site links to.