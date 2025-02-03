# React UseEffect setInterval Memory Leak
This repository demonstrates a common error in React applications involving the `useEffect` hook and `setInterval`. The incorrect implementation leads to a memory leak because the interval continues to run even after the component unmounts.

## Bug Description
The `MyComponent` uses `setInterval` to update the counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak. The solution below shows how to resolve this using a cleanup function returned by the `useEffect`'s callback function.

## How to Reproduce
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console for any warnings and memory leaks.