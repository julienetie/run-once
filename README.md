# run-once
Simply do something once, or once under a condition using a custom name space.

```javascript
function colorOfTheSky(color){
  var skyColor
  if(once('colorOfTheSky')){
   skyColor = 'The sky is' + color 
  }else{
   skyColor = 'The sky is falling'
  }
  console.log(skyColor)
}
colorOfTheSky('blue')
// Run once: The sky is blue
// Run again: The sky is falling
// Run and on: The sky is faling
// ...
```
***
```javascript
function colorOfTheSky(color){
  var skyColor
  if(once('colorOfTheSky' + color)){
   skyColor = 'The sky is' + color 
  }else{
   skyColor = 'The sky is falling'
  }
  console.log(skyColor)
}
colorOfTheSky('blue')
// Run once: The sky is blue
// Run again: The sky is falling
// Run and on: The sky is faling
// ...
colorOfTheSky('red')
// Run once: The sky is red
// Run again: The sky is falling
// Run and on: The sky is faling
// ...
```

(c) 2016 Julien Etienne
MIT
