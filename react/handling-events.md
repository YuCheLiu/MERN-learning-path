# Handling Events



### Function Component

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

```
//
function Func(props){
    const [name, setName]= useState(props.name);
    function handleClick(id){
        setName("Totoro"+id);
    }
    return (
        <div>
            <h1>Hello from {name}</h1>
            <button onClick={()=>handleClick(5)}>Click me</button>
        </div>
    )
}
```



### Class Component

function need to bind with the current class component using bind function and pass this keyword

