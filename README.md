<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="index.css">
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
