<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gina Line T. - Data Analyst</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .header .subtitle {
            font-size: 1.3em;
            color: #666;
            margin-bottom: 20px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #555;
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 25px;
            color: #333;
            border-bottom: 3px solid #667eea;
            padding-bottom: 10px;
        }

        .about-text {
            font-size: 1.1em;
            line-height: 1.8;
            color: #555;
            text-align: justify;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .project-card h3 {
            color: #333;
            margin-bottom: 15px;
            font-size: 1.4em;
        }

        .project-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .project-description {
            color: #555;
            margin-bottom: 15px;
        }

        .project-learnings {
            background: rgba(102, 126, 234, 0.1);
            border-left: 4px solid #667eea;
            padding: 15px;
            border-radius: 5px;
            margin-top: 15px;
        }

        .project-learnings h4 {
            color: #667eea;
            margin-bottom: 8px;
            font-size: 1.1em;
        }

        .experience-item {
            border-left: 4px solid #667eea;
            padding-left: 25px;
            margin-bottom: 30px;
            position: relative;
        }

        .experience-item::before {
            content: '';
            position: absolute;
            left: -8px;
            top: 0;
            width: 12px;
            height: 12px;
            background: #667eea;
            border-radius: 50%;
        }

        .experience-title {
            font-size: 1.3em;
            font-weight: bold;
            color: #333;
            margin-bottom: 5px;
        }

        .experience-company {
            color: #667eea;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .experience-duration {
            color: #777;
            font-style: italic;
            margin-bottom: 15px;
        }

        .experience-tasks {
            color: #555;
        }

        .education-item {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            border-radius: 10px;
            padding: 20px;
        }

        .skill-category h4 {
            color: #333;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        .skills-list {
            color: #555;
            line-height: 1.8;
        }

        .languages {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
        }

        .language-item {
            background: rgba(102, 126, 234, 0.1);
            padding: 15px 20px;
            border-radius: 25px;
            text-align: center;
        }

        .hobbies {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .hobby-item {
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%);
            padding: 15px 20px;
            border-radius: 25px;
            color: #333;
        }

        @media (max-width: 768px) {
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .container {
                padding: 10px;
            }
            
            .section, .header {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="profile-photo-container" style="margin-bottom: 20px;">
                <img src="https://imgur.com/npmSXxC.jpg" alt="Gina Line T." class="profile-photo" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; border: 4px solid #667eea; box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);">
            </div>
            <h1>Gina Line T.</h1>
            <div class="subtitle">Data Analyst</div>
            <p style="margin-top: 15px; font-style: italic; color: #666;">Candidature pour alternance, stage, CDI ou CDD</p>
            
            <div class="contact-info">
                <div class="contact-item">
                    <span>📱</span>
                    <span>06 63 25 33 85</span>
                </div>
                <div class="contact-item">
                    <span>✉️</span>
                    <span>line.tchokomakoua@gmail.com</span>
                </div>
                <div class="contact-item">
                    <span>💼</span>
                    <span>line-tchokomakoua</span>
                </div>
            </div>
        </div>

        <!-- À propos -->
        <div class="section">
            <h2>À propos</h2>
            <div class="about-text">
                Data Analyst passionnée, j'exploite la donnée de bout en bout pour guider les décisions stratégiques. 
                Mon parcours croise data engineering, web analyse et marketing digital, avec une approche orientée impact, 
                curiosité et autonomie. <strong>Je souhaite mettre la donnée au service de décisions concrètes et accessibles, 
                en alliant rigueur analytique et sens du design.</strong> Mon objectif est de transformer les insights 
                techniques en recommandations activables pour les équipes métiers.
            </div>
        </div>

        <!-- Projets -->
        <div class="section">
            <h2>Projets</h2>
            <div class="projects-grid">
                <!-- Projet 1: Détection de fake news -->
                <div class="project-card">
                    <h3>🔍 Outil de détection de fake news</h3>
                    <img src="https://imgur.com/t7ZZqVM.jpg" alt="Interface de détection de fake news" class="project-image">
                    <div class="project-description">
                        <strong>Technologies :</strong> Python & Machine Learning<br>
                        • Modélisation de classificateurs (SVM, Random Forest, Deep Learning)<br>
                        • Évaluation et amélioration des performances<br>
                        • Interface utilisateur intuitive pour l'analyse en temps réel
                    </div>
                    <div class="project-learnings">
                        <h4>Ce que j'ai appris / Impact</h4>
                        Maîtrise des algorithmes de classification et optimisation des hyperparamètres. 
                        J'ai développé une approche méthodique pour évaluer la fiabilité des modèles et 
                        créé une solution pratique contre la désinformation.
                    </div>
                </div>

                <!-- Projet 2: Pipeline ETL AWS -->
                <div class="project-card">
                    <h3>☁️ Pipeline ETL sur AWS</h3>
                    <img src="https://imgur.com/7y3jcAM.jpg" alt="Architecture Pipeline AWS" class="project-image">
                    <div class="project-description">
                        <strong>Technologies :</strong> AWS (Glue, Lambda, S3)<br>
                        • Traitement de données via AWS Glue et Lambda<br>
                        • Stockage optimisé sur S3<br>
                        • Documentation complète de l'architecture<br>
                        • Automatisation des flux de données
                    </div>
                    <div class="project-learnings">
                        <h4>Ce que j'ai appris / Impact</h4>
                        Expertise en architecture cloud et automatisation des pipelines de données. 
                        Cette expérience m'a permis de comprendre les enjeux de scalabilité et 
                        d'optimisation des coûts en environnement cloud.
                    </div>
                </div>

                <!-- Projet 3: Gestion d'établissement scolaire -->
                <div class="project-card">
                    <h3>🏫 Application de gestion d'établissement scolaire</h3>
                    <img src="https://imgur.com/vQWC3Fz.jpg" alt="Dashboard gestion scolaire" class="project-image">
                    <div class="project-description">
                        <strong>Technologies :</strong> Développement web & Analytics<br>
                        • Conception d'une plateforme web pour la gestion des élèves, paiements, enseignants<br>
                        • Intégration de dashboards d'analyse<br>
                        • Interface utilisateur adaptée aux différents profils
                    </div>
                    <div class="project-learnings">
                        <h4>Ce que j'ai appris / Impact</h4>
                        Développement de solutions complètes orientées utilisateur. J'ai appris à 
                        traduire les besoins métiers en fonctionnalités techniques et à créer des 
                        tableaux de bord pertinents pour le pilotage opérationnel.
                    </div>
                </div>

                <!-- Projet 4: Gestion de bibliothèque Scala -->
                <div class="project-card">
                    <h3>📚 Application de gestion de bibliothèque en Scala</h3>
                    <img src="https://imgur.com/ZnixMgP.jpg" alt="Code Scala gestion bibliothèque" class="project-image">
                    <div class="project-description">
                        <strong>Technologies :</strong> Scala & Programmation fonctionnelle<br>
                        • Développement d'une application Scala pour gestion des livres et utilisateurs<br>
                        • Optimisation des structures de données pour améliorer les performances<br>
                        • Architecture modulaire et maintenable
                    </div>
                    <div class="project-learnings">
                        <h4>Ce que j'ai appris / Impact</h4>
                        Maîtrise de la programmation fonctionnelle et des concepts avancés de Scala. 
                        Ce projet m'a permis d'approfondir l'optimisation algorithmique et la 
                        conception de systèmes performants.
                    </div>
                </div>
            </div>
        </div>

        <!-- Expériences Professionnelles -->
        <div class="section">
            <h2>Expériences Professionnelles</h2>
            
            <div class="experience-item">
                <div class="experience-title">Data Engineer</div>
                <div class="experience-company">DEVOTEAM</div>
                <div class="experience-duration">Janvier à Avril 2024 (4 mois - Stage)</div>
                <div class="experience-tasks">
                    • Pipelines ETL (Python, AWS Glue)<br>
                    • Traitement & stockage de données (S3, Lambda)<br>
                    • Dashboards & documentation technique
                </div>
            </div>

            <div class="experience-item">
                <div class="experience-title">Web Analyste</div>
                <div class="experience-company">KEVMAX SARL</div>
                <div class="experience-duration">Juin 2021 à Juin 2023 (2 ans - CDI)</div>
                <div class="experience-tasks">
                    • Suivi et optimisation des performances web<br>
                    • Création de dashboards décisionnels<br>
                    • Analyse des campagnes SEA, SEO, social ads ; reporting hebdomadaire<br>
                    • Recommandations stratégiques basées sur les données utilisateurs<br>
                    • Création de visuels (UI/UX) et portfolios clients
                </div>
            </div>

            <div class="experience-item">
                <div class="experience-title">Community Manager</div>
                <div class="experience-company">EED SARL</div>
                <div class="experience-duration">Août 2020 à Mars 2021 (8 mois - CDD)</div>
                <div class="experience-tasks">
                    • Élaboration des stratégies marketing<br>
                    • Pilotage des équipes de campagnes<br>
                    • Suivi des retours utilisateurs et amélioration de l'expérience client
                </div>
            </div>
        </div>

        <!-- Formation -->
        <div class="section">
            <h2>Formation</h2>
            
            <div class="education-item">
                <div class="experience-title">Mastère II en Intelligence Artificielle et Management (Data Analyst)</div>
                <div class="experience-company">IA SCHOOL PARIS</div>
                <div class="experience-duration">Septembre 2024</div>
                <div style="margin-top: 10px; color: #555;">
                    Spécialisation : Data Analyst, Data Scientist, Chef de projet
                </div>
            </div>

            <div class="education-item">
                <div class="experience-title">Master I en Marketing</div>
                <div class="experience-company">IUGE</div>
                <div class="experience-duration">Septembre 2019 à Septembre 2020</div>
                <div style="margin-top: 10px; color: #555;">
                    Économie des sciences et gestion
                </div>
            </div>
        </div>

        <!-- Compétences -->
        <div class="section">
            <h2>Compétences</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h4>Langages & Data</h4>
                    <div class="skills-list">
                        Python, SQL, R, Spark, SAS, MATLAB
                    </div>
                </div>

                <div class="skill-category">
                    <h4>Data Viz & Outils</h4>
                    <div class="skills-list">
                        Power BI, Tableau, Google Analytics, Git, Excel
                    </div>
                </div>

                <div class="skill-category">
                    <h4>Cloud & Big Data</h4>
                    <div class="skills-list">
                        AWS (S3, Glue, Lambda), Azure, BigQuery, Hadoop, Scala
                    </div>
                </div>

                <div class="skill-category">
                    <h4>Bases de données</h4>
                    <div class="skills-list">
                        MySQL, MongoDB
                    </div>
                </div>

                <div class="skill-category">
                    <h4>Soft Skills</h4>
                    <div class="skills-list">
                        Créativité, adaptabilité, esprit d'analyse, communication
                    </div>
                </div>

                <div class="skill-category">
                    <h4>Design & Création visuelle</h4>
                    <div class="skills-list">
                        Adobe Photoshop, Illustrator, InDesign
                    </div>
                </div>
            </div>
        </div>

        <!-- Langues -->
        <div class="section">
            <h2>Langues</h2>
            <div class="languages">
                <div class="language-item">
                    <strong>Français</strong><br>
                    Langue maternelle
                </div>
                <div class="language-item">
                    <strong>Anglais</strong><br>
                    B2 (TOEFL en cours)
                </div>
            </div>
        </div>

        <!-- Loisirs -->
        <div class="section">
            <h2>Loisirs</h2>
            <div class="hobbies">
                <div class="hobby-item">
                    📚 Lecture (actualités/sciences/finances et développement)
                </div>
                <div class="hobby-item">
                    👨‍🍳 Cuisine
                </div>
                <div class="hobby-item">
                    🤝 Bénévolat (cuisine et distribution de repas aux sans-abris)
                </div>
            </div>
        </div>
    </div>
</body>
</html>
