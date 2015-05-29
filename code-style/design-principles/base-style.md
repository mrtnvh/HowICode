# Base style

A Base style is applied to an element using an element selector, a descendent selector, or a child selector, along with any pseudo-classes. It doesn’t include any class or ID selectors. It is defining the default styling for how that element should look in all occurrences on the page.

```scss
/*
 * Example Base Styles
 */

body, form {
    margin: 0;
    padding: 0;
}

a {
    color: #039;

	&:hover {
    color: #03F;
}

```
Base styles include setting heading sizes, default link styles, default font styles, and body backgrounds. There should be no need to use !important in a Base style.


## CSS Resets
A CSS Reset is a set of Base styles designed to strip out—or reset—the default margin, padding, and other properties. Its purpose is to define a consistent foundation across browsers to build the site on.

Many reset frameworks can be overly aggressive and can introduce more problems than they solve. Removing margin and padding from elements only to introduce them again creates duplicated effort and increases the amount of code needed to be sent to the client.

Many find resetting styles a helpful tool in site development. Just be sure to understand the drawbacks of the framework you wish to use and plan accordingly.

Developing your own set of default styles that you consistently use from project to project can also be advantageous.

