# Java-Script-Problems

### ***Find Similar and Dissimilar items in below array of Objects***

```js
let Ar1 = [
  {
    id: "1",
    name: "Harman",
  },
  {
    id: "2",
    name: "Priya",
  },
  {
    id: "3",
    name: "Vikas",
  },
];

let Ar2 = [
  {
    id: "2",
    name: "Priya",
  },
  {
    id: "3",
    name: "Vikas",
  },
];
```
<details><summary><b>Answer</b></summary>
<p>

  ```javascript
const ArSimilar = [];
const Ardissimilar = [];

for (let i = 0; i < Ar1.length; i++) {
  
  for (let j = 0; j < Ar2.length; j++) {
    
    if (Ar1[i].id === Ar2[j].id) {
      ArSimilar.push(Ar1[i]);
      break;
    }

  }
  const findInArSimilar = ArSimilar.find(data => data.id === Ar1[i].id);
  if(findInArSimilar === undefined){
      Ardissimilar.push(Ar1[i]);
  }
} 

console.log("Similar Items", ArSimilar);
console.log("Dissimilar Items", Ardissimilar);
```

  
</p>
</details>

### ***Write JS function to calculate total toll charges need to pay to all the tolls where at each toll the charge will get double from previous toll charges. This function accepts NoOfTolls and Charges at Initial Toll***

<details><summary><b>Answer</b></summary>
<p>

```javascript
  const calculateTollCharges= (noOfTolls,initialCharges) =>{
  let prevCharges=initialCharges;
  let chargesForEachToll =[];
  for(let i=1;i<=noOfTolls;i++){
    prevCharges = prevCharges*2
    chargesForEachToll.push(prevCharges);
  }
  console.log(chargesForEachToll);
  const totalCharges = chargesForEachToll.reduce((aggregate,data)=>aggregate+data,0);
  console.log(totalCharges);
}
calculateTollCharges(4,100);
```

  
</p>
</details>

### ***Write JS function to calculate the color of tiles using the Array of Colors and each tile will have those colors sequentially.***

<details><summary><b>Answer</b></summary>
<p>

```javascript
let colors=['red','blue','pink','yellow'];
let tileColor = (tileNumber)=>{
let indexOfColor = tileNumber % colors.length;
  console.log(colors[indexOfColor-1]);
}
tileColor(10);
```
  
</p>
</details>


### ***Write JS function to find largest number in Array.***

<details><summary><b>Answer</b></summary>
<p>

```javascript
const largestNumber = (arr)=>{
arr.sort((a,b)=>a-b);
console.log(arr[arr.length -1]);
}
largestNumber([10,8,9,11,2,100,3]);
```
  
</p>
</details>

### ***Write JS function to find smallest number in Array.***

<details><summary><b>Answer</b></summary>
<p>

```javascript
const largestNumber = (arr)=>{
arr.sort((a,b)=>b-a);
console.log(arr[arr.length -1]);
}
largestNumber([10,8,9,11,2,100,3]);
```
  
</p>
</details>

### ***Write JS function to return key of objects in the comma seperated value***
```javascript
var student = {
    name : "David Rayy",
    sclass : "VI",
    rollno : 12 };
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const findKey =(obj)=>{
    const keys = Object.keys(obj);
    console.log(keys.join(','));
}
findKey(student);
```
  
</p>
</details>


### ***Find the store in the given array which are open stores***
```javascript
let StoreOBJ = {
    Store1 :"Open",
    Store2: "Closed",
    Store3: "Open",
    Store4: "Closed",
    Store5: "Open",
    Store6: "Closed",
}
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const findKeyEnteries =(obj)=>{
const openStore =[];
for(const [key,value] of Object.entries(obj)){
    if(value==="Open" ){
        openStore.push(key);
    }
}
console.log(openStore);
}
findKeyEnteries(StoreOBJ);

```
  
</p>
</details>

