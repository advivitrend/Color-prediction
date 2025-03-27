<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color Prediction Game</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; }
        .button { padding: 15px; margin: 10px; font-size: 18px; cursor: pointer; }
        .red { background-color: red; color: white; }
        .green { background-color: green; color: white; }
    </style>
</head>
<body>
    <h1>Color Prediction Game</h1>
    <button class="button red" onclick="placeBet('Red')">Bet on Red</button>
    <button class="button green" onclick="placeBet('Green')">Bet on Green</button>
    <h2 id="result"></h2>
    
    <script>
        function placeBet(choice) {
            let colors = ["Red", "Green"];
            let randomColor = colors[Math.floor(Math.random() * colors.length)];
            let resultText = choice === randomColor ? "🎉 You Won!" : "❌ You Lost!";
            document.getElementById("result").innerText = "Result: " + randomColor + " | " + resultText;
        }
    </script>
</body>
</html>
