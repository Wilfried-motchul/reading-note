# CSS Transforms, transition, and Animations


### Transforms

With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

Within this lesson we’ll take a look at both two-dimensional and three-dimensional transforms. Generally speaking, browser support for the transform property isn’t great, but it is getting better every day. For the best support vendor prefixes are encouraged, however you may need to download the nightly version of Chrome to see all of these transforms in action.



### Transform syntax

The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.



```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}

```

Notice how the transform property includes multiple vendor prefixes to gain the best support across all browsers. The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property.

In the interest of brevity, the remainder of this lesson will not include vendor prefixes. They are, however, strongly encouraged for any code in a production environment. Over time we will be able to remove these prefixes, however keeping them in is the safest approach for the time being.


##  Transitions & Animations

### Transitions

As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, with the first three are the most popular.

In the example below the box will change its background color over the course of 1 second in a linear fashion.

```
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}

```

### Transition properties

It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint. A handful of the more popular transitional properties include the following.

* background         
* colorbackground
- positionborder
- colorborder
- widthborder
- spacingbottomclipcolorcropfont
- sizefont
- weightheightleftletter
- spacingline
- heightmarginmax
- heightmax
- widthmin
- heightmin
- widthopacityoutline
- coloroutline
- offsetoutline
- widthpaddingrighttext
- indenttext
- shadowtopvertical
- alignvisibilitywidthword
- spacingz
- index


### Animations (Keyframes)

To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

```
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}

```


### Vendor Prefixing the Keyframe Rule

The @keyframes rule must be vendor prefixed, just like all of the other transition and animation properties. The vendor prefixes for the @keyframes rule look like the following:

* @-moz-keyframes
* @-o-keyframes
* @-webkit-keyframes


The animation above is named slide, stated directly after the opening @keyframes rule. The different keyframe breakpoints are set using percentages, starting at 0% and working to 100% with an intermediate breakpoint at 50%. The keywords from and to could be used in place of 0% and 100% if wished. Additional breakpoints, besides 50%, may also be stated. The element properties to be animated are listed inside each of the breakpoints, left and top in the example above.

It is important to note, as with transitions only individual properties may be animated. Consider how you might move an element from top to bottom for example. Trying to animate from top: 0; to bottom: 0; will not work, because animations can only apply a transition within a single property, not from one property to another. In this case, the element will need to be animated from top: 0; to top: 100%;.





