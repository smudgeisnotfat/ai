<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecting...</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #0f172a, #1e293b);
            color: #e2e8f0;
        }
        
        .container {
            text-align: center;
            background: rgba(15, 23, 42, 0.7);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 8px 32px rgba(2, 8, 20, 0.4);
            border: 1px solid rgba(94, 234, 212, 0.2);
            max-width: 500px;
            width: 90%;
        }
        
        .spinner {
            border: 4px solid rgba(94, 234, 212, 0.2);
            border-top: 4px solid #5eead4;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            animation: spin 1s linear infinite;
            margin: 0 auto 20px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .redirect-text {
            color: #cbd5e1;
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .countdown {
            color: #5eead4;
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        
        .link {
            color: #38bdf8;
            text-decoration: none;
            font-size: 16px;
        }
        
        .link:hover {
            text-decoration: underline;
            color: #0ea5e9;
        }
    </style>
    
    <!-- Meta refresh redirect (fallback) -->
    <meta http-equiv="refresh" content="5; url=https://www.example.com">
</head>
<body>
  <h1>REDIRECTING TO LOGIN</h1>
    <div class="container">
        <div class="spinner"></div>
        <p class="redirect-text">You will be redirected in</p>
        <p class="countdown" id="countdown">5</p>
        <p>If you are not redirected automatically, <a href="https://renewing-wondrous-reptile.ngrok-free.app/" class="link">click here</a></p>
    </div>

    <script>
        // JavaScript redirect with countdown
        let seconds = 5;
        const countdownElement = document.getElementById('countdown');
        const redirectUrl = 'https://renewing-wondrous-reptile.ngrok-free.app/'; // Change this to your desired URL
        
        // Update countdown every second
        const countdownInterval = setInterval(() => {
            seconds--;
            countdownElement.textContent = seconds;
            
            if (seconds <= 0) {
                clearInterval(countdownInterval);
                window.location.href = redirectUrl;
            }
        }, 1000);
    </script>
</body>
</html>
