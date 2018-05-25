# Kwuo

__Kwuo__ - A JavaScript testing framework.

# Installation

__kwuo__ should be installed as a development dependency:

```sh
npm install kwuo --dev
```

# Usage

__kwuo__ looks in test folder for test files. 
Your project must have a test folder with your test files in it:

```
your-project
 -+ src/
  -+ Http.js
 -+ test/
  -+ Http.spec.js
```

```js
// src/Http.js

export class Http {
    get(url) {
        return ['mango']
    }
}
```

```js
// test/Http.spec.js
const { Http } = require('../src/Http.js')

describe('Http',()=>{
    it('get method should return an array', ()=>{
        const http = new Http()
        expect(typeof http.get()).toBe('array')
        expect(typeof http).toBe('Http')
    })
})
```

#### describe 

This method is used to represent a group with related test blocks. This method needs to execute with two arguments –

* Test name
* A function


#### it 
This method executes a function to perform a test operation.

#### expect 
This method evaluates the result from the test block and performs the asserts statements.

#### toEqual 
This method is used to compare the expected result and the actual result.

#### beforeAll 
This method is executed only once in the test block to provide the description of the test suites. This function is called once, before all the specs in describe test suite are run.

#### afterAll

This function is called once after all the specs in a test suite are finished.

#### beforeEach
This function is called before each test specification, it function, has been run. beforeEach is fired before each test block.


#### afterEach

This function is called after each test specification has been run.


