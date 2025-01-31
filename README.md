# React Native useEffect Hook Asynchronous State Update

This repository demonstrates a common bug in React Native applications involving the `useEffect` hook and asynchronous state updates.  The issue arises when a callback within `useEffect` relies on the updated state, but the state update hasn't fully propagated yet.

## Bug Description

The provided code showcases a scenario where `useEffect`'s callback uses a stale closure.  Clicking the increment button updates the state; however, the `useEffect` callback might log the previous state value, leading to incorrect behavior.

## Solution

The solution involves using the functional update syntax of `useState` to ensure that the callback always uses the most recent state value.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npx react-native run-android` (or the equivalent command for your platform).
4. Observe that the console log might show an outdated count value.

## License

MIT