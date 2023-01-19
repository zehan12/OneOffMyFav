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

## Redux
# $\colorbox{white}{{\color{red}{Uncaught\ ReferenceError:\ useSelector\ is\ not\ defined\ }}}$

Uncaught ReferenceError: useSelector is not defined

do not use useSelector on Main app  with Provider
before
```js 
import { Provider } from "react-redux";
import { store } from "../store/store";

const Main = () => {
    const state = useSelector(state => state)
    console.log(store)
    return (
        <Fragment>
            <Provider store={store} >
                <AllRoute />
            </Provider>
        </Fragment>
    )
}

export default Main;
```
correct
after
```js
const Main = () => {
    const state = store.getState()
    console.log(store)
    return (
        <Fragment>
            <Provider store={store} >
               <AllRoute />
            </Provider>
        </Fragment>
    )
}
```

