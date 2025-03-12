<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Secret Code Proposal 🔐</title>
    <style>
        body {
            background-color: black;
            color: limegreen;
            font-family: "Courier New", monospace;
            text-align: center;
            padding: 50px;
        }
        #terminal {
            border: 2px solid limegreen;
            padding: 20px;
            width: 80%;
            max-width: 500px;
            margin: auto;
            text-align: left;
            min-height: 200px;
        }
        input {
            background: black;
            color: limegreen;
            border: none;
            font-family: "Courier New", monospace;
            font-size: 16px;
            width: 90%;
            outline: none;
        }
        #proposal {
            display: none;
            margin-top: 20px;
        }
        img {
            width: 50%;
            max-width: 400px;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <h1>🔐 Enter the Secret Code</h1>
    <div id="terminal">
        <p>System Initialized...</p>
        <p>Verifying user identity...</p>
        <p>Access requires correct password.</p>
        <p>Enter code: <input type="text" id="codeInput" onkeydown="checkCode(event)"></p>
        <p id="message"></p>
    </div>

    <div id="proposal">
        <h1>Correct! Will You Marry Me? 💍❤</h1>
        <img src="https://media.giphy.com/media/3oz8xKaR836UJOYeOc/giphy.gif" alt="Happy GIF">
    </div>

    <script>
        function checkCode(event) {
            if (event.key === "Enter") {
                let input = document.getElementById("codeInput").value.toLowerCase();
                let message = document.getElementById("message");

                if (input === "bably") { // Secret code is 'love'
                    document.getElementById("terminal").style.display = "none";
                    document.getElementById("proposal").style.display = "block";
                } else {
                    message.innerText = "Access Denied! Try again.";
                }
            }
        }
    </script>

</body>
</html>
