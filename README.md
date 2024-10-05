<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        input { width: 50px; }
        button { width: 50px; height: 50px; }
    </style>
</head>
<body>
    <h2>Simple Calculator</h2>
    <input type="text" id="result" disabled><br>
    <button onclick="clearDisplay()">C</button>
    <button onclick="deleteLast()">Del</button>
    <button onclick="appendValue('7')">7</button>
    <button onclick="appendValue('8')">8</button>
    <button onclick="appendValue('9')">9</button>
    <button onclick="appendValue('4')">4</button>
    <button onclick="appendValue('5')">5</button>
    <button onclick="appendValue('6')">6</button>
    <button onclick="appendValue('1')">1</button>
    <button onclick="appendValue('2')">2</button>
    <button onclick="appendValue('3')">3</button>
    <button onclick="appendValue('0')">0</button>
    <button onclick="appendValue('+')">+</button>
    <button onclick="appendValue('-')">-</button>
    <button onclick="appendValue('*')">*</button>
    <button onclick="appendValue('/')">/</button>
    <button onclick="calculate()">=</button>

    <script>
        function appendValue(val) {
            document.getElementById('result').value += val;
        }

        function clearDisplay() {
            document.getElementById('result').value = '';
        }

        function deleteLast() {
            let display = document.getElementById('result').value;
            document.getElementById('result').value = display.slice(0, -1);
        }

        function calculate() {
            let display = document.getElementById('result').value;
            document.getElementById('result').value = eval(display);
        }
    </script>
</body>
</html>
# calculator
