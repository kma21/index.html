<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AEROLIQ Industries - Pionniers de l'exploration spatiale</title>
    <style>
        /* Variables CSS pour une cohérence des couleurs */
        :root {
            --primary-color: #0a1128;
            --secondary-color: #00d4ff;
            --accent-color: #ff4d00;
            --text-color: #ffffff;
            --dark-bg: #050a1a;
            --card-bg: rgba(10, 17, 40, 0.8);
        }
        
        /* Reset et styles de base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--primary-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        a {
            text-decoration: none;
            color: var(--secondary-color);
            transition: color 0.3s;
        }
        
        a:hover {
            color: var(--accent-color);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--secondary-color);
            color: var(--primary-color);
            border: none;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .btn:hover {
            background-color: var(--accent-color);
            color: var(--text-color);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--secondary-color);
            color: var(--secondary-color);
        }
        
        .btn-outline:hover {
            background-color: var(--secondary-color);
            color: var(--primary-color);
        }
        
        section {
            padding: 100px 0;
        }
        
        h1, h2, h3, h4 {
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        h1 {
            font-size: 3.5rem;
            line-height: 1.2;
        }
        
        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        h2:after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--secondary-color);
        }
        
        p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }
        
        /* Header et Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 20px 0;
            transition: all 0.3s ease;
        }
        
        header.scrolled {
            background-color: rgba(5, 10, 26, 0.95);
            padding: 15px 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--text-color);
            display: flex;
            align-items: center;
        }
        
        .logo span {
            color: var(--secondary-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--text-color);
            font-weight: 500;
            position: relative;
        }
        
        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary-color);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover:after {
            width: 100%;
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(5, 10, 26, 0.7), rgba(5, 10, 26, 0.9)), url('https://images.unsplash.com/photo-1446776653964-20c1d3a81b06?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            text-align: center;
            position: relative;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            margin-bottom: 30px;
            animation: fadeInUp 1s ease;
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            animation: fadeInUp 1s ease 0.2s both;
        }
        
        .hero-btns {
            animation: fadeInUp 1s ease 0.4s both;
        }
        
        .hero-btns .btn {
            margin: 0 10px;
        }
        
        /* About Section */
        .about {
            background-color: var(--dark-bg);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        /* Rovers Section */
        .rovers {
            background-color: var(--primary-color);
        }
        
        .rovers-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .rover-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .rover-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
        }
        
        .rover-image {
            height: 250px;
            overflow: hidden;
        }
        
        .rover-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .rover-card:hover .rover-image img {
            transform: scale(1.1);
        }
        
        .rover-info {
            padding: 25px;
        }
        
        .rover-info h3 {
            color: var(--secondary-color);
            margin-bottom: 15px;
        }
        
        .rover-stats {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 15px;
        }
        
        .stat {
            text-align: center;
        }
        
        .stat-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--secondary-color);
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }
        
        /* Missions Section */
        .missions {
            background-color: var(--dark-bg);
        }
        
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline:before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 50%;
            width: 2px;
            background-color: var(--secondary-color);
            transform: translateX(-50%);
        }
        
        .timeline-item {
            padding: 20px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: var(--card-bg);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            position: relative;
        }
        
        .timeline-content:after {
            content: '';
            position: absolute;
            top: 20px;
            width: 20px;
            height: 20px;
            background-color: var(--card-bg);
            transform: rotate(45deg);
        }
        
        .timeline-item:nth-child(odd) .timeline-content:after {
            right: -10px;
        }
        
        .timeline-item:nth-child(even) .timeline-content:after {
            left: -10px;
        }
        
        .timeline-date {
            font-weight: bold;
            color: var(--secondary-color);
            margin-bottom: 10px;
        }
        
        .timeline-marker {
            position: absolute;
            top: 30px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: var(--secondary-color);
            z-index: 1;
        }
        
        .timeline-item:nth-child(odd) .timeline-marker {
            right: -10px;
        }
        
        .timeline-item:nth-child(even) .timeline-marker {
            left: -10px;
        }
        
        /* Contact Section */
        .contact {
            background-color: var(--primary-color);
        }
        
        .contact-content {
            display: flex;
            gap: 50px;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-form {
            flex: 1;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            background-color: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 4px;
            color: var(--text-color);
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--secondary-color);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .info-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
        }
        
        .info-icon {
            margin-right: 15px;
            color: var(--secondary-color);
            font-size: 1.2rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-bg);
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
        }
        
        .footer-column {
            flex: 1;
            margin-right: 30px;
        }
        
        .footer-column:last-child {
            margin-right: 0;
        }
        
        .footer-column h3 {
            color: var(--secondary-color);
            margin-bottom: 25px;
            font-size: 1.3rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--secondary-color);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: var(--text-color);
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background-color: var(--secondary-color);
            color: var(--primary-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .contact-content {
                flex-direction: column;
            }
            
            .footer-content {
                flex-wrap: wrap;
            }
            
            .footer-column {
                flex: 1 0 50%;
                margin-bottom: 30px;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .timeline:before {
                left: 30px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 0;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-marker {
                left: 20px !important;
            }
            
            .timeline-content:after {
                left: -10px !important;
            }
            
            .hero-btns .btn {
                display: block;
                margin: 10px auto;
                width: 80%;
                max-width: 250px;
            }
        }
        
        @media (max-width: 576px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            section {
                padding: 60px 0;
            }
            
            .footer-column {
                flex: 1 0 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container header-container">
            <a href="#" class="logo">AERO<span>LIQ</span></a>
            <div class="mobile-menu">☰</div>
            <ul class="nav-links">
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#a-propos">À propos</a></li>
                <li><a href="#rovers">Rovers</a></li>
                <li><a href="#missions">Missions</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="accueil">
        <div class="container">
            <div class="hero-content">
                <h1>L'avenir de l'exploration spatiale commence ici</h1>
                <p>AEROLIQ Industries repousse les limites de la technologie pour établir une présence humaine durable dans le système solaire.</p>
                <div class="hero-btns">
                    <a href="#rovers" class="btn">Découvrir nos Rovers</a>
                    <a href="#missions" class="btn btn-outline">Nos Missions</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="a-propos">
        <div class="container">
            <h2>À propos d'AEROLIQ</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Fondée en 2020, AEROLIQ Industries est une entreprise aérospatiale privée dédiée à la révolution de l'exploration spatiale. Notre mission est de rendre la vie multi-planétaire en établissant des colonies humaines sur Mars et la Lune.</p>
                    <p>Nous développons des technologies de pointe pour les voyages spatiaux, l'exploration robotique et les systèmes de support de vie durable. Nos équipes d'ingénieurs et de scientifiques travaillent sans relâche pour repousser les frontières de ce qui est possible.</p>
                    <p>Aujourd'hui, nous sommes fiers d'opérer deux rovers avancés : ARTEMIS sur la Lune et ARES sur Mars, collectant des données précieuses pour les futures missions habitées.</p>
                    <a href="#" class="btn">En savoir plus</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1446776877081-d282a0f896e2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Fusée AEROLIQ">
                </div>
            </div>
        </div>
    </section>

    <!-- Rovers Section -->
    <section class="rovers" id="rovers">
        <div class="container">
            <h2>Nos Rovers</h2>
            <div class="rovers-grid">
                <!-- Rover 1 -->
                <div class="rover-card">
                    <div class="rover-image">
                        <img src="https://images.unsplash.com/photo-1614728263952-84ea256f4e8c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Rover ARTEMIS sur la Lune">
                    </div>
                    <div class="rover-info">
                        <h3>ARTEMIS</h3>
                        <p>Notre rover lunaire de nouvelle génération explore la surface de la Lune depuis 2022. Équipé de technologies de pointe, ARTEMIS cartographie les ressources lunaires et prépare le terrain pour l'établissement d'une base permanente.</p>
                        <div class="rover-stats">
                            <div class="stat">
                                <div class="stat-value">18</div>
                                <div class="stat-label">Mois en service</div>
                            </div>
                            <div class="stat">
                                <div class="stat-value">42.7</div>
                                <div class="stat-label">Km parcourus</div>
                            </div>
                            <div class="stat">
                                <div class="stat-value">1,250</div>
                                <div class="stat-label">Échantillons</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Rover 2 -->
                <div class="rover-card">
                    <div class="rover-image">
                        <img src="https://images.unsplash.com/photo-1614313913007-2b4ae8ce32d6?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Rover ARES sur Mars">
                    </div>
                    <div class="rover-info">
                        <h3>ARES</h3>
                        <p>ARES est notre rover martien qui explore la planète rouge depuis 2023. Conçu pour résister aux conditions extrêmes de Mars, il recherche des signes de vie passée et teste des technologies essentielles pour les futures missions habitées.</p>
                        <div class="rover-stats">
                            <div class="stat">
                                <div class="stat-value">9</div>
                                <div class="stat-label">Mois en service</div>
                            </div>
                            <div class="stat">
                                <div class="stat-value">15.3</div>
                                <div class="stat-label">Km parcourus</div>
                            </div>
                            <div class="stat">
                                <div class="stat-value">687</div>
                                <div class="stat-label">Échantillons</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Missions Section -->
    <section class="missions" id="missions">
        <div class="container">
            <h2>Nos Missions</h2>
            <div class="timeline">
                <!-- Mission 1 -->
                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">Juin 2022</div>
                        <h3>Mission ARTEMIS I</h3>
                        <p>Lancement et atterrissage réussi du rover ARTEMIS sur la face visible de la Lune. Début des opérations d'exploration et de cartographie des ressources.</p>
                    </div>
                </div>
                
                <!-- Mission 2 -->
                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">Février 2023</div>
                        <h3>Mission ARES I</h3>
                        <p>Atterrissage du rover ARES dans le cratère Jezero sur Mars. Début de la recherche de biosignatures et d'analyse géologique.</p>
                    </div>
                </div>
                
                <!-- Mission 3 -->
                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">Septembre 2023</div>
                        <h3>Découverte majeure</h3>
                        <p>ARTEMIS découvre des dépôts de glace d'eau substantiels dans un cratère lunaire ombragé en permanence, une ressource cruciale pour les futures colonies.</p>
                    </div>
                </div>
                
                <!-- Mission 4 -->
                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">Avril 2024</div>
                        <h3>Mission ARTEMIS II</h3>
                        <p>Lancement prévu du deuxième rover lunaire ARTEMIS II, qui se concentrera sur l'exploration du pôle sud lunaire.</p>
                    </div>
                </div>
                
                <!-- Mission 5 -->
                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">2025</div>
                        <h3>Mission ARES II</h3>
                        <p>Préparation de la mission ARES II qui emportera des instruments plus avancés pour l'analyse in situ des échantillons martiens.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2>Contactez-nous</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Informations de contact</h3>
                    <div class="info-item">
                        <div class="info-icon">📍</div>
                        <div>
                            <h4>Siège social</h4>
                            <p>123 Avenue des Étoiles<br>75000 Paris, France</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">📞</div>
                        <div>
                            <h4>Téléphone</h4>
                            <p>+33 1 23 45 67 89</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">✉️</div>
                        <div>
                            <h4>Email</h4>
                            <p>contact@aeroliq-industries.com</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🌐</div>
                        <div>
                            <h4>Réseaux sociaux</h4>
                            <div class="social-links">
                                <a href="#" class="social-link">f</a>
                                <a href="#" class="social-link">t</a>
                                <a href="#" class="social-link">in</a>
                                <a href="#" class="social-link">ig</a>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Envoyez-nous un message</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Nom complet</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Adresse email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Sujet</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn">Envoyer le message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>AEROLIQ Industries</h3>
                    <p>Pionniers de l'exploration spatiale, repoussant les frontières de la science et de la technologie pour un avenir multi-planétaire.</p>
                    <div class="social-links">
                        <a href="#" class="social-link">f</a>
                        <a href="#" class="social-link">t</a>
                        <a href="#" class="social-link">in</a>
                        <a href="#" class="social-link">ig</a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Liens rapides</h3>
                    <ul class="footer-links">
                        <li><a href="#accueil">Accueil</a></li>
                        <li><a href="#a-propos">À propos</a></li>
                        <li><a href="#rovers">Rovers</a></li>
                        <li><a href="#missions">Missions</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Nos Rovers</h3>
                    <ul class="footer-links">
                        <li><a href="#">ARTEMIS (Lune)</a></li>
                        <li><a href="#">ARES (Mars)</a></li>
                        <li><a href="#">Futurs modèles</a></li>
                        <li><a href="#">Technologies</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Carrières</h3>
                    <ul class="footer-links">
                        <li><a href="#">Offres d'emploi</a></li>
                        <li><a href="#">Stages</a></li>
                        <li><a href="#">Culture d'entreprise</a></li>
                        <li><a href="#">Postuler</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 AEROLIQ Industries. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <script>
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Mobile menu toggle
        const mobileMenu = document.querySelector('.mobile-menu');
        const navLinks = document.querySelector('.nav-links');
        
        mobileMenu.addEventListener('click', function() {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });

        // Form submission
        const contactForm = document.querySelector('.contact-form form');
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Merci pour votre message! Nous vous répondrons dans les plus brefs délais.');
            contactForm.reset();
        });
    </script>
</body>
</html>