### ***Write a program to delete the key of object. For eg rollno in given snipet***
```javascript
var student = {
    name : "David Rayy",
    sclass : "VI",
    rollno : 12 };
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
var student = {
    name : "David Rayy",
    sclass : "VI",
    rollno : 12 };
let objkey = "rollno";
const deleteKey = (obj,objkey) =>{
    delete obj[objkey]; 
    console.log(student);
}
deleteKey(student,objkey);
```
  
</p>
</details>

### ***Write a program to find th length of object.***
```javascript
var student = {
    name : "David Rayy",
    sclass : "VI",
    rollno : 12 };
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const objLength = (obj) =>{
    let obsize = Object.keys(obj).length;
    console.log(obsize);
}
objLength(student);
```
  
</p>
</details>

### ***Display objects whose reading status true.***
```javascript
var library = [ 
    {
        author: 'Bill Gates',
        title: 'The Road Ahead',
        readingStatus: false
    },
    {
        author: 'Steve Jobs',
        title: 'Walter Isaacson',
        readingStatus: true
    },
    {
        author: 'Suzanne Collins',
        title:  'Mockingjay: The Final Book of The Hunger Games', 
        readingStatus: true
    }];
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
 const readingObj = library.filter((data)=>data.readingStatus===true);
 console.log(readingObj);
```
  
</p>
</details>

### ***Program to get the volume of a Cylinder with four decimal places using object classes.Volume of a cylinder : V = πr2h***


<details><summary><b>Answer</b></summary>
<p>

```javascript
 const findVolume = (height, radius)=>{
 console.log("Volume is : ",(Math.PI*(radius*radius)*height).toFixed(4));
}
findVolume(7,2);
```
  
</p>
</details>


### ***Check if input is an Array.***


<details><summary><b>Answer</b></summary>
<p>

```javascript
function is_aaray(arr){
    if(Array.isArray(arr)){
        return "true";
    }
    else
    return "false";
}
console.log(is_aaray([1, 2, 4, 0]));
```
  
</p>
</details>

### ***How can you do clone/copy of an array.***


<details><summary><b>Answer</b></summary>
<p>

```javascript

function clone(arr){
    clonedArr = [...arr];
    console.log("Cloned Array",clonedArr);
    clonedArr1 = arr.slice(0,arr.length);
    console.log("Cloned Array1",clonedArr1);
}
clone([1,2,3,4,5]);
```
  
</p>
</details>

### ***Accept a number as input and insert dashes (-) between each two even numbers.For example if you accept 025468 the output should be 0-254-6-8.***


<details><summary><b>Answer</b></summary>
<p>

```javascript
  function applyDash(num){
    const numarray = num.toString().split("");
    const newArr =[];
    for(let i=0;i<numarray.length;i++){
        if(numarray[i]%2===0 && numarray[i-1]%2===0){
            newArr.push("-",numarray[i]);
        }
        else{
            newArr.push(numarray[i]);
        }
    }
    console.log(newArr.join(""));
}
applyDash(9654256880);
```
  
</p>
</details>

### ***Write a JavaScript program to display the current day and time in the following format.  Go to the editor Sample Output : Today is : Tuesday.Current time is : 10 PM : 30 : 38***

<details><summary><b>Answer</b></summary>
<p>

```javascript
const date = new Date();
const dayArr = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"]; 
//get Day returns number so we have to pass day
console.log("Today is :",dayArr[date.getDay()]);
let Hour = date.getHours();
const minutes = date.getMinutes();
const seconds = date.getSeconds();
Hour = Hour>=12 ? Hour -12 : Hour;
prepend = Hour>=12? "PM": "AM";
console.log("Current time is :", Hour,prepend ,":",minutes,":",seconds);
```
  
</p>
</details>

### ***How will you print the contents of the current window***

<details><summary><b>Answer</b></summary>
<p>

```javascript
console.log(window.print());
```
  
</p>
</details>

