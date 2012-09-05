## Selectors

* have a space after the previous selector
* end in an opening brace
* be closed with a closing brace on a separate line without indentation
* Multiple selectors should each be on a single line, with no space after each comma

  /*single selector*/
  .gaia {
  }

  /*multiple selectors*/
  .b2g,
  .gaia,
  .firefoxOS {
  }

## Properties

* All properties should be on the following line after the opening brace.
* have a single space before the property value
* end in a semi-colon
* multiple values - each value should be separated with a space.
  .b2g {
    color: #efefef;
    font-size: 0.9rem;
    font-family: Open Sans, sans-serif;
  }

## Comments

Describe a section of code
  /**
   * Your Comment Here.
   */


Shorter inline comments may be added after a property, preceded with a space
  padding-left: 2em; /* LTR */
