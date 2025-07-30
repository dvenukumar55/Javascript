# Javascript
A collection of my JavaScript learning journey, including exercises, projects, and notes to track progress and reinforce concepts.

/* random num gen

 const mybutton=document.getElementById("mybutton");
 const label1= document.getElementById("label1");
 const label2= document.getElementById("label2");
 const label3= document.getElementById("label3");
 const min=1;
 const max=10;
 let randomnum1;
 let randomnum2;
 let randomnum3;
 mybutton.onclick=function(){
   randomnum1=Math.floor(Math.random()*max)+min;
     randomnum2=Math.floor(Math.random()*max)+min;
       randomnum3=Math.floor(Math.random()*max)+min;
       label1.textContent=randomnum1;
       label2.textContent=randomnum2;
       label3.textContent=randomnum3;
 }
       */

 /* ternary operator
 let age=12;
 let msg= age>=18 ? "eligible to vote" : "not eligible to vote";
 console.log(msg);
 */

 /* switch

 let day=4;
 switch(day){
   case 1:
       console.log("it is sunday");
       break;
   case 2:
       console.log("it is mon");
       break;

   case 3:
       console.log("it is tue");
       break;

   default:
      console.log("week has only 7 days");
      break;    

 }
*/


/* string methods

let uname="venukumar" ;

console.log(uname.charAt(7));

console.log(uname.indexOf("u"));

console.log(uname.length);

uname=uname.toUpperCase();
console.log(uname);
 
//uname=uname.repeat(3);
//console.log(uname);

let result= uname.startsWith(" ");
 if(result){
   console.log("not starts with space");

 }
 else{
   console.log(uname);
 }
 

 let result1= uname.endsWith(" ");
 if(result1){
   console.log("not ends with space");

 }
 else{
   console.log(uname);
 }
 

 let result3= uname.includes(" ");
 if(result3){
   console.log("not includes space");

 }
 else{
   console.log(uname);
 }
*/


/* number guessing game

const min=50;
const max=100;
const ans= Math.floor(Math.random()*(max-min+1))+min;
//console.log(ans);
let attem=0;
let guess;
let running=true;
while(running){
  guess=window.prompt(`guess num bw ${min}-${max}`);
  guess=Number(guess);
 if(isNaN(guess)){
  window.alert("plz enter the valid num")
 }
 else if(guess<min || guess>max){
  window.alert("not valid")
 }
 else{
  attem++;
  if(guess<ans){
    window.alert("low..try agian");
  }
  else if(guess>ans){
       window.alert("high...try again")
  }
  else{
    window.alert(`correct! the num is ${ans}.It took ${attem} attempts to guess answer`)
    running=false;
  }
 }
}
 */


/* functions

function add(x,y){
  return x+y;
}
function sub(x,y){
  return x-y;
}
function mul(x,y){
  return x*y;
}
function div(x,y){
  return x/y;
}

console.log(add(500,55))
console.log(sub(50,45))
console.log(mul(11,5))
console.log(div(165,3))


function even(num){
 return num %2 ===0?true:false;
}
console.log(even(43));
*/


/* temp converter

const tb=document.getElementById("tb");
const f=document.getElementById("f");
const c=document.getElementById("c");
const result=document.getElementById("result");
let temp;
function covert(){
  if (f.checked) {
    result.textContent=" u select to F ";
    temp=Number(tb.value);
    temp=temp*9/5 +32;
    result.textContent=temp+"F";

  }
  
  else if(c.checked){
      result.textContent="u select to C";
       temp=Number(tb.value);
    temp=(temp-32)*(5/9);
    result.textContent=temp+"C";


  }
  
  else{
    result.textContent="select unit";
  }
}
  */


/* array methods
let fr=["mango","apple","orange"];
//fr.push("coconut");
//fr.shift();
//fr.pop();
//fr.unshift("guava");
//console.log(fr[2]);
//console.log(fr);
//console.log(fr.length);
//console.log(fr.indexOf("orange"));
//fr.sort();
//fr.sort().reverse();

for (let i = 0; i< fr.length; i++) {
console.log(fr[i]);
}
*/

