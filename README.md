# Express Router Study

<br>

## What is Express Router Study?
The "Express Router Study" examines the Router functionality in express applications to essentially keep the server.js file a bit cleaner and organize the application better by "modularizing" application endpoints.

<br>

In an express application, when you want to create a "router" and "modularize" your routes, you need to follow relatively streamlined process that can be done for as many route groups as needed.

First, in your server.js file you import your router file(s):
```JavaScript  

    const shoppingListRouter = require('./myListRouter');              
            
```

Second, (still in your server.js file), use "app.use" to route the request to the right ROUTER:
```JavaScript
  
     app.use('./myList', myListRouter);

```
Third, in your new router file (e.g. myListRouter.js), load express and router:

```JavaScript

     const express = require('express');
     const router = express.Router();

```
Fourth, when you setup routes within this router file, use "/":
  o Note that in this example, "List.get" refers to a model imported earlier (e.g. const {List} = require('./models');)

```JavaScript

      router.get('/', (req, res) => {
        res.json(List.get());
      });

```

Fifth, setup a router instance at the bottom of the file:
```JavaScript
    
      module.exports = router;
  
```

<br>

## What are the key features of Express Router Study?
Since this study is ongoing, basic functionalities are covered first and more advanced features are added or will be added in the future.


| **Features:**                            | **Feature Notes:**                             |
| ---------------------------------------- | ----------------------------------------------|
| create a Router module                       | Seperates routes into more organized files        |

<br>

