# HTML Class

This README contains all points to go through during the brief HTML and CSS overview

We'll walk through these things in an .html file and in the Kraken visual editor UI for comparison's sake.

### Basic CSS, Specificity, and Selectors

- CSS stands for "Cascading Style Sheets"

- In most cases, it styles elements by selecting a class (.myClass), an ID (#myID), or an HTML element itself (div, span, et cetera)

Examples: 
```CSS
#redElement {
	color: red; /* Applies to the single element with the ID "redElement" */
}

.blueElements {
	color: blue; /* Applies to any element with the class "blueElements" */
}
```

- You can specify selectors inside a parent selector and chain selectors together to ensure styles only get applied to certain elements

- You can also use parent/child relationship specifiers to further filter down the list of elements that get your styles

Examples:
```CSS
section .red {
	color: red; /* Only elements with the "red" class inside of sections */
}

.blueParent div.blueDivs {
	color: blue; /* Only divs with the "blueDivs" class inside of elements with the "blueParent" class */
}

section > div {
	color: yellow; /* Only divs that are the immediate child of sections */
}

section > div > * {
	color: green; /* Any element that is the immediate child of a div that is an immediate child of a section */
}
```

- Lower rules in a stylesheet override higher rules

Example:
```CSS
.myClass {
	color: red; /* Is NOT applied */
}

.myClass {
	color: blue; /* Is applied */
}
```

- The "lower rule" override only applies when specificity is equal

- What is specificity? 
	+ Basic overview: CSS selectors have hidden "point" values that add up to determine what styles are actually applied
	+ Lower rules = higher point value, and thus are applied

- ID selectors (using # sign) have a higher specificity than classes

Example:
```CSS
#myID {
	color: red; /* Is applied, even though it's above the other selector, because it's an ID */
}

.myClass {
	color: blue; /* Is NOT applied */
}
```

- Each selector in a style adds specificity, so chained selectors have higher specificity

Example:
```CSS
.myClass.myOtherClass {
	color: red; /* Is applied, even though it's above the other selector, because it's a chained selector */
}

.myClass {
	color: blue; /* Is NOT applied */
}
```

### Block Model

- What is a block?

- Block vs. Inline Block vs. Inline

- Default block and non-block elements (div vs. span)

### Flex Model

- What is flex?

- "display: flex"

- "flex-wrap"

- "flex-direction"

- Adjusting element position with "justify-content" and "align-items"