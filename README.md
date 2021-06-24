# Tasks B251 WD
# Content
# Difference between HTTP 1.0 and HTTP 2.0
# Difference between browser JS engine and nodejs
# Typeof()
# Differeces between HTML Tags div article and section



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
```
//  typeof(1) gives number as output
```ruby 
console.log("typeof(1.1) gives " + typeof(1) + " as output"); 
```
// typeof(1.1) gives number as output
```ruby
console.log("typeof(true) gives " + typeof(true) + " as output"); 
```
// typeof(true) gives boolean as output
```ruby
console.log("typeof(null) gives " + typeof(null) + " as output"); 
```
// typeof(null) gives object as output. It is a bug. But still kept as such for legacy resons
```ruby
console.log("typeof(undefined) gives " + typeof(undefined) + " as output"); 
```
// typeof(undefined) gives undefined as output. It is primitive data type
```ruby
console.log("typeof([]) gives " + typeof(1) + " as output"); 
```
// typeof([]) gives object as output  
```ruby
console.log("typeof(NaN) gives " + typeof(NaN) + " as output"); 
```
// typeof(NaN) gives number as output because it is some type of values resulted from calculations like 0/0
```ruby
console.log("typeof({}) gives " + typeof({}) + " as output");  
```
// typeof({}) gives object as output
 
  
# Differeces between HTML Tags div article and section
   
        These are html tags used to group the content together
       
   ``` <section> and <article> ```
    
           content should contain heading h1,h2,h3 like that
           content together shoud make sense
  
    ```<article>```
    
           content shoulb be standalone
    
    ```<div>```
    
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
```
for (var i in obj) {  // i holds first obj in array
    for (var j in obj[i]) { // j hold properties of first object
        console.log(j,":", obj[i][j])
    }
}```

```
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
```
obj.forEach(function(val){
    console.log(Object.keys(val).join(" "))
    console.log(Object.values(val).join(" "))
})
```
// output as follows
person age company
Name 1 2 GUVI
person age company
Name 2 5 GUVI geek
person age company
Name 3 8 GUVI geek network
```
```
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
```

```
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

let equality = true;

if(Object.keys(obj1).length==Object.keys(obj2).length) {
    for (key in obj1) {
        if(obj1[key] == obj2[key]) {
            continue;
        }
        else {
            equality=flase;
            break;
        }
    }
}
else {
    equality=false;
}
console.log("is object equal? " + equality);
```

# 21.06.2021
# warmup functions


------------- addFive -------------
```ruby
var num = 10;
function addFive(num) {
    var result = num + 5;
    return result; 
}
console.log(addFive(13));
```
-------------- getOpposites -------------

``` ruby
var num = 5.0;
console.log(Number.isInteger(num));

function getOpposite(val) {
    if (((typeof val) === 'string') || (Number.isInteger(val) === false)) {
        console.log(-1);
    } else if ((typeof val) === 'number') {
        console.log(val * -1);
    }
}
getOpposite(5.0);
```


------------------- toSeconds ---------------
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
Truthy and Falsy values
```ruby
console.log(`"-0" is a truthy value ? ${-0 ? 'true' : 'false'}.`)
console.log(`"0n" is a truthy value ? ${0n ? 'true' : 'false'}.`)
console.log(`"" is a truthy value ? ${"" ? 'true' : 'false'}.`)
console.log(`'' is a truthy value ? ${'' ? 'true' : 'false'}.`)
console.log(`"null" is a truthy value ? ${null ? 'true' : 'false'}.`)
console.log(`"undefined" is a truthy value ? ${undefined ? 'true' : 'false'}.`)
console.log(`"NaN" is a truthy value ? ${NaN ? 'true' : 'false'}.`)
console.log(`"true" is a truthy value ? ${true ? 'true' : 'false'}.`)
console.log(`"{}" is a truthy value ? ${{} ? 'true' : 'false'}.`)
console.log(`"[]" is a truthy value ? ${[] ? 'true' : 'false'}.`)
console.log(`"42" is a truthy value ? ${42 ? 'true' : 'false'}.`)
console.log(`"0" is a truthy value ? ${0 ? 'true' : 'false'}.`)
console.log(`"false" is a truthy value ? ${false ? 'true' : 'false'}.`)
console.log(`""false"" is a truthy value ? ${"false" ? 'true' : 'false'}.`)
console.log(`"new Date()" is a truthy value ? ${new Date() ? 'true' : 'false'}.`)
console.log(`"-42" is a truthy value ? ${-42 ? 'true' : 'false'}.`)
console.log(`"12n" is a truthy value ? ${12n ? 'true' : 'false'}.`)
console.log(`"3.14" is a truthy value ? ${3.14 ? 'true' : 'false'}.`)
console.log(`"-3.14" is a truthy value ? ${-3.14 ? 'true' : 'false'}.`)
console.log(`"Infinity" is a truthy value ? ${Infinity ? 'true' : 'false'}.`)


// Output

