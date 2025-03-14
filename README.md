<!DOCTYPE html>
<html>
<head>
    <title>QR Code Info</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }
        #organizerInfo {
            display: none; /* Masqué par défaut */
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Informations publiques</h1>
    <p>Bienvenue à l'événement ! Voici les informations générales.</p>

    <!-- Formulaire pour les organisateurs -->
    <form onsubmit="checkPassword(event)">
        <label for="password">Mot de passe organisateur :</label>
        <input type="password" id="password" name="password" required>
        <button type="submit">Accéder aux infos organisateur</button>
    </form>

    <!-- Section cachée pour les organisateurs -->
    <div id="organizerInfo">
        <h2>Informations organisateur</h2>
        <p>Liste des participants : ...</p>
        <p>Statistiques : ...</p>
        <p>Autres détails confidentiels : ...</p>
    </div>

    <script>
        function checkPassword(event) {
            event.preventDefault(); // Empêche le rechargement de la page
            const password = document.getElementById('password').value;
            if (password === "Organisateur123") { // Remplacez par votre mot de passe
                document.getElementById('organizerInfo').style.display = 'block'; // Affiche les infos organisateur
            } else {
                alert("Mot de passe incorrect"); // Message d'erreur
            }
        }
    </script>
</body>
</html>
