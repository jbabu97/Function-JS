# JavaScriptRandomPractice
- [Function](#Function)
- [ThisKeyWordAndArrowFunction](#ThisKeyWordAndArrowFunction)
- [IIFE](#IIFE)
- [Date](#Date)
- [Number](#Number)
- [Operator](#Operator)
- [Math](#Operator)
- [Rudecer](#Rudecer)
- [Filter](#Filter)
- [Map](#Map)

 ### Function
### ThisKeyWordAndArrowFunction
 
 ```js
 
 const newUser = {
      userName: "Babu",
      id: 11097,
      welcomeMessage: function(){
         console.log(`${this.userName} , welcome to jBabu's website`);
        console.log(this);
     }
 };
 
  newUser.welcomeMessage();
  newUser.userName= 'JabbarBabu'
  newUser.welcomeMessage();
 
  console.log(this);

const arrowFunction = function (){
    let usrName = 'jBabau'
    console.log(this.usrName);
};

const arrowFunction =  () => {
    let usrName = 'jBabau'
    console.log(this);
};

arrowFunction();

```
### IIFE 
```js
  const iifeFunc1 = function(){
      console.log(`IIFE_1: DB connected`);
  }();
  
  (function iifeFunc2(){
      console.log(`IIFE_2: DB connected`);
  })();
  
  ((name)=> {
      console.log(`${name}DB connected`);
  })('Mongo');
```
### FunctionDeclare
  ```js
const addNumbers = function(num1, num2){
       // let result =  num1 + num2;
       // return result;
       return num1 + num2;

  let result = addNumbers(8,9);
  
  console.log("Result: ", result);
  
  const userLoggedIn = function (userName){
      if (!userName) {
          return ("Please enter a valid user name.")
      }
     return (`${userName} just logged in`);
  }
  
  console.log(userLoggedIn('2'));
  
  // object in function
  
  const user = {
      name: 'Jabbar Babu',
      IdNumber: 97
  };
  
  const getUser = function(anyObj){
       return (`User name is ${anyObj.name} And Id number is ${anyObj.IdNumber} `);
  };
  
  // console.log(getUser(user));
  console.log(getUser({
      name: 'JBabu',
      IdNumber: 5
  }));
  
  // array in function
  
  const myArr = [500, 333, 555, 222, 666];
  
  const arrayIntoFunction = function(arr){
      // console.log(arr[3]);
      return arr[2];
  };
  
  // console.log(arrayIntoFunction(myArr));
  console.log(arrayIntoFunction([500,333, 555, 222,666]));
```
### Date
```js
  const newDate = new Date();
  
  console.log(newDate);
  console.log(newDate);
  console.log(newDate.toTimeString());
  console.log(newDate.toLocaleString());
  console.log(newDate.toDateString());
```
### Number

```js
  const newNum = 45543;
  
  console.log(newNum.toFixed(2));
  console.log(newNum.toExponential(3));
  console.log(newNum.toLocaleString());
  console.log(newNum.toPrecision(3));
```

### Operator
```js
const myNumOne = 29;
const myNumTwo = 76;

const add = myNumOne + myNumTwo;
const sub = myNumOne - myNumTwo;
const multi = myNumOne * myNumTwo;
const divide = myNumOne / myNumTwo;
const greater = myNumOne > myNumTwo;
const less = myNumOne < myNumTwo;
```

### Math
```js
const randomMath = 123.456;

 console.log(Math.round(randomMath));
 console.log(Math.ceil(randomMath));
 console.log(Math.floor(randomMath));

const ranNum = Math.round(Math.random() *  10);
console.log(ranNum);

```
### Ruduce
```js
   const products = [
       {
           product: 'JS coursr',
           price: 444
       },
       {
           product: 'PY coursr',
           price: 777
       },
       {
           product: 'Web Analytics coursr',
           price: 333
       },
       {
           product: 'Book keeping coursr',
           price: 345
       },
   ];
   
   const myCart = products.reduce((acc, pd) => {
       return acc + pd.price
   }, 0);
    console.log(myCart);
```
### Filter

```js
   const team = [
       {
           name: 'Tamim',
           role: 'Batter'
       },
       {
           name: 'Liton',
           role: 'Batter'
       },
       {
           name: 'Shakib',
           role: 'Allrounder'
       },
       {
           name: 'Imrul',
           role: 'Batter'
       },
       {
           name: 'Mashrafi',
           role: 'Bowler'
       },
       {
           name: 'Mustafiz',
           role: 'Bowlwer'
       },
       {
           name: 'Mushfiq',
           role: 'Batter'
       },
       {
           name: 'Miraz',
           role: 'Allrounder'
       },
       {
           name: 'Mahmudullah',
           role: 'Batter'
       },
       {
           name: 'Shanto',
           role: 'Batter'
       },
   ];
   
   const batter =  team.filter((player) => player.role === 'Batter' );
   console.log(batter);
   const bowler =  team.filter((player) => player.role === 'Bowler' );
   console.log(bowler);
   const allrounder =  team.filter((player) => player.role === 'Allrounder' );
   console.log(allrounder);
```

### Map

```js
    const myNumbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
    
    const newNumbers = myNumbers
                                .map(num => num * 10)
                                .map(num => num + 1)
                                .filter(num => num >= 49)
    console.log(newNumbers);
```


















