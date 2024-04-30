# Calculater
<!DOCTYPE html>
<html>
<head>
  <title>Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .calculator {
      max-width: 600px;
      margin: 0 auto;
      background-color: #f0f0f0;
      border: 3px solid #ccc;
      padding: 20px;
    }
    .calculator input {
      width: 84%;
      margin-bottom: 10px;
      padding: 10px;
      font-size: 18px;
    }
    .calculator button {
      width: 29%;
      padding: 10px;
      font-size: 18px;
    }
    .calculator button:nth-child(),
    .calculator button:last-child {
      width: 100%;
    }
  </style>
</head>
<body>
  <br>
    <div>
    <h1 align="center" style="color: rebeccapurple;">THIS IS THE CALCULATOR</h1>
</div>
<br>
<br>
<br>
  <div class="calculator">
    <input type="text" id="result" readonly>
    <br>
    <button onclick="appendValue(9)">9</button>
    <button onclick="appendValue(8)">8</button>
    <button onclick="appendValue(7)">7</button>
    <button onclick="appendValue(6)">6</button>
    <button onclick="appendValue(5)">5</button>
    <button onclick="appendValue(4)">4</button>
    <button onclick="appendValue(3)">3</button>
    <button onclick="appendValue(2)">2</button>
    <button onclick="appendValue(1)">1</button>
    <button onclick="appendValue(0)">0</button>
    <button onclick="appendValue('.')">.</button>
    <button onclick="calculate()">=</button>
    <button onclick="appendValue('+')">+</button>
    <button onclick="appendValue('-')">-</button>
    <button onclick="appendValue('*')">*</button>
    <button onclick="appendValue('/')">/</button>
    <button onclick="percentage('%')">%</button>
    <button onclick="clearResult( )"> C </button>
   
  </div>

  <script>
    function appendValue(value) {
      document.getElementById('result').value += value;
    }

    function calculate() {
      try {
        const result = eval(document.getElementById('result').value);
        document.getElementById('result').value = result;
      } catch (error) {
        document.getElementById('result').value = 'Error';
      }
    }

    function clearResult() {
      document.getElementById('result').value = '';
    }
  </script>
  
</body>
</html>
