# Query Documents

### Select all the records

```
const cursor = db.collection('inventory').find({});
```

### Select records by single field and value

```
const cursor = db.collection('inventory').find({status : 'D'});
```

### Select records by field and multiple values

```
const cursor = db.collection('inventory').find({status : { $in : ['A', 'D']}});
```

### Select records by multiple field and  values

```
const cursor = db.collection('inventory').find({status : 'A', qty: '30'})
```



### Aggregate function - a powerful version of 'find' method

```javascript
//
async function findAggreate(db){
  const pipeline = [
    {
      '$match': {
        'price': 1000
      }
    },
    {
      '$project': {
        'name': 1,
        'price':1,
        'accommodates':1
      }
    }

  ]
  const cursor = await db.collection('listingsAndReviews').aggregate(pipeline).toArray();
  cursor.map( (list) => {console.log(list)})
```

$match => base on the rule to filter the result&#x20;

$project => only show require field.
