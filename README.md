<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Payment Page</title>
    <style>
        body {
            font-family:MAIANdra GD Regular, sans-serif;
            background-color: #61a4ad;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 400px;
        }
        h1 {
            font-size: 1.5em;
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 8px;
        }
        input[type="text"], input[type="number"], input[type="submit"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="C:\Users\HP\Desktop\logo ai thon.jpg" alt="My Image"
        width="100" height="60">
        <h1 style="color: #7b0d0c;"><center>Payblaze</center></h1>
        <h3>Payment Form</h3>
        <form action="/process-payment" method="POST">
            <label for="name">Name on Card:</label>
            <input type="text" id="name" name="name" required>

            <label for="card-number">Card Number:</label>
            <input type="text" id="card-number" name="card-number" pattern="\d{16}" required>

            <label for="expiry-date">Expiry Date (MM/YY):</label>
            <input type="text" id="expiry-date" name="expiry-date" pattern="\d{2}/\d{2}" required>

            <label for="cvv">CVV:</label>
            <input type="number" id="cvv" name="cvv" pattern="\d{3}" required>

            <label for="amount">Amount ($):</label>
            <input type="number" id="amount" name="amount" step="0.01" min="0" required>

            <input type="submit" value="Pay Now">
        </form>
    </div>
</body>
</html>
