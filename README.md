# Counter
The BabbleKingdom grows
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>BabbleCoin Counter</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #fdf6f0;
            color: #333;
            margin: 0;
            padding: 50px;
        }
        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
        }
        #counter {
            font-size: 3em;
            font-weight: bold;
            color: #ff6f61;
        }
        p {
            font-size: 1.2em;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>BabbleCoin is growing… 🍼</h1>
    <div id="counter">0</div>
    <p>Tracking estimated global births in real-time to power the BabbleKingdom!</p>

    <script>
        // ----- CONFIGURATION -----
        let totalBabies = 370000; // valeur initiale estimée aujourd'hui
        const birthsPerSecond = 4.2; // naissances par seconde approximatives
        const counterElement = document.getElementById('counter');

        // Fonction pour mettre à jour le compteur chaque seconde
        function updateCounter() {
            totalBabies += birthsPerSecond;
            counterElement.innerText = Math.floor(totalBabies).toLocaleString();
        }

        // Mise à jour toutes les secondes
        setInterval(updateCounter, 1000);

        // Initial display
        counterElement.innerText = Math.floor(totalBabies).toLocaleString();
    </script>
</body>
</html>
