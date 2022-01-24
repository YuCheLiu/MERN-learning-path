# React Class Component

If you haven't heard class before, checkout this page: [class.md](../../../website-fundamentals/javascript/class.md "mention")



React class extends React.Component, and class must have render function

```
class ClassComponent extends React.Component{
    constructor(props){
        super(props)
        this.state = {name: props.name}
    }

    render(){
        return <div>
                     <h1>Hello from {this.state.name}</h1>
                 </div>
    }
}
```

An instance of the Welcome class can be created like this:consComponent Lifecycle

```
const element = <Welcome />
```
