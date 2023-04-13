<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
    margin: 0;
    padding: 0;
    font-family: 'Poppins',sans-serif;
}
body{
    display: flex;
    justify-content:center ;
    align-items: center;
    min-height: 100vh;
    background: #373737;
}
h3{
    position: relative;
    font-size: 20px;
    color: #f9f9f9;
    letter-spacing: 1px;
    font-weight: 500;
    margin-bottom: 5px;
}
#form{
    position: relative;
}
#form #email{
    width: 300px;
    background: #292929;
    outline: none;
    border: none;
    padding: 10px;
    border-radius: #fff;
    font-style: 18px;
}
#form #inputbox{
    position: relative;
}
#text{
    display: block;
    color: #000;
    font-weight: 500i;
    font-style: italic;
    padding: 5px;

}


    </style>
</head>
<body>
   <div>
    <h3>Email validation check</h3>
    <form id="form" action="#">
        <div class="inputbox">
            <input type="text" name="" id="email" placeholder="Enter your email address" onkeydown="validation()">
            <span  id="text"></span>
        </div>

    </form>

   </div> 
   <script type="text/javascript">
    function validation(){
        var form=document.getElementById("form");
        var email=document.getElementById("email").value;
        var text=document.getElementById("text");
        var form=document.getElementById("form");
        var pattern= /^[^]+@[^]+\.[a-z]{2,3}$/;
        if(email.match(pattern)){
            form.classList.add("valid");
            form.classList.remove("invalid");
            text.innerHTML="Your email address is valid.";
            text.style.color="#00ff00";
        }
        else{
            form.classList.remove("valid");
            form.classList.add("invalid");
            text.innerHTML="Please Enter your valid email address";
            text.style.color="#ff0000";
        }
        
    }
   </script>
</body>
</html>
