<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loading Animation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Audio -->
    <audio id="bg-music" autoplay loop>
        <source src="1636266670_pink-soldiers.mp3" type="audio/mp3">
    </audio>

    <!-- Animasi Loading -->
    <div class="loader-container">
        <div class="loader">
            <svg viewBox="0 0 80 80">
                <circle cx="40" cy="40" r="32"></circle>
                <circle class="moving-dot" cx="40" cy="8" r="5"></circle>
            </svg>
        </div>
        <div class="loader">
            <svg viewBox="0 0 80 80">
                <polygon points="40,8 72,72 8,72"></polygon>
                <circle class="moving-dot" cx="40" cy="8" r="5"></circle>
            </svg>
        </div>
        <div class="loader">
            <svg viewBox="0 0 80 80">
                <rect x="8" y="8" width="64" height="64"></rect>
                <circle class="moving-dot" cx="8" cy="8" r="5"></circle>
            </svg>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
