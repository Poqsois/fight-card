<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>West Coast Double Header Fight Nights - Perth</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #121212;
            color: #f4f4f4;
            text-align: center;
            padding: 20px;
        }
        .fight-card {
            background-color: #282828;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            margin: 20px auto;
            max-width: 600px;
        }
        h1 { color: #f4b400; }
        .fight { border-bottom: 1px solid #444; padding: 15px 0; }
        .fight:last-child { border-bottom: none; }
        .fighter { display: inline-block; width: 45%; }
        .vs { font-weight: bold; font-size: 1.5em; }
        .pending { color: #f4b400; }
        .odds { font-size: 1.1em; margin-top: 20px; }
        .live-stream { margin-top: 30px; font-size: 1.2em; }
        .timer { font-size: 2em; font-weight: bold; margin-top: 30px; }
        .weigh-in { margin-top: 20px; font-size: 1.2em; color: #f4b400; }
    </style>
</head>
<body>
    <h1>West Coast Double Header Fight Nights - Perth</h1>
    <p>December 6th, 2024 | Ray Owen Sports Centre</p>
    <p>Weigh-ins: 8:00 AM | Fights Start: 11:30 AM</p>

    <div class="fight-card">
        <h2>Main Event</h2>
        <div class="fight">
            <div class="fighter">Jared McCallister (5-1-0)</div>
            <div class="vs">vs</div>
            <div class="fighter">Liam Jones (8-2-0)</div>
            <div class="pending">Result: Pending</div>
        </div>

        <h2>Co-Main Event</h2>
        <div class="fight">
            <div class="fighter">Chris Tanaka (3-2-0)</div>
            <div class="vs">vs</div>
            <div class="fighter">Ryan Jenkins (2-1-0)</div>
            <div class="pending">Result: Pending</div>
        </div>

        <h2>Main Card</h2>
        <div class="fight">
            <div class="fighter">Tynan Morris (1-0-0)</div>
            <div class="vs">vs</div>
            <div class="fighter">Mark Farrar (4-0-0)</div>
            <div class="pending">Result: Pending</div>
        </div>
        <div class="fight">
            <div class="fighter">Michael Sweeney (0-1-0)</div>
            <div class="vs">vs</div>
            <div class="fighter">Ethan Ray (Debut)</div>
            <div class="pending">Result: Pending</div>
        </div>
        <div class="fight">
            <div class="fighter">Damian Cross (2-2-0)</div>
            <div class="vs">vs</div>
            <div class="fighter">Lucas Brown (1-0-0)</div>
            <div class="pending">Result: Pending</div>
        </div>
    </div>

    <!-- Odds Section -->
    <div class="odds">
        <h3>Fighter Odds:</h3>
        <p><strong>Tynan Morris</strong> (1-0-0) - Odds: 1.5 (Favorite)</p>
        <p><strong>Jared McCallister</strong> (5-1-0) - Odds: 2.2</p>
        <p><strong>Liam Jones</strong> (8-2-0) - Odds: 2.1</p>
        <p><strong>Mark Farrar</strong> (4-0-0) - Odds: 2.0</p>
        <p><strong>Michael Sweeney</strong> (0-1-0) - Odds: 3.0</p>
        <p><strong>Ethan Ray</strong> (Debut) - Odds: 2.8</p>
        <p><strong>Damian Cross</strong> (2-2-0) - Odds: 2.4</p>
        <p><strong>Lucas Brown</strong> (1-0-0) - Odds: 2.5</p>
    </div>

    <!-- Weigh-in Section -->
    <div class="weigh-in">
        <h3>Weigh-ins:</h3>
        <p>Weigh-ins will take place at 8:00 AM at Ray Owen Sports Centre.</p>
    </div>

    <!-- Timer Section (Countdown to 11:30 AM Perth Time) -->
    <div class="timer" id="countdown"></div>

    <!-- Pending Live Stream Link -->
    <div class="live-stream">
        <h3>Pending Live Stream Link</h3>
        <p><a href="#" style="color: #f4b400;">Click here to watch the fight live</a></p>
    </div>

    <script>
        // Set the date we're counting down to (11:30 AM Perth time, December 6th, 2024)
        var countDownDate = new Date("Dec 6, 2024 11:30:00 GMT+0800").getTime();

        // Update the countdown every 1 second
        var x = setInterval(function() {

            // Get the current date and time
            var now = new Date().getTime();
            
            // Calculate the remaining time
            var distance = countDownDate - now;
            
            // Time calculations for days, hours, minutes, and seconds
            var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            // Display the result in the timer div
            document.getElementById("countdown").innerHTML = hours + "h " + minutes + "m " + seconds + "s ";

            // If the countdown is finished, display a message
            if (distance < 0) {
                clearInterval(x);
                document.getElementById("countdown").innerHTML = "Fights Begin Now!";
            }
        }, 1000);
    </script>

</body>
</html>