"-0" is a truthy value ? false.
"0n" is a truthy value ? false.
"" is a truthy value ? false.
'' is a truthy value ? false.
"null" is a truthy value ? false.
"undefined" is a truthy value ? false.
"NaN" is a truthy value ? false.
"true" is a truthy value ? true.
"{}" is a truthy value ? true.
"[]" is a truthy value ? true.
"42" is a truthy value ? true.
"0" is a truthy value ? false.
"false" is a truthy value ? false.
""false"" is a truthy value ? true.
"new Date()" is a truthy value ? true.
"-42" is a truthy value ? true.
"12n" is a truthy value ? true.
"3.14" is a truthy value ? true.
"-3.14" is a truthy value ? true.
"Infinity" is a truthy value ? true.
```

```ruby
let myvar = 1;
console.log(myvar);

let firstName = 'Gnanakkumaar';
let lastName = 'Perumal';
let maritalStatus = 'Single';
let age = 34;

let myInfo = [ 
    ['firsName', 'Gnanakkumaar'],
    ['lastName', 'Perumal'],
    ['maritalStatus', 'Single'],
    ['age', 34]
];

let myData = {
    firstName : 'Gnanakkumaar',
    lastName : 'Perumal',
    maritalStatus : 'Single',
    age: 34
}

console.log("This is ",parseInt('1322aasf5')); //This is  1322 and missed 5
console.log(Number('11123'));

//   Convert the string to integer

let numString = '34221';

console.log(parseInt(numString));
console.log(Number(numString));
console.log(+numString);

// Simple Programs todo for Operators

    // Square of a number

    function squareFinder(num) {

        return num * num;
    }

    console.log(`squareFinder: Square of 5 is ${squareFinder(5)}.`);

// Output: squareFinder: Square of 5 is 25.

    // Swapping 2 numbers
    function numSwaper(a, b) {
        let temp = a;
        a = b;
        b = temp;
        return `a = ${a}, b = ${b}`  
    }

    console.log(`numSwaper: given a = 10 and b = 8 after swaping ${numSwaper(10, 8)}.`);

    //  Addition of 3 numbers

    function add3Nums(a,b,c) {
    return a+b+c;
}

console.log(`add3Nums: given a: 5, b: 8, c: 12 and total is ${add3Nums(5,8,12)}.`)

// Output add3Nums: given a: 5, b: 8, c: 12 and total is 25.



    // Celsius to Fahrenheit conversion
    // (0°C × 9/5) + 32 = 32°F
function celsiusToFahrenheitConverter(Celsius) {

    let Fahrenheit = Celsius * (9/5) + 32;

    return `${Celsius} Celsius is equalent to ${Fahrenheit} Fahrenheit.`
}

console.log(`celsiusToFahrenheitConverter: ${celsiusToFahrenheitConverter(36)}`)

// Output: celsiusToFahrenheitConverter: 36 Celsius is equalent to 96.8 Fahrenheit.
        
// Meter to miles
        // miles = meter * 0.00062137

        function milesToMeter(mi) {

            return `${mi} miles equals to ${(mi/0.00062137).toFixed(2)} meters.`
}

console.log(`milesToMeter: ${milesToMeter(5)}`)

// Output: milesToMeter: 5 miles equals to 8046.74 meters.


    // Pounds to kg
    // kg = pound / 2.205

    function poundsToKg(pounds) {

        return `${pounds} is equals to ${(pounds/2.205).toFixed(2)} kilograms.`
}
        console.log(`// Output: poundsToKg: ${poundsToKg(5)}`);
    
        // Output: poundsToKg: 5 is equals to 2.27 kilograms.

    //    Calculate Batting Average
    // Batting Average = Runs Scored ÷ Times Out
    
    function battingAverage(runs, outs) {
    
        return `Batter scored ${runs} and out ${outs} time. Batting average is ${(runs/outs).toFixed(2)}.`
    }
    
    //    Calculate five test scores and print their average
    
    console.log(`// Output: ${battingAverage(739, 5)}`)

    // Output: Batter scored 739 and out 5 time. Batting average is 147.80.

    
    
    //    Power of any number x ^ y.

    function powerOfNum(num1, num2) {

        return `${num1} power of ${num2} is ${num1**num2}.`
}

console.log(`// Output: ${powerOfNum(4,5)}`);

// Output: 4 power of 5 is 1024.


    // Calculate Simple Interest
    // S.I. = (P × R × T)/100

    function simpleInterest(p,r,t) {

        return `Principle amount ${p}, interst rate ${r}, and year ${t}. Simple Interest is ${(p*r*t)/100}.`
}

console.log(`// Output: ${simpleInterest(3000, 2, 5)}`);

