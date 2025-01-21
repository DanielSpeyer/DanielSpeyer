/mon-site
  ├── <!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Joyeux Anniversaire Daniel !</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Joyeux Anniversaire, Speyer Nomenjanahary Daniel ! 🎉</h1>
        <p>Tu es né le <strong>14 février 2005</strong>.</p>
        <p>Aujourd'hui, tu as <span id="age"></span> ans !</p>
        <div class="balloons">
            <div class="balloon red"></div>
            <div class="balloon blue"></div>
            <div class="balloon yellow"></div>
        </div>
        <p>Profite bien de ta journée spéciale !</p>
    </div>
    <script src="script.js"></script>
</body>
</html>
  ├── body {
    font-family: Arial, sans-serif;
    background: linear-gradient(to bottom, #ffcccc, #ffe6e6);
    text-align: center;
    padding: 20px;
    margin: 0;
}

.container {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    padding: 20px;
    max-width: 500px;
    margin: 20px auto;
}

h1 {
    color: #ff6666;
    font-size: 2.5em;
}

p {
    font-size: 1.2em;
    color: #555;
}

.balloons {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin: 20px 0;
}

.balloon {
    width: 50px;
    height: 70px;
    border-radius: 50%;
    position: relative;
}

.balloon::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 2px;
    height: 20px;
    background-color: #333;
}

.red {
    background-color: #ff6666;
}

.blue {
    background-color: #66b3ff;
}

.yellow {
    background-color: #ffd966;
}
  ├── // Calcul de l'âge
const dateNaissance = new Date(2005, 1, 14); // Les mois commencent à 0 (janvier = 0)
const dateActuelle = new Date();
const age = dateActuelle.getFullYear() - dateNaissance.getFullYear();
const estAnniversaire = 
    dateActuelle.getMonth() === dateNaissance.getMonth() &&
    dateActuelle.getDate() === dateNaissance.getDate();

// Mise à jour de l'âge dans la page
document.getElementById("age").textContent = age;

// Message spécial si c'est aujourd'hui l'anniversaire
if (estAnniversaire) {
    alert("Joyeux Anniversaire, Speyer Nomenjanahary Daniel !");
}
  