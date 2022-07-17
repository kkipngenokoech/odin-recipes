this is a basic website that seeks to show use of links , images and lists in a basic website

# css notes
# using selectors
# universal selector
you use an asterisk - it would select elements of any type
* {
    property-type : property-value;
}
# type selector
it selects all elements of a given element type and the syntax is just the name of the element type i.e
div {
    property-type : property-value;
}

# class selector
it selects elements in a given class- all elements defined in that class
let say you have a p page of class selector <p class="selector">
so you declare this in your css variable:
.selector{
    property-name:property-value;
}
the class name is mostly preceeded with a . value so in which value is case sensitive
classes are not elements specific they are universal

# id selectors
they are similar to class selectors, they select an element with the said specific id attribute
though instead of a . you use #
#idname{
    property-name:property-value;
}

# group selectors
if there are two css declarations that have some common values but other additional distinguishing values, to avoid repetitions for this similar values you:
.read , unread{

}
# chaining selectors
if there is a class with sub class and you want to make changes only to the said sub class you
.mainclass.subclass{

}
if it is a sub id you
.mainclass#idname{

}
# descendant combinator
here the selectors are separated by spaces but it only select the subclass which has the main(ancestor class)
.ancestor .parent{
    //it selects the .parent class with the ancestor as a superclass
}

# common css properties
color: text color
background-color: sets the background of an element
it accepts actual color name, HEX, RGB, HSL value

font-family: it can be either a font-family-name or sans-serif
you can add as many values as possible so that when the browser doesn't find the first one it searches the next till it finds the one it supports

font-size: it sets the size of the font 
font-weight: it affects the boldness of text, it can be a word (bold) or a value like (700)
text-align: it aligns texts horizontally within an element :center... and so on are its values

image height and width
to adjust the image size without loosing its proportion you use auto on the height and play around with the width
img{
    height: auto;
    width: 200px
}

# cascades of css

# specificity
cascade with more specificity takes precedence of others
type selectors --> class selectors --> id selectors --> inline styles
if between elements of the same selector, the one with more specificity is used

# inheritance
it refers to css properties that when applied to an element are inherited automatically by its child descendants even when we don't explicitly write rules for those descendants.
font-family, font-size, color) that's typography based properties are mostly inherited

# rule order
if it comes to matters that tie breaker can't be broken , the rule that was declared later or more recently takes the winner medal and it is then applied

# ADDING CSS TO HTML
1. external css
you create a separate css file and then you link it inside an HTML's opening and closing head tag with a self closing <link> element
in the href we pass the name of the css file
the rel attribute is necessary since it specifies the relationship between the linked file and the html file
2. internal css
we place the css declarations inside a <style> tag in the <head> tags
3. inline css
you add css files directly into the html elements
<p style="color: blue;background-color:black;"></p>
