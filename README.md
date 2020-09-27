# Word Search

## HTML/CSS
The layout is fairly basic. On the left are placeholders for the timer, theme and score progress. The inner div of the progress meter changes its `margin-left` property as the score percentage grows.

On the right is the grid of `maxSize` by `maxSize` divs.

## JavaScript
jQuery is used here so as to minimize the effort of DOM manipulation.

### Main Objects
`themes` is an array of objects that contain a list of words, an image filename and description. `puzzle` is an object that contains all the methods and configured properties that are needed for the game to run.

### Logic
- When the game starts, the timer is decremented till it reaches 0. Upon each decrement, it will check if all the hidden words have been found, and update the score meter accordingly.
- A theme is decided on randomly, and the word list is derived from the theme.
- Words are placed into the grid, letter by letter.
- Words can be placed either horizontally, or vertically.
- Words can intersect each other as long as they are not in the same direction, or that letter is not already being intersected by another word.
