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

