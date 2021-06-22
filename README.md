# Tasks
# This file contain tasks that has been assigned in the weekday classes B251 WD

# Tasks on 14 and 15 June
#  Difference between HTTP 1.0 and HTTP 2.0
1. Spead of webpage loading is greatly enhanced with single TCP stream form HTTP request transfer.
2. HTTP 2.0 provides secure data transfer 'https' mandatory.
3. HPAC allows to compress header data, and enable to reuse in subsequent request.
4. PUSH allows to send js and css files along with response.
5. HTTP 2.0 is backward compatible.

# Difference between browser JS engine and nodejs
1. Browser js engines were developed based on OS platforms.
2. node js is working on V8 engine.
3. node js enable javascript functionality explored without browser support.
4. node js enable testing javascript for backend applications.
5. window and document are missing when compared with browser js engine.

# Tasks on 16 June
# Typeof()
  In javascript typeof() syntax gives nature of the variable
  
  For example 
  
```ruby
 console.log("typeof(1) gives " + typeof(1) + " as output"); 

//  typeof(1) gives number as output
 
console.log("typeof(1.1) gives " + typeof(1) + " as output"); 

// typeof(1.1) gives number as output

console.log("typeof(true) gives " + typeof(true) + " as output"); 

// typeof(true) gives boolean as output

console.log("typeof(null) gives " + typeof(null) + " as output"); 

// typeof(null) gives object as output. It is a bug. But still kept as such for legacy resons

console.log("typeof(undefined) gives " + typeof(undefined) + " as output"); 

// typeof(undefined) gives undefined as output. It is primitive data type

console.log("typeof([]) gives " + typeof(1) + " as output"); 

// typeof([]) gives object as output  

console.log("typeof(NaN) gives " + typeof(NaN) + " as output"); 

// typeof(NaN) gives number as output because it is some type of values resulted from calculations like 0/0

console.log("typeof({}) gives " + typeof({}) + " as output");  

// typeof({}) gives object as output
  ```
  
# Differeces between HTML Tags div article and section
   
        These are html tags used to group the content together
       
    <section> and <article>
    
           content should contain heading h1,h2,h3 like that
           content together shoud make sense
  
    <article>
    
           content shoulb be standalone
    
    <div>
    
           Everything else can be grouped under <div> like lists, links etc.
           

# Create simple portfolio in HTML
```ruby
<!doctype html>
<html>
    <head>
        <title>My First Portfolio ~ Gnanakkumaar P</title>
    </head>
    <body>
        <h1>P.Gnanakkumaar Phd</h1>
        <p>Email: pgnanakkumaar@gmail.com</p>
        <p> Biochemist, Reseacher in Nueroinformatics, Systembiologist, upcoming FullStackDeveloper</p>
        <br>
        <h2>Skills</h2>
            <ul>
                <li>Gene expression analysis</li> <br>
                <li>Biostatistics</li> <br>
                <li>Large data handling with R program</li> <br>
                <li>Natural language processing</li> <br>
                <li>Programming languages Python, R, MySQL, Javascript </li>

            </ul>
        <h2>Publication</h2>
       
        <p><b>Gnanakkumaar, P.</b>, Murugesan, R. & Ahmed, S.S.S.J. Gene Regulatory Networks in Peripheral 
        Mononuclear Cells Reveals <br>Critical Regulatory Modules and Regulators of Multiple Sclerosis. 
        <br><i>Sci Rep</i> 9, 12732 (2019). 
        <a href="https://doi.org/10.1038/s41598-019-49124-x">https://doi.org/10.1038/s41598-019-49124-x</a></p>
    </body>
</html>
```
  
# Date 17.06.2021 Tasks

