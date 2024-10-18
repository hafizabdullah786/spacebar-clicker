<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spacebar Clicker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }
        h1 {
            color: #333;
        }
        .counter {
            font-size: 48px;
            margin-top: 20px;
        }
        .instructions {
            margin: 20px 0;
        }
        .reset-btn {
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1>Spacebar Clicker</h1>
    <p class="instructions">Press the spacebar as many times as you can!</p>
    <div class="counter" id="counter">0</div>
    <button class="reset-btn" onclick="resetCounter()">Reset</button>

    <script>
        let count = 0;

        // Increase the counter when the spacebar is pressed
        document.addEventListener('keydown', function(event) {
            if (event.code === 'Space') {
                count++;
                document.getElementById('counter').innerText = count;
            }
        });

        // Function to reset the counter
        function resetCounter() {
            count = 0;
            document.getElementById('counter').innerText = count;
        }
    </script>
</body>
</html>
