# javascript

																											//tutorial
													//html

<body>
    <h1 id="myH1"></h1>
    <p id="myP"></p>

    <script src="main.js"></script>
</body>

													//js
													
console.log("Hello");
console.log(`I like pizza`)

window.alert("This is an alert")
window.alert("I like pizza!")

document.getElementById("myH1").textContent = "Hello";
document.getElementById("myP").textContent = "I like pizza!";

// this is a comment
/* This is 
   a comment 
*/


																												// varibles

let x;
x = 100;
//let x = 100;
console.log(x)

let age = 18;
let price = 10.99;
let gpa = 2.1;
console.log(typeof age); //number 
console.log(`You are ${age} years old`);
console.log(`The price is $${price}`);
console.log(`your GPA is ${gpa}`);

let first_name = "NANO";
let favourit_food = "pizza";
let email = "nano@gmail.com"
console.log(typeof first_name); //string
console.log(`Your name is ${first_name}`);
console.log(`You like ${favourit_food}`);
console.log(`Your email is ${email}`);

let online = true;
let forSale = false;
let isStudent = true;
console.log(typeof online); //boolean
console.log(`Nano is ${online}`);
console.log(`Is this car for sale : ${forSale}`);
console.log(`Enrolled : ${isStudent}`);

let fullName = "omar el ghazali";
age = 19;
let student = true;
document.getElementById("p1").textContent = `Your name is ${fullName}`;
document.getElementById("p2").textContent = `you are ${age} years old`;
document.getElementById("p3").textContent = `Enrolled : ${student}`;

                            //accept user input 
//1. easy = window promt 
//2.professional way = html textbox

//1->
let username;
username = window.prompt("what's your username ?");

console.log(username);

//2->
    //js
let username; 
document.getElementById("mySubmit").onclick = function(){
    username = document.getElementById("myText").value;
    document.getElementById("myH1").textContent = `Welcom ${username}`;
    console.log(username);
}
    //html
    <body>
        <h1 id="myH1">Welcom</h1>
        <label>username:</label>
        <input id="myText"><br><br>
        <button id="mySubmit">submit</button>
        <script src="main.js"></script>
    </body>

// type conversion 
let age = window.prompt("how old are you ?");

age = Number(age);
age += 1;
console.log(age);

let x ;
let y ; 
let z ;

x = Number(x);
y = String(y);
z = Boolean(z);

//const
const pi = 3.14159;
let raduis ;
let circumference;

raduis = window.prompt("Enter the reduis of the circule");
raduis = Number(raduis);

circumference = 2 * pi * raduis ;

console.log(circumference);

const PI = 3.14159;
let raduis ;
let circumference;

document.getElementById("mySubmit").onclick = function(){
    raduis = document.getElementById("myInput").value;
    raduis = Number(raduis);
    circumference = 2 * PI * raduis;
    document.getElementById("myH3").textContent = `result : ${circumference}`;
    console.log(circumference);
}

// html 
<h1 id="myH1">enter the raduis of a circule </h1>
    <label>raduis :</label>
    <input id="myInput"><br><br>
    <button id="mySubmit">Submit</button>
    <h3 id="myH3">result : </h3>
    <script src="main.js"></script>

// Counter program
const increase = document.getElementById("increase");
const decrease = document.getElementById("decrease");
const reset = document.getElementById("reset");
const label = document.getElementById("label");
let count = 0 ;

increase.onclick = function(){
    count++;
    label.textContent = count;
}
decrease.onclick = function(){
    count--;
    label.textContent = count;
}
reset.onclick = function(){
    count = 0;
    label.textContent = count;
}
    //html
    <label id="label">0</label><br>
        <div id="btncontainer">
            <button id="increase" class="btn">increase</button>
            <button id="reset" class="btn">reset</button>
            <button id="decrease" class="btn">decrease</button>
        </div>
     <script src="main.js"></script>

     //css
    #label{
    display: block;
    text-align: center;
    font-size: 10em;
    font-family: Helvetica, sans-serif;
}
#btncontainer{
    text-align: center;
}
.btn{
    padding: 10px;
    font-size: 1.5em;
    color: aliceblue;
    background-color: rgb(0, 0, 0);
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.25s;
}
.btn:hover{
    background-color: blue;
}

//math

console.log(Math.PI);

let x = 3;
let y = 2;
let z = 1;

console.log(Math.round(x)) //make it (int) 3.3 > 3  | 3.7 > 4
console.log(Math.floor(x)); // take the int part 
console.log(Math.ceil(x)); // take the next int 
console.log(Math.trunc(x)); //take the int part 
console.log(Math.pow(x , y)); // power
console.log(Math.sqrt(x)); //square
console.log(Math.log(x));
console.log(Math.cos(x));
console.log(Math.sin(x));
console.log(Math.tan(x));
console.log(Math.abs(x));
console.log(Math.max(x , y , z));//max
console.log(Math.min(x , y , z));//min

																																		//random numbers
//let randomNum = Math.random(); //rand num 0 -> 1
//let randomNum = Math.floor(Math.random() * 6) + 1; // rand num 1 -> 6
const max = 100;
const min = 50;
let randomNum = Math.floor(Math.random() * (max - min) + min);
console.log(randomNum);
 
 const btn = document.getElementById("myBtn");
const lbl = document.getElementById("myOutput");


let max = 1;
let min = 100


btn.onclick = function(){
    let randomNum = Math.floor(Math.random() * (max - min + 1)) + min;
    lbl.textContent = `> ${randomNum}`;
}
//htm
<h1>generate random number</h1>
    <button id="myBtn">generate</button>
    <label id="myOutput">></label>
     <script src="main.js"></script>

//css
body{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    text-align: center;
}

#myBtn {
    font-size: 3em;
    padding: 5px;
    border-radius: 5px;
}
#myOutput{
    font-size: 3em;
    color: red;
}

//fi steatment
let age = 16;

if (age > 18 ){
    console.log("you are adult");
}
else if (age < 0){
    console.log("you still did't born yet (liquide edition)");
}
else if (age == 0){
    console.log("fuck nuh you are a new born")
}
else {
    console.log("you are a child");
}

//checked : HTML checkbox and radio btn

const subscribe = document.getElementById("myckbx");
const visa = document.getElementById("visaBtn");
const mastercard = document.getElementById("mastercardBtn");
const paypal = document.getElementById("paypalBtn");
const submit = document.getElementById("submit");
const subResult = document.getElementById("subResult");
const paymentResult = document.getElementById("paymentResult");

submit.onclick = function(){
    if(subscribe.checked){
        subResult.textContent = `You are subscribed`;
    }
    else{
        subResult.textContent = `You are NOT subscribed`;
    }

    if(visa.checked){
        paymentResult.textContent = `you pay with visa`;
    }
    else if(mastercard.checked){
        paymentResult.textContent = `you pay with mastercard`;
    }
    else if(paypal.checked){
        paymentResult.textContent = `you pay with paypal`;
    }
    else {
        paymentResult.textContent = `you must select a payment type`;
    }
}

    //HTML
    <input type="checkbox" id="myckbx">
    <label for="myckbx">subscribe</label>

    <input type="radio" id="visaBtn" name="card">
    <label for="visaBtn">Visa</label>
    <input type="radio" id="mastercardBtn" name="card">
    <label for="mastercardBtn">Mastercard</label>
    <input type="radio" id="paypalBtn" name="card">
    <label for="paypalBtn">Paypal</label><br>

    <button id="submit">Submit</button>

    <p id="subResult"></p>
    <p id="paymentResult"></p>

//tenary operators
        //syntax : condition ? codeiftrue : codeiffalse

let age = 21;
let message = age >= 18 ? "you are an adult" : "You are a minor";

console.log(message);

let isStudent = true;
let message1 = isStudent ? "you are a student" : "you are not a student";
console.log(message1);

let purchaseAmount = 125;
let discount = purchaseAmount >=100 ? 10 : 0;
console.log(`your totale is $${purchaseAmount - (purchaseAmount * (discount / 100))}`);

//SWITCH
let day = 10;
switch(day){
    case 1 :
        console.log("it's Monday");
        break;
    case 2 :
        console.log("it's Tusday");
        break;
    case 3 :
        console.log("it's Wensday");
        break;
    case 4 :
        console.log("it's Thersday");
        break;
    case 5 :
        console.log("it's Friday");
        break;
    case 6 :
        console.log("it's Saturday");
        break;
    case 7 :
        console.log("it's Sunday");
        break;
    default :
        console.log(`${day} is not a day`);
}