# For loops on array of objects
```ruby
var obj = [
    { person: "Name 1", age: "2", company: "GUVI" },
    { person: "Name 2", age: "5", company: "GUVI geek" },
    { person: "Name 3", age: "8", company: "GUVI geek network" },
  ]
// for in loop

for (var i in obj) {  // i holds first obj in array
    for (var j in obj[i]) { // j hold properties of first object
        console.log(j,":", obj[i][j])
    }
}
// output as follows
person : Name 1
age : 2
company : GUVI
person : Name 2
age : 5
company : GUVI geek
person : Name 3
age : 8
company : GUVI geek network

obj.forEach(function(val){
    console.log(Object.keys(val).join(" "))
    console.log(Object.values(val).join(" "))
})

// output as follows
person age company
Name 1 2 GUVI
person age company
Name 2 5 GUVI geek
person age company
Name 3 8 GUVI geek network

// for of loop
for (let i of obj) {
    for (let j of i) // i is not iterable
    console.log(j)
} // throughs type error i &  j is not iterable
```
# REST country JSON
```ruby
for (let i in obj) {
     console.log(`RESTapi country name ${obj[i].name}, Region ${obj[i].region} and Subregion of ${obj[i].subregion}. This country's population ${obj[i].population} and the national flag link is ${obj[i].flag}`)
    
}

RESTapi country name Afghanistan, Region Asia and Subregion of Southern Asia. This country's population 27657145 and the national flag link is https://restcountries.eu/data/afg.svg
```
# 18.06.2021
# myResume in JSON format
```ruby
[
    {"title": "Reusme in JSON Format"},
    {"Name": "Gnanakkumaar P", "email" : "pgnanakkumaar@gmail.com"}, 
    {"AboutMe":["Biochemist", "Reseacher in Nueroinformatics", "Systembiologist",
         "upcoming FullStackDeveloper"]},
    {"Skills":["Gene expression analysis", "Biostatistics","Large data handling with R program",
        "Natural language processing"]},
        {"programming languages known": ["R", "Python", "mySQL","JavaScript"]
         },
    {"Publications": "Gnanakkumaar, P., Murugesan, R. & Ahmed, S.S.S.J. Gene Regulatory Networks in Peripheral Mononuclear Cells Reveals Critical Regulatory Modules and Regulators of Multiple Sclerosis. Sci Rep 9, 12732 (2019). 'https://doi.org/10.1038/s41598-019-49124-x'"}
        
]
```
# Comparing JSON objects without order

```ruby

var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };

let flag = true;

if(Object.keys(obj1).length==Object.keys(obj2).length) {
    for (key in obj1) {
        if(obj1[key] == obj2[key]) {
            continue;
        }
        else {
            flag=flase;
            break;
        }
    }
}
else {
    flag=false;
}
console.log("is object equal? " + flag);
```

# 21.06.2021
# warmup functions
```ruby

 // addFive
var num = 10;
function addFive(num) {
    var result = num + 5;
    return result; 
    // console.log(result); 
}
console.log(addFive(13));
// getOpposites

// var num = 5.0;
// console.log(Number.isInteger(num));
function getOpposite(val) {
    if (((typeof val) === 'string') || (Number.isInteger(val) === false)) {
        console.log(-1);
    } else if ((typeof val) === 'number') {
        console.log(val * -1);
    }
}
getOpposite(5.0);



// toSeconds
var num = 5;
function toSeconds(min) {
    if (typeof min === 'number') {
        console.log(min *  60);

    }
    
}
toSeconds(3);


// toInteger

var myStr = "5";
function toInteger(myStr) {
    console.log(parseInt(myStr));
}
toInteger('8');

// nextNumber
var myInt = 0;

function nextNumber (myInt) {
    console.log(myInt + 1);
}
nextNumber(5);


// getFirstElement

function getFirstElement(arr) {
    console.log(arr[0]);
}
getFirstElement([-32, 2, 3, 5]);

// hourToSeconds
function hoursToSeconds(hr) {
    if ((typeof hr) === obj ) {
    for(let i = 0; i < hr.length; i++)
    console.log(+hr[i] * 60 * 60);}
    else {
        console.log(+hr * 60 * 60)
    }
}
// var arr = [1, 2, 3];

hoursToSeconds(arr);


// findPerimeter
function findPerimeter(num1, num2) {
    console.log(num1 * num2);
}
findPerimeter(6,9);

// lessThan100
function lessThan100(num1, num2) {
    if ((num1 + num2) < 100) {
        console.log(true);
    } else {
        console.log(false);
    }
}
lessThan100(93, 45);

// reminder
function remainder(num1, num2) {
    console.log(num1 % num2)
}
remainder(51,10);

// countAnimals
function countAnimalsLegs(tur, horse, pigs) {
    console.log((tur*2) + (horse *4) + (pigs*4))
}
countAnimalsLegs(2,3,5);

