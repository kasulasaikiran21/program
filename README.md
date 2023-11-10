<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            margin: 50px;
        }

        #converter {
            max-width: 400px;
            margin: auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 8px;
        }

        input {
            width: 100%;
            padding: 8px;
            margin-bottom: 16px;
            box-sizing: border-box;
        }

        button {
            background-color: #4caf50;
            color: #fff;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #result {
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <div id="converter">
        <h2>Temperature Converter</h2>
        <label for="celsius">Enter Celsius temperature:</label>
        <input type="number" id="celsius" placeholder="Enter temperature in Celsius">

        <button onclick="convertTemperature()">Convert</button>

        <div id="result"></div>
    </div>

    <script>
        function convertTemperature() {
            var celsius = document.getElementById("celsius").value;
            var fahrenheit = (celsius * 9/5) + 32;
            var result = celsius + " Celsius is equal to " + fahrenheit.toFixed(2) + " Fahrenheit.";
            document.getElementById("result").innerHTML = result;
        }
    </script>

</body>
</html>
