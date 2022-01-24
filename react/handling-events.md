# Handling Events



```
//
function Func(props){
    const [name, setName]= useState(props.name);
    function handleClick(){
        setName("Totoro");
    }
    return (
        <div>
            <h1>Hello from {name}</h1>
            <button onClick={handleClick}>Click me</button>
        </div>
    )
}
```

onClick can pass function directly, if you want to pass extra paramaters, use arrow function
