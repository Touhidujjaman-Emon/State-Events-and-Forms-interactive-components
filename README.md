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

- useState is a React hook that allows you to add state to functional components
- it is typically used in the top-level scope of a functional component
- It returns an array with two elements: the current state value and a function to update that value
- The update function is typically used in event handlers or other functions to update the state
- The state is re-rendered whenever the state value changes
- The state value should be immutable, meaning it should not be directly mutated, but rather replaced with a new value
- useState is typically used in combination with useEffect to handle side effects, such as fetching data from an API

```js
const [step, setStep] = useState(1);

function handleNext() {
  if (step < 3) setStep(step + 1);
}

function handlePrevious() {
  if (step > 1) setStep(step - 1);
}
```

- **Example**
  ![state-example](state-example.png)
