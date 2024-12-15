# Unintended useEffect Side Effect in React Component

This repository demonstrates an example of an unintended side effect caused by the `useEffect` hook in a React component.

The component, `MyComponent`, uses `useEffect` without specifying any dependencies. This means the effect runs after every render. In this example, this causes the message 'Component rendered' to be logged to the console after every click of the button which is inefficient and might indicate an underlying issue with your component's logic.

The `bug.js` file contains the buggy component, while `bugSolution.js` provides a corrected version that addresses the issue.

## Solution
The solution involves specifying dependencies for the `useEffect` hook. By including `count` as a dependency, the effect only runs when the value of `count` changes.