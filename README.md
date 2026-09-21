<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Days Since LSU Beat Ole Miss</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #1C0A35; /* LSU Deep Purple */
            color: #FFFFFF;
            text-align: center;
            padding: 40px 20px;
            margin: 0;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background: #2D144B;
            padding: 30px;
            border-radius: 16px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.6);
            border: 4px solid #FDD023; /* LSU Gold */
        }
        h1 {
            font-size: 2rem;
            margin-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #FDD023; /* LSU Gold */
        }
        .meme-img {
            width: 100%;
            max-width: 320px;
            height: auto;
            border-radius: 8px;
            border: 3px solid #FDD023;
            margin: 15px auto;
            display: block;
        }
        .ticker-container {
            display: flex;
            justify-content: space-around;
            margin: 25px 0;
            background: rgba(0, 0, 0, 0.3);
            padding: 15px;
            border-radius: 10px;
        }
        .ticker-box {
            flex: 1;
        }
        .ticker-num {
            font-size: 2.8rem;
            font-weight: bold;
            color: #FDD023;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            line-height: 1;
        }
        .ticker-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            color: #A090B5;
            margin-top: 5px;
            letter-spacing: 0.5px;
        }
        p {
            font-size: 1.1rem;
            color: #E0DBE7;
            margin: 10px 0;
        }
        .footer {
            font-size: 0.85rem;
            margin-top: 25px;
            color: #A090B5;
            border-top: 1px solid rgba(253, 208, 35, 0.2);
            padding-top: 15px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Days Since LSU Last Beat Ole Miss</h1>
        
        <!-- CORNDOG IMAGE PLACEHOLDER -->
        <!-- Save your edited image as "corndog.png" in the same folder as this HTML file -->
        <img src="corndog.jpg" alt="LSU  Fan Eating a Corndog" class="meme-img">

        <p>It has been...</p>
        
        <!-- LIVE TICKER CONTAINER -->
        <div class="ticker-container">
            <div class="ticker-box">
                <div class="ticker-num" id="days">--</div>
                <div class="ticker-label">Days</div>
            </div>
            <div class="ticker-box">
                <div class="ticker-num" id="hours">--</div>
                <div class="ticker-label">Hours</div>
            </div>
            <div class="ticker-box">
                <div class="ticker-num" id="minutes">--</div>
                <div class="ticker-label">Mins</div>
            </div>
            <div class="ticker-box">
                <div class="ticker-num" id="seconds">--</div>
                <div class="ticker-label">Secs</div>
            </div>
        </div>
        
        <p>...since the Tigers took home the Magnolia Bowl trophy.</p>
        
        <div class="footer">
            Last LSU Win: October 12, 2024 (LSU 29, Ole Miss 26)
        </div>
    </div>

    <script>
        function updateCountdown() {
            // Target date: Last time LSU won
            const lastWinDate = new Date("October 12, 2024 22:30:00").getTime(); 
            const now = new Date().getTime();
            
            const timeDifference = now - lastWinDate;
            
            // Time calculations for days, hours, minutes and seconds
            const days = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeDifference % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeDifference % (1000 * 60)) / 1000);
            
            // Output the results into the HTML elements
            document.getElementById("days").innerText = days;
            document.getElementById("hours").innerText = hours;
            document.getElementById("minutes").innerText = minutes;
            document.getElementById("seconds").innerText = seconds;
        }

        // Update the count down every 1 second
        setInterval(updateCountdown, 1000);
        
        // Run immediately on load
        updateCountdown();
    </script>
</body>
</html>
