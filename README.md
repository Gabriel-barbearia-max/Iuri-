<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Biel Barbearia | Cortes Masculinos Premium</title>
  <meta name="description" content="Barbearia premium especializada em cortes masculinos, tratamentos de barba e cuidados capilares. Agende seu horário!">
  <meta name="keywords" content="barbearia, corte masculino, barba, tratamento capilar">
  <meta name="author" content="Biel Barbearia">
  
  <!-- Meta Redes Sociais -->
  <meta property="og:title" content="Biel Barbearia | Cortes Premium">
  <meta property="og:description" content="Cortes premium e serviços especializados para cuidados masculinos.">
  <meta property="og:image" content="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80">
  <meta property="og:url" content="https://www.bielbarbearia.com">
  <meta property="og:type" content="website">
  <meta property="og:locale" content="pt_BR">
  
  <!-- Favicon -->
  <link rel="icon" type="image/x-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>✂️</text></svg>">
  
  <!-- Fontes -->
  <link rel="preload" href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Playfair+Display:wght@400;700&display=swap" as="style" onload="this.onload=null;this.rel='stylesheet'">
  <noscript><link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Playfair+Display:wght@400;700&display=swap"></noscript>
  
  <style>
    /* VARIÁVEIS E CONFIGURAÇÕES GLOBAIS */
    :root {
      --primary: #0a0a0a;
      --secondary: #1a1a1a;
      --accent: #d4af37;
      --accent-hover: #e6c350;
      --text: #f5f5f5;
      --text-muted: #b0b0b0;
      --card-bg: rgba(26, 26, 26, 0.9);
      --card-border: rgba(212, 175, 55, 0.2);
      --header-height: 80px;
      --border-radius: 12px;
      --transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
      -webkit-tap-highlight-color: transparent;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--primary);
      color: var(--text);
      line-height: 1.6;
      font-size: 16px;
      min-height: 100vh;
      overflow-x: hidden;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 4%;
    }

    /* ELEMENTOS FLUTUANTES */
    .back-to-top {
      position: fixed;
      right: 20px;
      bottom: 85px;
      width: 55px;
      height: 55px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
      transition: var(--transition);
      background: var(--accent);
      color: var(--primary);
      font-size: 18px;
      box-shadow: 0 4px 15px rgba(212, 175, 55, 0.4);
      opacity: 0;
      visibility: hidden;
      cursor: pointer;
      border: none;
    }

    .back-to-top.visible {
      opacity: 1;
      visibility: visible;
    }

    .back-to-top:hover {
      transform: scale(1.1);
      background: var(--accent-hover);
    }

    /* CABEÇALHO */
    header {
      background: rgba(10, 10, 10, 0.95);
      backdrop-filter: blur(10px);
      padding: 15px 0;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 20px rgba(0, 0, 0, 0.4);
      height: var(--header-height);
      border-bottom: 1px solid var(--card-border);
      transition: var(--transition);
    }

    header.scrolled {
      height: 70px;
      padding: 10px 0;
    }

    header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-img {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      border: 2px solid var(--accent);
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--accent);
      color: var(--primary);
      font-size: 22px;
      box-shadow: 0 0 15px rgba(212, 175, 55, 0.5);
    }

    .logo h1 {
      font-size: 24px;
      font-weight: 800;
      color: var(--accent);
      font-family: 'Playfair Display', serif;
      letter-spacing: 1px;
    }

    /* NAVEGAÇÃO */
    nav {
      display: flex;
      gap: 20px;
      align-items: center;
    }

    nav a {
      color: var(--text);
      text-decoration: none;
      font-weight: 600;
      transition: var(--transition);
      font-size: 15px;
      padding: 8px 16px;
      border-radius: 5px;
      position: relative;
    }

    nav a:after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: 0;
      left: 50%;
      background: var(--accent);
      transition: var(--transition);
      transform: translateX(-50%);
    }

    nav a:hover {
      color: var(--accent);
    }

    nav a:hover:after {
      width: 80%;
    }

    /* MENU MÓVEL */
    .menu-toggle {
      display: none;
      flex-direction: column;
      justify-content: space-around;
      width: 30px;
      height: 24px;
      background: transparent;
      border: none;
      cursor: pointer;
      padding: 0;
    }

    .menu-toggle span {
      width: 100%;
      height: 3px;
      background-color: var(--accent);
      border-radius: 5px;
      transition: var(--transition);
    }

    /* SEÇÃO HERO */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 100px 0 60px;
      background: linear-gradient(rgba(10, 10, 10, 0.85), rgba(26, 26, 26, 0.9)), url('https://images.unsplash.com/photo-1585747860715-2ba37e788b70?ixlib=rb-4.0.3&auto=format&fit=crop&w=1476&q=80');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      text-align: center;
      position: relative;
      overflow: hidden;
    }

    .hero:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at 30% 50%, rgba(212, 175, 55, 0.1) 0%, transparent 50%);
    }

    .hero-content {
      width: 100%;
      max-width: 900px;
      margin: 0 auto;
      padding: 0 15px;
      position: relative;
      z-index: 1;
    }

    .hero-content h2 {
      font-size: clamp(2.2rem, 6vw, 3.5rem);
      margin-bottom: 20px;
      color: var(--accent);
      font-weight: 800;
      line-height: 1.1;
      font-family: 'Playfair Display', serif;
      text-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }

    .hero-content p {
      font-size: clamp(1.1rem, 3vw, 1.3rem);
      margin-bottom: 35px;
      opacity: 0.9;
      color: var(--text-muted);
      max-width: 700px;
      margin-left: auto;
      margin-right: auto;
    }

    .hero-buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
      margin: 40px 0 25px;
      justify-content: center;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 16px 28px;
      text-decoration: none;
      border-radius: 50px;
      font-weight: 700;
      transition: var(--transition);
      box-shadow: 0 4px 15px rgba(0,0,0,0.4);
      border: none;
      cursor: pointer;
      font-size: clamp(15px, 3vw, 17px);
      min-height: 50px;
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }

    .primary-btn {
      background: var(--accent);
      color: var(--primary);
    }

    .secondary-btn {
      background: transparent;
      color: var(--text);
      border: 2px solid var(--accent);
    }

    .btn:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 25px rgba(0,0,0,0.6);
    }

    .primary-btn:hover {
      background: var(--accent-hover);
    }

    .secondary-btn:hover {
      background: var(--accent);
      color: var(--primary);
    }

    /* DESTAQUES */
    .highlights {
      padding: 80px 0;
      background: var(--secondary);
    }

    .section-title {
      text-align: center;
      font-size: clamp(1.8rem, 5vw, 2.5rem);
      margin-bottom: 50px;
      color: var(--accent);
      font-weight: 700;
      font-family: 'Playfair Display', serif;
      position: relative;
    }

    .section-title:after {
      content: '';
      position: absolute;
      width: 80px;
      height: 3px;
      background: var(--accent);
      bottom: -15px;
      left: 50%;
      transform: translateX(-50%);
    }

    .highlights-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .highlight {
      text-align: center;
      padding: 30px 20px;
      background: var(--card-bg);
      border-radius: var(--border-radius);
      backdrop-filter: blur(10px);
      border: 1px solid var(--card-border);
      transition: var(--transition);
      position: relative;
      overflow: hidden;
    }

    .highlight:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 4px;
      background: var(--accent);
      transform: scaleX(0);
      transition: transform 0.3s;
    }

    .highlight:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.3);
    }

    .highlight:hover:before {
      transform: scaleX(1);
    }

    .highlight i {
      font-size: clamp(32px, 8vw, 40px);
      color: var(--accent);
      margin-bottom: 20px;
    }

    .highlight h4 {
      margin-bottom: 15px;
      color: var(--accent);
      font-size: clamp(1.1rem, 3vw, 1.2rem);
      font-weight: 700;
    }

    .highlight p {
      opacity: 0.9;
      line-height: 1.6;
      font-size: clamp(0.9rem, 2.5vw, 1rem);
      color: var(--text-muted);
    }

    /* SERVIÇOS */
    .services {
      padding: 80px 0;
      background: var(--primary);
      position: relative;
    }

    .services:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at 70% 30%, rgba(212, 175, 55, 0.05) 0%, transparent 50%);
    }

    .services-container {
      position: relative;
      z-index: 1;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 25px;
    }

    .service-card {
      background: var(--card-bg);
      border-radius: var(--border-radius);
      overflow: hidden;
      border: 1px solid var(--card-border);
      transition: var(--transition);
      position: relative;
    }

    .service-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.3);
    }

    .service-img {
      width: 100%;
      height: 200px;
      overflow: hidden;
    }

    .service-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s;
    }

    .service-card:hover .service-img img {
      transform: scale(1.1);
    }

    .service-content {
      padding: 25px;
    }

    .service-content h3 {
      font-size: 1.4rem;
      margin-bottom: 15px;
      color: var(--accent);
      font-weight: 700;
    }

    .service-content p {
      color: var(--text-muted);
      margin-bottom: 20px;
      line-height: 1.6;
    }

    .service-features {
      list-style: none;
      margin-bottom: 25px;
    }

    .service-features li {
      margin-bottom: 8px;
      padding-left: 25px;
      position: relative;
      color: var(--text);
    }

    .service-features li:before {
      content: "✓";
      color: var(--accent);
      position: absolute;
      left: 0;
      font-weight: bold;
      font-size: 1.1rem;
    }

    .service-btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 12px 24px;
      background: var(--accent);
      color: var(--primary);
      text-decoration: none;
      border-radius: 50px;
      font-weight: 600;
      transition: var(--transition);
      box-shadow: 0 4px 12px rgba(212, 175, 55, 0.4);
      font-size: 0.9rem;
      min-height: 44px;
    }

    .service-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 18px rgba(212, 175, 55, 0.6);
      background: var(--accent-hover);
    }

    /* SOBRE */
    .about {
      padding: 80px 0;
      background: var(--primary);
    }

    .about-content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      align-items: center;
    }

    .about-text h3 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: var(--accent);
      font-family: 'Playfair Display', serif;
    }

    .about-text p {
      color: var(--text-muted);
      margin-bottom: 25px;
      line-height: 1.7;
    }

    .about-stats {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
      margin-top: 30px;
    }

    .stat {
      text-align: center;
      padding: 20px;
      background: var(--card-bg);
      border-radius: 10px;
      border: 1px solid var(--card-border);
    }

    .stat-number {
      font-size: 2.5rem;
      font-weight: 800;
      color: var(--accent);
      margin-bottom: 5px;
    }

    .stat-label {
      font-size: 0.9rem;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .about-image {
      border-radius: var(--border-radius);
      overflow: hidden;
      box-shadow: 0 15px 30px rgba(0,0,0,0.3);
    }

    .about-image img {
      width: 100%;
      height: auto;
      display: block;
    }

    /* CONTATO */
    .contact {
      padding: 80px 0;
      background: var(--primary);
      text-align: center;
    }

    .contact-container {
      max-width: 800px;
      margin: 0 auto;
    }

    .contact-form {
      background: var(--card-bg);
      padding: 40px;
      border-radius: var(--border-radius);
      border: 1px solid var(--card-border);
      margin-top: 40px;
      text-align: left;
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
      margin-bottom: 8px;
      color: var(--accent);
      font-weight: 600;
    }

    .form-control {
      width: 100%;
      padding: 12px 15px;
      background: rgba(255,255,255,0.05);
      border: 1px solid var(--card-border);
      border-radius: 8px;
      color: var(--text);
      font-size: 1rem;
      transition: var(--transition);
    }

    .form-control:focus {
      outline: none;
      border-color: var(--accent);
      box-shadow: 0 0 0 2px rgba(212, 175, 55, 0.2);
    }

    textarea.form-control {
      min-height: 120px;
      resize: vertical;
    }

    .submit-btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 14px 30px;
      background: var(--accent);
      color: var(--primary);
      border: none;
      border-radius: 50px;
      font-weight: 700;
      transition: var(--transition);
      box-shadow: 0 4px 15px rgba(212, 175, 55, 0.4);
      font-size: 1rem;
      cursor: pointer;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .submit-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(212, 175, 55, 0.6);
      background: var(--accent-hover);
    }

    .contact-info {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      margin-top: 40px;
    }

    .contact-card {
      background: var(--card-bg);
      padding: 30px;
      border-radius: var(--border-radius);
      border: 1px solid var(--card-border);
      transition: var(--transition);
    }

    .contact-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    .contact-card i {
      font-size: 2rem;
      color: var(--accent);
      margin-bottom: 15px;
    }

    .contact-card h4 {
      margin-bottom: 10px;
      color: var(--accent);
    }

    .contact-card p {
      color: var(--text-muted);
    }

    /* RODAPÉ */
    footer {
      background: #050505;
      padding: 60px 0 20px;
      border-top: 1px solid var(--card-border);
    }

    .footer-content {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      gap: 30px;
      margin-bottom: 40px;
      align-items: start;
    }

    .footer-logo {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    .footer-logo .logo {
      justify-content: flex-start;
    }

    .footer-logo p {
      color: var(--text-muted);
      line-height: 1.6;
    }

    .footer-contact {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    .footer-contact h4 {
      color: var(--accent);
      margin-bottom: 10px;
      font-size: 1.2rem;
    }

    .footer-contact p {
      display: flex;
      align-items: center;
      gap: 10px;
      color: var(--text-muted);
      margin-bottom: 8px;
    }

    .footer-social {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    .footer-social h4 {
      color: var(--accent);
      margin-bottom: 10px;
      font-size: 1.2rem;
    }

    .social-links {
      display: flex;
      gap: 15px;
    }

    .social-link {
      width: 45px;
      height: 45px;
      background: var(--card-bg);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text);
      text-decoration: none;
      transition: var(--transition);
      font-size: 1.1rem;
      border: 1px solid var(--card-border);
    }

    .social-link:hover {
      background: var(--accent);
      color: var(--primary);
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(212, 175, 55, 0.4);
    }

    .footer-bottom {
      text-align: center;
      padding-top: 20px;
      border-top: 1px solid rgba(255,255,255,0.1);
    }

    .footer-bottom p {
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    /* ANIMAÇÕES E RESPONSIVIDADE */
    section {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.8s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    @media (max-width: 1024px) {
      .footer-content {
        grid-template-columns: 1fr 1fr;
        gap: 30px;
      }
      
      .footer-logo {
        grid-column: span 2;
      }
      
      .about-content {
        grid-template-columns: 1fr;
        gap: 40px;
      }
      
      .about-image {
        order: -1;
      }
    }

    @media (max-width: 768px) {
      .hero {
        padding: 120px 0 60px;
      }
      
      .hero-buttons {
        flex-direction: column;
        align-items: center;
      }
      
      .btn {
        width: 100%;
        max-width: 300px;
        justify-content: center;
      }
      
      .section-title {
        margin-bottom: 40px;
      }
      
      .footer-content {
        grid-template-columns: 1fr;
        gap: 30px;
      }
      
      .footer-logo {
        grid-column: span 1;
      }
      
      .contact-form {
        padding: 25px;
      }
      
      /* Menu móvel */
      .menu-toggle {
        display: flex;
      }
      
      nav {
        position: fixed;
        top: 80px;
        left: 0;
        width: 100%;
        background: rgba(10, 10, 10, 0.98);
        flex-direction: column;
        padding: 30px;
        gap: 20px;
        transform: translateY(-100%);
        opacity: 0;
        visibility: hidden;
        transition: var(--transition);
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        backdrop-filter: blur(10px);
      }
      
      nav.active {
        transform: translateY(0);
        opacity: 1;
        visibility: visible;
      }
      
      .highlights-grid {
        grid-template-columns: 1fr;
        gap: 20px;
      }
      
      .services-grid {
        grid-template-columns: 1fr;
        gap: 20px;
      }
    }

    @media (max-width: 480px) {
      .hero {
        min-height: 90vh;
        padding: 100px 0 40px;
      }
      
      .footer-content {
        gap: 25px;
      }
      
      .about-stats {
        grid-template-columns: 1fr;
      }
      
      .contact-info {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <!-- Botão Voltar ao topo -->
  <button class="back-to-top" aria-label="Voltar ao topo">
    <i class="fas fa-arrow-up"></i>
  </button>

  <!-- Header -->
  <header id="header">
    <div class="container">
      <div class="logo">
        <div class="logo-img">
          <i class="fas fa-scissors"></i>
        </div>
        <h1>BIEL BARBEARIA</h1>
      </div>
      <button class="menu-toggle" aria-label="Abrir menu">
        <span></span>
        <span></span>
        <span></span>
      </button>
      <nav>
        <a href="#servicos">Serviços</a>
        <a href="#sobre">Sobre</a>
        <a href="#contato">Contato</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="hero">
    <div class="container">
      <div class="hero-content">
        <h2>EXPERIÊNCIA MASCULINA PREMIUM</h2>
        <p>Descubra a excelência em cortes masculinos e cuidados capilares. Uma experiência única de barbearia.</p>
        <div class="hero-buttons">
          <button class="btn primary-btn">
            <i class="fas fa-calendar-alt"></i> Agendar Horário
          </button>
          <button class="btn secondary-btn">
            <i class="fas fa-map-marker-alt"></i> Localização
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- Destaques -->
  <section class="highlights">
    <div class="container">
      <h2 class="section-title">Por Que Escolher a Biel?</h2>
      <div class="highlights-grid">
        <div class="highlight">
          <i class="fas fa-cut"></i>
          <h4>Cortes Precision</h4>
          <p>Técnicas avançadas para resultados impecáveis que valorizam seu estilo único.</p>
        </div>
        <div class="highlight">
          <i class="fas fa-user-tie"></i>
          <h4>Profissionais Experts</h4>
          <p>Barbeiros especializados com anos de experiência no mercado premium.</p>
        </div>
        <div class="highlight">
          <i class="fas fa-spa"></i>
          <h4>Ambiente Exclusivo</h4>
          <p>Um espaço sofisticado e aconchegante para sua experiência de cuidado pessoal.</p>
        </div>
        <div class="highlight">
          <i class="fas fa-flask"></i>
          <h4>Produtos Especializados</h4>
          <p>Linha exclusiva de produtos para crescimento e fortalecimento capilar.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Serviços -->
  <section id="servicos" class="services">
    <div class="container services-container">
      <h2 class="section-title">Nossos Serviços</h2>
      <div class="services-grid">
        <div class="service-card">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1562322140-8baeececf3df?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Corte de Cabelo" loading="lazy">
          </div>
          <div class="service-content">
            <h3>Corte Premium</h3>
            <p>Transforme seu visual com nossos cortes precision, utilizando as técnicas mais modernas do mercado.</p>
            <ul class="service-features">
              <li>Análise personalizada do formato do rosto</li>
              <li>Técnicas de degradê e texturização</li>
              <li>Produtos premium durante o procedimento</li>
              <li>Acabamento impecável com navalha</li>
            </ul>
            <button class="service-btn">
              <i class="fas fa-calendar-alt"></i> Agendar Corte
            </button>
          </div>
        </div>
        <div class="service-card">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1599351431202-1e0f0137899a?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Barba" loading="lazy">
          </div>
          <div class="service-content">
            <h3>Tratamento de Barba</h3>
            <p>Cuide da sua barba com nossos tratamentos especializados para um visual impecável.</p>
            <ul class="service-features">
              <li>Hidratação profunda com produtos naturais</li>
              <li>Modelagem personalizada conforme seu estilo</li>
              <li>Toalha quente para relaxamento muscular</li>
              <li>Finalização com óleos e bálsamos premium</li>
            </ul>
            <button class="service-btn">
              <i class="fas fa-calendar-alt"></i> Agendar Tratamento
            </button>
          </div>
        </div>
        <div class="service-card">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Combo Completo" loading="lazy">
          </div>
          <div class="service-content">
            <h3>Experiência Completa</h3>
            <p>O pacote definitivo para quem busca a excelência em cuidados masculinos.</p>
            <ul class="service-features">
              <li>Corte de cabelo premium</li>
              <li>Tratamento completo para barba</li>
              <li>Massagem relaxante capilar</li>
              <li>Desconto especial no combo</li>
            </ul>
            <button class="service-btn">
              <i class="fas fa-calendar-alt"></i> Agendar Experiência
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Sobre -->
  <section id="sobre" class="about">
    <div class="container">
      <div class="about-content">
        <div class="about-text">
          <h3>Excelência em Cuidados Masculinos</h3>
          <p>Na Biel Barbearia, não oferecemos apenas cortes de cabelo e barba - proporcionamos uma experiência completa de bem-estar e cuidado pessoal. Nossa missão é elevar a autoestima masculina através de serviços premium e produtos de alta qualidade.</p>
          <p>Com anos de experiência no mercado, nossa equipe de profissionais especializados está sempre atualizada com as últimas tendências e técnicas, garantindo que cada cliente saia satisfeito e com a confiança renovada.</p>
          <div class="about-stats">
            <div class="stat">
              <div class="stat-number">5+</div>
              <div class="stat-label">Anos de Experiência</div>
            </div>
            <div class="stat">
              <div class="stat-number">2K+</div>
              <div class="stat-label">Clientes Satisfeitos</div>
            </div>
            <div class="stat">
              <div class="stat-number">98%</div>
              <div class="stat-label">Avaliação Positiva</div>
            </div>
            <div class="stat">
              <div class="stat-number">1</div>
              <div class="stat-label">Produto Exclusivo</div>
            </div>
          </div>
        </div>
        <div class="about-image">
          <img src="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Interior da Biel Barbearia" loading="lazy">
        </div>
      </div>
    </div>
  </section>

  <!-- Contato -->
  <section id="contato" class="contact">
    <div class="container contact-container">
      <h2 class="section-title">Entre em Contato</h2>
      <p>Estamos sempre à disposição para atender você da melhor forma possível.</p>
      <form class="contact-form" id="contact-form">
        <div class="form-group">
          <label for="name">Nome</label>
          <input type="text" id="name" class="form-control" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" class="form-control" required>
        </div>
        <div class="form-group">
          <label for="phone">Telefone</label>
          <input type="tel" id="phone" class="form-control" required>
        </div>
        <div class="form-group">
          <label for="message">Mensagem</label>
          <textarea id="message" class="form-control" required></textarea>
        </div>
        <button type="submit" class="submit-btn">
          <i class="fas fa-paper-plane"></i> Enviar Mensagem
        </button>
      </form>
      <div class="contact-info">
        <div class="contact-card">
          <i class="fas fa-map-marker-alt"></i>
          <h4>Localização</h4>
          <p>Endereço da barbearia</p>
        </div>
        <div class="contact-card">
          <i class="fas fa-clock"></i>
          <h4>Horário de Funcionamento</h4>
          <p>Segunda a Sexta: 8h às 20h</p>
          <p>Sábado: 8h às 18h</p>
        </div>
        <div class="contact-card">
          <i class="fas fa-phone-alt"></i>
          <h4>Telefone</h4>
          <p>(XX) XXXX-XXXX</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Rodapé -->
  <footer>
    <div class="container">
      <div class="footer-content">
        <div class="footer-logo">
          <div class="logo">
            <div class="logo-img">
              <i class="fas fa-scissors"></i>
            </div>
            <h1>BIEL BARBEARIA</h1>
          </div>
          <p>Excelência em cortes premium e cuidados masculinos.</p>
        </div>
        <div class="footer-contact">
          <h4>Contato</h4>
          <p><i class="fas fa-phone-alt"></i> (XX) XXXX-XXXX</p>
          <p><i class="fas fa-map-marker-alt"></i> Endereço da barbearia</p>
          <p><i class="far fa-clock"></i> Seg-Sex: 8h-20h | Sáb: 8h-18h</p>
        </div>
        <div class="footer-social">
          <h4>Redes Sociais</h4>
          <div class="social-links">
            <a href="#" class="social-link" aria-label="Instagram">
              <i class="fab fa-instagram"></i>
            </a>
            <a href="#" class="social-link" aria-label="WhatsApp">
              <i class="fab fa-whatsapp"></i>
            </a>
            <a href="#" class="social-link" aria-label="Facebook">
              <i class="fab fa-facebook-f"></i>
            </a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>© 2023 Biel Barbearia - Todos os direitos reservados</p>
        <p>Desenvolvido com <i class="fas fa-heart" style="color:var(--accent);"></i> para elevar sua experiência</p>
      </div>
    </div>
  </footer>

  <!-- Scripts -->
  <script>
    // ===== OBSERVADOR DE INTERSEÇÃO PARA ANIMAÇÕES =====
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, observerOptions);

    // ===== ROLAGEM SUAVE PARA LINKS INTERNOS =====
    function setupSmoothScroll() {
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
          const href = this.getAttribute('href');
          if (href !== '#' && href.startsWith('#')) {
            e.preventDefault();
            const targetElement = document.querySelector(href);
            if (targetElement) {
              targetElement.scrollIntoView({
                behavior: 'smooth'
              });
              
              // Fechar menu mobile após clicar em um link
              if (window.innerWidth <= 768) {
                document.querySelector('nav').classList.remove('active');
                document.body.style.overflow = 'auto';
              }
            }
          }
        });
      });
    }

    // ===== MENU MÓVEL ALTERNAR =====
    function setupMobileMenu() {
      const menuToggle = document.querySelector('.menu-toggle');
      const nav = document.querySelector('nav');
      
      menuToggle.addEventListener('click', () => {
        nav.classList.toggle('active');
        document.body.style.overflow = nav.classList.contains('active') ? 'hidden' : 'auto';
      });
    }

    // ===== BOTÃO VOLTAR AO TOPO =====
    function setupBackToTop() {
      const backToTopButton = document.querySelector('.back-to-top');
      
      window.addEventListener('scroll', () => {
        if (window.pageYOffset > 300) {
          backToTopButton.classList.add('visible');
        } else {
          backToTopButton.classList.remove('visible');
        }
        
        // Header shrink on scroll
        const header = document.getElementById('header');
        if (window.pageYOffset > 100) {
          header.classList.add('scrolled');
        } else {
          header.classList.remove('scrolled');
        }
      });
      
      backToTopButton.addEventListener('click', () => {
        window.scrollTo({
          top: 0,
          behavior: 'smooth'
        });
      });
    }

    // ===== FORMULÁRIO DE CONTATO =====
    function setupContactForm() {
      const contactForm = document.getElementById('contact-form');
      if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
          e.preventDefault();
          // Simulação de envio do formulário
          const submitBtn = this.querySelector('.submit-btn');
          const originalText = submitBtn.innerHTML;
          
          submitBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Enviando...';
          submitBtn.disabled = true;
          
          // Simulação de tempo de envio
          setTimeout(() => {
            alert('Mensagem enviada com sucesso! Entraremos em contato em breve.');
            contactForm.reset();
            submitBtn.innerHTML = originalText;
            submitBtn.disabled = false;
          }, 2000);
        });
      }
    }

    // ===== INICIALIZAÇÃO GERAL =====
    document.addEventListener('DOMContentLoaded', function() {
      // Observar todas as seções para animações
      document.querySelectorAll('section').forEach(section => {
        observer.observe(section);
      });

      // Configurar funcionalidades
      setupSmoothScroll();
      setupMobileMenu();
      setupBackToTop();
      setupContactForm();
    });

    // Carregar Font Awesome de forma assíncrona
    setTimeout(() => {
      const faScript = document.createElement('script');
      faScript.src = 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js';
      faScript.crossOrigin = 'anonymous';
      document.head.appendChild(faScript);
    }, 1000);
  </script>
</body>
</html>
