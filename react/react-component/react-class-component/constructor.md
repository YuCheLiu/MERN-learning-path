# Constructor

```javascript
//
constructor(props) {
  super(props);
  // Don't call this.setState() here!
  this.state = { counter: 0 };
  this.handleClick = this.handleClick.bind(this);
}
```

you should always assign this.state directly in constructor, In other class, use this.setState()
