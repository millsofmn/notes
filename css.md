# CSS

## Positioning Block-level Elements
| CSS Positioning Scheme | Description |
| --- | --- |
| static | normal default positioning of the element on the page | 
| relative | position relative to others on the page usually because of top, bottom, left and right properties |
| absolute | element apears to float above the document and can be positioned as needed separate from the rest of the page flow |
| fixed | element remains in same position in the browser window even when the page is scrolled |
| inherit | element inherits it's position from it's parents |

## CSS3 Selectors
| Selector | Description | Example |
| --- | --- | --- |
| element[attribute$=value] | '$' selects attribute ending with value | a[href$=".pdf"] - selects all links that the href ends with pdf |
| element[attribute\*=value] | '\*' selects attribute containing value | a[href\*="city"] - selects all links that the href contains city |
| element[attribute^=value] | '^' selects attribute begining with value | a[href^="https"] - selects all links that begin with https |
| element:checked | selects all elements that are checked | |
| element:disabled | selects all elements that are disabled | |
| element:enabled | slects all elements that are enabled | |
| element:first-of-type | selects first element of type | |
| element:last-of-type | slects last element of type | |
| element1~element2 | selects every instance of element2 that is preceded by element 1 | |
