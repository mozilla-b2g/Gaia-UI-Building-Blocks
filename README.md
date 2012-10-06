# Gaia UI Building Blocks (*BB*)

## What are the Building Blocks?
HTML + CSS visual integrations packaged separatedly for using it in FirefoxOS applications and having visual consistency betwen them.
The are a wiki page from the UX teams with detailed information about each Building Block: 
https://wiki.mozilla.org/Gaia/Design/BuildingBlocks

## There is a preview?
Yes, you can preview all of them visiting this page:
http://mozilla-b2g.github.com/Gaia-UI-Building-Blocks/index.html

## Why to use it?
 * Because we need visual consistency among all our applications, and what the hell, all the html&css is done, you don't have to code it twice!
 * Speed up development.
 * We have been using aria roles, so is updated with the latest W3C standards.
 * You can choose to use the ones that you need, there is no dependencies
 * It could be used in multiples contexts and is up to you to use it or not.

## How to use it?
### Stable components
Link from your application `.html` to the desired aviable styles in `shared/style/`, I.E:
`<link rel="stylesheet" href="shared/style/headers.css">`
When you run`make install-gaia` all resources needed for that component will be automatically copied to your application  in `yourappname/shared`.
Doing it in this way, ensures you for having the latest working version of *BB*


### Unstable component
Download this repository and just copy & paste the desired *BB* that you need into a location inside your application styles folder called "bb".
So the folder shema will look like this:

**/apps/myapplication/styles/bb/mybbname**

If you need to extend some *BB* apperance never ever edit the base files, you should extend this from your own application CSS.

## Coding style guidelines
### Indentation
* No tabs.
* Indent by two spaces.
* No whitespace at the end of a line.

### Units
* <b>em</b>, <b>rem</b>, <b>%</b>
* You don't have to add any units, if the value is 0
<pre>
body {
  font-size: 10px;
}

  1rem = 10px
  1px = 0.1rem
</pre>

### Selectors

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

### Comments

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

### Properties

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


##### Colors
<pre>
... {
  color: #0f0; /* HEX color - defined using the 3-character dash notation */
  color: #00ff00 /* HEX color - defined using the 6-character dash notation */
  color: rgba( 34, 12, 64, 0.3);  /* rgba(R,G,B,a) - using only for transparent colors */
}
</pre>