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
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #000;
}

.loader-container {
    display: flex;
    gap: 20px;
}

.loader svg {
    width: 80px;
    height: 80px;
    fill: none;
    stroke: #fff;
    stroke-width: 10px;
    stroke-linejoin: round;
    stroke-linecap: round;
    animation: animate 2s linear infinite;
}

/* Animasi untuk lingkaran bergerak */
.moving-dot {
    fill: #800080;
    animation: move-dot 2s linear infinite;
}

@keyframes animate {
    0% {
        stroke-dasharray: 0, 150;
        stroke-dashoffset: 0;
    }
    50% {
        stroke-dasharray: 100, 150;
        stroke-dashoffset: -40;
    }
    100% {
        stroke-dasharray: 100, 150;
        stroke-dashoffset: -100;
    }
}

/* Animasi bulatan ungu */
@keyframes move-dot {
    0% {
        transform: translate(0, 0);
    }
    25% {
        transform: translate(32px, 32px
