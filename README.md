<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Black Revolution SpaceX</title>
    <style>
        body { background-color: #000; color: #fff; font-family: 'Courier New', Courier, monospace; margin: 0; padding: 0; text-align: center; }
        header { padding: 20px; border-bottom: 2px solid #ff0000; }
        .red { color: #ff0000; }
        
        /* Style des "poches" photos */
        .photo-container { display: none; padding: 20px; }
        .poche { background: #111; border: 1px solid #333; margin-bottom: 20px; border-radius: 8px; overflow: hidden; }
        .poche img { width: 100%; height: auto; display: block; filter: grayscale(50%); }
        .poche-info { padding: 15px; border-top: 1px solid #ff0000; }

        button { background: none; border: 2px solid #fff; color: #fff; padding: 15px 30px; font-size: 18px; cursor: pointer; margin-top: 50px; }
        button:active { background-color: #fff; color: #000; }
    </style>
</head>
<body>

    <header>
        <h1>BLACK <span class="red">REVOLUTION</span></h1>
        <p style="font-size: 12px;">PROJET SPACEX - UNITÉ SECRÈTE</p>
    </header>

    <div id="lock-screen">
        <button onclick="validerAcces()">ACCÈS SERVEUR</button>
    </div>

    <div id="project-list" class="photo-container">
        <h2 class="red">DOSSIERS CLASSÉS</h2>

        <div class="poche">
            <img src="votre_image_1.jpg" alt="Projet Alpha">
            <div class="poche-info">
                <h3>PROJET ALPHA</h3>
                <p>Propulsion ionique expérimentale.</p>
            </div>
        </div>

        <div class="poche">
            <img src="votre_image_2.jpg" alt="Projet Starship">
            <div class="poche-info">
                <h3>STARSHIP REVOLUTION</h3>
                <p>Architecture de colonisation martienne.</p>
            </div>
        </div>
    </div>

    <script>
        function validerAcces() {
            // Pour que cela fonctionne sur localhost sans erreur :
            // Nous simulons la vérification du cryptage
            if (window.location.protocol !== 'https:' && window.location.hostname !== 'localhost') {
                alert("Accès refusé : Cryptage requis");
            } else {
                // Si c'est ok, on cache le bouton et on montre les photos
                document.getElementById('lock-screen').style.display = 'none';
                document.getElementById('project-list').style.display = 'block';
            }
        }
    </script>
</body>
</html>