### ***Write a JavaScript program to get the current date.***

<details><summary><b>Answer</b></summary>
<p>

```javascript
const date = new Date();
console.log(date);
console.log(date.getDate()+'-'+(date.getMonth()+1)+'-'+date.getFullYear());
```
  
</p>
</details>


### ***Write a Bubble Sort algorithm in JavaScript.Note : Bubble sort is a simple sorting algorithm that works by repeatedly stepping through the list to be sorted.Sample Data: [6,4,0, 3,-2,1] Expected Output : [-2, 0, 1, 3, 4, 6]***

<details><summary><b>Answer</b></summary>
<p>

```javascript
const bubbleSort = (arr) =>{
    for(let i=0;i<arr.length;i++){
        for(let j=0;j<arr.length;j++){
            if(arr[j]>arr[j+1]){
                var temp =arr[j];
                arr[j] =arr[j+1];
                arr[j+1] =temp;
        }
    }
    }
console.log(data);
}
 const data = [6,4,0, 3,-2,1];
 bubbleSort(data);
```
  
</p>
</details>



### ***Write a JavaScript program which returns a subset of a string. Go to the editor. Sample Data:dog.Expected Output: ["d", "do", "dog", "o", "og", "g"]***

<details><summary><b>Answer</b></summary>
<p>

```javascript
const data = "priyanshi";
function subsetString(data){
    const output =[];
    for(let i=0;i<data.length ;i++){
        for(let j=i+1;j<data.length+1;j++){
            output.push(data.slice(i,j));
        }
    }
    console.log(output);
}
subsetString(data);
```
  
</p>
</details>

### ***Write a JavaScript program to sort an array of JavaScript objects based on its LibraryID. Sample Object :***
```javascript
var library = [ 
   {
       title:  'The Road Ahead',
       author: 'Bill Gates',
       libraryID: 1254
   },
   {
       title: 'Walter Isaacson',
       author: 'Steve Jobs',
       libraryID: 4264
   },
   {
       title: 'Mockingjay: The Final Book of The Hunger Games',
       author: 'Suzanne Collins',
       libraryID: 3245
   }];

```

<details><summary><b>Answer</b></summary>
<p>

```javascript
let res =library.sort((a,b)=>{
    if(a.libraryID>b.libraryID){
    return -1;
    }else if(a.libraryID<b.libraryID){
        return 1;
    }
    else{
        return 0;
    }

})
console.log(res);
```
  
</p>
</details>



### ***Write a JavaScript program to find the most frequent item of an array. Go to the editor. Sample array : var arr1=[3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];Sample Output : a : 5 times***

<details><summary><b>Answer</b></summary>
<p>

```javascript
var arr1=[3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];
function itemFrequecy(arr){
let obj = {};
    for(let i=0;i<arr.length;i++){
        if(obj.hasOwnProperty(arr[i])){
            obj[arr[i]] += 1 ;
        }
        else{
            obj[arr[i]]= 1;
        }
    }
    let hightkey;
    let hightvlaue;
    console.log(obj);
    for (const [key,value] of Object.entries(obj)) {
        if(hightkey===undefined && hightvlaue===undefined){
            hightkey=key;
            hightvlaue=value;
        }else{
            if(hightvlaue<value){
            hightkey=key;
            hightvlaue=value;
            }
        }
    }
 console.log(hightkey ,":", hightvlaue,"times");
}
itemFrequecy(arr1);
```
  
</p>
</details>

### ***Write a JavaScript program to return a new Array by making the value of name property in uppercase***

```js
const arr = [{
    name:"harman",
    rollno:12
},
{name:"Priya",
rollno:20
},
{name:"chulli",
rollno:4
}] 
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const newarr=[];
for(let i=0;i<arr.length;i++){
    const newobj={...arr[i]};
    newobj.name = newobj.name.toUpperCase();
    newarr.push(newobj);
}
console.log(arr);
console.log(newarr);
```
  