let testScore = 90;
let letterGrade ;

switch(testScore){
    case testScore >= 90:
        letterGrade = "A";
        break;
    case testScore >= 80:
        letterGrade = "B";
        break;
    case testScore >= 70:
        letterGrade = "C";
        break;
    case testScore >= 60:
        letterGrade = "D";
        break;
    default :
        letterGrade = "F";

}
console.log(letterGrade);

let testScore = 10000;
let letterGrade ;

switch(true){
    case testScore >= 90:
        letterGrade = "A";
        break;
    case testScore >= 80:
        letterGrade = "B";
        break;
    case testScore >= 70:
        letterGrade = "C";
        break;
    case testScore >= 60:
        letterGrade = "D";
        break;
    default :
        letterGrade = "F";

}
console.log(letterGrade);


//string methods
let username = "Nano";

console.log(username.charAt(0));
console.log(username.indexOf("o"));
console.log(username.lastIndexOf("n"));
console.log(username.length);
username = username.trim(); //remove white spaces
console.log(username);

username = username.toUpperCase(); 
console.log(username);

username = username.toLowerCase(); 
console.log(username);

username = username.repeat(3); 
console.log(username);

let username = " Nano";

let result = username.startsWith(" "); //return boolein
//let result = username.endtsWith(" ");
//let result = username.includes(" ");

console.log(result);

if(result){
    console.log("your username can't begin with ' ");
    //console.log("your username can't end with ' ");
    //console.log("your username can't include  with ' ");
}
else {
    console.log(username)
}

let phoneNumber = "123-456-7890";

//phoneNumber = phoneNumber.replaceAll("-" , "");
//phoneNumber = phoneNumber.padStart(15 , "0");
phoneNumber = phoneNumber.padEnd(15 , "0");

console.log(phoneNumber);


//string slicing    string.slice(start , end);

const fullName = "omar el ghazali";

//let firstName = fullName.slice(0 , 4);
//let lastName = fullName.slice(5);
//let firstChar = fullName.slice(0 , 1);
//let lastChar = fullName.slice(-1);

let firstName = fullName.slice(0 , fullName.indexOf(" ") + 1);
let lastName = fullName.slice(fullName.indexOf(""));

console.log(firstName);
console.log(lastName);
//console.log(firstChar);
//console.log(lastChar);

const email = "gahzali1235565@gmail.com";

let username = email.slice(0 , email.indexOf("@"));
console.log(username);
let exxtention = email.slice(email.indexOf("@"));
console.log(exxtention);


//METHD CHANING 
let username = window.prompt("Enter yor user name");

//ahh method 
username = username.trim();
let firstLetter = username.charAt("0");
firstLetter = firstLetter.toUpperCase();

let otherlettters = username.slice(1);
otherlettters = otherlettters.toLowerCase;

username = firstLetter + otherlettters;
console.log(username);

//

username = username.trim().charAt(0).toUpperCase()
           + username.trim().slice(1).toLowerCase();
        
console.log(username);


//Logical operators and = && ; OR = || ; NOT = !;
// = asignment operators
// == cmparaison 
// === strict equality (compare the value an datatype are equal)

//while loop 
//while
let username = "";
while(username === "" || username === null){
    username = window.prompt("Enter your name :")
}

console.log(`Hello ${username}`);

//do while
let nano;
do{
    nano = window.prompt("Enter your name :")
}while(nano === "" || nano === null)

console.log(`Hello ${nano}`);


let loggedIn = false;
let password = "";
let username = "";

do{
    username = window.prompt("Enter your username:");
    password = window.prompt("Enter your password:");

    if(username === "myUsername" && password === "myPassword"){
        loggedIn = true;
        console.log("You are connected");
    }
    else{
        console.log("Invalid credentials! Please try again");
    }

}while(!loggedIn);

//for loop continue break
for(let i = 0 ; i <= 10 ; i++){
    console.log(i);
}
console.log("Happy New year");

for(let i = 0 ; i < 21 ; i++){
    if(i == 13){
        continue;
        //break;
    }
    else{
        console.log(i);
    }
}

																									//number gessing game 
const min = 1 ; 
const max = 100;
let isRunning = true;
const answer = Math.floor(Math.random() * (max - min + 1)) + min;
let attemps = 0;
let geuss;

while(isRunning){
    console.log("geuss a number between 1 - 100");
    geuss = window.prompt("enter your geuss :");
    geuss = Number(geuss);

    if(isNaN(geuss)){
        window.alert("Please enter a valid number ");
    }
    else if(geuss > max || geuss < min){
        window.prompt(`enter avalid number between ${min} & ${max}`);
    }
    else{
        attemps++;
        if(geuss < answer){
            window.alert("Too low !try again!");
        }
        else if(geuss > answer){
            window.alert("Too hight !try agin!");
        }
        else{
            window.alert(`CORRECT! THE answer is ${answer} . it took you ${attemps} attemps`);
            isRunning = false;
        }
    }


}

																													//function

function happyBirthday(username , age){
    console.log("happy birthday to you");
    console.log("happy birthday to you");
    console.log(`happ birthday dear ${username}`);
    console.log("happy birthday to you");
    console.log(`you are now ${age} years old`);
}

happyBirthday("Nano" , 19);

function add(x , y){
    let result = x + y;
    return result;
}

let answear = add(1 , 2);
console.log(answear);


function isEven(num){
    /*if(num % 2 === 0){
        return true;
    }
    else{
        return false;
    }*/
   return num % 2 === 0 ? true : false;
}

console.log(isEven(10));

//functions

function isValidEmail(email){
    if(email.includes("@")){
        return true;
    }
    else{
        return false
    }
}
console.log(isValidEmail("negatron@gmail.com"));

																																//number geussing game 
console.log("js connected");

let max = 100;
let min = 1;
let attemps = 0;
let guess;
let answer = Math.floor(Math.random() * (max - min + 1) )+ min;
let isRunning = true;
console.log(answer);

