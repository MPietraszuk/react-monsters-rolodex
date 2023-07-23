# react-monsters-rolodex

This project is demonstrating React Functional Components. It's enabling the user to search via an API. ( monsters-rolodex-react-functions-hooks )

A functional component is just a plain JavaScript pure function that accepts props as an argument and returns a React element(JSX). A class component requires you to extend from React. Component and create a render function that returns a React element.

React Hooks vs Class Components. In today's world React has ...
The major difference between Hooks and class-based state is that hooks are used inside of the functional component. One thing to keep in mind is that never call hooks inside of a any logic, it should always be on the top level! useState() is a hook that allows you to play with state in functional components in react.

Can you mix React classes and functions?
You can't use Hooks inside a class component, but you can definitely mix classes and function components with Hooks in a single tree. Whether a component is a class or a function that uses Hooks is an implementation detail of that component.


```
import './search-box.styles.css';

const SearchBox = ({className, placeholder, onChangeHandler}) => (
      <input
          className={`search-box ${className}`}
          type='search'
          placeholder={placeholder}
          onChange={onChangeHandler}
      />
);

export default SearchBox;
```
```
import { Component } from "react";
import './search-box.styles.css';

class SearchBox extends Component {
  render() {
    return (
      <input
          className={`search-box ${this.props.className}`}
          type='search'
          placeholder={this.props.placeholder}
          onChange={this.props.onChangeHandler}
      />
    )
  }
}

export default SearchBox;
```
