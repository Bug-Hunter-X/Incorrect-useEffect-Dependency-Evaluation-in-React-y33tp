# Incorrect useEffect Dependency Evaluation in React

This repository demonstrates a common error in React's `useEffect` hook where the dependency array isn't properly handling falsy values, leading to unexpected behavior.

## The Bug

The `MyComponent` function uses `useEffect` to log a message when the `count` state is greater than 0.  However, the condition `if (count)` incorrectly treats 0 as truthy, resulting in the message being logged even when `count` is 0.

## The Solution

The solution modifies the conditional statement to explicitly check `count > 0`, ensuring that the message is only logged when the count is actually greater than zero.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the increment button.