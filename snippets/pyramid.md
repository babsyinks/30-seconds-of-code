---
title: Pyramid
tags: number, array, math
expertise: intermediate
firstSeen: 2022-07-06T07:00:00-04:00
---

print a pyramid with a max base of n, where n is your input.

- The function receives a number n that determines the max length of base
- The input determines the length and width of the pyramid
- The # is used to represent a unit of the pyramid

```js
const pyramid=n=>{
    let str = ''
    let midIndex = Math.floor(n/2)
    for (let i = 0; i < n; i++) {
        str+= (i === midIndex?'#':' ')
    }
let leftIndex,rightIndex
leftIndex = rightIndex = midIndex
const pyramidArray = []
pyramidArray.push(str)
while((rightIndex - leftIndex) < n){
   const arr = Array.from(str)
   if(leftIndex !== rightIndex){
    arr[leftIndex] = '#'
    arr[rightIndex] = '#'
    str = arr.join('')
    pyramidArray.push(str)  
   }
   leftIndex--
   rightIndex++
}
pyramidArray.forEach(str=>{
    console.log(str)
    /n
})
}
```

```js
pyramid(10)  
/*   #
    ###
   #####
  #######
 ######### */
```
