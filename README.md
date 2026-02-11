# MK
<!DOCTYPE html>
<html>
<head>
    <title>Welcome Minnu</title>
    <style>
        body {
            text-align: center;
            font-family: Arial;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            padding-top: 100px;
        }

        h1 { font-size: 40px; }
        h3 { font-weight: normal; }

        button {
            padding: 10px 20px;
            font-size: 18px;
            margin: 10px;
            cursor: pointer;
        }

        #noBtn {
            position: relative;
        }

        #quiz, #level2, #level3, #finalPage {
            display: none;
        }

        img {
            width: 250px;
            margin-top: 20px;
        }
    </style>
</head>

<body>

    <!-- Welcome Page -->
    <div id="welcome">
        <h1>Welcome Minnu</h1>
        <h3>The person who has the most awesome boyfriend</h3>
        <button onclick="startQuiz()">Start</button>
    </div>

    <!-- Level 1 -->
    <div id="quiz">
        <h2>After marriage will you give me peace?</h2>
        <button onclick="nextLevel(2)">Yes</button>
        <button id="noBtn" onmouseover="errorMessage()">No</button>
    </div>

    <!-- Level 2 -->
    <div id="level2">
        <h2>After marriage will you let me go out with my friends?</h2>
        <button onclick="nextLevel(3)">Yes</button>
        <button onmouseover="errorMessage()">No</button>
    </div>

    <!-- Level 3 -->
    <div id="level3">
        <h2>After marriage will you buy me Classic 650?</h2>
        <button onclick="showFinal()">Yes</button>
        <button onmouseover="errorMessage()">No</button>
    </div>

    <!-- Final Page -->
    <div id="finalPage">
        <h1>Yes I'll be your valentine ❤️</h1>
        <img src="https://i.imgur.com/4M34hi2.png" alt="Love Image">
    </div>

<script>
    function startQuiz() {
        document.getElementById("welcome").style.display = "none";
        document.getElementById("quiz").style.display = "block";
    }

    function nextLevel(level) {
        document.getElementById("quiz").style.display = "none";
        document.getElementById("level2").style.display = "none";
        document.getElementById("level3").style.display = "none";

        if(level == 2) {
            document.getElementById("level2").style.display = "block";
        } else if(level == 3) {
            document.getElementById("level3").style.display = "block";
        }
    }

    function showFinal() {
        document.getElementById("level3").style.display = "none";
        document.getElementById("finalPage").style.display = "block";
    }

    function errorMessage() {
        alert("Error! This option is not allowed 😜");
    }
</script>

</body>
</html>
