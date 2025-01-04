# React useEffect without dependencies causing unnecessary re-renders

This repository demonstrates a common React bug where the `useEffect` hook is used without specifying dependencies, leading to unnecessary re-renders and potential performance problems.

## Bug Description

The `useEffect` hook in the `bug.js` file is defined without an empty dependency array (`[]`).  This means it runs after every render, even when the component's props and state haven't changed. In this specific example, this leads to the log message being printed excessively, causing performance overhead.

## Solution

The solution, implemented in `bugSolution.js`, involves adding an empty dependency array (`[]`) to the `useEffect` hook. This ensures the effect runs only after the initial render and not on subsequent renders, unless one of the specified dependencies change. 

## How to run

1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.