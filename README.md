# algoSeekAndDestroyJS
You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments.
```function destroyer(arr) {
  // Remove all the 
 var args = Array.prototype.slice.call(arguments)
  args.splice(0,1);
  var placeholder = [];
  for(var i =0 ;i<arr.length;i++){
    for(var j = 0;j<args.length;j++){
      if(arr[i]==args[j]){
        delete arr[i];
      }
    }
  }
  function removeFalse(value){
    return Boolean(value)
  }
  placeholder = arr.filter(removeFalse);
  return placeholder;
  }


console.log(destroyer([1, 2, 3, 1, 2, 3], 2, 3));
```
