# Handling Events



### Function Component

```javascript
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

```javascript
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

call function => we can use this keyword to access this keyword to find the function that we binded

```javascript
//
class ClassComponent extends React.Component{
    constructor(props){
        super(props)
        this.state = {name: props.name}
        this.handleClick = this.handleClick.bind(this);
    }
    handleClick(event,id){
        this.setState({name:"Qoo"+id})
    }

    render(){
        return <div>
                     <h1>Hello from {this.state.name}</h1>
                     <button onClick={(event)=>this.handleClick(event, 5)}>Click me</button>
                 </div>
    }
}
```
