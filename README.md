<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>pageweb-geii-Dumont</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
/* ===== BASE ===== */
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(180deg, #e6ebf2, #f4f7fb);
    color: #333;
}

/* ===== HEADER ===== */
header {
    background: linear-gradient(135deg, #003366, #0055a5);
    color: white;
    padding: 60px 20px;
    text-align: center;
}

.photo-profil {
    width: 130px;
    height: 130px;
    border-radius: 50%;
    border: 4px solid white;
    object-fit: cover;
    margin-bottom: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.25);
}

header h1 {
    margin: 0;
    font-size: 44px;
}

header p {
    margin: 6px 0;
    font-weight: 300;
}

/* ===== NAV ===== */
nav {
    background-color: #002a52;
    padding: 14px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

nav button {
    background: transparent;
    border: 2px solid white;
    color: white;
    padding: 10px 20px;
    margin: 6px;
    border-radius: 25px;
    cursor: pointer;
    font-weight: 600;
    transition: 0.3s;
}

nav button:hover {
    background: white;
    color: #002a52;
}

/* ===== CONTAINER ===== */
.container {
    max-width: 950px;
    margin: auto;
    padding: 40px 20px;
}

/* ===== SECTIONS ===== */
section {
    background: white;
    padding: 35px;
    border-radius: 18px;
    box-shadow: 0 15px 35px rgba(0,0,0,0.08);
    margin-bottom: 30px;
    display: none;
    animation: fade 0.5s ease;
}

section.active {
    display: block;
}

@keyframes fade {
    from { opacity: 0; transform: translateY(15px); }
    to { opacity: 1; transform: translateY(0); }
}

/* ===== TITRES ===== */
h2 {
    color: #003366;
    border-left: 6px solid #0055a5;
    padding-left: 14px;
    margin-top: 0;
    margin-bottom: 20px;
}

/* ===== TEXTE ===== */
p, li {
    font-size: 15px;
}

ul {
    line-height: 1.9;
    padding-left: 18px;
    margin: 0;
}

.info {
    font-weight: 600;
    color: #003366;
    margin-top: 18px;
}

/* ===== CV ===== */
.cv-button {
    display: inline-block;
    margin-top: 10px;
    padding: 12px 22px;
    background: linear-gradient(135deg, #0055a5, #003366);
    color: white;
    text-decoration: none;
    border-radius: 10px;
    font-weight: 600;
    transition: 0.3s;
}

.cv-button:hover {
    transform: scale(1.05);
}

/* ===== BLOCS TEXTE + IMAGE ===== */
.bloc-avec-image-droite {
    display: inline-flex;
    align-items: center;
    gap: 6px;
}

.bloc-image img,
.competences-images img {
    width: 70px;
    padding: 6px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.15);
}

/* ===== COMPÉTENCES ===== */
.competences-images {
    display: inline-flex;
    gap: 6px;
    margin-left: 4px;
}

/* ===== FOOTER ===== */
footer {
    background-color: #002a52;
    color: white;
    text-align: center;
    padding: 18px;
    font-size: 14px;
}

/* ===== RESPONSIVE ===== */
@media (max-width: 700px) {
    .bloc-avec-image-droite {
        flex-direction: column;
        align-items: flex-start;
    }
}
</style>

<script>
function afficherSection(id) {
    document.querySelectorAll("section")
        .forEach(section => section.classList.remove("active"));
    document.getElementById(id).classList.add("active");
}
</script>
</head>

<body>

<header>
    <img src="mathis.jpg" class="photo-profil">
    <h1>Mathis Dumont</h1>
    <p>Étudiant BUT GEII</p>
    <p>Alternant technicien de maintenance</p>
</header>

<nav>
    <button onclick="afficherSection('accueil')">Accueil</button>
    <button onclick="afficherSection('profil')">Profil</button>
    <button onclick="afficherSection('experience')">Expérience</button>
    <button onclick="afficherSection('formation')">Formation</button>
    <button onclick="afficherSection('competences')">Compétences</button>
    <button onclick="afficherSection('contact')">Contact</button>
</nav>

<div class="container">

<section id="accueil" class="active">
    <h2>Bienvenue</h2>
    <p>Bienvenue sur mon site personnel <strong>pageweb-geii-Dumont</strong>.</p>
    <p>Vous y trouverez mon parcours, mes compétences et mon expérience professionnelle.</p>
</section>

<section id="profil">
    <h2>Profil</h2>
    <p>Étudiant en Génie Électrique et Informatique Industrielle, passionné par la maintenance et l’automatisation.</p>

    <p class="info">Mon CV</p>
    <a href="CV_Mathis_Dumont.pdf" target="_blank" class="cv-button">📄 Télécharger mon CV</a>

    <iframe src="CV_Mathis_Dumont.pdf" width="100%" height="500"
        style="border-radius:12px; border:1px solid #dde3ec; margin-top:18px;"></iframe>
</section>

<section id="experience">
    <h2>Expérience</h2>

    <div class="bloc-avec-image-droite">
        <div>
            <p class="info">Alternant technicien de maintenance</p>
            <p>SICAL Groupe Rossmann – Creil</p>
            <ul>
                <li>Maintenance industrielle</li>
                <li>Dépannage</li>
                <li>Diagnostic</li>
            </ul>
        </div>
        <div class="bloc-image">
            <img src="sical.png">
        </div>
    </div>
</section>

<section id="formation">
    <h2>Formation</h2>

    <div class="bloc-avec-image-droite">
        <div>
            <p class="info">BUT GEII</p>
            <p>IUT Cuffies Jules Verne</p>
            <ul>
                <li>Automatisation</li>
                <li>API Siemens</li>
                <li>Électrotechnique</li>
            </ul>
        </div>
        <div class="bloc-image">
            <img src="geii.jpg">
        </div>
    </div>
</section>

<section id="competences">
    <h2>Compétences</h2>

    <div class="bloc-avec-image-droite">
        <ul>
            <li>Maintenance industrielle</li>
            <li>Automatisation</li>
            <li>API Siemens</li>
            <li>Électricité industrielle</li>
        </ul>

        <div class="competences-images">
            <img src="elec.png">
            <img src="siemens.png">
        </div>
    </div>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email : <strong>mathis.dumont60@gmail.com</strong></p>
    <p>Téléphone : <strong>06 42 31 13 63</strong></p>
</section>

</div>

<footer>
    © 2026 – pageweb-geii-Dumont | Mathis Dumont
</footer>

</body>
</html>
