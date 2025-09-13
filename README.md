# mon_portfolio

Bienvenue sur mon portfolio en ligne ! Je suis étudiant en Master  de Modélisation et Analyse Numérique à l'Université de Montpellier.

## À propos

Ce site présente mes travaux de recherche, projets académiques et compétences techniques.

## Structure du Projet

- `index.html`:  Page principale de mon portfolio.
  <!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio de Marwane Tchabanna</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Portfolio de Marwane Tchabanna</h1>
    <p>Étudiant en Master  - Modélisation et Analyse Numérique à l’Université de Montpellier</p>
    <p><strong>Cours suivis :</strong> Optimisation, Analyse Numérique, ODP, Mécanique, Analyse Fonctionnelle, Géométrie Différentielle</p>
  </header>

  <main>
    <section id="intro">
      <h2>Introduction</h2>
      <p>Bienvenue sur mon site personnel ! Ici, je partage mes travaux, mes projets et mes réflexions en mathématiques. 
         L’objectif est de rendre accessibles mes recherches et exercices pour progresser ensemble dans ce beau voyage numérique et analytique.</p>
    </section>

    <section id="travaux">
      <h2>Mes Travaux</h2>   
      <div id="travaux-list"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 - Marwane Tchabanna</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

- `style.css`: Feuille de style pour le design du site.
- body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #f9f9f9;
  color: #333;
}

header {
  background: #2c3e50;
  color: white;
  text-align: center;
  padding: 2rem 1rem;
}

h1 {
  margin: 0;
  font-size: 2.2rem;
}

main {
  max-width: 900px;
  margin: 2rem auto;
  padding: 1rem;
}

section {
  margin-bottom: 2rem;
}

#travaux-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1rem;
}

.travail {
  background: white;
  padding: 1rem;
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform 0.2s ease;
}

.travail:hover {
  transform: translateY(-5px);
}

.travail h3 {
  margin-top: 0;
  color: #2c3e50;
}

.travail a {
  display: inline-block;
  margin-right: 10px;
  text-decoration: none;
  color: #3498db;
  font-weight: bold;
}

footer {
  text-align: center;
  background: #2c3e50;
  color: white;
  padding: 1rem;
  margin-top: 2rem;
}
- `script.js`: Scripts JavaScript pour les fonctionnalités dynamiques.
- // Charger les travaux depuis travaux.json
fetch('travaux.json')
  .then(response => response.json())
  .then(data => {
    const travauxList = document.getElementById('travaux-list');
    data.forEach(travail => {
      const div = document.createElement('div');
      div.className = 'travail';

      div.innerHTML = `
        <h3>${travail.titre}</h3>
        <p>${travail.description}</p>
        <a href="${travail.page}" target="_blank">Voir plus</a>
        <a href="${travail.pdf}" target="_blank">Télécharger PDF</a>
      `;
      travauxList.appendChild(div);
    });
  })
  .catch(error => {
    console.error("Erreur lors du chargement du JSON :", error);
  });
- `travaux.json`: Données concernant mes travaux et projets.
- [
  {
    "titre": "Optimisation",
    "description": "Travaux dirigés et projets autour des méthodes d’optimisation.",
    "page": "travaux/optimisation_td1.html",
    "pdf": "pdf/td_monte_carlo.pdf"
  },
  {
    "titre": "ODP (Optimisation des Processus)",
    "description": "Exercices et applications pratiques en ODP.",
    "page": "travaux/odp_exercices.html",
    "pdf": "pdf/odp.pdf"
  },
  {
    "titre": "Mécanique",
    "description": "Problèmes et solutions en mécanique mathématique.",
    "page": "travaux/mecanique_td.html",
    "pdf": "pdf/mecanique.pdf"
  },
  {
    "titre": "Analyse Fonctionnelle",
    "description": "Cours et TD d'analyse fonctionnelle appliquée.",
    "page": "travaux/af_cours.html",
    "pdf": "pdf/af.pdf"
  },
  {
    "titre": "Géométrie Différentielle",
    "description": "Notes et travaux pratiques en géométrie différentielle.",
    "page": "travaux/geo_diff.html",
    "pdf": "pdf/geo_diff.pdf"
  }
]
<section id="travaux">
    <h2>Mes Travaux</h2>
    <div class="travaux-list">
        <div class="travail">
            <h3>Projet d'Optimisation</h3>
            <p>Description du projet d'optimisation que tu as réalisé. Tu peux parler des méthodes utilisées, des résultats obtenus, etc.</p>
        </div>
        <div class="travail">
            <h3>Analyse Numérique</h3>
            <p>Description d'un projet ou exercice en analyse numérique. Par exemple, la résolution d'une équation différentielle.</p>
        </div>
        <div class="travail">
            <h3>Projet en Géométrie Différentielle</h3>
            <p>Description d'un projet ou étude en géométrie différentielle.</p>
        </div>
    </div>
</section>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: #f9f9f9;
    color: #333;
}

header {
    background: #2c3e50;
    color: white;
    text-align: center;
    padding: 2rem 1rem;
}

h1 {
    margin: 0;
    font-size: 2.2rem;
}

main {
    max-width: 900px;
    margin: 2rem auto;
    padding: 1rem;
}

section {
    margin-bottom: 2rem;
}

.travaux-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 1rem;
}

.travail {
    background: white;
    padding: 1rem;
    border-radius: 10px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease;
}

.travail:hover {
    transform: translateY(-5px);
}

footer {
    text-align: center;
    padding: 1rem;
    background: #2c3e50;
    color: white;
    position: fixed;
    bottom: 0;
    width: 100%;
}


## Comment naviguer

Visitez mon site en ligne : [https://danladi-boop.github.io/mon_portfolio/](https://danladi-boop.github.io/mon_portfolio/)

