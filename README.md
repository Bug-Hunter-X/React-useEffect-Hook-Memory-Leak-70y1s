# React useEffect Hook Memory Leak

This repository demonstrates a common error in React applications: using the `useEffect` hook without a cleanup function, which can lead to memory leaks or unexpected behavior.

## The Bug
The `bug.js` file contains a simple component that updates a count value using the `useState` hook. The `useEffect` hook logs the count to the console after every render, but it does not return a cleanup function. This means that the effect will continue to run even after the component unmounts, potentially leading to memory leaks or unexpected side effects.

## The Solution
The `bugSolution.js` file provides a solution to this problem by adding a cleanup function to the `useEffect` hook. The cleanup function is responsible for cleaning up any resources that were created by the effect, ensuring that the component does not leave behind any unnecessary data or processes.

## How to Reproduce
1. Clone this repository.
2. Navigate to the `bug` directory and run `npm install`.
3. Run `npm start` to start the development server.
4. Observe the console output. You will see that the count value is logged repeatedly, even after the component unmounts.  This demonstrates the memory leak.
5. Repeat step 3-4 with the `bugSolution` directory for a corrected example.
