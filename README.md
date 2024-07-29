<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meine GitHub Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 1em;
            text-align: center;
        }
        nav {
            margin: 0;
            padding: 0;
            background-color: #444;
            overflow: hidden;
        }
        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        nav ul li {
            float: left;
        }
        nav ul li a {
            display: block;
            padding: 1em;
            color: white;
            text-decoration: none;
        }
        nav ul li a:hover {
            background-color: #555;
        }
        .content {
            padding: 2em;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        .generator {
            margin-top: 2em;
            padding: 1em;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .generator label {
            margin-right: 1em;
        }
        .generator input {
            margin-right: 1em;
            padding: 0.5em;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        .generator button {
            padding: 0.5em 1em;
            border: none;
            background-color: #333;
            color: white;
            border-radius: 3px;
            cursor: pointer;
        }
        .generator button:hover {
            background-color: #555;
        }
        .generator .result {
            margin-top: 1em;
            font-size: 1.5em;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <header>
        <h1>Willkommen auf meiner GitHub Page</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#">Startseite</a></li>
            <li><a href="#">Über mich</a></li>
            <li><a href="#">Projekte</a></li>
            <li><a href="#">Kontakt</a></li>
        </ul>
    </nav>
    <div class="content">
        <h2>Hallo Welt!</h2>
        <p>Dies ist eine Beispielseite, die über GitHub Pages gehostet wird.</p>

        <div class="generator">
            <h3>Zufallszahlengenerator</h3>
            <label for="min">Min:</label>
            <input type="number" id="min" name="min" value="1">
            <label for="max">Max:</label>
            <input type="number" id="max" name="max" value="100">
            <button onclick="generateRandomNumber()">Generate</button>
            <button onclick="generateRandomNumber()">ReRoll</button>
            <div class="result" id="result">-</div>
        </div>
    </div>
    <footer>
        <p>&copy; 2024 Mein Name</p>
    </footer>

    <script>
        function generateRandomNumber() {
            const min = parseInt(document.getElementById('min').value);
            const max = parseInt(document.getElementById('max').value);
            const result = Math.floor(Math.random() * (max - min + 1)) + min;
            document.getElementById('result').textContent = result;
        }
    </script>
</body>
</html>
