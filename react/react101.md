# React101

### 1.Initializing

```
$ mkdir React101

$ cd React101

$ npm init
```

npm init command can generate package.json file.

### 2. Installing Web Server Dependencies

install express package in node\_modules folder

```
$ npm install express

$ npm install react-dom

$ npm i webpack webpack-cli
```

### 3. Installing babel Development Dependencies

```
$ npm install --save-dev @babel/core @babel/preset-env @babel/preset-react
```



### 3. Installing webpack Development Dependencies

```
$npm install --save-dev @webpack/cli
```



### 4. Creating an Initial Directory Structure

```
React101/
    public/
        main.js
    src/
        index.js
        App.js
    server/
        server.js
```

### 5. Configuring Webpack and Babel

babel.config.js

{% code title="babel.config.js" %}
```javascript
module.exports = {
  presets: ["@babel/preset-env", "@babel/preset-react"],
};
```
{% endcode %}

### create webpack.config.js file

```javascript
// 
const path = require("path");

module.exports={
    mode:"development",
    entry:path.resolve(__dirname,'src/app/App.jsx'),
    output:{
        path: path.resolve(__dirname, 'dist'),
        filename: "bundle.js",
        publicPath: '/'
    },
    resolve:{
        extensions:['.js','.jsx']
    },
    devServer:{
        static:'./dist',
        historyApiFallback: true
    },
    module:{
        rules:[{
            test: /\.jsx?/,
            loader: 'babel-loader'
            }
        ]
    }
}
```

### 6. Creating npm Scripts for Development

{% code title="package.json" %}
```javascript
scripts: {
  "test": "jest"
}
```
{% endcode %}

{% code title="package.json" %}
```javascript
scripts: {
    "start-web-server": "nodemon --exec babel-node src/server/server.js --ignore dist/",
    "compile": "webpack -w --mode=development"
}
```
{% endcode %}

### 7. Test with simaple React Application

src/App.jsx

```javascript
class HelloWorld extends React.Component {
    render() {  
      return (
        <div title="Outer div">
          <h1>CS628 - React Scold folder</h1>
        </div>
      );
    }
  }
  const element = <HelloWorld />;
  
  ReactDOM.render(element, document.getElementById('contents'));
```

public/index.html

```html
<!DOCTYPE HTML>
<html>

<head>
  <meta charset="utf-8">
  <title>CS628</title>
</head>

<body>
  <div id="contents"></div>
  <script src="/App.js"></script>
</body>

</html>
```
