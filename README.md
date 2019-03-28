# React Codegen

React codegen is an interactive CLI to generate boilerplate code for views, reducers, sagas, routes etc. You can specify the name of the component or feature you want to build react-coden writes the code for you along with test cases. So, you can focus on logics only.

### Installation:

`yarn add -g react-codegen`

### Init:
This will install all the dependencies required for your project ( Redux, Redux-saga, Redux-logger, Redux-actions, React-redux, @reach/router).
`react-codegen init`

**Note:** *You need to have yarn installed for init to work*

### Usage:

In your root folder of react project run `react-codegen`. Once you generate the first view and store configuration by selecting redux. Go to App.js and wrap routes with Redux Provider with proper store.

```javascript
import React, { Component } from "react";
import { Provider } from "react-redux";
import ConfigureStore from "./store/store";
import Routes from "./routes";

const store = ConfigureStore();

class App extends Component {
  render() {
    return (
      <Provider store={store}>
        <Routes />
      </Provider>
    );
  }
}

export default App;
```

### Libraries Used

- **Routing**: Reach Router
- **Testing**: Jest + Enzyme
- **State Mangement**: Redux
- **Side Effects**: Redux-saga
