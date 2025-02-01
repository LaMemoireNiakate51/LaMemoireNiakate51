<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>La Mémoire Niakate</title>
    <style>
        /* Style général */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px 0;
            text-align: center;
        }

        header h1 {
            margin: 0;
        }

        nav {
            background-color: #444;
            overflow: hidden;
        }

        nav a {
            color: white;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
            display: inline-block;
        }

        nav a:hover {
            background-color: #ddd;
            color: black;
        }

        .container {
            width: 80%;
            margin: 20px auto;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }

        .section-title {
            text-align: center;
            margin: 20px 0;
            color: #333;
        }

        /* Formulaire de contact */
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .contact-form button {
            background-color: #333;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .contact-form button:hover {
            background-color: #555;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>La Mémoire Niakate</h1>
        <p>Préserver et partager les histoires du XXIe siècle</p>
    </header>

    <!-- Navigation -->
    <nav>
        <a href="#accueil">Accueil</a>
        <a href="#histoire">Notre Histoire</a>
        <a href="#services">Nos Services</a>
        <a href="#contact">Contact</a>
    </nav>

    <!-- Section Accueil -->
    <div id="accueil" class="container">
        <h2 class="section-title">Bienvenue sur La Mémoire Niakate</h2>
        <p>Notre objectif est de conserver et transmettre les mémoires et les histoires du XXIe siècle, avec une plateforme interactive et sécurisée.</p>
    </div>

    <!-- Section Histoire -->
    <div id="histoire" class="container">
        <h2 class="section-title">Notre Histoire</h2>
        <p>La Mémoire Niakate a été fondée avec la vision de préserver la mémoire collective à travers les générations. Grâce à des outils numériques avancés, nous pouvons collecter, organiser et partager des récits uniques.</p>
    </div>

    <!-- Section Services -->
    <div id="services" class="container">
        <h2 class="section-title">Nos Services</h2>
        <ul>
            <li>Collecte et numérisation de mémoires</li>
            <li>Plateforme de partage sécurisée</li>
            <li>Préservation des archives et des documents historiques</li>
            <li>Consultation et recherche personnalisée</li>
        </ul>
    </div>

    <!-- Section Contact -->
    <div id="contact" class="container">
        <h2 class="section-title">Contactez-Nous</h2>
        <div class="contact-form">
            <form onsubmit="return validateForm()">
                <input type="text" id="name" placeholder="Votre Nom" required>
                <input type="email" id="email" placeholder="Votre Email" required>
                <textarea id="message" rows="4" placeholder="Votre Message" required></textarea>
                <button type="submit">Envoyer</button>
            </form>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 La Mémoire Niakate - Tous droits réservés</p>
    </footer>

    <script>
        function validateForm() {
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;

            if (name === "" || email === "" || message === "") {
                alert("Veuillez remplir tous les champs !");
                return false;
            }

            if (!validateEmail(email)) {
                alert("Veuillez entrer un email valide !");
                return false;
            }

            alert("Message envoyé avec succès !");
            return true;
        }

        function validateEmail(email) {
            const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return regex.test(email);
        }
    </script>

</body>
</html> 
