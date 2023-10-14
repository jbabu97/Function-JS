# Function-JS
- [Function](#Function)
- [ThisKeyWordAndArrowFunction](#ThisKeyWordAndArrowFunction)

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
