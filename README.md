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

