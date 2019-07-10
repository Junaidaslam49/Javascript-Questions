# Javascript-Questions


###### 1. Write a JavaScript program to sum the multiples of 3 and 5 under 1000
#### Answer:

```javascript
function multiplesOf3and5(number) {
  var sum = 0;
  for (var i = 1 ; i <= number; i++) {
    if( (i % 3 == 0) && (i % 5 == 0) ){
      sum = sum + i;
    }
  }
  return sum;
}
```

###### 2. Write a JavaScript program which iterates the integers from 1 to 100. But for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".

#### Answer:

```javascript
function fizzBuzz () {
    var total = 0;
    for (var i = 1 ; i < 100 ; i++){
          if  (i % 3 == 0) {
              total = 'Fizz';
              console.log(total);
              } 
          if (i % 5 == 0) {
              total = 'Buzz';
              console.log(total);
              }
      if( (i % 3 == 0) && (i % 5 == 0) ){
              total = 'FizzBuzz';
              console.log(total);
              } 
            total = i;
            console.log(total);
            }
          }
  ```
  ###### 3. Write a JavaScript program to compute the union of two arrays.Sample Data:

#### Answer:

```javascript 
function union(array1,array2) {
// in combination we are combining two arrays
    let combination = array1.concat(array2);
// in result we have use filter method to iterate value and index of array and all elements of that of combination are stored in self    
    let result = combination.filter(function(value, index, self) {
// in shouldAdd we are commparing value of index of value of self with index we used in filter and returning true and false       
    let shouldAdd = self.indexOf(value) === index;
        return shouldAdd;
    });

    return result;  
}
```
###### 4. //Write a JavaScript function to remove. 'null', '0', '""', 'false', 'undefined' and 'NaN' values from an array.Sample array : [NaN, 0, 15, false, -22, '',undefined, 47, null] Expected result : [15, -22, 47]
#### Answer:

```javascript
function filterArray() {
  let sampleArray = [NaN, 0, 15, false, -22, '',undefined, 47, null, "ahsan"];
  //Used filter method to check each value of sampleArray.  
  var sampleArrayFixed = sampleArray.filter(value => {
  //Apllied if condition to get the expected result  
  if ((value !== false) && (value !== undefined) && (value !== null)  && (value !== 0) && ((isNaN(value) && typeof value === 'number') !== true) && (value !== "")){
          return true; //output: [15, -22, 47]
          }
      return false;
      });
  return sampleArrayFixed;
}
  ```

