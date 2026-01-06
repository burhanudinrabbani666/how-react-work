## Rules for rendering logic

### The two type of logic in react components

1. Render Logic

- Code that lives at the top level of the component function
- Participates in describing how the computer view look lke
- Executed every time the component renders

2. Evet Handler functions

- Executed as a consequance of the event thet the handler is listening for (change in this example)
- Code that actually does things: update state, preform an http request, read an inpt field, navigate to another page, etc

## Functional Programming

- **Side Effect:** dependency on or modification of any data outside the function scope. "interaction with the outside world". Examples: mutating external variable, HTTP request, writing DOM.

**Notes:** Side Effect are not bad! A program can only be useful if it has some interaction with th outside world

Impure function: ⬇️

```jsx
const areas = {};
function cirleArea(r) {
  areas.circle = 3.14 * r * r;
}
```

- **Pure function:** a function has no side effects
  - Does ont change any varibale outside its scope
  - Given the same input, are pure function always returns the same output

```jsx
function cicrleArea(r) {
  return 3.14 * r * r;
}
```

## Rules for render Logic

- 👆 **Components must be pure when it comes to render logic:** given the same props(input), a compoenents instance should always return the same jsx (output)
- 👆 **Render ogic must produce no side effects:** no interaction with the "outside world" is a allowed. so, in render logic:
  - Do NOT perform network request (API Calls)
  - Do NOT start timers
  - Do NOT directly use the DOM API
  - Do NOT mutate objects or variable outside or variables outside of the function scope
  - Do NOT **update state (or refs):** this will create an infinite loop

[Next: state update batching ](./12-state-update-batching.md)
