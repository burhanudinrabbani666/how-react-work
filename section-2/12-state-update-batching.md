## State Update Batching

### How state updates are batched

- Renders are not triggered immidiately , but scheduled for when the JS engine has some "free time". There is also batching of multiaple setState calls in event handlers

[Next: state update in practice](./13-state-update-batching-in-practice.md)
