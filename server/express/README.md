# Express

### Here is a code snippet to demo a simple express website

```
const express = require('express');

const app = express();

app.use(express.static('public'));

app.listen(3000, function () {
  console.log('App started on port 3000');
});
```