while(isRunning){
    guess = Number(window.prompt("enter num # "));
    while(isNaN(guess)){
        guess = Number(window.prompt("enter num # "));
    }

    if(guess === answer){
        console.log(`GG you get the right answer \n attemps : ${attemps}`);
        isRunning = false;
    }
    else{
        if(guess < answer){
            console.log("too low !");
            attemps++;
        }
        else{
            console.log("too hight !");
            attemps++;
        }
    }
// }

                                            //function 

function happyBirthDay(username , age){
    console.log(`happy birthday  to you `);
    console.log(`happy birthday  to you `);
    console.log(`happy birthday  dear ${username} `);
    console.log(`happy birthday  to you `);
    console.log(`You are now ${age} years old !`);
}

happyBirthDay("nano" , 12);

function add(x , y){
    return x + y;
}

function subb(x , y){
    return x - y;
}

function isEven(v){
    return v % 2 === 0 ? true : false;
}

function isValidEmail(email){
    if(email.includes("@gmail.com")){
        return true;
    }
    else {
        return false;
    }
}



																																					//Temperature conversion 

let userInput = document.getElementById("userInput");
let cls = document.getElementById("cls");
let fhr = document.getElementById("fhr");
let myButton = document.getElementById("myButton");
let result = document.getElementById("result");
let calcul ;

myButton.onclick =  function(){
    let value =  Number(userInput.value);
    
    
    
    if(cls.checked){
        
        calcul = value * 1.8 + 32;
        result.textContent = calcul.toFixed;
        
    }
    else if(fhr.checked){
        
        calcul = (value - 32) / 1.8;
        result.textContent = calcul.toFixed(1);
    }
    else{
        result.textContent = "Select an option please!";
    }
}

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css.css">
</head>
<body>

    <form>
        <h1>Temperature Conversion</h1><br>
        <input type="text" id="userInput"><br>
        <input type="radio" name="choice" id="cls">
        <label for="toFah">celsius -> fahrenheit</label><br>
        <input type="radio" name="choice" id="fhr">
        <label for="toCel">fahrenheit  -> celsius</label><br>
        <input type="button" id="myButton" value="submit">
        <p id="result">select unit</p>
    </form>
        
    </div>
    <script src="main.js"></script>
</body>
</html>


																																										//Array

let fruits = ["apple" , "orange" , "banana"];

fruits.push("mango"); //Add at the end
fruits.pop(); //Remove the last element + return it 
fruits.unshift("coconut");//Add at the bigining
fruits.shift();//Remove the first element 

let numOfFruits = fruits.length;
let index = fruits.indexOf("banana"); //if dosen't exist return -1

console.log(numOfFruits);
console.log(index);

for(let i = 0 ; i < fruits.length ; i++){
    console.log(fruits[i]);
}

for(let fruit of fruits){
    console.log(fruit);
}

fruits.sort().reverse();
console.log(fruits);

																																		//sepread operator : ...
																																		// (unpack the element)


let numbers = [1 , 2 , 3 , 4 , 5];
let maximum = Math.max(...numbers);
let minimum = Math.min(...numbers);

console.log(maximum);
console.log(minimum);

let myName = "Nano";
let arrName = [...myName];
console.log(arrName);
let letters = [...myName].join("-");
console.log(letters);

let fruits = ["orange" , "banana" , "coconut"];
let vegetebales = ["carrots" , "tomato" , "potatoes" , "eggs" , "milk"];

let foods = [...fruits , ...vegetebales];
console.log(foods);




                                                //resr parameters : accept n arguments



function openFridge(...foods){
    console.log(...foods);
}
function getFood(...foods){
    return foods
}

let food1 = "pizza";
let food2 = "humberger";
let food3 = "hotdog";
let food4 = "sushi";


openFridge(food1 , food2 , food3 , food4);
let food = getFood(food1 , food2 , food3 , food4);
console.log(food);



function sum(...numbers){
    let result = 0;
    for (let number of numbers){
        result += number;
    }
    return result;
}

function avg(...numbers){
    let result = 0;
    for (let number of numbers){
        result += number;
    }
    return result / numbers.length;
}


let total = avg(1 , 2 , 3 , 4 , 54);
console.log(total)


function combineString(...names){
    return names.join(" ");
}

const fullName = combineString("Mr." , "Spongebob" , "Squarepants" , "III");

console.log(fullName)


																													


																																			//genarate a password 

function passwordGenerator(length , lowerChar , numbers , upperChar , symboles){
    const includeLowerChar = "abcdefghijklmnopqrstuvwxyz";
    const includeNumbers = "1234567890";
    const includeupperChar = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    const includeSymbols = "!@#$%^&*()_=+_"
    let allowedChar = ``;
    let password = ``;

    allowedChar += lowerChar ? includeLowerChar : ``;
    allowedChar += numbers ? includeNumbers : ``;
    allowedChar += upperChar ? includeupperChar : ``;
    allowedChar += symboles ? includeSymbols : ``;
    console.log(allowedChar);
    if(length <= 0 ){
        return `(password can't be less than 1)`;
    }
    else if(allowedChar.length === 0){
        return `(At least 1 set of caracter need to be selected)`;
    }
    else{
        for(let i = 0 ; i < length ; i++){
            let value = Math.floor(Math.random() * allowedChar.length) ;
            console.log(allowedChar[value])
            password += allowedChar[value];
        }
        
    }
    return password;
}
passwordLength = 12;
includeLowerChar = true;
includeNumbers = true;
includeupperChar = true;
includeSymbols = true;

let password = passwordGenerator(passwordLength , 
                                 includeLowerChar, 
                                 includeNumbers,
                                 includeupperChar,
                                 includeSymbols);

console.log(password);



																																				//calback = a function that is passed as an argument t anther function 
																																				//"hey when you'r done call this next!"
																																				//reading fies , network requests , interacting with data base;
sum(displayPage , 1 , 2);
function sum(callback , x , y){
    let result = x + y;
    callback(result);
}

function dispay_cnsole(result){
    console.log(result)
}

function displayPage(result){
    document.getElementById("myH1").textContent = result
}


																																//forEach() = method used to iterate ver the elements
																																//            of an array and appay a specified function (callback);
																																//            to each element 

																																//          array.forEach(callback);
																																//          element , index , array are provided


let numbers  = [1 , 2 , 3 , 4 , 5];

numbers.forEach(square);
numbers.forEach(display);


function double(element , index , array){
    array[index] = element * 2;
}
function display(element){
    console.log(element);
}
function double(element , index , array){
    array[index] = element * 3;
}
function square(element , index , array){
    array[index] = Math.pow(element , 2)
}

let fruits = ["orange" , "banana" , "coconut" , "apple"];

fruits.forEach(captlize);
fruits.forEach(dispaly);

function uppercase(element , index , array){
    array[index] = element.toUpperCase();
}
function lowerCase(element , index , array){
    array[index] = element.toLowerCase();
}
function captlize(element , index , array){
    array[index] = element.charAt(0).toUpperCase() + element.slice(1);
}
function dispaly(element){
    console.log(element);
}


//.map() accept a call back and applies that function to 
//       each element of an array  , then return a new array

let numbers = [1 , 2 , 3 , 4 , 5];

numSquare = numbers.map(cube);

function squar(element){
    return Math.pow(element, 2);
}

function cube(element){
    return Math.pow(element , 3);
}

console.log(numSquare);



const names = ["omar" , "nano" , "el" , "ghazali"];

let uppNames = names.map(captlize);
console.log(uppNames)

function upperCase(element){
    return element.toUpperCase();
}
function lowerCase(element , index , array){
    return element.toUpperCase();
}
function captlize(element , index , array){
    return element.charAt(0).toUpperCase() + element.slice(1);
}



const date = ["2020-01-10" , "2021-02-20" , "2022-03-30"];

const formatedDate = date.map(formatDate);
console.log(formatedDate)

function formatDate(element){
    let parts = element.split("-");
    return `${parts[2]}/${parts[1]}/${parts[0]}`;
}




																			//.filter() = create a a new array buy filtering out element 

let numbers = [1 , 2 , 3 , 4 , 5 , 6 , 7];
let evenNum = numbers.filter(isEven);
let oddNum = numbers.filter(isOdd);

console.log(oddNum);

function isEven(element){
    return element % 2 === 0;
}

function isOdd(element){
    return element % 2 !== 0;
}




let ages = [16 , 17 , 18 , 18 , 19 , 20 , 60];
let adults = ages.filter(isAdult);
let children = ages.filter(isChildren);
console.log(children);

function isAdult(element){
    return element >= 18
}
function isChildren(element){
    return element < 18
}




let fruits = ["banana" , "apple" , "coconut" , "pomegranate" , "kiwi" , "orange"];
let shortWords = fruits.filter(getShortWords);
let longWords = fruits.filter(getLongWords);
console.log(shortWords);

function getShortWords(element){
    return element.length <= 6;
}

function getLongWords(element){
    return element.length > 6;
}




																				//.reduce() = reduce the elements of an array to single value!!
const numbers = [1 , 20 , 30 , 1 , 15 , 29];
const total = numbers.reduce(sum);
console.log(total);

function sum(accumulator , element){
    return accumulator + element;
}
//function sum(privious , next){ (0 , 1) -> (1 , 20) -> (20 , 30)
//    return privious + next;
//



let garades = [75 , 66 , 80 , 95 , 88];
let maximum = garades.reduce(maxGrade);
let minimum = garades.reduce(minGrade)

console.log(minimum);

function maxGrade(accumalator , element){
    return Math.max(accumalator , element);
}

function minGrade(accumalator , element){
    return Math.min(accumalator , element);
}



//function declaration : 
function hello(){
    console.log("hello");
}
hello();

//function expretion = a way to define a function as value or a varibale

setTimeout(function(){console.log("hello")} , 3000);


//
const numbers = [1 , 2 , 3 , 4 , 5 , 6];
const squares = numbers.map(square);

function square(element){
    return Math.pow(element , 2);
}

console.log(squares);


const numbers = [1 , 2 , 3 , 4 , 5 , 6];
const squares = numbers.map(function(element){
    return Math.pow(element , 2);});
const cube = numbers.map(function(element){
    return Math.pow(element , 3)});
const isEven = numbers.filter(function(element){
    return element % 2 === 0;});
const isOdd = numbers.filter(function(element){
    return element % 2 !== 0;});
const total = numbers.reduce(function(accumulator , element){
    return accumulator + element;
})

console.log(total);

																															//			//arrow function = (parameters) => some code													//

const hello = function(){
    console.log("hello");
}
hello();

const hello = (name , age) => {console.log(`hello ${name}`)
                         console.log(`you are ${age} years old`)};

hello("nega" , 18);


setTimeout( () => console.log("hello"), 3000);
const numbers = [1 , 2 , 3 , 4 , 5];
const square = numbers.map((element) => {return Math.pow(element , 2)});
const cube = numbers.map((element) => {return Math.pow(element , 3)});
const isEven = numbers.filter((element) => {return element % 2 === 0});
const isOdd = numbers.filter((element) => {return element % 2 !== 0});
const total = numbers.reduce((accumulator , element) => {return accumulator + element })

console.log(total);



//Objects

const person1 = {
    //key:value
    name : "Omar",
    lastName : "El Ghazali",
    age : 19,
    isInAIntership : true,
    sayHello : () => console.log("I am omar the real one"),
    eat : () => console.log("I love to eat aaa idk forget about this question"),
}

const person2 = {
    name : "nano",
    lastName : "??",
    age : 12,
    isInAIntership : false,
    sayHello : () => console.log("I am Nano the dominater"),
    eat : () => console.log("I love to eat chicken barbeque"),
}

console.log(person1.name);
console.log(person1.lastName);
console.log(person1.age);
console.log(person1.isInAIntership);
person1.sayHello();
person1.eat();




																											//this = is reference keyword  
																											//          person.name = this.name
																											//this dosen't work with arrow function

const person1 = {
    name : "Nano",
    favFood : "chicken barbeque",
    sayHello : function(){console.log(`Hi , i'am ${this.name}` )},
    eat : function(){console.log(`${this.name} is eating ${this.favFood}`)}
}

person1.sayHello();
person1.eat();




//constructor = special method  for define the propreties and method of objects
function Car(make , model , year , color){
    this.make = make,
    this.model = model,
    this.year = year,
    this.color = color
    this.drive = function(){console.log(`You are driving ${this.model}`)}
}

const car1 = new Car("Ford" , "Mustang" , 2024 , "red");
const car2 = new Car("Chevrolet" , "Camaro" , 2025 , "bleu");
const car3 = new Car("Dodge" , "Charger" , 2026 , "Silver");
console.log(car1.make , car1.model , car1.year , car1.color);
console.log(car2.make , car2.model , car2.year , car2.color);
console.log(car3.make , car3.model , car3.year , car3.color);

car1.drive();
car2.drive();
car3.drive();



																																				//class


class Product{
    constructor(name , price){
        this.name = name,
        this.price = price
    }

    displayProduct(){
        console.log(`Product ${this.name}`);
        console.log(`Price : $${this.price.toFixed(2)}`);
    }

    calculateTotal(salesTax){
        return this.price + (this.price * salesTax);
    }
}
const salesTax = 0.05;

const product1 = new Product("Shirt" , 19.99);
const product2 = new Product("Pants" , 25.50);
const product3 = new Product("Underwear" , 100.00);

const total = product3.calculateTotal(salesTax);

product3.displayProduct();
console.log(`the total after add taxes is : ${total.toFixed(2)}`);





																					//static
class MathUtil{
    static PI = 3.14159

    static getdiametre(reduis){
        return reduis * 2;
    }

    static getcircomference(reduis){
        return reduis * 2 * this.PI;
    }
    static getArea(reduis){
        return reduis * reduis * this.math;
    }

}

console.log(MathUtil.PI);
console.log(MathUtil.getdiametre(3));
console.log(MathUtil.getcircomference(3))



													

class User {
    static userCount = 0;

    constructor(username){
        this.username = username,
        User.userCount ++
    }

    static getCountUser(){
        console.log(`There are ${User.userCount}`);
    }
    sayHello(){
        console.log(`hello this is ${this.username}`);
    }   
}

const user1 = new User("Nano");
const user2 = new User("Omar");

user1.sayHello();
user2.sayHello();
User.getCountUser();

console.log(User.userCount);





																					//inheretence


class Animle{
    isAlive = true;

    eat(){
        console.log(`the ${this.name} is eating`);
    }
    sleep(){
        console.log(`the ${this.name} is sleeping`);
    }
}

class Rabbit extends Animle{
    name = "Rabbit";
    run(){
        console.log(`This ${this.name} is running`);
    }
}
class Fish extends Animle{
    name = "Fish";
    swim(){
        console.log(`This ${this.name} is swiming`);
    }
}
class Hawk extends Animle{
    name = "Hawk";
    fly(){
        console.log(`This ${this.name} is flying`);
    }
}

const rabbit = new Rabbit("rabbit");
const fish = new Rabbit("fish");
const hawk = new Rabbit("hawk");

console.log(rabbit.name);
rabbit.eat();
rabbit.sleep();
rabbit.run();   




																											//super();


class Animal{
    constructor(name , age){
        this.name = name;
        this.age = age;
    }

    move(speed){
        console.log(`the ${this.name} move at speed of ${speed} mph`);
    }
}

class Rabbit extends Animal{

    constructor(name, age, runSpeed){
        super(name , age);
        this.runSpeed = runSpeed;
    }   
    
    run(){
        console.log(`this ${this.name} can run`);
        super.move(this.runSpeed);
    }
}

class Fish extends Animal{
    
    constructor(name, age, swimSpeed){
        super(name , age);
        this.swimSpeed = swimSpeed;
    }   

    swim(){
        console.log(`this ${this.name} can swim`);
        super.move(this.runSpeed);
    }
}

class Hawk extends Animal{

    constructor(name, age, flySpeed){
        super(name , age);
        this.swimSpeed = flySpeed;
    }   
    fly(){
        console.log(`this ${this.name} can fly`);
        super.move(this.runSpeed);
    }
}

const fish = new Fish("fish" , 1 , 40);
const rabbit = new Rabbit("rabit" , 1 , 10);
const hawk = new Hawk("hawk" , 1 , 40);

console.log(fish.name , fish.age , fish.swimSpeed)
fish.move(fish.swimSpeed)
fish.swim();


                                        //get
                                        //set


class Rectangle{

    constructor(width , height){
        this.width = width;
        this.height = height;
    }

    set width(newWidth){
        if(newWidth < 0){
            console.error("negroooooo");
        }
        else{
            this._width = newWidth
        }
    }

    set height(newHeight){
        if(newHeight > 0){
            
            this._height = newHeight;

        }
        else{
            console.error("negroooooo");
        }
    }

    get width(){
        return `${this._width.toFixed(1)} cm`;
    }
    get height(){
        return `${this._height.toFixed(1)} cm`;
    }

    get area(){
        return (this._height * this._width).toFixed(2);
    }
}

const reactangle = new Rectangle(1 , 2);

console.log(reactangle.width , reactangle.height)

console.log(reactangle.area)







class Person{
    constructor(firstName , lastName , age){
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    set firstName(newFirstName){
        if(typeof newFirstName === "string" && newFirstName.length > 0){
            
            this._firstName = newFirstName;
        }
        else{
            console.error("firstname can't be empty or a number");
        }
    }

    set lastName(newLastName){
        if(typeof newLastName === "string" && newLastName.length > 0){
            this._lastName = newLastName;
        }
        else{
            console.error("firstname can't be empty or a number");
        }
    }

    set age(newAge){
        if(newAge > 0 && typeof newAge === "number" ){
            this._age = newAge;
       }
       else{
        console.error("tebi age must be > 0 wik wiik");
       }
    }

    get age(){
        return `age : ${this._age}`;
    }
    get firstName(){
        return `first name : ${this._firstName}`;
    }
    get lastName(){
        return `lat name : ${this._lastName}`
    }
    get fullName(){
        return `full name : ${this._firstName} ${this._lastName}`
    }
    
}

const person = new Person("nano" , "omar" , 1); 

console.log(person.firstName +"\n" + person.lastName +"\n"+ person.age);
console.log(person.fullName);



// destructuring = extract values from arrays and objects,
//                then assign them to variables in a convenient way
//
//                [] = to perform array destructuring
//                {} = to perform object destructuring

// ---------- EXAMPLE 1 ----------
// SWAP 2 ELEMENTS of tow varibels

let a = 1;
let b = 2;

[a , b] = [b , a];
console.log(a);
console.log(b);


// ---------- EXAMPLE 2 ----------
// SWAP 2 ELEMENTS IN AN ARRAY

let color = ["red" , "green" , "bleu" , "black" , "white"];
[color[0] , color[4]] = [color[4] , color[0]];

console.log(color)

// ---------- EXAMPLE 3 ----------
// ASSIGN ELEMENTS TO VARIBLES

let colors = ["red" , "green" , "bleu" , "black" , "white"];
const [firstColor , secondColor , thirdColor , ...extraColors] = colors;

console.log(firstColor);
console.log(secondColor);
console.log(thirdColor);
console.log(extraColors); // <-- array 

// ---------- EXAMPLE 3 ----------
// EXTRACT VALUES FROM OBJECTS {}

const person1 = {
    firstName : "Spongebob",
    lastName : "squarepants",
    age : 39,
    job :"Fry Cook",
}

const person2 = {
    firstName : "Patrick",
    lastName : "Star",
    age : 32,
}

const {firstName , lastName , age , job="Uneployed"} = person2;

console.log(firstName);
console.log(lastName);
console.log(age);
console.log(job);



// ---------- EXAMPLE 3 ----------
// DISTRUCT IN FUNCTUION PARAMETERS

function displayPerson(firstName , lastName , age , job="Uneployed"){
    console.log(firstName);
    console.log(lastName);
    console.log(age);
    console.log(job);
}

const person1 = {
    firstName : "Spongebob",
    lastName : "squarepants",
    age : 39,
    job :"Fry Cook",
}

const person2 = {
    firstName : "Patrick",
    lastName : "Star",
    age : 32,
}

displayPerson(person1);








																																//nested object  = Objects inside of other objects
																																//							allow you to erepresent more complex data structure
																																//						Person {Adress{} , ContactInfo{}}
																																 //						ShopingCart(Monitor{} , Graphic card{}}


const person = {
    name : "Nano",
    last_name : "Omar",
    age : 19,
    isStudent : true,
    hobbies : ["mlbb" , "coding" , "gym"],
    adress : {
        street : "douarchemss",
        city : "Ouarzazate",
        counrtry : "Morocco",
    }
}

console.log(person.name);
console.log(person.hobbies[2]);

for(const proprety in person.adress){
    console.log(person.adress[proprety]);
}




class Adress{
    constructor(street , city , country){
        this.street = street;
        this.city = city;
        this.country = country;
    }

}

class Person {
    constructor(name , age , ...adress){
        this.name = name;
        this.age = age;
        this.adress = new Adress(...adress);
    }

}

const person1 = new Person ("Nano" , 19 , "douarchemss"
                                        , "Ouarzazate"
                                        , "Morocco"
)

console.log(person1.name);
console.log(person1.adress.street);



																																			//Array Objects


const fruits = [
    { name: "apple",      color: "red",    calories: 95 },
    { name: "orange",     color: "orange", calories: 45 },
    { name: "banana",     color: "yellow", calories: 105 },
    { name: "coconut",    color: "white",  calories: 159 },
    { name: "pineapple",  color: "yellow", calories: 37 }
];


//fruits.push({name:"grapes" ,zolor : "purple" , calories : 62});
//fruits.pop();
//fruits.splice(1 ,2)
//-------forEach()----------
fruits.forEach(fruits => console.log(fruits.name));

//-------map()----------
const fruits_name = fruits.map(fruits => fruits.name);

//-------filter()----------
const fruits_color_y = fruits.filter(fruit => fruit.color === "yellow");
console.log(fruits_color_y)

//------reduce()----------
const fruits_max = fruits.reduce((max , fruit) => fruit.calories > max.calories ?
                                                  fruit : max);
												  
												  
												  
																																			//sort();

numbers = [1 , 10 , 2 , 3 , 4 , 5 , 6 , 7 , 8 , 9];
numbers.sort((a , b) => a - b);

console.log(numbers)


const people = [{name: "Spongbob" , age: 30 , gpa: 3.0} ,
                {name: "Patrick" , age: 37 , gpa: 1.0} , 
                {name: "SquidWard" , age: 51 , gpa: 2.5} , 
                {name: "Sandy" , age: 27 , gpa: 4.0}];

people.sort((a , b) => a.age - b.age);
people.sort((a , b) => a.name.localeCompare(b.name));
console.log(people);

																																			//dates

date = new Date("2024-01-02T12:00:00Z");

console.log(date);



date = new Date();

const year  = date.getFullYear();
const month  = date.getMonth();
const day = date.getDate();
const hour = date.getHours();
const minute = date.getMinutes();
const sec = date.getSeconds();
const weekDays = date.getDay();

console.log(day);


date = new Date();

date.setFullYear(2027);
date.setMonth(0);
date.setDate(1);
date.setHours(2);
date.setMinutes(3);
date.setSeconds(4);

console.log(date);




const date1 = new Date("2026-12-31");
const date2 = new Date("2027-01-01");

if(date1 < date2){
    console.log("Happy new Year")
}




																																//closers



function creatCount(){
    let count = 0;
    function increment(){
        count++;
        console.log(`bitch ass is ${count}`);
    }
    function getCount(){
        return count;
    }

    return {increment , getCount};
}


const counter = creatCount();

counter.increment();
counter.increment();
counter.increment();
counter.increment();

console.log(counter.getCount());







function createGame(){
    let score = 0;

    function increeseScore(points){
        score+= points;
        console.log(`add +${points}`);
    }

    function decreaseScore(points){
        score-= points;
        console.log(`add -${points}`);
    }

    function getScore(){
        return score;
    }

    return {increeseScore , decreaseScore , getScore};
}

const game = createGame();

game.increeseScore(10);
game.increeseScore(10);
game.decreaseScore(6)
console.log(game.getScore())   

let timeoutId;

function staertTimeout(){
    timeoutId = setTimeout(() => window.alert("HELLO WORLD") , 3000);
    console.log("start")
}

function stopTimeout(){
    clearTimeout(timeoutId);
    console.log("stop");
}

<body>
    
    <button onclick="staertTimeout()">start</button>
    <button onclick="stopTimeout()">sopt</button>
    <script src="main.js"></script>
</body>


																																										//clock program

function updateClock(){
    const now = new Date();
    const hours = now.getHours().toString().padStart(2 , "0");
    const min = now.getMinutes().toString().padStart(2 , "0");
    const sec = now.getSeconds().toString().padStart(2 , "0");
    const time = `${hours}:${min}:${sec}`;
    document.getElementById("clock").textContent = time;
}

updateClock();
setInterval(updateClock , 1000);

    <div id="clock_container">
        <div id="clock">00:00:00</div>
    </div>
	
	body{
    background-color: hsl(0, 0%, 71%);
}

#clock_container{
    display: flex;
    justify-content: center;
}

#clock{
    font-size: 6.5em;
}

																																										//stopwatch program 

