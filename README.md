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
    let count = 0;
  arr.forEach((elem, index) => {
     if (elem == val) {
          count++;
        } 
  })
    return count;
}
 ```
 
 #### 14. Create a method named dropLeft It accepts two arguments. One is an Array and second is a Number n 
  ####    It returns a new array with n number of elements removed from the left.
 
#### Answer:


```javascript
function dropLeft(arr,n) {
    let indexArray = [];
    arr.forEach((elem, index) => {
       if (index > n-1) {
             indexArray.push(elem);
       } 
    })
   return indexArray;
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


#### 16. Create a method named indexOfAll It accepts two arguments. One is array and second is value.It returns all indices of val in an array

#### Answer:


```javascript
function indexOfAll (arr, val) {
    let indexArray = [];
    arr.forEach((elem, index) => {
       if (elem === val) {
             indexArray.push(index);
       } 
    })
return indexArray;  
  }
 ```
 
#### 17. Create a method named last It accepts an array as an argument.It returns the last element of a list.

#### Answer:


```javascript
 function last(arr) {
  let newArray = arr.slice(-1);
  return newArray; 
 }
 ```
 #### Detail:
  The first element has an index of 0. Use negative numbers to select from the end of an array. An integer that specifies     where to end the selection. If omitted, all elements from the start position and to the end of the array will be selected.   Use negative numbers to select from the end of an array.
 
 #### 18.Create a method named reverse It accepts an array as an argument.It returns the new array but elements in reversed order.

#### Answer:

###### Using for loop
```javascript
function reverse(arr) {
    let newArray=[];
  for (var i=0, j=arr.length-1 ; i < arr.length ; i++,j--) {
           newArray[i] = arr[j];
       }
    
    return newArray;
}
```
###### Using reverse method

```javascript
function reverse(arr) {
    return arr.reverse();
}
```
 #### 19.Create a method named randomIt accepts an array as an argument.It returns a random element from the given array.

#### Answer:

```javascript
function random(arr) {
   return arr[Math.floor(Math.random() * arr.length)];
}
```

#### 20.Apply method without arguments.

#### Answer:

```javascript
var person = {
      fullName: function() {
          return this.firstName + " " + this.lastName;
      }
  }
  var person1 = {
  firstName: "Mary",
  lastName: "Doe"
  }
  var x = person.fullName.apply(person1); 
  document.getElementById("demo").innerHTML = x;
```
#### Detail:
With the apply() method, you can write a method that can be used on different objects.


#### 21.Apply method with arguments.

#### Answer:

```javascript
let customer1 = { name: 'Leo', email: 'leo@gmail.com' };
let customer2 = { name: 'Nat', email: 'nat@hotmail.com' };
function greeting(text, text2) {
   console.log(`${text} ${this.name}, ${text2}`);
}
greeting.apply(customer1, ['Hello', 'How are you?']); // output Hello Leo, How are you?
greeting.apply(customer2, ['Hello', 'How are you?']); // output Hello Natm How are you?
```
#### Detail:
The apply() method takes arguments as an array.The apply() method is very handy if you want to use an array instead of an argument list.


#### 22.Call method without arguments.

#### Answer:

```javascript
var personA = {
        fullPersonName: function() {
        return this.firstName + " " + this.lastName;
    }
}
  var person2 = {
  firstName:"John",
  lastName: "Doe"
  }
  var y = personA.fullPersonName.call(person2); 
  document.getElementById("demo").innerHTML = y;
  
```
#### Detail:
The call() method is a predefined JavaScript method.
It can be used to invoke (call) a method with an owner object as an argument (parameter).With call(), an object can use a method belonging to another object.


#### 23.Call method with arguments.

#### Answer:

```javascript
let customer1 = { name: 'Leo', email: 'leo@gmail.com' };
let customer2 = { name: 'Nat', email: 'nat@hotmail.com' };

function greeting(text) {
    console.log(`${text} ${this.name}`);
}

greeting.call(customer1, 'Hello'); // Hello Leo
greeting.call(customer2, 'Hello'); // Hello Nat
  
```
#### Detail:
The difference is:
The call() method takes arguments separately.
The apply() method takes arguments as an array.


#### 24.Write all possible ways to clone a JavaScript object.Also provide examples.After clone the new object should not have reference to old object. It should be a deep copy.

#### Answer:

###### Converting to JSON and back

```javascript          
function jasonCopy(src) {
    return JSON.parse(JSON.stringify(src));
      }
   const source = {a:1,b:2,c:3};
   const target = jasonCopy(source);
   console.log(target);

// Check if clones it and not changing it
   source.a = 'a';
   console.log(source.a);
   console.log(target.a);
Detail:
The JSON object, available in all modern browsers, has two very useful methods to deal with JSON-formatted content: parse and stringify. JSON.parse() takes a JSON string and transforms it into a JavaScript object. JSON.stringify() takes a JavaScript object and transforms it into a JSON string.
Be careful about using this method as your source object must be JSON safe. So it may need some sort of exception handling to keep it safe in cases in which the source object is not convertible to JSON.

// Object.assign:

function bestCopyEver(src) {
  return Object.assign({},src);
  }

const newSource = {d:4,e:5,f:6};
const newTarget = bestCopyEver(source);
console.log(target);

//Check if clones it and not changing it
 
newSource.d = 'd';
console.log(newSource.d);
console.log(newTarget.d);

Detail:
The Object.assign() method can be used to copy the values of all enumerable own properties from one or more source objects to a target object, and it will return the target object.

// Spread Operator:
 This one is shortest and simple method to copy/merge an object. See below example:

var obj = { foo: "foo", bar: "bar" };
var clonedObj = { ...obj };
// Object { foo: "foo", bar: "bar" } 
```

#### 25.Write a method which reverse the key and values in an object.After reversal the keys will be values and values will be keys.

#### Answer:

```javascript
function reverseObject(obj) {
    var array = Object.entries(obj)
    var convert = array.map( arr => ({[arr[1]]:arr[0]}));
    let output = Object.assign(...convert);
    return output;
}  
```
#### Detail:
First we have use Object.entries() method to convert object into array to use .map method and then converted key into value and value into key and in return we used Object.assign() and used (...) spread operator on convert to show multiple objects in one object.


#### 26.Write a function that takes a string as argument and returns the number of vowels contained in that string.

#### Answer:

```javascript
function findVowels(str) {
  let vowelCount = 0; 
  for (i=0; i< str.length; i++){
      if(str.toLowerCase()[i] == 'a' | str.toLowerCase()[i] == 'e' | str.toLowerCase()[i] == 'i' | str.toLowerCase()[i] == 'o' | str.toLowerCase()[i] == 'u')
      {
          vowelCount++;
      }
}
  return vowelCount;               
}  
```

#### 27.You've got chickens (2 legs), cows (4 legs) and pigs (4 legs) on your farm. Return the total number of legs on your farm.

#### Answer:

```javascript
function animals(chickens,cows,pigs) {
    return chickens*2 + cows*4 + pigs*4;
}  
```

#### 28.Anagram (A word is an anagram of another word if both use the same letters in the same quantity, but arranged differently.Create a method named Anagram It accepts two words as an argument. It returns true if A word is an anagram of another word otherwise returns false.

#### Answer:

```javascript
function anagram(word1,word2) {
    let wrd1Array = word1.split("").sort().join("");
    let wrd2Array = word2.split("").sort().join("");

    return wrd1Array === wrd2Array;
}  
```

#### Detail:
So we start by running the split() string method on our string. This will turn our word into an array by breaking it up after each letter.sort() uses the sort() array method to alphabetically sort that array of letters.Lastly we take our array of alphabetized letters and smush them back together into a string using the join() array method.
#### Note:
Using split() method with argument split("") will sperate the string charactierwise with comma for example: // ["w","o","r","d"] and without argument split() wil give // ["word"].
The join() method returns the array as a string.
The elements will be separated by a specified separator. The default separator is comma (,) bu using join("") argument.


#### 29.The problem can be stated along the following lines: given a string, return true if the string is a palindrome and false if it isn’t. Include spaces and punctuation in deciding if the string is a palindrome.

#### Answer:

```javascript
function palindrome(str) {
    let reverseStr = str.toLowerCase().replace(/\s/g, '').split("").reverse().join("");
    let lowCase = str.toLowerCase().replace(/\s/g, '');
    if (lowCase === reverseStr){
        return true;
    }
    return false;
}  
```

#### 30.Given an array A of N distinct and positive elements, the task is to find number of unordered pairs whose sum already exists in given array.

#### Answer:

```javascript
function unorderedSum(arr) {
  let count = 0;
     for(i=0 ; i < arr.length-1; i++){
         for(j=0; j < i; j++){
             let result = arr[i] + arr[j];
             if(arr.find(elem  => elem  === result)){
                 count++;
             }
         }
     }
     return count;
 }  
```
#### 31.Write a function that returns the nth entry in the Fibonacci sequence, where n is a number you pass in as argument to the function.

#### Answer:

```javascript
function fibonacci(n) {
   if (n == 0) {
       return 0;
   }
   if (n == 1) {
       return 1;
   }else{
     return  fibonacci(n-1) + fibonacci(n-2);
   }
}  
```

#### 32.Give a string and a number n you have to rotate the string right n times

#### Answer:

```javascript
function keepRotating(str,n) {
    var reverseStr = '';
    var newStr = str.slice(0, str.length-n);
    reverseStr = str.slice(str.length-n)
    return reverseStr+newStr;
}  
```
#### 33.Using recursion print an array in reverse order

#### Answer:

```javascript
function printReverseRecursive (array) {
    var output = [];
    if (output.length===array.length) {
        return output;
    } else {
        var reversedArray = output.concat(printReverseRecursive(array.slice(1)),array[0]);
        reversedArray.forEach((elem) => {
            console.log (elem); 
        }) 
    }
};  
```