// Output: Principle amount 3000, interst rate 2, and year 5. Simple Interest is 300.

        // Calculate area of an equilateral triangle
        // Area = √3/4 × (side)2

        function areaEquilateralTriangle(a) {

            return `Sides of equilateral triangle is ${a} and area is ${(((Math.sqrt(3))/4)*a*a).toFixed(2)} .`
        }

        console.log(`// Output: ${areaEquilateralTriangle(6)}`);

        // Output: Sides of equilateral triangle is 6 and area is 15.59.


    // Area Of Isosceles Triangle
    // Area = ½ × base × Height

    function areaOfIsoscelesTriangle(base, height) {

        return `Isosceles triangle base ${base} and height ${height}. Area of the Isosceles Triangle is ${base*height*0.5}.`
    }

    console.log(`// Output: ${areaOfIsoscelesTriangle(4,7)}`);

    // Output: Isosceles triangle base 4 and height 7. Area of the Isosceles Triangle is 14.

    
    // Volume Of Sphere
// 4/3 pi r cube

function volumeOfSphere(radius) {

    return `Radius of the sphere is ${radius}. Volume of the sphere is ${((4/3)*3.14*radius**3).toFixed(2)}.`
}

console.log(`// Output: ${volumeOfSphere(4)}`);

// Output: Radius of the sphere is 4. Volume of the sphere is 267.95.    


//    Volume Of Prism
// V=Bh

function volumeOfPrism(base, height) {

    return `Prism base and height is ${base} and ${height}. Volume of the prism is ${base * height}.`
}

console.log(`// Output: ${volumeOfPrism(7, 9)}`);

// Output: Prism base and height is 7 and 9. Volume of the prism is 63.

  //  Find area of a triangle.
// 1/2 bh

function areaOfTriangle(base, height) {

    return `Base and height of triangle is ${base} and ${height}. Area of the triangle is ${0.5*base*height}.`
}

console.log(`// Output: ${areaOfTriangle(5,7)}`);

// Output: Base and height of triangle is 5 and 7. Area of the triangle is 17.5.


    //  Give the Actual cost and Sold cost, Calculate Discount Of Product

    function discountCalculater(actualPrice, soldPrice) {

        return `Actual Price is ${actualPrice} and sold price is ${soldPrice}. Discount percentage is ${((actualPrice/soldPrice)*100).toFixed(2)}.`
}

console.log(`// Output: ${discountCalculater(5423, 4389)}`);

// Output: Actual Price is 5423 and sold price is 4389. Discount percentage is 123.56.

        //  Given their radius of a circle and find its diameter, circumference and area.
        //  d=2r, C=πd, a=2π r square

        function diameterCircumferenceAreaFinder(radius) {

            return `/* Output:
Raduis of the circle: ${radius},
Didameter of the circle: ${2*radius},
Circumference of the circle: ${(3.14 * 2 * radius).toFixed(2) },
Area of the circle: ${(2*3.14*radius*radius).toFixed(2)}.*/`
}

console.log(diameterCircumferenceAreaFinder(5));

/* Output:
Raduis of the circle: 5,
Didameter of the circle: 10,
Circumference of the circle: 31.40,
Area of the circle: 157.00.*/



    // Given two numbers and perform all arithmetic operations.

    function arithmeticOperations(num1, num2) {

        return `/* 
        Output: 
        Function: arithmeticOperations(),
        Input numbers: ${num1}, ${num2}
        Addition: ${num1 + num2},
        Substraction: ${num1 - num2},
        Multiplication: ${num1 * num2},
        Divison: ${(num1/num2).toFixed(2)}.
        */`
    }

    console.log(arithmeticOperations(34, 84));

    // Display the asterisk pattern as shown below(No loop needed):

    console.log(`*****\n*****\n*****\n*****\n*****`);

/*  *****
    *****
    *****
    *****
    *****
*/
    
    // Calculate electricity bill?
    /*    For example, a consumer consumes 100 watts per hour daily for one month. 
    Calculate the total energy bill of that consumer if per unit rate is 10?
*/

function electricityBillCalculator(consumption, unitRate) {
        let unitsConsumedIn30Days = (consumption*24*30)/1000 // 1000 watts = 1 unit
    return `/*
    Output:
    Function: electricityBillCalculator()
    Consumption is per hour ${consumption} watts,
    Total Units consumed: ${unitsConsumedIn30Days}, 
    Unit rate: ${unitRate},
    Monthly electricity bill: ${unitsConsumedIn30Days * unitRate}.
    */`
}

console.log(electricityBillCalculator(100,10));

/*
    Output:
    Function: electricityBillCalculator()
    Consumption is per hour 100 watts,
    Total Units consumed: 72, 
    Unit rate: 10,
    Monthly electricity bill: 720.
    */
    
 // Program To Calculate CGPA

    function cgpaCalculator(scoresArr) {
        let sum = 0; let cgpa = 0; n = scoresArr.length;
            for (let i = 0; i < scoresArr.length; i++) {
                sum += scoresArr[i]/10;
            }
         
         cgpa = sum/n;
         return `
/* Output
Fucntion: cgpaCalculator()
Total Marks obtained ${scoresArr} and CGPA is ${cgpa}
*/`  
}

 
console.log(cgpaCalculator([54,65,67,85,76]))

/* Output
Fucntion: cgpaCalculator()
Total Marks obtained 54,65,67,85,76 and CGPA is 6.94
*/```