const stopwatch = document.getElementById("stopwatch");
let timer = null;
let startTime = 0;
let elapsedTime = 0;
let isRunning = false;

function start(){
    if(!isRunning){
        startTime = Date.now() - elapsedTime;
        timer = setInterval(update , 1000);
        isRunning = true;
    }
}

function stop(){
    if(isRunning){
        clearInterval(timer);
        elapsedTime = Date.now() - startTime;
        isRunning = false;
    }
}

function reset(){
    clearInterval(timer);
    
    startTime = 0;
    elapsedTime = 0;
    isRunning = false;
    stopwatch.textContent = "00:00:00";
}

function update(){
    const currentTime = Date.now();
    elapsedTime = currentTime - startTime;
    let hours = Math.floor(elapsedTime / (1000 * 60 * 60));
    let min = Math.floor(elapsedTime / (1000 * 60) % 60);
    let sec = Math.floor(elapsedTime / 1000 % 60);

    hours = hours.toString().padStart(2, "0");
    min = min.toString().padStart(2, "0");
    sec = sec.toString().padStart(2, "0");


    stopwatch.textContent = `${hours}:${min}:${sec}`;
}

//
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css.css">
</head>
<body>
    <h1>Stopwatch</h1>
    <div id="container">
        <div id="stopwatch">00:00:00</div><br>
        <div id="btns">
            <button id="startBtn" onclick="start()">Start</button>
            <button id="stopBtn" onclick="stop()">Stop</button>
            <button id="restBtn" onclick="reset()">Reset</button>
        </div>
    </div>
    <script src="main.js"></script>
