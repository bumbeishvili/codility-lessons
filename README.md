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
