# 222
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Finance | Умные финансовые решения</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* CSS Reset и базовые стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #4361ee;
            --secondary-color: #3a0ca3;
            --accent-color: #4cc9f0;
            --gold-color: #FFD700;
            --text-color: #2b2d42;
            --text-light: #8d99ae;
            --bg-light: #f8f9fa;
            --bg-white: #ffffff;
            --success-color: #4ade80;
            --warning-color: #f59e0b;
            --danger-color: #ef4444;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            --border-radius: 12px;
            --transition: all 0.3s ease;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--bg-light);
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Типография */
        h1, h2, h3, h4 {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            line-height: 1.2;
        }

        h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            color: var(--text-color);
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        p {
            margin-bottom: 1rem;
            color: var(--text-light);
        }

        /* Специальный стиль для дорогого дипсика */
        .special-mention {
            position: relative;
            padding: 20px;
            margin: 30px 0;
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1), rgba(67, 97, 238, 0.1));
            border-radius: var(--border-radius);
            border-left: 4px solid var(--gold-color);
        }

        .special-mention::before {
            content: "💎";
            position: absolute;
            top: -15px;
            left: -15px;
            font-size: 2rem;
            background: white;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: var(--shadow);
        }

        /* Кнопки */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 12px 24px;
            border-radius: var(--border-radius);
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            gap: 8px;
            text-decoration: none;
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: white;
        }

        .btn-primary:hover {
            background-color: var(--secondary-color);
            transform: translateY(-2px);
            box-shadow: var(--shadow);
        }

        .btn-outline {
            background-color: transparent;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }

        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
        }

        .btn-gold {
            background: linear-gradient(135deg, #FFD700, #FFA500);
            color: #333;
            font-weight: 700;
            border: none;
        }

        .btn-gold:hover {
            background: linear-gradient(135deg, #FFA500, #FFD700);
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 10px 20px rgba(255, 215, 0, 0.3);
        }

        .btn-large {
            padding: 16px 32px;
            font-size: 1.1rem;
        }

        .btn-block {
            width: 100%;
        }

        /* Навигация */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .logo i {
            font-size: 1.8rem;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-link {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .nav-link:hover {
            color: var(--primary-color);
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary-color);
            transition: var(--transition);
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .nav-actions {
            display: flex;
            gap: 1rem;
        }

        .hamburger {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-color);
            cursor: pointer;
        }

        /* Герой секция */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, #f5f7ff 0%, #f0f4ff 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 40%;
            height: 100%;
            background: linear-gradient(135deg, rgba(67, 97, 238, 0.1) 0%, rgba(76, 201, 240, 0.1) 100%);
            clip-path: polygon(100% 0, 100% 100%, 0 100%);
        }

        .hero .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-title {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-subtitle {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: var(--text-light);
        }

        .hero-actions {
            display: flex;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .hero-stats {
            display: flex;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .stat-item {
            text-align: center;
        }

        .stat-item h3 {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .stat-item p {
            font-size: 0.9rem;
            color: var(--text-light);
        }

        .hero-image {
            position: relative;
        }

        .hero-image img {
            width: 100%;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .hero-image:hover img {
            transform: scale(1.02);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .image-badge {
            position: absolute;
            bottom: -20px;
            right: -20px;
            background: linear-gradient(135deg, #FFD700, #FFA500);
            color: #333;
            padding: 15px 25px;
            border-radius: 50px;
            font-weight: 700;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            z-index: 2;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        /* Секции */
        section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-subtitle {
            display: inline-block;
            padding: 8px 16px;
            background-color: rgba(67, 97, 238, 0.1);
            color: var(--primary-color);
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .section-title {
            margin-bottom: 1rem;
            color: var(--text-color);
        }

        .section-description {
            max-width: 600px;
            margin: 0 auto;
        }

        /* О нас */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-image {
            position: relative;
        }

        .about-image img {
            width: 100%;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .about-image:hover img {
            transform: scale(1.02);
        }

        .about-text {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .about-item {
            display: flex;
            gap: 1.5rem;
            align-items: flex-start;
        }

        .about-icon {
            width: 60px;
            height: 60px;
            background-color: rgba(67, 97, 238, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            transition: var(--transition);
        }

        .about-icon:hover {
            background-color: var(--primary-color);
            transform: rotate(15deg);
        }

        .about-icon:hover i {
            color: white;
        }

        .about-icon i {
            font-size: 1.5rem;
            color: var(--primary-color);
            transition: var(--transition);
        }

        /* Услуги */
        .services {
            background-color: var(--bg-light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background-color: var(--bg-white);
            padding: 2rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.5s ease;
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .service-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, rgba(67, 97, 238, 0.1), rgba(76, 201, 240, 0.1));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            transform: scale(1.1) rotate(10deg);
        }

        .service-icon i {
            font-size: 1.8rem;
            color: var(--primary-color);
        }

        .service-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            margin-top: 1.5rem;
            transition: var(--transition);
        }

        .service-link:hover {
            gap: 12px;
            color: var(--secondary-color);
        }

        /* Преимущества */
        .features-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .features-text {
            display: flex;
            flex-direction: column;
            gap: 2.5rem;
        }

        .feature-item {
            display: flex;
            gap: 1.5rem;
            align-items: flex-start;
        }

        .feature-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: rgba(67, 97, 238, 0.2);
            line-height: 1;
            transition: var(--transition);
        }

        .feature-item:hover .feature-number {
            color: var(--primary-color);
        }

        .features-image {
            position: relative;
        }

        .features-image img {
            width: 100%;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .features-image:hover img {
            transform: scale(1.02);
        }

        /* Отзывы */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background-color: var(--bg-white);
            padding: 2rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }

        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 4rem;
            color: rgba(67, 97, 238, 0.1);
            font-family: Georgia, serif;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 1.5rem;
            color: var(--text-color);
            position: relative;
            z-index: 1;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .testimonial-author img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary-color);
            padding: 2px;
        }

        .testimonial-author h4 {
            margin-bottom: 0.25rem;
            color: var(--text-color);
        }

        .testimonial-author span {
            font-size: 0.9rem;
            color: var(--text-light);
        }

        /* Контакты */
        .contact {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .contact::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 30%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            clip-path: polygon(100% 0, 100% 100%, 0 100%);
        }

        .contact .section-title,
        .contact .section-description {
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .contact-info {
            margin-top: 2rem;
        }

        .contact-item {
            display: flex;
            gap: 1rem;
            margin-bottom: 1.5rem;
            align-items: flex-start;
        }

        .contact-item i {
            font-size: 1.2rem;
            color: var(--gold-color);
            margin-top: 5px;
        }

        .contact-item h4 {
            margin-bottom: 0.25rem;
            color: white;
        }

        .contact-item p {
            color: rgba(255, 255, 255, 0.9);
        }

        .contact-form {
            background-color: white;
            padding: 2.5rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 16px;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            font-family: 'Inter', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.1);
        }

        /* Футер */
        .footer {
            background-color: #1e293b;
            color: white;
            padding: 80px 0 30px;
            position: relative;
        }

        .footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color), var(--gold-color));
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-col h4 {
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
            color: white;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.75rem;
            display: flex;
            align-items: center;
        }

        .footer-col a {
            color: #cbd5e1;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-col a:hover {
            color: var(--gold-color);
            transform: translateX(5px);
        }

        .footer-col i {
            margin-right: 10px;
            color: var(--accent-color);
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
            font-size: 1.2rem;
        }

        .social-links a:hover {
            background-color: var(--primary-color);
            transform: translateY(-5px) rotate(10deg);
            color: white;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #94a3b8;
            font-size: 0.9rem;
        }

        /* Галерея изображений */
        .gallery-section {
            padding: 80px 0;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .gallery-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 15px;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }

        .gallery-item:hover .gallery-caption {
            transform: translateY(0);
        }

        /* Адаптивность */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .hero .container,
            .about-content,
            .features-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }
            
            .hero {
                padding: 120px 0 80px;
            }
            
            section {
                padding: 80px 0;
            }
            
            .hero-stats {
                justify-content: center;
            }
            
            .image-badge {
                right: 20px;
            }
        }

        @media (max-width: 768px) {
            .nav-menu,
            .nav-actions {
                display: none;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero-title {
                font-size: 2rem;
            }
            
            .hero-actions {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
                justify-content: center;
            }
            
            .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 576px) {
            .container {
                padding: 0 15px;
            }
            
            .hero-title {
                font-size: 1.8rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .hero-stats {
                flex-direction: column;
                gap: 1.5rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
            }
            
            .image-badge {
                position: relative;
                bottom: auto;
                right: auto;
                margin-top: 20px;
                width: 100%;
                text-align: center;
            }
        }

        /* Анимации */
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

        .hero-content,
        .about-content,
        .services-grid,
        .features-content,
        .testimonials-grid,
        .contact-content,
        .gallery-grid {
            animation: fadeInUp 0.8s ease-out;
        }

        /* Дополнительные украшения */
        .floating-element {
            position: absolute;
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, rgba(67, 97, 238, 0.1), rgba(76, 201, 240, 0.1));
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            animation: float 6s ease-in-out infinite;
            z-index: 0;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .floating-1 {
            top: 20%;
            left: 5%;
            width: 80px;
            height: 80px;
        }

        .floating-2 {
            bottom: 20%;
            right: 5%;
            width: 60px;
            height: 60px;
            animation-delay: 2s;
        }

        /* Декоративные разделители */
        .section-divider {
            height: 3px;
            width: 100px;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color), var(--gold-color));
            margin: 40px auto;
            border-radius: 3px;
        }
    </style>
</head>
<body>
    <!-- Навигация -->
    <header class="header">
        <nav class="navbar container">
            <a href="#" class="logo">
                <i class="fas fa-chart-line"></i>
                <span>DigitalFinance</span>
            </a>
            
            <ul class="nav-menu">
                <li><a href="#home" class="nav-link">Главная</a></li>
                <li><a href="#about" class="nav-link">О нас</a></li>
                <li><a href="#services" class="nav-link">Услуги</a></li>
                <li><a href="#gallery" class="nav-link">Галерея</a></li>
                <li><a href="#features" class="nav-link">Преимущества</a></li>
                <li><a href="#contact" class="nav-link">Контакты</a></li>
            </ul>
            
            <div class="nav-actions">
                <button class="btn btn-outline">Вход</button>
                <button class="btn btn-primary">Регистрация</button>
            </div>
            
            <button class="hamburger" id="hamburger">
                <i class="fas fa-bars"></i>
            </button>
        </nav>
    </header>

    <!-- Декоративные элементы -->
    <div class="floating-element floating-1"></div>
    <div class="floating-element floating-2"></div>

    <!-- Главный баннер (Экран 1) -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="special-mention">
                    <h3 style="color: var(--gold-color); margin-bottom: 10px;">✨ Специально для дорогого дипсика! ✨</h3>
                    <p style="color: #333; margin: 0;">Самый красивый и современный финансовый лендинг с роскошными картинками!</p>
                </div>
                
                <h1 class="hero-title">Премиальные финансовые решения для успешных людей</h1>
                <p class="hero-subtitle">Элитный сервис финансового консалтинга с индивидуальным подходом к каждому клиенту. Мы создаем стратегии, которые работают.</p>
                <div class="hero-actions">
                    <button class="btn btn-primary btn-large">
                        <i class="fas fa-crown"></i> Премиум консультация
                    </button>
                    <button class="btn btn-gold btn-large">
                        <i class="fas fa-gem"></i> VIP доступ
                    </button>
                </div>
                <div class="hero-stats">
                    <div class="stat-item">
                        <h3>99%</h3>
                        <p>Удовлетворенных клиентов</p>
                    </div>
                    <div class="stat-item">
                        <h3>10+</h3>
                        <p>Лет опыта</p>
                    </div>
                    <div class="stat-item">
                        <h3>24/7</h3>
                        <p>Персональная поддержка</p>
                    </div>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Роскошный финансовый офис">
                <div class="image-badge">⭐ Премиум сервис</div>
            </div>
        </div>
    </section>

    <!-- О нас (Экран 2) -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-header">
                <span class="section-subtitle">Элитный сервис</span>
                <h2 class="section-title">Почему выбирают нас?</h2>
                <p class="section-description">Мы создаем эксклюзивные финансовые решения для избранных клиентов</p>
            </div>
            
            <div class="about-content">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1551836026-d5c2c7615f07?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Роскошный интерьер офиса">
                </div>
                <div class="about-text">
                    <div class="about-item">
                        <div class="about-icon">
                            <i class="fas fa-gem"></i>
                        </div>
                        <div>
                            <h3>Эксклюзивность</h3>
                            <p>Работаем только с избранными клиентами, обеспечивая максимальное внимание к деталям.</p>
                        </div>
                    </div>
                    
                    <div class="about-item">
                        <div class="about-icon">
                            <i class="fas fa-user-tie"></i>
                        </div>
                        <div>
                            <h3>Персональный менеджер</h3>
                            <p>Каждый клиент получает персонального финансового советника высшего уровня.</p>
                        </div>
                    </div>
                    
                    <div class="about-item">
                        <div class="about-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <div>
                            <h3>Абсолютная конфиденциальность</h3>
                            <p>Ваши финансовые данные защищены по высшим стандартам безопасности.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Услуги (Экран 3) -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-header">
                <span class="section-subtitle">Наши услуги</span>
                <h2 class="section-title">Эксклюзивные предложения</h2>
                <p class="section-description">Премиальные финансовые услуги для состоятельных клиентов</p>
            </div>
            
            <div class="services-grid">
                <article class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <h3>Управление капиталом</h3>
                    <p>Индивидуальные стратегии управления капиталом с фокусом на сохранение и приумножение активов.</p>
                    <a href="#" class="service-link">Подробнее <i class="fas fa-arrow-right"></i></a>
                </article>
                
                <article class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-globe-europe"></i>
                    </div>
                    <h3>Международные инвестиции</h3>
                    <p>Доступ к эксклюзивным международным инвестиционным возможностям и рынкам.</p>
                    <a href="#" class="service-link">Подробнее <i class="fas fa-arrow-right"></i></a>
                </article>
                
                <article class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <h3>Управление недвижимостью</h3>
                    <p>Комплексное управление портфелем недвижимости по всему миру.</p>
                    <a href="#" class="service-link">Подробнее <i class="fas fa-arrow-right"></i></a>
                </article>
                
                <article class="service-card">
                    <div class="service-icon">
                        <i class="
