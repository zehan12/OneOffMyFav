# Most Common

## React

#  $\colorbox{white}{{\color{red}{each\ child\ in\ an\ array\ or\ iterator\ should\ have\ a\ unique\ key\ prop\}}}$
### solution
```js 
    items.mmap((item)=>(<Card key={item.id} item={item} />)
```

## Redux 
# $\colorbox{white}{{\color{red}{Uncaught\ TypeError:\ Cannot\ read\ properties\ of\ undefined\ (reading\ 'getState')\ }}}$
### solution:

store come there not value
```js
    <Provider store={store}>
```

