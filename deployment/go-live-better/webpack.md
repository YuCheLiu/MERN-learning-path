# Webpack

{% embed url="https://webpack.js.org/loaders" %}

### require package in package.json

```
// 
"devDependencies": {
    "@babel/cli": "^7.2.3",
    "@babel/core": "^7.2.2",
    "@babel/preset-env": "^7.2.3",
    "@babel/preset-react": "^7.0.0"
  }
```

use npm install to install all the depencies



### Create webpack.config.js file

First, we are going to build a module for webpack to import when we execute webpack command.

```
// 
module.exports{

}
```

declare mode of webpack&#x20;

```
//
module.exports{
    mode:"development"
}
```

add entry directory for target folder location.

```
// 
module.exports{
    mode:"development",
    entry: "/src/app/App.jsx"
}
```

add output file location

```
//
module.exports{
    mode: "development",
    entry: "/src/app/App.jsx",
    output:{
        path: "/dis",
        filename: "bundle.js",
        publicPath:'/'
    }
}
```

add what type of file we want webpack to execute

```
//
module.exports{
    mode:"development",
    entry: "/src/app/App.jsx",
    output:{
        path: "/dist",
        filename: "bundle.js",
        public: '/'
    },
    resolve:{
        extensions:['.js','.jsx']
    }
}
```

add module to tell webpack what rule we want to use

```
//
module.exports{
    mode: "development",
    entry:"/src/app/App.jsx",
    output:{
        path:"/dist",
        filename: "bundle.js",
        public:'/'
    }
    resolve:{
        extensions:['.js','.jsx']
    }
    module:{
        rules:[
            {
                test:/\.jsx?/,
                loader: ''babel-loader
            }
        ]
    }
}    
```

