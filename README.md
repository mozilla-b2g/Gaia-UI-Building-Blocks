## Indentation
* No tabs.
* Indent by two spaces.
* No whitespace at the end of a line.

## Units
* <b>em</b>, <b>rem</b>, <b>%</b>
* You don't have to add any units, if the value is 0
<pre>
body {
  font-size: 10px;
}

/*
  1rem = 10px
  1px = 0.1rem
*/
</pre>

## Selectors

* have a space after the previous selector
* end in an opening brace
* be closed with a closing brace on a separate line without indentation
* Multiple selectors should each be on a single line, with no space after each comma

<pre>
 /*single selector*/
 .gaia {
  ...
 }

 /*multiple selectors*/
 .b2g,
 .gaia,
 .firefoxOS {
  ...
 }
</pre>

## Comments

Describe a section of code

<pre>
/**
 * Your Comment Here.
 */
</pre>


Shorter inline comments may be added after a property, preceded with a space
  
<pre>
... {
  padding-left: 2em; /* dir="ltr" */
}
</pre>

## Properties

* All properties should be on the following line after the opening brace.
* have a single space before the property value
* end in a semi-colon
* multiple values - each value should be separated with a space.

<pre>
.b2g {
  color: #efefef;
  font-size: 0.9rem;
  font-family: Open Sans, sans-serif;
}
</pre>

#### Background

* color is first
* image path without "" or ''
* background repeat
* background position with <b>%</b> or <b>rem</b>
<pre>
... {
  background: #fff url(images/default.png) no-repeat 3rem 100%;
}
</pre>

#### Multiple Backgrounds
<pre>
... {
  background: url(images/image-3.png),
              url(images/image-2.png),
              url(images/image-1.png),
              #fff;
}
</pre>

#### Gradients
<pre>
... {
  background: linear-gradient(to bottom, #fff, #000);
}
</pre>

#### Borders
<pre>
... {
  border: solid 0.1rem #fff;
}
</pre>


## Colors
<pre>
... {
  color: #0f0; /* HEX color - defined using the 3-character dash notation */
  color: #00ff00 /* HEX color - defined using the 6-character dash notation */
  color: rgba( 34, 12, 64, 0.3);  /* rgba(R,G,B,a) - using only for transparent colors */
}
</pre>