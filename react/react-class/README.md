# React class

React class extends React.Component, and class must have render function

```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

An instance of the Welcome class can be created like this:consComponent Lifecycle

```
const element = <Welcome />
```
