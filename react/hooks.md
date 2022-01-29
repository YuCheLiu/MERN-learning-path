---
description: only use function component
---

# Hooks

Hook allows function component access to state and other React features.



#### State Hook - useState()

allow you to change state inside function component

in function component&#x20;

```javascript
//
function Example(){
    const [count, setCount] = useState(0);
    return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

in class component

```javascript
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```

Effect Hook: Do something after rendering&#x20;

