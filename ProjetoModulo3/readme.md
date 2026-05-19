<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

<!-- Font Awesome (Ícones) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- Animate on Scroll Library -->
<script src="https://unpkg.com/scrollreveal"></script>

<style>
    /* --- VARIÁVEIS E RESET --- */
    :root {
        --primary-color: #D4AF37; /* Dourado */
        --secondary-color: #1a1a1a; /* Preto Suave */
        --bg-dark: #0a0a0a; /* Preto Profundo */
        --text-light: #ffffff;
        --text-gray: #b0b0b0;
        --transition: all 0.3s ease;
    }

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        text-decoration: none;
        list-style: none;
        scroll-behavior: smooth;
    }

    body {
        font-family: 'Montserrat', sans-serif;
        background-color: var(--bg-dark);
        color: var(--text-light);
        line-height: 1.6;
        overflow-x: hidden;
    }

    h1, h2, h3 {
        font-family: 'Playfair Display', serif;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .btn {
        display: inline-block;
        padding: 15px 35px;
        background-color: var(--primary-color);
        color: #000;
        font-weight: bold;
        border-radius: 5px;
        transition: var(--transition);
        border: 2px solid var(--primary-color);
        text-transform: uppercase;
        letter-spacing: 1px;
        cursor: pointer;
    }

    .btn:hover {
        background-color: transparent;
        color: var(--primary-color);
    }

    section {
        padding: 100px 0;
    }

    .section-title {
        text-align: center;
        margin-bottom: 60px;
    }

    .section-title h2 {
        font-size: 2.5rem;
        color: var(--primary-color);
    }

    .section-title span {
        display: block;
        font-size: 0.9rem;
        text-transform: uppercase;
        letter-spacing: 3px;
        color: var(--text-gray);
        margin-bottom: 10px;
    }

    /* --- HEADER & NAV --- */
    header {
        position: fixed;
        top: 0;
        width: 100%;
        z-index: 1000;
        padding: 20px 0;
        transition: var(--transition);
    }

    header.scrolled {
        background: rgba(0, 0, 0, 0.95);
        padding: 15px 0;
        border-bottom: 1px solid var(--primary-color);
    }

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        font-family: 'Playfair Display', serif;
        font-size: 1.8rem;
        font-weight: bold;
        color: var(--primary-color);
    }

    .nav-links {
        display: flex;
        gap: 30px;
    }

    .nav-links a {
        color: var(--text-light);
        font-size: 0.9rem;
        font-weight: 500;
        transition: var(--transition);
    }

    .nav-links a:hover {
        color: var(--primary-color);
    }

    .mobile-menu-icon {
        display: none;
        font-size: 1.8rem;
        color: var(--primary-color);
        cursor: pointer;
    }

    /* --- HERO SECTION --- */
    .hero {
        height: 100vh;
        background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                    url('https://images.unsplash.com/photo-1503951914875-452162b0f3f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
        background-size: cover;
        background-position: center;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
    }

    .hero-content h1 {
        font-size: 4rem;
        margin-bottom: 20px;
        letter-spacing: 2px;
    }

    .hero-content p {
        font-size: 1.2rem;
        margin-bottom: 35px;
        color: var(--text-gray);
    }

    /* --- SOBRE NÓS --- */
    .about-flex {
        display: flex;
        align-items: center;
        gap: 50px;
    }

    .about-img img {
        width: 100%;
        border-radius: 10px;
        border-bottom: 10px solid var(--primary-color);
        border-right: 10px solid var(--primary-color);
    }

    .about-text h3 {
        font-size: 2rem;
        margin-bottom: 20px;
        color: var(--primary-color);
    }

    .about-text p {
        margin-bottom: 20px;
        color: var(--text-gray);
    }

    /* --- SERVIÇOS --- */
    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
    }

    .service-card {
        background: var(--secondary-color);
        padding: 40px 30px;
        text-align: center;
        border-radius: 10px;
        transition: var(--transition);
        border: 1px solid #333;
    }

    .service-card:hover {
        transform: translateY(-10px);
        border-color: var(--primary-color);
    }

    .service-card i {
        font-size: 3rem;
        color: var(--primary-color);
        margin-bottom: 20px;
    }

    .service-card h3 {
        margin-bottom: 15px;
        font-size: 1.5rem;
    }

    .price {
        font-size: 1.8rem;
        font-weight: bold;
        color: var(--primary-color);
        display: block;
        margin-top: 15px;
    }

    /* --- GALERIA --- */
    .gallery-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 15px;
    }

    .gallery-item {
        height: 300px;
        overflow: hidden;
        border-radius: 5px;
    }

    .gallery-item img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: var(--transition);
        filter: grayscale(100%);
    }

    .gallery-item:hover img {
        transform: scale(1.1);
        filter: grayscale(0%);
    }

    /* --- DEPOIMENTOS --- */
    .testimonials-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
    }

    .testimonial-card {
        background: #111;
        padding: 30px;
        border-left: 4px solid var(--primary-color);
    }

    .testimonial-card p {
        font-style: italic;
        margin-bottom: 20px;
    }

    .client-name {
        font-weight: bold;
        color: var(--primary-color);
    }

    .stars {
        color: var(--primary-color);
        margin-bottom: 10px;
    }

    /* --- LOCALIZAÇÃO E CONTATO --- */
    .contact-flex {
        display: flex;
        flex-wrap: wrap;
        gap: 50px;
    }

    .contact-info {
        flex: 1;
        min-width: 300px;
    }

    .map-container {
        flex: 1;
        min-width: 300px;
        height: 400px;
    }

    .contact-item {
        display: flex;
        align-items: center;
        gap: 20px;
        margin-bottom: 30px;
    }

    .contact-item i {
        font-size: 1.5rem;
        color: var(--primary-color);
    }

    .social-links {
        display: flex;
        gap: 20px;
        margin-top: 30px;
    }

    .social-links a {
        font-size: 1.8rem;
        color: var(--text-light);
        transition: var(--transition);
    }

    .social-links a:hover {
        color: var(--primary-color);
    }

    /* --- WHATSAPP FIXO --- */
    .whatsapp-float {
        position: fixed;
        bottom: 30px;
        right: 30px;
        background-color: #25d366;
        color: #FFF;
        width: 60px;
        height: 60px;
        border-radius: 50px;
        text-align: center;
        font-size: 35px;
        box-shadow: 2px 2px 3px #999;
        z-index: 1000;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    /* --- FOOTER --- */
    footer {
        padding: 50px 0;
        text-align: center;
        border-top: 1px solid #333;
        background-color: #000;
    }

    /* --- RESPONSIVIDADE --- */
    @media (max-width: 768px) {
        .nav-links {
            display: none; /* Seria necessário JS para menu mobile completo */
        }

        .mobile-menu-icon {
            display: block;
        }

        .hero-content h1 {
            font-size: 2.5rem;
        }

        .about-flex {
            flex-direction: column;
        }

        .section-title h2 {
            font-size: 2rem;
        }
    }
</style>