</p>
</details>

### ***In the below object find the employees having experience up to 5 years, having exp between 6-9 and having exp greater than 12.***

```js
const arr =[
        {
         name:"harman",
         yearofexp:14
        },
        {name:"Priya",
        yearofexp:20
        },
        {name:"chulli",
        yearofexp:18
        },
        {name:"chulli",
        yearofexp:19
        },
        {name:"chulli",
        yearofexp:8
        },
        {name:"chulli",
        yearofexp:9
        },
        {name:"chulli",
        yearofexp:2
        },
        {name:"chulli",
        yearofexp:3
        },
        {name:"chulli",
        yearofexp:4
        }      
        
]
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
let countupto5 = 0;
let countfrom6to9 =0;
let countmorethan12=0;
for(let i=0;i<arr.length;i++){
    if(arr[i].yearofexp>0 && arr[i].yearofexp<=5 ){
        countupto5++;
    }else if(arr[i].yearofexp>5 && arr[i].yearofexp<=9 ){
        countfrom6to9++;
    }else if(arr[i].yearofexp>12){
        countmorethan12++;
    }
}
console.log("Employees up to 5 yrs Exp",countupto5);
console.log("Employees betwwen 6 to 9 yrs Exp",countfrom6to9);
console.log("Employees more than 12 yrs Exp",countmorethan12);
```
  
</p>
</details>
  
### ***Write a JavaScript program to compare two objects***

```js
const obj1 = {
    name: "Priyanshi",
    rollno1:"21",
    class:"BE",
    depart:"mm"
}

const obj2 = {
    name: "Priyanshi",
    depart:"mm",
    rollno:"20",
    class:"BE",
    pachu :"rik"
}
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
let isSame=true;
for(const [key,value] of Object.entries(obj2)){
   // if(key in obj2){
       if(obj5.hasOwnProperty(key)){
        if(obj5[key]!==value){
            isSame=false;
            break;
        }
    }
    else{
        isSame=false;
        break;
    }
}
isSame ? console.log("Obj are Same") : console.log("Obj are not Same");
```
  
</p>
</details>

  ### ***Write a JavaScript function that reverse a number.Example x = 32243,Expected Output : 34223***

<details><summary><b>Answer</b></summary>
<p>

```javascript
  const reverseNumber = (num) =>{
    let numArray = JSON.stringify(num).split('');
    let reversedNum = [];
    for(let i=numArray.length-1;i>-1;i--){
        reversedNum.push(numArray[i]);
    }
    console.log(reversedNum.join(""));
    //return reversedNum.join("");
}
reverseNumber(34223);
```
  
</p>
</details>
  
 ### ***Write a JavaScript function that checks whether a passed string is palindrome or not? A palindrome is word, phrase, or sequence that reads the same backward as forward, e.g., madam.***
  
  <details><summary><b>Answer</b></summary>
<p>

```javascript
 const checkPalindrome =(name)=>{
let reversedName="";
for(let i=name.length-1 ;i >-1; i--){
    reversedName = reversedName+name[i];
}
console.log(reversedName);
(reversedName===name) ? console.log("String is Palindrome") : console.log("Not a Palindrome");
}
checkPalindrome("madam");
```
  
</p>
</details>
  
### ***Write a JavaScript function that accepts a string as a parameter and find the longest word within the string.Example string : 'Web Development Tutorial'.Expected Output : 'Development'***
  

  <details><summary><b>Answer</b></summary>
<p>

```javascript
 const findLargestNumber = (sent) =>{
    const eachWord = sent.split(" ");
    let largestLength = 0;
    let largestWord = "";
    for(let i=0;i<eachWord.length;i++){
        if(largestLength < eachWord[i].length){
            largestLength = eachWord[i].length;
            largestWord = eachWord[i];
        }
    }
    console.log(largestWord);
}
findLargestNumber('Web Development Lecture');
```
    
