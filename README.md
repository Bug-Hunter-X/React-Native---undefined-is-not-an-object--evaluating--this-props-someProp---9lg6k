# React Native: undefined is not an object (evaluating 'this.props.someProp')

This repository demonstrates a common error in React Native applications: attempting to access `this.props` or `this.state` before the component has fully mounted. This often results in the error "undefined is not an object (evaluating 'this.props.someProp')".

## Problem
The `bug.js` file shows the incorrect usage where `this.props` is accessed in the constructor, before the component receives its props. This leads to `this.props.someProp` being undefined.

## Solution
The `bugSolution.js` file demonstrates the correct approach. Access `this.props` within `componentDidMount()` lifecycle method (for class components) or inside an `useEffect` hook (for functional components) after the component has mounted and received its props and state.