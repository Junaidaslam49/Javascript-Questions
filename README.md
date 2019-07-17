# Javascript-Questions


#### 1. Write a JavaScript program to sum the multiples of 3 and 5 under 1000
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

#### 2. Write a JavaScript program which iterates the integers from 1 to 100. But for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".

#### Answer:

```javascript
function fizzBuzz () {
    for (var i = 1 ; i < 100 ; i++){
      if  (i % 15 == 0 ) {
          console.log('FizzBuzz');
      } 
      else if (i % 5 == 0) {
          console.log('Buzz');
      }
      else if (i % 3 == 0 ){
          console.log ('Fizz');
      }else{
      console.log(i);
      }
    }
}  
 ```
#### 3. Write a JavaScript program to compute the union of two arrays.Sample Data:

#### Answer:

```javascript 
function union(array1,array2) { 
    let combination = array1.concat(array2);   
    let result = combination.filter(function(value, index, self) {       
    let shouldAdd = self.indexOf(value) === index;
        return shouldAdd;
    });

    return result;  
}
```
#### Detail: 
In combination we are combining two arrays and in result we have use filter method to iterate value and index of array and all elements of that of combination are stored in self in shouldAdd we are commparing value of index of value of self with index we used in filter and returning true and false.

#### 4. Write a JavaScript function to remove. 'null', '0', '""', 'false', 'undefined' and 'NaN' values from an array.Sample array : [NaN, 0, 15, false, -22, '',undefined, 47, null] Expected result : [15, -22, 47]
#### Answer:

```javascript
function filterArray(sampleArray) {  
  var sampleArrayFixed = sampleArray.filter(value => {  
  if ((value !== false) && (value !== undefined) && (value !== null)  && (value !== 0) && ((isNaN(value) && typeof value === 'number') !== true) && (value !== "")){
          return true;
          }
      return false;
      });
  return sampleArrayFixed;
}
  ```
#### Detail:
Used filter method to check each value of sampleArray and apllied if condition to get the expected result

#### 5. Write a JavaScript program to remove a character at the specified position of a given string and return the new string.

#### Answer:

```javascript
function removeString(myString,position) {
    part1 = myString.substring(0, position);   
    part2 = myString.substring(position + 1, myString.length); 
  return (part1 + part2);     
}
```
#### Detail:
In part1 removing character from the given position whose starting position is 0  as starting position is inclusive and ending position is excluded.In part 2 one is added in position as first parametre  of substring function and total length as second parametre of given string which is ending point of substring function.

#### 6. Write a JavaScript program to list the properties of a JavaScript object.

#### Answer:

```javascript
function getObjectProperties(obj) {
      Object.keys(obj).forEach(item => {console.log(item);});
    }
```
#### Details:
Object.keys(obj) method gives keys of the object.
There are not methods such as Objects.forEach().
So, if we want to iterate through all the keys, then we can use Array.forEach() function.


#### 7. Write a JavaScript program to delete the rollno property from the following object.Also print the object before or after deleting the property.

#### Answer:

```javascript
function deletPropertyObject(student) {
     console.log('Before Deleting sclass of object student');
     console.log(student);
     let removeProperty = delete student.rollno;
     console.log('After Deleting sclass of object student'); 
     return student;
   }
 ```              
#### 8. Write a JavaScript program to create a Clock. Go to the editor Note: The output will come every second.

#### Answer:

```javascript
function getTime() {
    var time = new Date().toLocaleTimeString();
    console.log(time);
}
setInterval(getTime, 1000);
 ```              
 #### Detail:
  Date() is method which return date time in javascript And toLocaleTimeString() method gives time in string form.
  getTime function will return time now we need to put timer to fullfill our requirement.setInterval(getTime, 1000)
  will give time after every second.
  
#### 9. Create a method named *dropRight* It accepts two arguments. One is an Array and second is a Number `n`
#### It returns a new array with `n` number of elements removed from the right

#### Answer:

```javascript
function dropRight(array,n) {
   let newArray= array.slice(0,array.length-n);
   return newArray;
   }
 ```
 
#### 10. Create a method named head It accepts an array as an argument.It returns the head of a list

#### Answer:

```javascript
function head (arr) {
   let f = arr[0];
   return f;
   }
 ```
 
#### 11. Create a method named initial It accepts an array as an argument.It returns all the elements of an array except the last one.

#### Answer:

```javascript
function initial(arr) {
  let newArr=arr.slice(0,arr.length-1);
  return newArr;
}
 ```
 #### 12. Create a method named allEqual It accepts an array as an argument.It returns true if all elements in an array are equal otherwise returns false.
 
#### Answer:


```javascript
function allEqual(arr) {
 return arr.every( (val, i, arr) => val === arr[0] );
 }
 ```
 
 #### 13. Create a method named countOccurrences It accepts an array and a value as arguments It returns the occurrences (count) of a value in an array.
 
#### Answer:


```javascript
function countOccurrences(arr,val) {
    let a = 0;
  arr.forEach((elem, index) => {
     if (elem == val) {
          a++;
        } 
  })
    return a;
}
 ```
 
 #### 14. Create a method named dropLeft It accepts two arguments. One is an Array and second is a Number n 
  ####    It returns a new array with n number of elements removed from the left.
 
#### Answer:


```javascript
function dropLeft(arr,n) {
    let newArray= arr.splice(0,n);
    return arr;
}
 ```
#### Details:
We have used splice instead of slice because slice (from,until) and until is excluded in slice so we have used splice (index,number of counts).

 #### 15. Create a method named everyNth It accepts two arguments. One is Array and second is Number n.It returns every nth element in an array.

#### Answer:


```javascript
function everyNth(arr, n) {
    let newArray = arr.filter((index,item) => index%n === 0);
    return newArray;
 }
 ```