// framesPerSecond
function framesPerSecond(num1, num2) {
    console.log(num1*60 * num2);
}
framesPerSecond(10,25);

// divisibleByFive
function divisibleByFive(num) {
    if (num % 5 === 0) {
        console.log(true)
    } else {
        console.log(false)
    }
}
divisibleByFive(5);
divisibleByFive(-55);
divisibleByFive(37);

// isEven
function isEven(num) {
    if((typeof num) === 'string') {
        console.log(-1);
    }
    else if (num % 2 === 0) {
        console.log(true);
    } else {
        console.log(false);
    }
}
isEven(12);
isEven(0);
isEven(11);
isEven('11h');

// areBothOdd
function areBothOdd(num1,num2) {
    if((num1%2 !== 0) && (num2%2 !== 0)) {
        console.log(true);
    } else {
        console.log(false);
    }
}
areBothOdd(1,3);
areBothOdd(1,4);
areBothOdd(2,3);
areBothOdd(0,0);

// getFullName
function getFullName(firstName,lastName) {
    console.log(firstName + " " + lastName);
}
getFullName("GUVI", "GEEK");
getFullName("GUVI",);
getFullName(",", "GEEK");
getFullName('""','""');

// getLengthOfWord

function getLengthOfWord(str) {
    if((typeof str === "number") || (str === undefined)) {
        console.log(-1);
    } else {
        console.log(str.length);
    }

}
getLengthOfWord("GUVI");
getLengthOfWord("");
getLengthOfWord();
getLengthOfWord(9);

// isSameLength
function isSameLength(word1, word2) {
    if(word1.length === word2.length) {
        console.log(true)
    } else {
        console.log(false);
    }
}
isSameLength("GUVI","GEEK");

// getNthElement
function getNthElement(array, n) {
    console.log(array[n]);
}
getNthElement([1, 3, 5], 2);

// getLastElement
function getLastElement(array) {
    console.log(array.pop());
}
getLastElement([1,2,3,4]);
 
// getProperty

var obj = {
    mykey: "value"
};
 
var getProperty = function getProperty(obj, key) {
    console.log(obj[key]);
}
getProperty(obj, 'mykey');
// getProperty(obj, 'dummykey');

// add property

let addProperty = function addProperty(obj, key) {
    obj[key] = 'true'
    console.log(obj[key]);
}

addProperty(obj, 'myname');

// remove property

let removeProperty = function removeProperty(obj, key) {
    delete obj[key];
    console.log(obj);
}

removeProperty(obj, 'myname');

// getPositives

let ar = [-5, 10, -3, 12, -9, 5, 90, 0, 1];

let getPositives = function getPositives(arr) {
    let temp = [];
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] >= 0) {
            temp.push(arr[i]);
        }
    }
    return temp;
}



let ar2 = getPositives(ar);
console.log(ar2);

// powersOfTwo

function powersOfTwo(n){
    let res = 2**n;
    return res;
}

console.log(powersOfTwo(5));

// findMax
function findMax(ar)
{
  let temp = Math.max(...ar);
  return temp;
}
var ar = [-5, 10, -3, 12, -9, 5, 90, 0, 1];
var max = findMax(ar);
console.log("Max: ", max);



// printPrimeNumbers

function printPrimeNumbers(n) {
    let temp = [];
    for (let i = 1; i <= n; i++) {
        if (i % 2 !== 0) {
            temp.push(i);// console.log(i);
        }
    }
    return temp;
}
console.log(printPrimeNumbers(100));

function isPrime(n) {
    if (n % 2 == 0) {
        console.log(false);
    } else {
        console.log(true)
    }
}

isPrime(36);



// reverse a string

var s = reverseString("JavaScript");
console.log(s);
function reverseString(s)
{
    let temp = "";
   for (let i = s.length - 1; i >= 0; i--) {
        temp += s[i];
   }
   return temp;
}

function mergeArrays(arr1, arr2) {
    return [...arr1,...arr2];
}

let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];

console.log(mergeArrays(arr1, arr2));

console.log(sumCSV('1.5, 2.4, 3.1, 4, 5.5, 6, 7, 8, 9, 10.9'));
function sumCSV(s)
{
  let sum = 0;
  let arr = s.split(",").map(Number);
  for (let i = 0; i < arr.length; i++) {
        sum += i;
  }
  return sum;
}

```