</body>
</html>

//q
body{
    background-color: rgb(206, 206, 206);
    justify-content: center;
}
h1{
    font-size: 3rem;
    font-family: "Gill Sans", sans-serif;
    display: flex;
    justify-content: center;

}

#container{
    background-color: rgb(239, 239, 239);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    
    border: 5px solid black;
    height: 150px;
    border-radius: 30px;
}

#stopwatch{
    font-size: 6rem;
}

#btns{
    display: flex;
    gap: 10px;
    margin-bottom: 15px;
    
}
#btns button{
    width: 80px;
    height: 30px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    border-radius: 7px;
    border: none;
}


#startBtn{
    background-color: rgb(0, 203, 37);
}
#startBtn:hover{
    background-color: rgba(0, 203, 37, 0.236);
}

#stopBtn{
    background-color: rgb(247, 27, 27);
}
#stopBtn:hover{
    background-color: rgba(247, 27, 27, 0.361);
}

#restBtn{
    background-color: rgb(0, 123, 216);
}
#restBtn:hover{
    background-color: rgba(0, 122, 216, 0.378);
}





																																		//ES6 Module = file for a reusable code

export const PI = 3.14159

export function getCircomference(raduis){
    return raduis * PI * 2;
}

export function getArea(raduis){
    return raduis * raduis * PI;
}

 <script type="module" src="main.js"></script>
 
 import {PI , getCircomference , getArea} from './mathUtil.js';