</p>
</details>
  
### ***Write a JavaScript function that accepts a string as a parameter and counts the number of vowels within the string.***
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
const vowelsCount =(sentance)=>{
    let lowercaseSentance = sentance.toLowerCase();
    let count =0;
    
    for(let i=0;i<lowercaseSentance.length;i++){
        if(lowercaseSentance[i]==='a' ||lowercaseSentance[i]==='e'||lowercaseSentance[i]==='i'||lowercaseSentance[i]==='o'||lowercaseSentance[i]==='u')
        count++;
    }
console.log(count);
}

vowelsCount('The quIck brOwn fox');
```
    
</p>
</details>

### ***Write a JavaScript function that accepts a object as a parameter and returns a deep cloned Object. Example Object :***
```javascript
const obj = {
username:"Priyanshi",
rollno:20,
getUserDateils:()=>{
    const fncObj = {
        username : "Harman"
    }
    return fncObj;
},
subjects: {
    sub1: "math",
    sub2:"science",
    sub3:"business"
} 
}
```
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
const deepClone = (obj)=>{
    const clonedObject ={};
    for(const [key,value] of Object.entries(obj)){
        if(typeof value === 'object' && value !==null){
            clonedObject[key]=deepClone(value);
        }
        else{
            clonedObject[key] = value;
        }
    }
return clonedObject;
}

const newObj=deepClone(obj);
console.log(newObj);
```
  
</p>
</details>
  
### ***Write a JavaScript function that Implements enqueue and dequeue using only two stacks only pop ,push can be used.***

<details><summary><b>Answer</b></summary>
<p>
  
```javascript
let inputStack = [];
let outputStack = [];

const enque = (stackInput , item) =>{
  stackInput.push(item);
  console.log(stackInput);
  return stackInput;
} 

const dequeue = (inputStack , outputStack) =>{

    if(outputStack<=0){
        for(let i=inputStack.length-1;i>-1;i--){
            outputStack.push(inputStack[i]);
        }
    }

    console.log(outputStack.pop());
 //   return outputStack.pop();

}

enque(inputStack,12);
enque(inputStack,19);
enque(inputStack,15);

dequeue(inputStack,outputStack);
dequeue(inputStack,outputStack);
dequeue(inputStack,outputStack);

```
    
</p>
</details>
  
### ***Write a JavaScript function that takes array of Object and retrun total no of properties value count in object form Sample :var arr = [{age:10},{age:20},{age:10},{age:80},,{age:20},{age:80},{age:80},{age:10}]***
  Output : obj ={
    10 :3,
    20 :2,
    80:3
 }

<details><summary><b>Answer</b></summary>
<p>
  
```javascript
//Using ForEach
let obj={}
arr.forEach((data)=>{
    if(obj.hasOwnProperty(data.age)){
        obj[data.age]++;
    }
    else{
        obj[data.age] = 1;
    }
}
);
console.log(obj);
// Using Reduced 
const reducedobj = arr.reduce((aggregate,data)=>{
    console.log(aggregate);
    if(aggregate.hasOwnProperty(data.age)){
        aggregate[data.age] = aggregate[data.age]+1 ;
    }
    else{
        aggregate[data.age] = 1;
    }
    return aggregate;
},{});

console.log(reducedobj);

```
    
</p>
</details>
  
### ***Write a JavaScript function that accepts an array and returns array without holding duplicates***
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
const removeDuplicates = (arr) =>{
    arr.sort((a,b)=>a-b);
    const newArr = arr.filter((data,index)=>{
        if(arr[index]!==arr[index+1]){
            return arr[index];
        }
    }
    )
    console.log(newArr);
}

removeDuplicates(arr);
```
    
</p>
</details>

### ***Write a JavaScript function for multiply(2)(3)(4) function call***
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
  
function multiply(a){
    return function(b){
        return function(c){
            return a*b*c;
        }
    }
}
  
```
    
