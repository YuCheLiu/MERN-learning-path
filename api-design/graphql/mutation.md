# Mutation

schema&#x20;

```javascript
//
type Mutation
    changeBooks(bookname:String):String
}vava
```

resolvers

```javascript
//
const resolvers = {
Query: {
    books: () => result,
},
Mutation:{
    changeBooks,
}
}
```

main function&#x20;

```javascript
//
function changeBooks(_, {bookname}){
    return result = bookname+" Yio"
};
```
