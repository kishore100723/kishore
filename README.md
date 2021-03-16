<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .container {
            display: flex;
            justify-content: space-between;
            background-color: rgb(0, 0, 0);
            margin: 10px;
            padding: 12px;
        }
        
        .header {
            padding: 15px;
            background-color: rgb(175, 175, 175);
            color: rgb(80, 80, 80);
            font-size: 22px;
            font-weight: 800;
            cursor: pointer;
        }
        
        .header:hover {
            color: rgb(255, 255, 255);
            background-color: rgb(78, 78, 78);
        }
        
        .header:active {
            color: whitesmoke;
            background-color: black;
        }
    </style>
</head>

<body>
    <div class="container">
        <span class="header" onclick="myFunction()">Home</span>
        <span class="header" onclick="myFunction2()">About Us</span>
        <span class="header" onclick="myFunction3()">Contact Us</span>
    </div>
    <div id="home" style="display: none; background-color: cornflowerblue; font-size: 25px; border: 7px solid rgb(0, 0, 146); text-align: center; color: white; font-size: 46px;">Welcome to Allu Group</div>
    <div id="about" style="display: none; background-color: rgb(255, 59, 59); border: 7px solid brown; font-size: 25px; margin: 16px 0px; text-align: center; color: white; font-size: 33px;">Software Craftsmen</div>
    <form action="" id="contact" style="display: none; margin: 12px;" method="post" onsubmit="alert('Allu group will contact you soon')">
        <label for="name">Name</label>
        <br>
        <input type="text" name="name" id="name" class="sess" required>
        <br>
        <label for="mail">E-mail</label>
        <br>
        <input type="text" name="" id="mail" class="sess" required>
        <br>
        <label for="numb">Phone Number</label>
        <br>
        <input type="text" name="" id="numb" class="sess" required>
        <br>
        <label for="message">Leave your message</label>
        <br>
        <textarea name="message" id="message" cols="30" rows="10" class="sess"></textarea>
        <br>
        <input type="submit" value="submit">
    </form>

    <script>
        function myFunction() {
            var x = document.getElementById("home");
            var y = document.getElementById("about");
            var z = document.getElementById("contact");
            if (x.style.display === "block") {
                x.style.display = "none";
            } else {
                x.style.display = "block";
                y.style.display = "none";
                z.style.display = "none";
            }
        }

        function myFunction2() {
            var y = document.getElementById("about");
            var x = document.getElementById("home");
            var z = document.getElementById("contact");
            if (y.style.display === "block") {
                y.style.display = "none";
            } else {
                y.style.display = "block";
                z.style.display = "none";
                x.style.display = "none";
            }
        }

        function myFunction3() {
            var z = document.getElementById("contact");
            var y = document.getElementById("about");
            var x = document.getElementById("home");
            if (z.style.display === "none") {
                z.style.display = "block";
                x.style.display = "none";
                y.style.display = "none";
            } else {
                z.style.display = "none";
            }
        }
    </script>
</body>

</html>