console.group(PI);
console.log(getCircomference(5));


																																								//idk

function fun1(callback){
    setTimeout(() => {
        console.log("Task 1");
        callback();
    }, 3000);
}

function fun2(){
    console.log("Task 2");
    console.log("Task 3");
    console.log("Task 4");
}

fun1(fun2)


																																								//error handling
																																									//try{}catch(error){}finally{}
try{
    console.log(x);
}
catch(error){
    //Network Errors
    //Promise Rejection
    //Security Error
    console.error(error);
}
finally{
    //Close file
    //Close connection
    //Release ressources

    console.log("always this executed !");
}

console.log("This is the end ");



																																										//calculator program

try{
    const dividen = Number(window.prompt("num")); 
    const divisor = Number(window.prompt("num")); 

    if(divisor == 0){
        throw new Error("you can't divide by 0");
    }
    if(isNaN(dividen) || isNaN(divisor)){
        throw new Error("isNaN")
    }
    const result = dividen / divisor;
    console.log(result);
}
catch(error){
    console.error(error);
}


console.log("This is the end ");

const display = document.getElementById("display");


function appendToDisplay(input){
    display.value += input;
}



function clearDisplay(){
    display.value = "";
}
function display_element(){
    try{
    
        display.value = eval(display.value)
    }
    catch(error){
        console.log("zebi ");
        display.value = "ERROR ZEBI";
    }
}

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css.css">
</head>
<body>
    <div id="calculator_container">
        <input id="display" readonly>
            <div id="btn">
                <div id="963=">
                    <button onclick="appendToDisplay('9')" class="number">9</button>
                    <button onclick="appendToDisplay('6')" class="number">6</button>
                    <button onclick="appendToDisplay('3')" class="number">3</button>
                    <button onclick="display_element()" class="symbole">=</button>
                </div>
            
                <div id="852.">
                    <button id="8" class="number" onclick="appendToDisplay('8')">8</button>
                    <button id="5" class="number" onclick="appendToDisplay('5')">5</button>
                    <button id="2" class="number" onclick="appendToDisplay('2')">2</button>
                    <button id="." class="symbole" onclick="appendToDisplay('.')">.</button>
                </div>
                    
                <div id="7410">
                    <button id="7" class="number" onclick="appendToDisplay('7')">7</button>
                    <button id="4" class="number" onclick="appendToDisplay('4')">4</button>
                    <button id="1" class="number" onclick="appendToDisplay('1')">1</button>
                    <button id="0" class="number" onclick="appendToDisplay('0')">0</button>
                </div>
                    
                    
                <div id="symboles">
                    <button id="+" onclick="appendToDisplay('+')">+</button>
                    <button id="-" onclick="appendToDisplay('-')">-</button>
                    <button id="*" onclick="appendToDisplay('*')">*</button>
                    <button id="/" onclick="appendToDisplay('/')">/</button>
                    <button id="C" onclick="clearDisplay()">C</button>
                </div>
            </div>
    </div>
    <script src="main.js"></script>
    
</body>
</html>


body{

    display: flex;
    justify-content: center;
}

#calculator_container{
    background-color: hsl(0, 0%, 9%);
    margin: 10px;
    border-radius: 20px;
    width: 400px;
}

#display{
    background-color: rgb(55, 55, 55);
    width: 348px;
    height: 100px;
    border-radius: 20px 20px 0 0 ;
    padding: 0px;
    margin: 0%;
    margin-bottom: 10px;
    
}

#btn{
    width: 300px;
    display: flex;
}
#btn button{
    border-radius: 50%;
    width: 80px;
    height: 80px;
    padding: 25px;
    margin: 10px;
    font-size: 3.5rem;
    align-items: center;
    display: flex;
    justify-content: center;
    font-weight: bold;
}

.number{
    background-color: rgb(124, 124, 124);
    color: white;
}
.number:hover{
    background-color: rgb(171, 171, 171);
}
    

#symboles button{
    background-color: rgb(237, 165, 30);
}
#symboles button:hover{
    background-color: rgba(255, 189, 66, 0.754);
}

.symbole{
    background-color: rgb(237, 165, 30);
}
.symbole:hover{
    background-color: rgba(255, 189, 66, 0.754);
}
#display{
    padding: 25px;
    color: rgb(197, 255, 60);
    font-size: 3.5rem;
    align-items: center;
    display: flex;
    justify-content: center;
    font-weight: bold;
}




                                                            //DOM
                                                    
                                                            

document.title = "My website";
document.body.style.backgroundColor = "grey";
console.dir(document);

const username = " nano";
const wlcomMsg = document.getElementById("welcom_msg");
wlcomMsg.textContent += username === "" ? "Guest" : username




																													//1.getelementbyid();     ELEMENT / NULL
																													//2.getelementsbyclassname(); HTML COLLECTION
																													//3.getElementsByClassName(); HTML COLLECTION
																													//4.querySelector(); FIRTS ELEMENT OR NULL
																													//5.querySelectorAll(); NODELIST

const fruits = document.getElementsByClassName("fruits");

//fruits[0].style.backgroundColor = "red";

Array.from(fruits).forEach((fruit) => 
       fruit.style.backgroundColor = "red" );


const header = document.getElementsByTagName("h1");
const list = document.getElementsByTagName("li");

Array.from(header).forEach((element) => element.style.backgroundColor = "yellow" );
Array.from(list).forEach((element) => element.style.backgroundColor = "green" );

/*for(let element of header){
    element.style.backgroundColor = "yellow";
}

for(let element of list){
    element.style.backgroundColor = "green";
}*/

const element = document.querySelector(".fruits");
element.style.backgroundColor = "black";

const FRUITS = document.querySelectorAll(".fruits");
FRUITS[0].style.backgroundColor = "pink";

const FOODS = document.querySelectorAll("li");
FOODS.forEach((element) => element.style.backgroundColor = "purple");





<div class="fruits">Apple</div>
    <div class="fruits">Banana</div>
    <div class="fruits">Orange</div>

    <h1>root vegetebeles</h1>
    <ul>
        <li>Beets</li>
        <li>Carrots</li>
        <li>Potatoes</li>
    </ul>

    <h1>not root vegetebeles</h2>
    <ul>
        <li>Broccoli</li>
        <li>Celery</li>
        <li>Onions</li>
    </ul>
	
	
	
	
	
																														//-------- .firstElementChild ---------

const element = document.getElementById("fruits");

const firstchild = element.firstElementChild;
firstchild.style.backgroundColor = "pink";

const ulElement = document.querySelectorAll("ul");
ulElement.forEach(ulelement => {
    const firstchild = ulelement.firstElementChild;
    firstchild.style.backgroundColor = "purple"
});



																															//-----------.lastElementChild------------
const element = document.getElementById("fruits");

const lastChild = element.lastElementChild;
lastChild.style.backgroundColor = "pink";

const ulElement = document.querySelectorAll("ul");
ulElement.forEach((ulelement) => {
    const lastchild = ulelement.lastElementChild;
        lastchild.style.backgroundColor = "red";
    
});


																																	//---------.nextElementSibling-----------

const element = document.getElementById("apple");
const nextSebling = element.nextElementSibling;
nextSebling.style.backgroundColor = "green";0

																																			//---------.nextElementSibling-----------

const element1 = document.getElementById("onions");
const privousSibling = element1.previousElementSibling;
privousSibling.style.backgroundColor = "green";

																																		//------------.parentElement--------------
const element2 = document.getElementById("pie");
const parent = element2.parentElement;
parent.style.backgroundColor = "yellow"

const element3 = document.getElementById("vegetebales");
const children = element3.children;
Array.from(children).forEach(elem => 
    elem.style.backgroundColor = "orange"
)
children[0].style.backgroundColor = "pink"




																																			//ADD AND CHANGE HTML

// Step1 : creat the element
const newH1 = document.createElement("h1");

// Step2 : Add attributes/Prpreties
newH1.textContent = "I like pizza";
newH1.id = "myH1";
newH1.style.color = "tomato";
newH1.style.textAlign = "center"

