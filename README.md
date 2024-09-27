# palindrome<!DOCTYPE html>
<html lang = "en">
  <head>
    <meta charset= "UTF-8">
    <meta name = "viewport" content = "width=device-width, initial-scale=1.0">
    <link rel = "stylesheet" href= "./styles.css">
    <title>Is it a Palindrome</title>
    </head>

    <body>
      <div id= "result">
      <img src = "https://www.npmjs.com/npm-avatar/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdmF0YXJVUkwiOiJodHRwczovL3MuZ3JhdmF0YXIuY29tL2F2YXRhci9mY2RhNDM4NTI2MDg2MjZmZTQ2ZDdmZDQzMTQ1NzY2ZT9zaXplPTQ5NiZkZWZhdWx0PXJldHJvIn0.l-5iyLZMhxA8NPM6apqba6oCeJ4p8f63d6aVep6utAI" />
      <input id = "text-input" placeholder= "Enter Text Here"></input>
      <button id ="check-btn">Check</button>
      </div>
      <script src= "script.js">
        
      </script>
      <a href ="https://adampalindrome.com">Adam's Webpage</a>

img  {
  width: 203;
margin: 200 650
}
input {
  width: 203;
  height: 30;
  margin: -199 648 ;
  border-radius:
  20px;
}
button{
  width: 60;
  height: 30;
  border-radius: 20px;
  margin: -199 795;
  font-weight: bold;
  ;
}
const text = document.getElementById('text-input');
 const button = document.getElementById('check-btn');
 const result = document.getElementById('result');


 const PalCheck = () => {
  const Text = text.value.trim();
  

       if (Text === ""){alert("Please input a value");
                                                return;}
      const NText = Text.toLowerCase().match(/[a-z0-9 ]/g);
     
            if (!NText || NText.length === 0){result.innerText = `${Text} is not a palindrome`
    return;
  } const reg = NText.join("")
  const revText = reg.split("").reverse().join("");
  

      if (reg === revText) {
  
    result.innerText = `${Text} is a palindrome`
  }  else {
    result.innerText = `${Text} is not a palindrome`
  }
               }

 button.addEventListener("click", PalCheck);
