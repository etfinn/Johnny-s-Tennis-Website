<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tennis Lessons | Professional Coaching</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Karla:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --court-green: #2d5016;
            --tennis-yellow: #d4ff00;
            --clay-orange: #e85d04;
            --white: #ffffff;
            --off-white: #fafafa;
            --dark: #1a1a1a;
            --gray: #666666;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Karla', sans-serif;
            color: var(--dark);
            background: var(--off-white);
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
        }

        .logo {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2rem;
            color: var(--court-green);
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links li {
            color: var(--dark);
            font-weight: 600;
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            height: 90vh;
            background: linear-gradient(135deg, var(--court-green) 0%, #1a3a0f 100%);
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            padding: 0 5%;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 70%;
            height: 200%;
            background: radial-gradient(circle, rgba(212, 255, 0, 0.15) 0%, transparent 70%);
            animation: pulse 8s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1) rotate(0deg); opacity: 0.3; }
            50% { transform: scale(1.1) rotate(10deg); opacity: 0.5; }
        }

        .hero-content {
            max-width: 700px;
            z-index: 2;
            animation: slideInLeft 1s ease-out;
        }

        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .hero h1 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 4rem;
            color: var(--white);
            line-height: 0.9;
            margin-bottom: 1.5rem;
            letter-spacing: 3px;
        }

        .hero h1 span {
            color: var(--tennis-yellow);
            display: block;
            font-size: 7.5rem;
        }

        .hero p {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.3rem;
            margin-bottom: 2.5rem;
            line-height: 1.6;
        }

        .cta-button {
            display: inline-block;
            background: var(--tennis-yellow);
            color: var(--dark);
            padding: 1.2rem 3rem;
            font-weight: 600;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-radius: 2px;
            border: none;
            font-family: 'Karla', sans-serif;
            box-shadow: 0 10px 30px rgba(212, 255, 0, 0.3);
        }

        /* About Section */
        .about {
            padding: 8rem 5%;
            background: var(--white);
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .about-content h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 4rem;
            color: var(--court-green);
            margin-bottom: 1.5rem;
            letter-spacing: 2px;
        }

        .about-content p {
            font-size: 1.15rem;
            line-height: 1.8;
            color: var(--gray);
            margin-bottom: 1.5rem;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .stat {
            text-align: center;
            padding: 2rem;
            background: var(--off-white);
            border-left: 4px solid var(--tennis-yellow);
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .stat-number {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 3.5rem;
            color: var(--court-green);
            line-height: 1;
        }

        .stat-label {
            font-size: 0.9rem;
            text-transform: uppercase;
            color: var(--gray);
            margin-top: 0.5rem;
            letter-spacing: 1px;
        }

        .about-visual {
            position: relative;
            height: 500px;
            background: linear-gradient(45deg, var(--tennis-yellow), var(--clay-orange));
            border-radius: 4px;
            overflow: hidden;
        }

        .about-visual::before {
            content: '🎾';
            position: absolute;
            font-size: 20rem;
            opacity: 0.2;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
        }

        /* Services Section */
        .services {
            padding: 8rem 5%;
            background: var(--off-white);
        }

        .section-header {
            text-align: center;
            margin-bottom: 5rem;
        }

        .section-header h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 5rem;
            color: var(--court-green);
            letter-spacing: 3px;
        }

        .section-header p {
            font-size: 1.2rem;
            color: var(--gray);
            margin-top: 1rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }

        .service-card {
            background: var(--white);
            padding: 3rem 2.5rem;
            border-radius: 4px;
            position: relative;
            overflow: hidden;
            transition: all 0.4s;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--tennis-yellow), var(--clay-orange));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.4s;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.1);
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }

        .service-card h3 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2rem;
            color: var(--court-green);
            margin-bottom: 1rem;
            letter-spacing: 1px;
        }

        .service-card p {
            color: var(--gray);
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        .service-price {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2.5rem;
            color: var(--clay-orange);
            margin-top: 1rem;
        }

        /* Contact Section */
        .contact {
            padding: 8rem 5%;
            background: var(--court-green);
            color: var(--white);
            text-align: center;
        }

        .contact h2 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 5rem;
            margin-bottom: 2rem;
            letter-spacing: 3px;
        }

        .contact p {
            font-size: 1.3rem;
            margin-bottom: 3rem;
            opacity: 0.9;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 4rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .contact-item {
            text-align: center;
        }

        .contact-icon {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }

        .contact-item h3 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.8rem;
            margin-bottom: 1rem;
            letter-spacing: 1px;
        }

        .contact-item p {
            color: var(--tennis-yellow);
            font-size: 1.3rem;
            font-weight: 600;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: var(--white);
            padding: 3rem 5%;
            text-align: center;
        }

        footer p {
            opacity: 0.7;
            font-size: 0.95rem;
        }

        .social-links {
            margin-top: 1.5rem;
            display: flex;
            justify-content: center;
            gap: 2rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 3.5rem;
            }

            .hero h1 span {
                font-size: 4.5rem;
            }

            .about {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            .stats {
                grid-template-columns: 1fr;
            }

            .section-header h2 {
                font-size: 3rem;
            }

            .contact h2 {
                font-size: 3rem;
            }

            .contact-info {
                flex-direction: column;
                gap: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="logo">Tennis Lessons with Johnny</div>
        <ul class="nav-links">
            <li>Home</li>
            <li>About</li>
            <li>Services</li>
            <li>Contact</li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>
                Equip yourself with the
                <span>Finnie</span>
                difference
            </h1>
            <p>My name is Johnny Finnie. I will provide you with professional tennis coaching tailored to your goals. From beginners to advanced players, unlock your full potential on the court.</p>
            <button class="cta-button">Book a Lesson Today!</button>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="about-content">
            <h2>About Your Coach</h2>
            <p>With years of experience on the court and a passion for teaching, I'm dedicated to helping players of all levels improve their game. Whether you're picking up a racket for the first time or looking to compete at a higher level, I'll create a personalized training program that fits your goals.</p>
            <p>My coaching philosophy focuses on building strong fundamentals, developing strategic thinking, and fostering a love for the game that lasts a lifetime.</p>
            <p>Located at 10516 Conway Road, I will give you a personal approach to growing your tennis game.</p>
            
            <div class="stats">
                <div class="stat">
                    <div class="stat-number">2+</div>
                    <div class="stat-label">Years of Coaching Experience</div>
                </div>
                <div class="stat">
                    <div class="stat-number">100+</div>
                    <div class="stat-label">Students Coached</div>
                </div>
                <div class="stat">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Dedication</div>
                </div>
            </div>
        </div>
        <div class="about-visual"></div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="section-header">
            <h2>Coaching Programs</h2>
            <p>Customized lessons designed to match your skill level and ambitions</p>
        </div>

        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">👤</div>
                <h3>Private Lessons</h3>
                <p>One-on-one coaching sessions focused entirely on your development. Perfect for rapid improvement and personalized attention.</p>
                <div class="service-price">$40/hr</div>
            </div>

            <div class="service-card">
                <div class="service-icon">👥</div>
                <h3>Group Lessons</h3>
                <p>Train with others at your level. Great for building consistency, competitive spirit, and making tennis friends.</p>
                <div class="service-price">$20/hr</div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Get In Touch</h2>
        <p>Ready to elevate your game? Reach out to book your lesson today</p>

        <div class="contact-info">
            <div class="contact-item">
                <div class="contact-icon">📱</div>
                <h3>Phone</h3>
                <p>314-346-8680</p>
            </div>

            <div class="contact-item">
                <div class="contact-icon">📧</div>
                <h3>Email</h3>
                <p>johnsfinnie@icloud.com</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
        </div>
    </footer>

    <script>
        // Animate stats on scroll
        const observerOptions = {
            threshold: 0.5,
            rootMargin: '0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationPlayState = 'running';