// Step3 : append element to DOM
// document.body.append(newH1);//append at the end
// document.body.prepend(newH1);//append at the bigining1 
// document.getElementById("box1").append(newH1);
 document.getElementById("box1").prepend(newH1);

// const box2 = document.getElementById("box2");
// document.body.insertBefore(newH1 , box2);

//const boxes = document.querySelectorAll(".box");
//document.body.insertBefore(newH1 , boxes[2]);

//REMOVE HTML 
//document.body.removeChild(newH1);
document.getElementById("box1").removeChild(newH1)




// Step1 : creat the element
const newH1 = document.createElement("h1");

// Step2 : Add attributes/Prpreties
newH1.textContent = "I like pizza";
newH1.id = "myH1";
newH1.style.color = "tomato";
newH1.style.textAlign = "center"

// Step3 : append element to DOM
// document.body.append(newH1);//append at the end
// document.body.prepend(newH1);//append at the bigining1 
// document.getElementById("box1").append(newH1);
 document.getElementById("box1").prepend(newH1);

// const box2 = document.getElementById("box2");
// document.body.insertBefore(newH1 , box2);

//const boxes = document.querySelectorAll(".box");
//document.body.insertBefore(newH1 , boxes[2]);

//REMOVE HTML 
//document.body.removeChild(newH1);
document.getElementById("box1").removeChild(newH1);




const newFruit = document.createElement("li");

newFruit.textContent = "yellow";
newFruit.style.backgroundColor = "yellow";


//document.getElementById("fruits").append(newFruit);

//const orange = document.getElementById("orange");
//document.getElementById("fruits").insertBefore(newFruit , orange);

//if no id
const listitems = document.querySelectorAll("#fruits li");
document.getElementById("fruits").insertBefore(newFruit , listitems[0]);


<ol id="fruits">
            <li id="apple">apple</li>
            <li id="orange">orange</li>
            <li id="banana">banana</li>
        </ol>
    
	
	
	
																																							//event listener:  .addEventListener("event" , callback);
																																						//mouseover , click , mouseout

const mybox = document.getElementById("box");
const mybtn = document.getElementById("myBtn");
/*function changeColor(event){
    event.target.style.backgroundColor = "tomato";
    event.target.textContent = "OUCH 🫨";
}*/

/*mybox.addEventListener("click" , (event) => {
        event.target.style.backgroundColor = "tomato";
        event.target.textContent = "OUCH 🫨";
});

mybox.addEventListener("mouseover" , (event) => {
        event.target.style.backgroundColor = "pink";
        event.target.textContent = "hmmm .. ☺️";
});

mybox.addEventListener("mouseout" , event => 
{
    event.target.style.backgroundColor = "lightgreen";
    event.target.textContent = "click me 😉";
}
)*/

mybtn.addEventListener("click" , (event) => {
        mybox.style.backgroundColor = "tomato";
        mybox.textContent = "OUCH 🫨";
});

mybtn.addEventListener("mouseover" , (event) => {
        mybox.style.backgroundColor = "pink";
        mybox.textContent = "hmmm .. ☺️";
});

mybtn.addEventListener("mouseout" , event => 
{
    mybox.style.backgroundColor = "lightgreen";
    mybox.textContent = "click me 😉";
}
)


//css

#box{
    background-color: lightgreen;
    width: 300px;
    height: 300px;
    font-size: 4.5rem;
    font-weight: bold;
    display: flex;
    align-items: center;
    text-align: center;
    cursor: pointer;
}

#myBtn{
    height: auto;
    width: auto;
    font-size: 2rem;
    
}

																													//Key events


 <div id="box">😉</div>
 
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css.css">
</head>
<body>
    
        <div id="box">😉</div>

        
    

    <script src="main.js"></script>
    
</body>
</html>





const box = document.getElementById("box");
const movAmont = 50;
let x = 0;
let y = 0;

box.style.position = "absolute";
box.style.top = "0px";
box.style.left = "0px";

document.addEventListener("keydown" , () => {
    box.textContent = "🙂‍↔️";
    box.style.backgroundColor = "lightblue";
});

document.addEventListener("keyup" , () => {
    box.textContent = "😉";
    box.style.backgroundColor = "lightgreen";
});



document.addEventListener("keydown" , (event) => {
    if(event.key.startsWith("Arrow")){
        event.preventDefault();
        switch(event.key){
            case "ArrowUp":
                y -= movAmont;
                break;
            case "ArrowDown":
                y += movAmont;
                break;
            case "ArrowLeft":
                x -= movAmont;
                break;
            case "ArrowRight":
                x += movAmont;
                break;
        }
        box.style.top = `${y}px`;
        box.style.left = `${x}px`;
    }
});


#box{
    background-color: lightgreen;
    width: 300px;
    height: 300px;
    font-size: 15rem;
    font-weight: bold;
    display: flex;
    align-items: center;
    text-align: center;
    cursor: pointer;
}


																																			//hide and show html
	
<img id="myImage"src="photo.jpeg" width="300px"><br>
    <button id="btnHide">Hide</button><br>
	
	
	
	

const btn = document.getElementById("btnHide");
const img = document.getElementById("myImage");


/*btn.addEventListener("click" , event => {

    if(img.style.display === "none"){ //better use visibility to preseve the space of the photo 
        img.style.display = "block";
        btn.textContent = "Hide";
    }
    else{
        img.style.display = "none";
        btn.textContent = "Show";
    }

    
})*/


btn.addEventListener("click" , event => {

    if(img.style.visibility === "hidden"){ //better use visibility to preseve the space of the photo 
        img.style.visibility = "visible";
        btn.textContent = "Hide";
    }
    else{
        img.style.visibility = "hidden";
        btn.textContent = "Show";
    }

    
})









																																												//node list  : static colection  

let btn = document.querySelectorAll(".btn");
                                                                            //event click mouse over mouseout

/*btn.forEach(button => {
    button.style.backgroundColor = "green";
    button.textContent += "🫠";
});*/

/*btn.forEach(button => {
    button.addEventListener("click" , (event) => {
        button.style.backgroundColor = "tomato";
    })
});*/

/*btn.forEach(button => {
    button.addEventListener("mouseover" , (event) => {
        event.target.style.backgroundColor = "tomato";

    })
});

btn.forEach(button => {
    button.addEventListener("mouseout" , (event) => {
        event.target.style.backgroundColor = "hsl(197, 100%, 59%)";

    });
});*/


/*
const newBtn = document.createElement("button");
newBtn.textContent = "BUtton 5";
newBtn.classList = "btn";
document.body.appendChild(newBtn);

btn = document.querySelectorAll(".btn"); //=> to add the new element to the node 
*/


                                                              //remove an element

btn.forEach(element => {
    element.addEventListener("click" , (event) => {
        event.target.remove(); //still in the nodelist
        document.querySelectorAll(".btn");
    });
})


<button id="btn1" class="btn">button 1</button><br>
    <button id="btn2" class="btn">button 2</button><br>
    <button id="btn3" class="btn">button 3</button><br>
    <button id="btn4" class="btn">button 4</button><br>
    
	
	
	
	
	
	
	
	

const btn = document.getElementById("btn");
    //add remove togle
/*btn.classList.add("enabled");
btn.classList.remove("enabled");

btn.addEventListener("mouseover" , (event) => {
    event.target.classList.add("hover"); //togle
});

btn.addEventListener("mouseout" , (event) => {
    event.target.classList.remove("hover"); //togle
});*/





const btn = document.getElementById("btn");
const myH1 = document.getElementById("myH1");

        //replace

/*btn.classList.add("enabled");

btn.addEventListener("click" , event => {
    event.target.classList.replace("enabled" , "disabled");
})
*/

myH1.classList.add("enabled");
btn.classList.add("enabled");

myH1.addEventListener("click" , event => {

    if(event.target.classList.contains("disabled")){
        event.target.textContent += "🤬"
    }else{
        event.target.classList.replace("enabled" , "disabled");
    }
    
});


btn.addEventListener("click" , event => {

    if(event.target.classList.contains("disabled")){
        event.target.textContent += "🤬"
    }else{
        event.target.classList.replace("enabled" , "disabled");
    }
    
});



<button id="btn" >button 1</button><br>

#btn{
    font-size: 3rem;
    
    
    border-radius: 10px;
    border:none;
    padding: 10px;
    margin: 10px;
}

.enabled{
    background-color: crimson;

}

.hover{
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.309);
    font-weight: bold;
}

