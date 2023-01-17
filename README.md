# Most Common

## React

#  $\colorbox{white}{{\color{red}{each\ child\ in\ an\ array\ or\ iterator\ should\ have\ a\ unique\ key\ prop\}}}$
### solution
```js 
    items.mmap((item)=>(<Card key={item.id} item={item} />)
```

## Jest Vitest
#  $\colorbox{white}{{\color{red}{ReferenceError:\ expect\ is\ not\ defined\ }}}$
### solution
In stepupTest.js
```js
import { expect, afterEach } from "vitest";
import  { cleanup } from "@testing-library/react";
import matchers from "@testing-library/jest-dom/matchers";

expect.extend(matchers);

afterEach(()=>{
    cleanup()
})
```

## Redux 
# $\colorbox{white}{{\color{red}{Uncaught\ TypeError:\ Cannot\ read\ properties\ of\ undefined\ (reading\ 'getState')\ }}}$
### solution:

store come there not value
```js
    <Provider store={store}>
```

