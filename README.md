# oibsip_taskno.3
Temperature converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Temperature Converter</title>
</head>
<body>
    <header>
        <h1>Temperature Converter</h1>
    </header>

    <main>
        <section class="converter">
            <h2>Convert Fahrenheit to Celsius and Kelvin</h2>
            <label for="fahrenheit">Enter Temperature in Fahrenheit:</label>
            <input type="number" id="fahrenheit" placeholder="Enter temperature">
            <button id="convert">Convert</button>
        </section>

        <section class="result">
            <h3>Results:</h3>
            <p><span id="celsiusResult">Celsius: </span></p>
            <p><span id="kelvinResult">Kelvin: </span></p>
        </section>
    </main>
</body>
</html>



/* Reset some default styles */
body, h1, h2, h3, p, label, input, button {
    margin: 0;
    padding: 0;
}

/* Apply basic styles to the header */
header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 20px;
}

/* Style the main content */
main {
    text-align: center;
    padding: 20px;
}

/* Style the temperature converter section */
.converter {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 10px;
}

input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
    margin-bottom: 10px;
}

button {
    background-color: #333;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}

/* Style the result section */
.result {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
}

/* Style the result spans */
#celsiusResult, #kelvinResult {
    font-weight: bold;
}






document.addEventListener('DOMContentLoaded', function () {
    const convertButton = document.getElementById('convert');
    const fahrenheitInput = document.getElementById('fahrenheit');
    const celsiusResult = document.getElementById('celsiusResult');
    const kelvinResult = document.getElementById('kelvinResult');

    convertButton.addEventListener('click', function () {
        const fahrenheit = parseFloat(fahrenheitInput.value);
        if (!isNaN(fahrenheit)) {
            const celsius = (fahrenheit - 32) * 5/9;
            const kelvin = celsius + 273.15;

            celsiusResult.textContent = `Celsius: ${celsius.toFixed(2)}°C`;
            kelvinResult.textContent = `Kelvin: ${kelvin.toFixed(2)}K`;
        } else {
            celsiusResult.textContent = 'Invalid input';
            kelvinResult.textContent = 'Invalid input';
        }
    });
});






<script src="script.js"></script>
