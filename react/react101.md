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

### 3. Installing Development Dependencies

```
$ npm i -D eslint babel-eslint eslint-plugin-react eslint-plugin-react-hooks
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

```
module.exports = {
  presets: ["@babel/preset-env", "@babel/preset-react"],
};
```

webpack.config.js

```
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader",
        },
      },
    ],
  },
};
```

### 6. Creating npm Scripts for Development

```
// In package.json
scripts: {
  "test": "jest"
}
```

```
// In package.json
scripts: {
    "start-web-server": "nodemon --exec babel-node src/server/server.js --ignore dist/",
    "compile": "webpack -w --mode=development"
}
```

### 7. Test with simaple React Application

src/App.jsx

```
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

```
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