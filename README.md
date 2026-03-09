<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Classic Design Studio</title>
    <!-- Google Fonts for Traditional Look -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- CSS VARIABLES (Color Palette) --- */
        :root {
            --primary-color: #1a252f; /* Deep Navy Blue */
            --accent-color: #c5a059;  /* Muted Gold */
            --bg-color: #fdfbf7;      /* Off-white / Cream */
            --text-color: #333333;
            --white: #ffffff;
        }

        /* --- GLOBAL STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif; /* Traditional Serif Font */
            color: var(--primary-color);
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: 0.3s;
        }

        /* --- HEADER --- */
        header {
            background-color: var(--white);
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid var(--accent-color);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: 700;
            letter-spacing: 2px;
            color: var(--primary-color);
        }

        .logo span {
            color: var(--accent-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            font-size: 14px;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--primary-color);
        }

        nav ul li a:hover {
            color: var(--accent-color);
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 90vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: linear-gradient(rgba(26, 37, 47, 0.9), rgba(26, 37, 47, 0.8)), url('https://images.unsplash.com/photo-1558655146-d09347e0b7a8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            color: var(--white);
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            color: var(--white);
            margin-bottom: 20px;
            font-style: italic;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 40px;
            color: #ddd;
        }

        .btn {
            padding: 15px 40px;
            background-color: var(--accent-color);
            color: var(--white);
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: bold;
            border: 1px solid var(--accent-color);
        }

        .btn:hover {
            background-color: transparent;
            color: var(--accent-color);
        }

        /* --- SERVICES SECTION --- */
        .section {
            padding: 80px 50px;
            text-align: center;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .section-subtitle {
            color: var(--accent-color);
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.9rem;
            margin-bottom: 50px;
            display: block;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: var(--white);
            padding: 40px;
            border: 1px solid #e0e0e0;
            transition: 0.3s;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            border-color: var(--accent-color);
        }

        .service-card h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        /* --- PORTFOLIO SECTION --- */
        .portfolio {
            background-color: var(--white);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .portfolio-item {
            position: relative;
            height: 300px;
            overflow: hidden;
            background-color: #ddd;
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: 0.5s;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
            opacity: 0.7;
        }

        .overlay {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: var(--white);
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            opacity: 0;
            transition: 0.3s;
        }

        .portfolio-item:hover .overlay {
            opacity: 1;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 50px;
            text-align: center;
        }

        footer p {
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 20px;
            }
            nav ul {
                margin-top: 20px;
            }
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">ARTISAN<span>.</span></div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Portfolio</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Timeless Design for Modern Brands</h1>
        <p>We blend traditional aesthetics with contemporary strategy to create visual identities that last a lifetime.</p>
        <a href="#" class="btn">View Our Work</a>
    </section>

    <!-- Services Section -->
    <section class="section">
        <span class="section-subtitle">What We Do</span>
        <h2 class="section-title">Our Expertise</h2>
        
        <div class="services-grid">
            <div class="service-card">
                <h3>Brand Identity</h3>
                <p>Creating logos and visual systems that tell your story with elegance and clarity.</p>
            </div>
            <div class="service-card">
                <h3>Print Design</h3>
                <p>From business cards to brochures, we ensure every texture and color is perfect.</p>
            </div>
            <div class="service-card">
                <h3>Editorial Layout</h3>
                <p>Typography and layout design for magazines, books, and high-end publications.</p>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="section portfolio">
        <span class="section-subtitle">Selected Works</span>
        <h2 class="section-title">Portfolio</h2>
        
        <div class="portfolio-grid">
            <!-- Using placeholder images -->
            <div class="portfolio-item">
                <img src="https://images.unsplash.com/photo-1600607686527-6fb886090705?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Design 1">
                <div class="overlay">Luxury Packaging</div>
            </div>
            <div class="portfolio-item">
                <img src="https://images.unsplash.com/photo-1561070791-2526d30994b5?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Design 2">
                <div class="overlay">Editorial Layout</div>
            </div>
            <div class="portfolio-item">
                <img src="https://images.unsplash.com/photo-1558655146-d09347e0b7a8?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Design 3">
                <div class="overlay">Brand Identity</div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <h2>ARTISAN.</h2>
        <p>123 Design Street, Creative City, India</p>
        <br>
        <p>&copy; 2023 Artisan Design Studio. All Rights Reserved.</p>
    </footer>

</body>
</html>
