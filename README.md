<!DOCTYPE html>
<html lang="en">
<head>
    <!-- SEO Tags -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EMI Wizard - Free Loan Calculator</title>
    <meta name="description" content="Calculate your loan EMIs instantly. Free, easy-to-use EMI calculator with ad-supported service.">
    <meta name="keywords" content="EMI calculator, loan calculator, finance tool, monthly installments, free EMI tool">

    <!-- Simple CSS -->
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
        }
        .calculator-box {
            background: #f0f4f8;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }
        input, button {
            padding: 10px;
            margin: 5px;
            width: 95%;
            max-width: 300px;
        }
        .ad-banner {
            text-align: center;
            margin: 20px 0;
        }
    </style>
</head>

<body>
    <!-- Header -->
    <h1>📱 EMI Wizard</h1>
    <p>Free Instant Loan Calculator</p>

    <!-- Calculator -->
    <div class="calculator-box">
        <h2>Calculate Your EMI</h2>
        <input type="number" placeholder="Loan Amount (₹)" id="amount">
        <input type="number" placeholder="Interest Rate (%)" id="rate">
        <input type="number" placeholder="Loan Tenure (months)" id="tenure">
        <button onclick="calculateEMI()">Calculate Now</button>
        <div id="result" style="margin-top:15px; font-weight:bold;"></div>
    </div>

    <!-- Features Section -->
    <div>
        <h2>Why Choose EMI Wizard?</h2>
        <ul>
            <li>✅ 100% Free to Use</li>
            <li>✅ Mobile-Friendly Design</li>
            <li>✅ Instant Results</li>
        </ul>
    </div>

    <!-- Adsterra Ad Code (Replace with your ad script) -->
    <div class="ad-banner">
        <!-- Your Adsterra Ad Code Here -->
    </div>

    <!-- Footer -->
    <footer style="margin-top:30px; text-align:center;">
        <p>© 2023 EMI Wizard | <a href="/privacy">Privacy Policy</a></p>
    </footer>

    <script>
        function calculateEMI() {
            // Get values
            const amount = document.getElementById('amount').value;
            const rate = document.getElementById('rate').value;
            const tenure = document.getElementById('tenure').value;

            // Calculation
            const monthlyRate = rate / 1200;
            const emi = (amount * monthlyRate * Math.pow(1 + monthlyRate, tenure)) / 
                       (Math.pow(1 + monthlyRate, tenure) - 1);

            // Show result
            document.getElementById('result').innerHTML = 
                Monthly EMI: ₹${emi.toFixed(2)};
        }
    </script>
</body>
</html>



