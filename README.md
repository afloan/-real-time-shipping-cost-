# -real-time-shipping-cost-
Real time shipping cost for freight train and trucks
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shipping Costs</title>
</head>
<body>
    <h1>Check Shipping Costs</h1>
    <button onclick="getShippingCost()">Get Shipping Cost</button>
    <p id="cost">Cost will appear here.</p>

    <script>
        function getShippingCost() {
            // Replace with your actual API endpoint
            fetch('https://api.example.com/shipping-cost')
                .then(response => response.json())
                .then(data => {
                    document.getElementById('cost').textContent = `Shipping Cost: $${data.cost}`;
                })
                .catch(error => {
                    document.getElementById('cost').textContent = 'Error fetching shipping cost';
                });
        }
    </script>
</body>
</html>
