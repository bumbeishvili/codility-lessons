# codility-lessons


# Lesson 1 - Iterations

## BinaryGap
```javascript
function solution(N) {
      var str  = Number(N).toString(2);
      var arr =  str.split('1');
      var filtered = arr.filter((d,i,arr)=>{
               if(!arr[0] && !arr[arr.legth-1]) {
                  return i>0 && i<arr.length-1;
               }
      })
      if(filtered.length==0) {return 0; }
      var result = Math.max.apply(null, filtered.map(d=>d.length))
      return result;
}
```


# Lesson 2 - Arrays

## CyclicRotation

```javascript
function solution(A, K) {
   K = K % A.length
   return A.map((d,i,arr)=>{
      if(i-K>=0){
          return arr[i-K]
      }
      else{
         return arr[arr.length+i-K]
      }
   })
}
```

## OddOccurrencesInArray
```javascript
function solution(A) {
    var obj = {};
    A.forEach(d=>{
      obj[d] = !obj[d]; 
    });
    var value = Object.keys(obj).filter(key=>obj[key])[0];

    return Number(value);
    // write your code in JavaScript (Node.js 8.9.4)
}
```



# Lesson 3 - Time Complexity

## FrogJmp


```javascript
function solution(X, Y, D) {
  return Math.ceil((Y-X)/D)
}
```

## PermMissingElem

```javascript
function solution(A) {
  var map = Array(A.length+1).fill().map(d=>true);
  
  A.forEach(d=>{
     map[d-1] = false
  });
  
  return map.indexOf(true)+1

}
```


## TapeEquilibrium


```javascript
function solution(A) {
    var obj = {};
    A.forEach(d=>{
      obj[d] = !obj[d]; 
    });
    var value = Object.keys(obj).filter(key=>obj[key])[0];

    return Number(value);
    // write your code in JavaScript (Node.js 8.9.4)
}
```



# Lesson 4 - Time Complexity

## FrogRiverOne


```javascript
function solution(X, A) {
    var count = X;
    var arr = Array(X).fill().map(d=>true);
    for(var i=0; i<A.length; i++){
        var el = A[i]-1;
        if(arr[el]){
            arr[el]=false;
            count--;
        }
        if(count==0){
           return i;
        }
    }
    return -1
}
```

## MissingInteger


```javascript
function solution(A) {
    var arr = Array(A.length).fill().map(d=>true);
    A.forEach(d=>{
        if(d>0 && d<A.length){
            arr[d] = false;
        }
    })
    arr[0]=false;
    var index =  arr.indexOf(true);
    if(index==-1){
        if(arr.length==1 && A[0]!=1){ return 1;}
        return A.length+1
    }else{
        return index
    }
}
```


## PermCheck



```javascript
function solution(A) {
    var obj = {};
    A.forEach(d=>{
      obj[d] = !obj[d]; 
    });
    var value = Object.keys(obj).filter(key=>obj[key])[0];

    return Number(value);
    // write your code in JavaScript (Node.js 8.9.4)
}
```

## MaxCounters



```javascript
function solution(A) {
    var obj = {};
    A.forEach(d=>{
      obj[d] = !obj[d]; 
    });
    var value = Object.keys(obj).filter(key=>obj[key])[0];

    return Number(value);
    // write your code in JavaScript (Node.js 8.9.4)
}
```
