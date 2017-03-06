# dash-blockchain-helpers

### What for ? 

Dash-blockchain-helpers will provides you some utils and helpers in order to help you doing simple stuff.


### How To :
- Install : 
	- From github :
		-  `git clone https://github.com/Alex-Werner/dash-blockchain-helpers`
		- `npm install`
	- From NPM : 
		- `npm install dash-blockchain-helpers`
- Use it
```
const DBH = require('dash-blockchain-helpers')    
var config = {   
    insightAPI:{   
        uri:"http://192.168.0.15:3001/insight-api-dash"   
    }   
}   
var blockchain = new DBH(config)   
```

### Exemple : 

See the exemple directory for some use-cases exemple.

### API : 

#### `new DBH(config)`

Create a new DBH object.

#### `blockchain.getHashFromHeight(height)`

From an height integer will return it's equivalent hash.

#### `blockchain.getHeightFromHash(hash)`

From an hash hexstring will return it's equivalent height.

#### `blockchain.getLastBlockHash()`

Will return the last block hash.

#### `blockchain.getLastBlockHeight()`

Will return the last block height.

#### `blockchain.getStatus()`

Will return basic status information from the API.

### `blockchain.expectNextDifficulty()`

Will return the expected next difficulty (bits) given the last 25 headers.  

### `blockchain.retrieveBlockHeaders([startingHeight,[numberOfBlockheaders,[direction,]]])`

Will return an array of a defined number of block headers from a starting point (height).   
- startingHeight will be a Number representing the height from which you want to fetch the data.  
- numberOfBlockheaders is the number of continious block headers you want to fetch from that starting point  
- direction is an integer representing the direction of headers to fetch, where 1 is forward and -1 backward.  

Every parameters are optional, if so,  
- startingHeight will be 0  
- numberOfBlock will be 25  
- direction will be 1.   

N.B : It is also possible to use an hash as a starting point.  