/* spread operator(...) used to separete char
let num=[1,2,3,4,5,6];
let maxi=Math.max(...num);
let mini=Math.min(...num);
console.log(maxi);
console.log(mini);

let name1="venukumar";
let letter=[...name1].join(".");
console.log(letter);
*/


/* rest parameters(opp to spread)
function names(...namess)
{
  console.log(namess);
}
const n1="venu";
const n2="suddhi";
names(n1,n2);
*/

/* random password generator

function genpas(length,il,iu,inu,isy){
  const lc="abcdefghijhklmnopqrstuvwxyz";
  const uc="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  const nc="1234567890";
  const sc="!@#$%^&*()_+=-~`";

  let allowchars="";
  let pw="";

  allowchars+=il?lc:"";
  allowchars+=iu?uc:"";
  allowchars+=inu?nc:"";
  allowchars+=isy?sc:"";

 if (length<=0) {
  return`(pw must be atleast 1 char)`;
 }
 if (allowchars.length===0) {
  return`(atleast 1 char)`;
 }

 for(let i=0;i<length;i++){
  const ranind=Math.floor(Math.random()* allowchars.length);
  pw+=allowchars[ranind];
 }

  return pw;
}
const pl=8;
const il=true;
const iu=true;
const inu =true;
const isy =true;


const pw= genpas(pl,il,iu,inu,isy);

console.log(`gen pw:${pw}`);
*/

// CALLBACK: is a func is passed to an argument to another func

/* forEach: used to iterate over the items

let num=[1,2,3,4,5];
num.forEach(double);
num.forEach(dispaly);

function double(element,index,array){
  array[index]=element*2;
}
function dispaly(element){
  console.log(element);
}
  */


/* map: accepts a cllback and applies that func
to each element of an array ,then return a new array

const num=[1,2,3,4,5];
const sq=num.map(squ);
console.log(sq);

 function squ(element){
  return Math.pow(element,2);
   
 }
  */


 /* filter: craetes new array by filtering out elemnts

 let num=[1,2,3,4,5,6,7,8];
 let evennum=num.filter(even);
 console.log(evennum);

 function even(element){
  return element%2===0;
 }
 */


 /* filter: reduce the elements of an array to single value

 const prices=[24,36,20,12,8];
 const total=prices.reduce(sum);

 console.log(`$${total.toFixed(2)}`);

 function sum(prev,next){
  return prev+next;
 }
*/

/* func expression: way to define fun's as variables or
    values

const hello=function(){
  console.log("hiiii");
}

setTimeout(function(){
  console.log("goodbye");
})
*/


/*
arrow fun's: way to write function expressions good for simple
fun's that you use only oncle => some code
const hello=(name1,age)=>{console.log(`hello ${name1}`)
                          console.log(`you are ${age} years old`)};
hello("venu",20);
*/

/* objects: collection of related properties and or methods
can reprseent real world objects{key:value
                                  funtion()}

 const person1={
  fn:"venu",
  ln:"dandetikar",
  age:20,
  hii:function(){console.log("hey..this is venukumar")}
}
//console.log(person1.fn);
//console.log(person1.ln);
//console.log(person1.age);
 person1.hii();
 */


 /*
 THIS:ref to obj where it is used
 const person1={
  fn:"venu",
  ln:"dandetikar",
  age:20,
  hii:function(){console.log(`hey..this is ${this.fn}`)},
  hey:function(){ console.log(`${this.fn} age is ${this.age}`)},
}

 person1.hii();
  person1.hey();
*/

/* constructo: method to define properties 
and method of objects

function stu(id,nm,st)
{
  this.id=id,
  this.nm=nm,
  this.st=st
}
const stu1=new stu(1,"venu","cse");
 console.log(stu1.id);
  console.log(stu1.nm);
   console.log(stu1.st);
   */

