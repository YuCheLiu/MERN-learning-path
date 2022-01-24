# Map function



```jsx
function App() {
  const names = ["Jessy", "James", "Jack"];
  const items = [];

  for (let i = 0; i < names.length; i++) {
    items.push(<li>{names[i]}</li>);
  }
  
  return <ul>{items}</ul>;
}
```
