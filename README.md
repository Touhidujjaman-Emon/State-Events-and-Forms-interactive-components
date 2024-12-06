## Handling events

**Correct way to handle events in React:**

- Pass a function reference to the event handler, like this: `onClick={() => alert("previous")}`
- Ensure the event handler is a function that takes an event object as an argument

**Incorrect way to handle events in React:**

- Directly call the event handler function, like this: `OnMouseEnter={alert("wrong")}` (this will execute the function immediately)

**Correct prop name for mouse enter event:** `onMouseEnter` (lowercase "o")

```js
const handlePrevious = function(){
    alert("previous")
}
<button
  // right way
  onClick={() => alert("previous")}
  onClick={handlePrevious}

  //   wrong way
  onClick={alert("worng")}
  onClick={handlePrevious()}
>
  Previous
</button>
```

## What is State

![state](state.png)

**Example**
![state-example](state-example.png)
