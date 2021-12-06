# Package.json file

### Here is the example package.json file:

learn more about json file: json&#x20;

```
{
  "name": "MERN Stack Learning Path",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "nodemon -w server server/server.js",
    "compile": "babel src --out-dir public",
    "watch": "babel src --out-dir public --watch --verbose",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "spencer.yucheliu@gmail.com",
  "license": "ISC",
  "homepage": "",
  "dependencies": {
    "express": "^4.16.4",
    "nodemon": "^1.18.9"
  },
  "devDependencies": {
    "@babel/cli": "^7.2.3",
    "@babel/core": "^7.2.2",
    "@babel/preset-env": "^7.2.3",
    "@babel/preset-react": "^7.0.0"
  }
}
```
