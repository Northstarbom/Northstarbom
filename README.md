<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crypto Exchange</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            background-color: #121212;
            color: #fff;
            line-height: 1.5;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        header {
            background-color: #1e1e1e;
            padding: 20px;
            text-align: center;
        }
        header h1 {
            font-size: 2em;
            color: #f0b90b;
        }
        .market-summary, .trading-section, .order-book, .trade-history, .wallet-summary {
            background-color: #1e1e1e;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
        }
        .section-title {
            font-size: 1.5em;
            margin-bottom: 10px;
            color: #f0b90b;
        }
        .market-summary table, .order-book table, .trade-history table {
            width: 100%;
            margin-top: 10px;
            color: #ddd;
            border-spacing: 0;
        }
        table th, table td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #333;
        }
        .trading-section form, .wallet-summary {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        .trading-section form input, .trading-section form button {
            padding: 10px;
            font-size: 1em;
            border-radius: 5px;
            border: none;
            color: #000;
        }
        .trading-section form input {
            background-color: #fff;
        }
        .trading-section form button {
            background-color: #f0b90b;
            color: #000;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>Crypto Exchange</h1>
        <p>Your platform to trade cryptocurrency securely and instantly.</p>
    </header>

    <div class="container">

        <!-- Market Summary Section -->
        <section class="market-summary">
            <h2 class="section-title">Market Summary</h2>
            <table>
                <thead>
                    <tr>
                        <th>Asset</th>
                        <th>Price</th>
                        <th>24h Change</th>
                        <th>Volume</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Bitcoin (BTC)</td>
                        <td>$60,000</td>
                        <td>+2.5%</td>
                        <td>$1B</td>
                    </tr>
                    <tr>
                        <td>Ethereum (ETH)</td>
                        <td>$4,000</td>
                        <td>-1.2%</td>
                        <td>$800M</td>
                    </tr>
                    <tr>
                        <td>Ripple (XRP)</td>
                        <td>$1.10</td>
                        <td>+3.8%</td>
                        <td>$300M</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- Trading Section -->
        <section class="trading-section">
            <h2 class="section-title">Trade Cryptocurrency</h2>
            <form>
                <input type="text" placeholder="Enter Amount in USD" required>
                <input type="text" placeholder="Enter Cryptocurrency (e.g., BTC)" required>
                <button type="submit">Buy Crypto</button>
                <button type="submit">Sell Crypto</button>
            </form>
        </section>

        <!-- Order Book Section -->
        <section class="order-book">
            <h2 class="section-title">Order Book</h2>
            <table>
                <thead>
                    <tr>
                        <th>Price</th>
                        <th>Amount (BTC)</th>
                        <th>Total (USD)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>$59,900</td>
                        <td>0.5</td>
                        <td>$29,950</td>
                    </tr>
                    <tr>
                        <td>$60,100</td>
                        <td>0.3</td>
                        <td>$18,030</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- Trade History Section -->
        <section class="trade-history">
            <h2 class="section-title">Trade History</h2>
            <table>
                <thead>
                    <tr>
                        <th>Time</th>
                        <th>Type</th>
                        <th>Price</th>
                        <th>Amount (BTC)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>12:45 PM</td>
                        <td>Buy</td>
                        <td>$60,000</td>
                        <td>0.1</td>
                    </tr>
                    <tr>
                        <td>12:43 PM</td>
                        <td>Sell</td>
                        <td>$60,200</td>
                        <td>0.2</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- Wallet Summary Section -->
        <section class="wallet-summary">
            <h2 class="section-title">Your Wallet</h2>
            <p>BTC Balance: 0.5</p>
            <p>USD Balance: $30,000</p>
        </section>

    </div>

</body>
</html>