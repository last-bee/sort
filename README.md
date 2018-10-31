# sort
Sorting method

#js的快速排序
###原理
####找个基数，大于基数放后边，其他方左边
####循环自调知道数组为1 返回

``` javascript
  function quickSort(arr) {
      if(arr.length <=1 ){
          return arr
      }
      var pivotIndex = Math.floor(arr.length/2)
      var pivot = arr.splice(pivotIndex,1)[0]
      var left = [], right = []
      for(var i = 0; i< arr.length; i++){
        if(arr[i] < pivot){
            left.push(arr[i])
        } else {
            right.push(arr[i])
        }
      }
      
      return quickSort(left).concat([pivot],quickSort(right))
  }
  ```
