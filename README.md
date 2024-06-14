<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tom's Content</title>
    <style>
        body {
            font-family: 'Lato', sans-serif;
            background-color: #e0f7fa;
            color: #0077b6;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #0077b6;
            color: #ffffff;
            padding: 10px 0;
            text-align: center;
        }
        .container {
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
        }
        .section-title {
            font-size: 24px;
            margin-top: 20px;
            border-bottom: 2px solid #0077b6;
            padding-bottom: 5px;
        }
        .about-me, .services, .experience, .contact {
            margin-top: 20px;
        }
        .contact label {
            display: block;
            margin: 10px 0 5px;
        }
        .contact input, .contact textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid #0077b6;
            border-radius: 4px;
        }
        .contact button {
            background-color: #0077b6;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 4px;
            margin-top: 10px;
        }
        .contact button:hover {
            background-color: #005f8b;
        }
        .flags {
            display: flex;
            justify-content: center;
            margin: 10px 0;
        }
        .flag {
            cursor: pointer;
            margin: 0 10px;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap" rel="stylesheet">
    <script>
        const translations = {
            en: {
                aboutMe: "Hello! I'm Tom, a Salesforce Admin and a devoted family man. I love working with Salesforce to help businesses manage their customer relationships and improve their sales processes. When I'm not working, I enjoy spending time with my family and exploring the great outdoors.",
                services: "I offer a range of services including Salesforce consultancy, operational effectiveness, and head of operations experience.",
                experience: "My experiences include working as a Salesforce consultant and as the head of operations.",
                contact: "Contact",
                name: "Name",
                email: "Email",
                message: "Message",
                send: "Send"
            },
            de: {
                aboutMe: "Hallo! Ich bin Tom, ein Salesforce-Administrator und ein engagierter Familienvater. Ich arbeite gerne mit Salesforce, um Unternehmen dabei zu helfen, ihre Kundenbeziehungen zu verwalten und ihre Verkaufsprozesse zu verbessern. Wenn ich nicht arbeite, verbringe ich gerne Zeit mit meiner Familie und erkunde die Natur.",
                services: "Ich biete eine Reihe von Dienstleistungen an, darunter Salesforce-Beratung, operative Effizienz und Erfahrung als Leiter des operativen Geschäfts.",
                experience: "Meine Erfahrungen umfassen die Arbeit als Salesforce-Berater und als Leiter des operativen Geschäfts.",
                contact: "Kontakt",
                name: "Name",
                email: "E-Mail",
                message: "Nachricht",
                send: "Senden"
            },
            fr: {
                aboutMe: "Bonjour! Je suis Tom, administrateur Salesforce et père de famille dévoué. J'aime travailler avec Salesforce pour aider les entreprises à gérer leurs relations clients et à améliorer leurs processus de vente. Quand je ne travaille pas, j'aime passer du temps avec ma famille et explorer le grand air.",
                services: "Je propose une gamme de services, y compris le conseil Salesforce, l'efficacité opérationnelle et l'expérience en tant que responsable des opérations.",
                experience: "Mon expérience inclut le travail en tant que consultant Salesforce et en tant que responsable des opérations.",
                contact: "Contact",
                name: "Nom",
                email: "E-mail",
                message: "Message",
                send: "Envoyer"
            }
        };

        function setLanguage(lang) {
            document.getElementById('aboutMeText').innerText = translations[lang].aboutMe;
            document.getElementById('servicesText').innerText = translations[lang].services;
            document.getElementById('experienceText').innerText = translations[lang].experience;
            document.getElementById('contactTitle').innerText = translations[lang].contact;
            document.getElementById('labelName').innerText = translations[lang].name;
            document.getElementById('labelEmail').innerText = translations[lang].email;
            document.getElementById('labelMessage').innerText = translations[lang].message;
            document.getElementById('sendButton').innerText = translations[lang].send;
        }
    </script>
</head>
<body onload="setLanguage('en')">
    <header>
        <h1>Welcome to Tom's Personal Webpage</h1>
        <div class="flags">
            <img src="https://flagcdn.com/w20/de.png" alt="German" class="flag" onclick="setLanguage('de')">
            <img src="https://flagcdn.com/w20/ch.png" alt="French" class="flag" onclick="setLanguage('fr')">
            <img src="https://flagcdn.com/w20/gb.png" alt="English" class="flag" onclick="setLanguage('en')">
        </div>
    </header>
    <div class="container">
        <div class="about-me">
            <h2 class="section-title">About Me</h2>
            <p id="aboutMeText"></p>
        </div>
        <div class="services">
            <h2 class="section-title">Services</h2>
            <p id="servicesText"></p>
        </div>
        <div class="experience">
            <h2 class="section-title">Experience</h2>
            <p id="experienceText"></p>
        </div>
        <div class="contact">
            <h2 class="section-title" id="contactTitle">Contact</h2>
            <form action="mailto:haukidoki@web.de" method="post" enctype="text/plain">
                <label for="name" id="labelName">Name:</label>
                <input type="text" id="name" name="name" required>
                <label for="email" id="labelEmail">Email:</label>
                <input type="email" id="email" name="email" required>
                <label for="message" id="labelMessage">Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>
                <button type="submit" id="sendButton">Send</button>
            </form>
        </div>
    </div>
</body>
</html>