/* class: cleaner way to work with objects
   class product{
    constructor(name,price){
      this.name=name;
      this.price=price;
    }
    display(){
      console.log(`product:${this.name}`);
      console.log(`product:${this.price}`);
    }
   }
   const product1=new product("cargoo",500);

   product1.display();
   */

   /* inheritance:allow new class to to inherit prop
   and meth from an existing class

class animal{
  eat(){
    console.log(`this is ${this.name} and i am  eating my lollipop`);
  }
}
class Lion extends animal{
  name="lion";
}

const lion = new Lion();
lion.eat();
*/


/*
super keyword:used inclasses to call the consrtuctor or access the
properties and methods of parent

class animal{
  constructor(name,age){

  }
}
class Lion extends animal{
  constructor(name,age){
    super(name,age)
    this.name=name;
    this.age=age;
  }
}

const lion=new Lion("lion",20);
console.log(lion.name);
console.log(lion.age);
*/

/* setters and getters

//setter:method makes prop readable
//getter:method that makes writeable

class per{
  constructor(fn,ln,age){
    this.fn=fn;
    this.ln=ln;
    this.age=age;
  }
  set fn(newfn){
    if (typeof newfn==="string"&& newfn.length>0) {
      this._fn=newfn;
    }
    else{
      console.error("fn not be empty");
    }
  }
  set ln(newln){
    if (typeof newln==="string"&& newln.length>0) {
      this._ln=newln;
    }
    else{
      console.error("ln not be empty");
    }
  }
  set age(newage){
    if (typeof newage=== "number" && newage >= 0) {
      this._age = newage;
    }
    else{
      console.error("age not be empty");
    }
  }
  get fn(){
    return this._fn;
  }
   get ln(){
    return this._ln;
  }
  get fln(){
    return this._fn + " " + this._ln;
  }
   get age(){
    return this._age;
  }
}
const person=new per("venu","kumar",20);
console.log(person.fn);
console.log(person.ln);
console.log(person.fln);
console.log(person.age);
*/


/* destructuring: extarct values from arrays and objects
then assign them in a convenient way
[]= perform array destructuring
()=perform object destructuring 
//
let a=1;
let b=2;
[a,b]=[b,a];
console.log(a)
console.log(b)
//
const names=["venu","himam"];
[names[0],names[1]]=[names[1],names[0]];
console.log(names)
//
const name1=["venu","himam","vamshi","daya"];
const[fn,sn,...rn]=name1;
console.log(fn);
console.log(sn);
console.log(rn);
//
const person1={
  fin:"venu",
  lan:"kumar",
  age:20,
}
const{fin,lan,age}=person1;
console.log(fin)
console.log(lan)
console.log(age)
*/


/* nested objects:objects inside other object
const person={
  fn:"venukumar
   dandetikar",
  age:20,
  student:true,
  hobbies:["code","learn","apply"],
  add:{
    street:"padmavathi nagar",
    city:"chandur",
    coun:"ind"
  }
}
console.log(person.fn);
console.log(person.age);
console.log(person.student);
console.log(person.hobbies[1]);
console.log(person.add.street);
console.log(person.add.city);
*/


/*sort
let num=[1,2,4,8,3,9,5];
num.sort((a,b)=>a-b);
console.log(num)*/


/* shuffling an array

const nums=[1,2,3,4,5,6,7,7,8,9,0,7];
shuffle(nums);
console.log(nums);
 function shuffle(array){
  for (let i = array.length-1; i > 0; i--){
    const random = Math.floor(Math.random()*(i+1));
    [array[i],array[random]]=[array[random],array[i]];   
  }
 }
  */


 /*dates
 // Date(yr,mn,dy,hr,min,sec,msec)
 const dt=new Date();
 console
 */