.disabled{
    background-color: hsl(0, 0%, 50%);
    color: hsl(0, 0%, 80%);
}






																																												//


let btns = document.querySelectorAll(".btns");

btns.forEach(btn => {
    btn.classList.add("enabled");
})

btns.forEach(btn => {
    btn.addEventListener("mouseover" , event => {
        event.target.classList.toggle("hover");
    });
});

btns.forEach(btn => {
    btn.addEventListener("mouseout" , event => {
        event.target.classList.toggle("hover");
    });
});

btns.forEach(btn => {
    btn.addEventListener("click" , event => {
        if(event.target.classList.contains("disabled")){
            btn.textContent += "😶‍🌫️";
        }
        else{
            event.target.classList.replace("enabled" , "disabled");
        }
         
    });
});


<button class="btns">button 1</button><br>
    <button class="btns">button 2</button><br>
    <button class="btns">button 3</button><br>
    <button class="btns">button 4</button><br>
	
	.btns{
    font-size: 3rem;
    
    
    border-radius: 10px;
    border:none;
    padding: 10px;
    margin: 10px;
}

.enabled{
    background-color: crimson;

}

.hover{
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.309);
    font-weight: bold;
}

.disabled{
    background-color: hsl(0, 0%, 50%);
    color: hsl(0, 0%, 80%);
}

#myH1{
    font-size: 4rem;
}


																											//Callback Hell = <><><><><><<><><><>><><><><><><
																											//use Promise +asyc/await to avoide callbacks hell 


function task1(callback){
    setTimeout(() => {
        console.log("Task 1 compleate");
        callback();
    }, 3000);
}

function task2(callback){
    setTimeout(() => {
        console.log("Task 2 compleate");
        callback();
    }, 2000);
}

function task3(callback){
    setTimeout(() => {
        console.log("Task 3 compleate");
        callback();
    }, 15000);
}

function task4(callback){
    setTimeout(() => {
        console.log("Task 4 compleate");
        callback();
    }, 1000);
}

task1(() => {
    task2(() => {
        task3(() => {
            task4(() => {
                console.log("All tasks complet");
            })
        })
    })
})



																																					//Promise = 

/*function walkDog(callback){
    setTimeout(() => {
        console.log("You walk the Dog");
        callback();
    } , 1000);
}

function cleanKitchen(callback){
    setTimeout(() => {
        console.log("You clean the kithen");
        callback();
    } , 2000);
}

function takeTrash(callback){
    setTimeout(() => {
        console.log("You take out the trash");
        callback();
    } , 800);
}


walkDog(() => {
    cleanKitchen(() => {
        takeTrash(() =>{
            console.log("You finsh all tasks")
        })
    })
})*/




//Promise = new Promise((resolve , reject) => {code})

function walkDog(){
    return new Promise((resolve , reject) => {
        setTimeout(() => {
            const walkTheDog = true;

            if(walkTheDog){
                resolve("You walk the Dog");
            }
            else{
                reject("You DIDN'T walk the Dog");
            }
        } , 1000);
    })
}

function cleanKitchen(){
    

    return new Promise((resolve , reject) => {
        setTimeout(() => {
            const cleanTheKitchen = true;
            if(cleanTheKitchen){
                resolve("You clean the kithen");
            }
            else{
                reject("You DIDN'T clean the kithen")
            }
            
        } , 2000);
    })
}

function takeTrash(){
    
    return new Promise((resolve , reject) => {
        setTimeout(() => {
            const takeOutTrash = false;
            if(takeOutTrash){
                resolve("You take out the trash");
            }
            else{
                reject("You DIDN'T take out the trash")
            }
            
        } , 800);
    })
}


walkDog().then(value => {console.log(value); return cleanKitchen()})
         .then(value => {console.log(value); return takeTrash()})
         .then(value => {console.log(value); console.log("you finished all the chores")})
         .catch(error => console.error(error)); //reject//
		 
		 
		 
		 
																																			 
																																			 
																																	// Async/Await = Async = make the a function to return a promise 
																																	//               Await = make a Async function to wait a promise 


function walkDog(){
    return new Promise((resolve , reject) => {
        setTimeout(() => {
            const walkTheDog = true;

            if(walkTheDog){
                resolve("You walk the Dog");
            }
            else{
                reject("You DIDN'T walk the Dog");
            }
        } , 1000);
    })
}

function cleanKitchen(){
    

    return new Promise((resolve , reject) => {
        setTimeout(() => {
            const cleanTheKitchen = true;
            if(cleanTheKitchen){
                resolve("You clean the kithen");
            }
            else{
                reject("You DIDN'T clean the kithen")
            }
            
        } , 2000);
    })
}

function takeTrash(){
    
    return new Promise((resolve , reject) => {
        setTimeout(() => {
            const takeOutTrash = false;
            if(takeOutTrash){
                resolve("You take out the trash");
            }
            else{
                reject("You DIDN'T take out the trash")
            }
            
        } , 800);
    })
}


async function doChores(){

    try{
        const doWalkDog = await walkDog();
        console.log(doWalkDog);

        const doCleanKitchen = await cleanKitchen();
        console.log(doCleanKitchen);

        const doTakeTrash = await takeTrash();
        console.log(doTakeTrash);

    }
    catch(error){
        console.error(error)
    }
}
doChores();

																															// JSON = (JavaScript Object Notation) data-interchange format
																															//        Used for exchanging data between a server and a web application
																															//        JSON files {key:value} OR [value1, value2, value3]

																															// JSON.stringify() = converts a JS object to a JSON string.
																															// JSON.parse() = converts a JSON string to a JS object
//  JSON.stringify() = convert a JS object to string 

const names = ["nano" , "omar" , "el" , "ghazali"];
const person = {
    "name" : "nano",
    "age" : 19,
    "isStudent" : true,
    "hobbies" : ["coding" , "watching" , "idk"]
}

const people = [
{
    "name" : "nano",
    "age" : 19,
    "isStudent" : true

},
{
    "omar" : "nano",
    "age" : 27,
    "isStudent" : true
    
},
{
    "name" : "el",
    "age" : 15,
    "isStudent" : true

},
{
    "name" : "ghazali",
    "age" : 19,
    "isStudent" : false

}
];



// JSON.parse = convert a JSON string to a JS object

const jsonNames = `["nano" , "omar" , "el" , "ghazali"]`;
const jsonPerson = `{"name" : "nano","age" : 19,"isStudent" : true,"hobbies" : ["coding" , "watching" , "idk"]}`;

const jsonPeople = `[
                {"name" : "nano","age" : 19,"isStudent" : true},
                {"omar" : "nano","age" : 27,"isStudent" : true},
                {"name" : "el","age" : 15,"isStudent" : true},
                {"name" : "ghazali","age" : 19,"isStudent" : false}]`;

const parsedData = JSON.parse(jsonNames)
console.log(parsedData)




fetch("names.json")
.then(response => response.json())
.then(values => values.forEach((value) => console.log(value))).catch(error => console.error(error))


																																// fetch = Function used for making HTTP requests to fetch resources.
																																//         (JSON style data, images, files)
																																//         Simplifies asynchronous data fetching in JavaScript and
																																//         is used for interacting with APIs to retrieve and send
																																//         data asynchronously over the web.
																																//
																																//         fetch(url, {options})



fetch("https://pokeapi.co/api/v2/pokemon/pikachu")
    .then(response => {
        if(!response.ok){
            throw new Error("could not fetch the data");
        }
        return response.json();
    })
    .then(data => console.log(data.name))
    .catch(error => console.error(error))
	
	
	
async function fetchData(){

    try{
        const response = await fetch("https://pokeapi.co/api/v2/pokemon/pikachu");
        if(!response.ok){
            throw new Error("could not fetch data");
        }
        const data = await response.json();
        console.log(data);
    }
    catch(error){
        console.error(error);
    }
}

fetchData();







async function fetchData(){

    try{

        const pokemonName = document.getElementById("pokemonName").value.toLowerCase();
        const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${pokemonName}`);
        if(!response.ok){
            throw new Error("could not fetch data");
        }
        const data = await response.json();
        const pokemonSprite = data.sprites.front_default;
        const imgElemnt = document.getElementById("pokemonSprite");

        imgElemnt.src = pokemonSprite;
        imgElemnt.style.display = "block"
        console.log(data);
    }
    catch(error){
        console.error(error);
    }
}

    <input type="text" id="pokemonName" placeholder="Enter Pokemon name">
    <button onclick="fetchData()">fetch data</button>

    <img src="" style="display: none" id="pokemonSprite">
arr

