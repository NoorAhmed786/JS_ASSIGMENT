# JS_ASSIGMENT

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="Apps.js" defer></script>
</head>
 <body onload="newContent();">
      <p>HElloW I m NOor</p>
    
      <!-- <select id="bgchoice" onchange="changeBG()">
        <option></option>
        <option value="red">Red</option>
        <option value="ivory">Ivory</option>
        <option value="pink">Pink</option>
    </select> -->
    <div id="bg-color">
         <b>hello!</b>
    </div>
    <ul id="paraList">
        <li>glass</li>
        <li>soap</li>
        <li>table</li>
        <li>chair</li>
        <li>cutlery</li>

    </ul>
   
</body>
</html>


// //// question no 2 ////////

function nurSearch(arr, l, r, x) 
{ 
    if (r < l) 
        return -1; 
    if (arr[l] == x) 
        return l; 
    if (arr[r] == x) 
        return r; 
     return nurSearch(arr, l+1, r-1, x); 
} 
    
    // Driver Code 
    let arr = [12, 34, 54, 2, 3,23]; 
    let i; 
    let n = arr.length; 
    let x = 23; 
    let index = nurSearch(arr, 0, n - 1, x); 
  
    if (index != -1){
      console.log(`Element ${x} is true at index ${index}`); 
    }
    else{
        console.log("false" + x); 
    }

/////// question no 3 //////

function newContent() {
  
    const para = document.createElement("p");
    para.innerText = " I M A WEB DEVELOPER";
    document.body.appendChild(para);
  }






//////=======question no 1 ======/////////

  function outer() {
    let counter = 5;
    // this variable is outside incrementCounter's scope
    function incrementCounter() {
      counter++;
      console.log("counter", counter);
    }
    return incrementCounter;
  }
  
  const willCounter = outer();
  const jasCounter = outer();
  willCounter();
  willCounter();
  willCounter();
  
  jasCounter();
  willCounter();

 
// /==========question no 8=======///////
//   let prevStudent= localStorage.getItem("students");
//   let students= prevStudent ? JSON.parse(prevStudent) : [];

//   function provideStudent(){
//     let std ={
//         name:prompt("Enter Your Name"),
//         rollno:+prompt("Enter Your roll no"),
//         teacher:prompt("Enter Teacher name"),
//         className:prompt("Enter Your Class")

//     };
//     students.push(std);
//     console.log(students);
//     let stringify= JSON.stringify(students);
//     localStorage.setItem("students",stringify);
//   }


  const myObject = {
    name : "john doe",
    age : 32,
    gender : "male",
    profession : "optician" 
  }
  
  window.localStorage.setItem("myObject", JSON.stringify(myObject));

  let newObject = window.localStorage.getItem("myObject");
  console.log(JSON.parse(newObject));


   
 //////====question no 5 =====////////
   
        let myPara= document.getElementById("bg-color");
        myPara.style.backgroundColor="pink";
       
////======question no 4 ====/////
  

        let myList=document.getElementById("paraList");
        myList.append("<ol><li>cake</li><li>ice-cream</li><li>colddrinks</li></ol>");
        // $("#paraList").append("<li><a href="/user/messages"><span class="tab">Message Center</span></a></li>");