/*closure: func inside other func
 function counterr(){
  let count=0;
  function inc(){
    count++;
    console.log(`count is ${count}`);
  }
  return{inc};
 }
 const counter=counterr();
 counter.inc();
  counter.inc();
   counter.inc();
   */

   /* setTimeout(),clearTimeout()
let cl=function saygreet(){
  window.alert("Hi venu");
}
setTimeout(saygreet,3000);
clearTimeout(cl);
*/

/* digital clock program

function updateclock(){

  const now=new Date();
  let hrs=now.getHours().toString().padStart(2,0);
  const meridian = hrs => 12 ? "PM" : "AM";
  hrs = hrs % 12||12;
  const mins=now.getMinutes().toString().padStart(2,0);
  const sec=now.getSeconds().toString().padStart(2,0);

  const timestri=`${hrs}:${mins}:${sec}`;
  document.getElementById("clock").textContent=timestri;
}
updateclock();
setInterval(updateclock,1000);
*/

/* stopwatch

  const dis=document.getElementById("dis");
  let timer=null;
  let stime=0;
  let elapsetime=0;
  let isrun=false;

  function start(){
   if (!isrun) {
    stime=Date.now()-elapsetime;
      timer=setInterval(update,10);
    isrun=true;
   }
  }
  function stop(){
       if (isrun)
        {
  clearInterval(timer);
  elapsetime=Date.now()-stime;
  isrun=false; 
  }
}

  function reset(){
    clearInterval(timer);
    let stime=0;
  let elapsetime=0;
  let isrun=false;
  dis.textContent="00:00:00:00";
  }
 


  function update(){
    const curt=Date.now();
    elapsetime=curt-stime;

    let hrs=Math.floor(elapsetime / (1000 * 60 * 60));
    let mins=Math.floor(elapsetime / (1000 * 60) % 60);
    let secs=Math.floor(elapsetime / 1000 % 60);
    let msec=Math.floor(elapsetime % 1000 / 10);

    hrs=String(hrs).padStart(2,"0");
    mins=String(mins).padStart(2,"0");
    secs=String(secs).padStart(2,"0");
    msec=String(msec).padStart(2,"0");
  dis.textContent= `${ hrs}:${mins}:${secs}:${msec}`;
  }
*/

/* asynchronus :allows multiple operations performed concurrently
without waiting

function func1(callback){
setTimeout(()=>{console.log("t1");
                 callback()},3000);
}
function func2(){
console.log("t2");
console.log("t3");
console.log("t4");
}
func1(func2);
func2(func1);
*/


/* error : try catch finally
try{
  console.log("venu");
}
catch(error){
  console.error(error);
}
finally{
  console.log("this always executed");
}
console.log("HELLO");



try{
     divd=Number(window.prompt("enter dividend"));
   divs=Number(window.prompt("enter divisor"));
   
   const res= divd / divs;
   console.log(res);

   if (divs===0) {
    throw new Error("impossible to divide by 0");
   }
   if (isNaN(divd)||isNaN(divs)) {
    throw new Error("it must be a number");
   }
}
catch(error){
  console.error(error);
}
finally{
  console.log("hiii");
}
console.log("u can't cheat me okay!");
*/


/*DOM document object model:represents the poage you see
in the page in web browser and provides you API to intercat with it

document.title="helloo";
document.body.style.backgroundColor="pink";
*/


/* element selectors

//const head=document.getElementById("h1");
//head.style.backgroundColor="blue";
//head.style.textAlign="left";

//const tl=document.getElementsByClassName("nm");
//tl[1].style.backgroundColor="pink";
//console.log(tl);


//const ff=document.getElementsByTagName("h3");
//ff.style.textAlign="center";

//const kk=document.querySelector("h1");
//kk.style.backgroundColor="black";
//console.log(kk);

//const jj=document.querySelectorAll("h3");   
//console.log(jj);
*/

/*html changing elemnts
const item=document.createElement("li");
item.textContent="banana";
document.body.append(item);
document.getElementById("frt").append(item);
//document.body.prepend(item);

const mango=document.getElementById("ma");
document.getElementById("frt").insertBefore(item,mango);
*/
