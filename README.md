<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Visitor Counter</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #f4f4f4;
        }

        .container {
            text-align: center;
        }

        h1 {
            color: #333;
        }

        p {
            font-size: 18px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Welcome to the Website!</h1>
        <p>Total Visitors: <span id="counter">0</span></p>
    </div>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // Check if there is a counter value in local storage
            let counter = localStorage.getItem("counter");

            // If counter is not present in local storage, initialize it to 0
            if (!counter) {
                counter = 0;
            }

            // Display the initial counter value
            document.getElementById("counter").textContent = counter;

            // Increment the counter on each visit
            counter++;
            
            // Save the updated counter value to local storage
            localStorage.setItem("counter", counter);
        });
    </script>
</body>
</html>
