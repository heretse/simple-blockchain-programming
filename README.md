# simple-blcokchain-programming

A simple blockchain program to demo how the Bitcoin Blockchain works. 

## Execution

You can execute many nodes to simulate a P2P blcokchain network.

```sh
node app.js <specificied-port-default-is-3000>
```

## Usage with Node.js

### Prerequisite
```sh
npm install node-fetch --save
```

### Add Transaction
```js
import fetch from 'node-fetch';

// post
fetch()('http://localhost:3000/transactions', { method: 'POST', body:
    {
        "from": "Winston",
        "to": "Andy",
        "amount": 99
    }})
	.then(res => res.json())
	.then(json => console.log(json));

```

### Mining
```js
import fetch from 'node-fetch';

// get
fetch()('http://localhost:3000/mine', 
	.then(res => res.json())
	.then(json => console.log(json));

```

### Show Blockchain
```js
import fetch from 'node-fetch';

// get
fetch()('http://localhost:3000/blockchain', 
	.then(res => res.json())
	.then(json => console.log(json));

```

### Register Nodes
```js
import fetch from 'node-fetch';

// post
fetch()('http://localhost:3000/nodes/register', { method: 'POST', body:
    {
        "urls": [
            {
                "url": "http://localhost:3001"
            },
            {
                "url": "http://localhost:3002"
            }
        ]
    }})
	.then(res => res.json())
	.then(json => console.log(json));

```

### Resolve Conflict
```js
import fetch from 'node-fetch';

// get
fetch()('http://localhost:3000/resolve', 
	.then(res => res.json())
	.then(json => console.log(json));

```