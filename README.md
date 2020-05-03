# nulldb
 

#### How to install
```js
npm install nulldb
```


#### example

```js
const db = require('null.db');
 
db.set('userInfo', { difficulty: 'Easy' })
// -> { difficulty: 'Easy' }
 
db.push('userInfo.items', 'Sword')
// -> { difficulty: 'Easy', items: ['Sword'] }
 
db.add('userInfo.balance', 500)
// -> { difficulty: 'Easy', items: ['Sword'], balance: 500 }
 

db.push('userInfo.items', 'Watch')
// -> { difficulty: 'Easy', items: ['Sword', 'Watch'], balance: 500 }
db.add('userInfo.balance', 500)
// -> { difficulty: 'Easy', items: ['Sword', 'Watch'], balance: 1000 }
 
db.fetch('userInfo.balance') // -> 1000
db.fetch('userInfo.items') // ['Sword', 'Watch']
```