</p>
</details>
  
### ***Write a JavaScript function which acepts a string and produce the result in object of properties ahving every char and value as repeatation of that char Sample Input :const str = "Hello World"; Sample Output: {h:1, e:1, l:3, o:2, w:1, r:1, d:1}***
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
const outputObj = (str) =>{
const newStr = str.split('');
const newObj = newStr.reduce((aggregate, data)=>{
    if(data!==" "){
        if (aggregate.hasOwnProperty(data)){
            aggregate[data] = aggregate[data] +1;
        }
        else{
            aggregate[data]=1;
        }
    }  
return aggregate;
},{});
console.log(newObj);
}
outputObj(str);
```
</p>
</details>
  
### ***Write your own reduce function which will do exact same functionality as of Array's reduce function also that function should be abilable for any Array***
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
  const arr = [1, 2, 3, 4, 5, 6, 7];
 // Normal reduce function
const sum = arr.reduce((agg,data)=>{
return agg+data;
});
console.log(sum);
  // Custom Reduce Function 
//Callback Sum
const sumReducer = (initialValue,currentValue) => initialValue+currentValue;
//Callback Multiply
const multiplyReduce = (initialValue,currentValue) => initialValue*currentValue;
//Custom Reduced Functionality (reusable for any callback operation) 
Array.prototype.myReduce = function (reducerCallBack,initialValue) {
    let value = initialValue;
   for(let i=0;i<this.length;i++){
       value =(reducerCallBack(value,this[i]));
   }
   return value;
}
console.log(arr.myReduce(sumReducer,0));
console.log(arr.myReduce(multiplyReduce,1));

```
    
</p>
</details>
  
### ***Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.You may assume that each input would have exactly one solution, and you may not use the same element twice.You can return the answer in any order.Input: nums = [3,2,4], target = 6 Output: [1,2]***
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
  
  // Way 1 : complexity o(n^2)
  
  const outputIndex = (arr, target) =>{
    for(let i=0;i<arr.length;i++){
        for(let j=i+1;j<arr.length;j++){
            if(arr[i]+arr[j]===target){
                return [i,j];
            }else if(arr[j]===target){
                return [j];
            }else if(arr[i]===target){
                return [i];
            }
        }
    }
}

console.log(outputIndex([1,9,3,1],4));
  
  //Way 2 : complexity o(n)
  
const outputIndex = (arr,target)=>{
    for(let i=0;i<arr.length;i++){
        const diff = target - arr[i];
        const diffIndex = arr.indexOf(diff);
        //console.log(diff,diffIndex)
        if(diffIndex != i && diffIndex !=-1){
            return [i,diffIndex];        
        }else if(diff===0){
            return[i];
        }
    }
}
console.log(outputIndex([7,9,-2,-1],-3));

```
                                   
</p>
</details>
  
### ***Write a JavaScript function Counter in such a way that it will count the function context each time..For Eg.***
```js
const a = counter(); 
const b = counter(); 
console.log(a()); // output: 1
console.log(b()); // output: 1
console.log(a()); // output: 2
```
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
function counter() {
let count=0; 
   return function(){
       return count=count+1;
   }
}
// Second way bind
function counter() {
    this.count++;
    return this.count;
}
const obj1 = {
    count: 0
}
const obj2 = {
    count: 0
}
const a = counter.bind(obj1);
const b = counter.bind(obj2);

console.log(a()); // 1
console.log(b()); // 1
console.log(a()); // 2
  
```
  
</p>
</details>

  
### ***Write a JavaScript function to achieve below pattern***
```js
1
1 1 
1 1 1
1 1 1 1
```
  
<details><summary><b>Answer</b></summary>
<p>
  
```javascript
let n = 5;
for (let i = 0; i < n; i++) {
  let output = " ";
  for (let j = 0; j <= i; j++) {
    output = output + " 1";
  }

  console.log(output + "\n");
}
```
  
</p>
</details>
