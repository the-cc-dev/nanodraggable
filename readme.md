# nanodraggable
Draggable nanocomponent

## installation
```
npm i -S nanodraggable
```

## example
#### Using classes
```javascript
var Nanodraggable = require('nanodraggable')

class DraggableObject extends Nanodraggable {
    constructor(x, y) {
    	super(x, y, function() {
	    return html`<div>Drag me</div>`
	})
    }
}

var draggable = new DraggableObject(0, 0)

function view (state, emit) {
    return html`
        <div>
            ${draggable.render()}
        </div>
    `
}
```

#### ES5 way
```javascript
var Nanodraggable = require('nanodraggable')

var draggable = new Nanodraggable(0, 0, function() {
    return html`
        <div>Drag me</div>
    `
})

function view (state, emit) {
    return html`
        <div>
            ${draggable.render()}
        </div>
    `
}
```

## api
#### ```draggable = Draggable(x, y, content)```
Creates a new component. Takes ```x``` and ```y``` as default position and ```content``` a function that returns HTML template string (```bel```, ```choo/html```, ```nanohtml```).
