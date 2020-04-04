# Notes for Node.js

## Node.js

-   with Node.js installed, we can run JS codes on the computer instead of only running on the browser
    -   run index.js in terminal
        -   `$ node index.js`
    -   open the Node.js REPL (Read Evaluation Print Loop)
        -   `$ note`
        -   just like JS console on the browser

## npm (Node Package Manager)

-   npm init
    -   `$ npm init`
-   npm install packages
    -   `$ npm install <package_name>`
-   include packages in JS
    -   `let package = require("<package_name>")`

## Node.js setup

### include express

```js
const express = require("express");

const app = express();
```

### set up server listening port

```js
app.listen(<port_num>, () => {
  console.log("Server start on port <port_num>");
})
```

### set up response for HTTP GET request to each route

-   send HTML directly

```js
app.get("/", (req, res) => {
    res.send("<h1>Hello, world!</h1>");
});
```

-   send a file

```js
app.get("/", (req, res) => {
    res.sendFile(__dirname + "index.html");
});
```

**`__dirname` gives the current working directory path**
