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
