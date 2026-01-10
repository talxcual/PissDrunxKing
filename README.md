<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PissDrunxKing - La App Definitiva de Skate</title>
    <meta name="description" content="Gestiona tus misiones de skate, sube tus trucos y compite con la comunidad en PissDrunxKing.">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Anton&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-color: #ffcc00; /* Amarillo Skate */
            --secondary-color: #1a1a1a; /* Negro Asfalto */
            --accent-color: #e63946; /* Rojo Acción */
            --text-light: #f1f1f1;
            --text-dark: #333;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--secondary-color);
            color: var(--text-light);
            overflow-x: hidden;
        }

        /* Tipografía */
        h1, h2, h3 {
            font-family: 'Anton', sans-serif;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* Header */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
            background-color: rgba(26, 26, 26, 0.95);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 2px solid var(--primary-color);
        }

        .logo {
            font-size: 1.8rem;
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            font-weight: 700;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--primary-color);
        }

        .btn-download-nav {
            background-color: var(--primary-color);
            color: var(--secondary-color);
            padding: 10px 20px;
            border-radius: 5px;
            font-weight: bold;
            transition: transform 0.2s;
        }

        .btn-download-nav:hover {
            transform: scale(1.05);
            background-color: #e6b800;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1520045864981-8d49230f7978?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            text-align: center;
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            padding: 20px;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 40px;
            font-weight: 300;
        }

        .hero-btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 15px 40px;
            font-size: 1.2rem;
            border-radius: 50px;
            text-transform: uppercase;
            font-weight: bold;
            transition: background-color 0.3s;
            box-shadow: 0 4px 15px rgba(230, 57, 70, 0.4);
        }

        .hero-btn:hover {
            background-color: #d62828;
        }

        /* Features Section */
        .features {
            padding: 80px 5%;
            background-color: #222;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            color: var(--primary-color);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .feature-card {
            background-color: #333;
            padding: 40px 20px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            background-color: #3a3a3a;
        }

        .feature-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .feature-card h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        /* App Preview Section */
        .preview {
            padding: 80px 5%;
            text-align: center;
            background-color: var(--secondary-color);
        }

        .phone-mockup {
            width: 300px;
            border: 10px solid #111;
            border-radius: 30px;
            overflow: hidden;
            margin: 0 auto;
            box-shadow: 0 20px 50px rgba(0,0,0,0.5);
            position: relative;
        }
        
        /* Simulación de pantalla de app */
        .app-screen {
            background-color: #fff;
            height: 550px;
            display: flex;
            flex-direction: column;
            color: #333;
        }
        
        .app-header {
            background-color: var(--primary-color);
            padding: 15px;
            font-family: 'Anton', sans-serif;
            font-size: 1.2rem;
            color: var(--secondary-color);
        }

        .mission-item {
            padding: 15px;
            border-bottom: 1px solid #eee;
            text-align: left;
        }

        .mission-title {
            font-weight: bold;
            font-size: 1.1rem;
        }

        .mission-loc {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 5px;
        }

        .btn-accept {
            background-color: var(--secondary-color);
            color: var(--primary-color);
            border: none;
            padding: 5px 15px;
            border-radius: 4px;
            font-size: 0.8rem;
            cursor: pointer;
            font-weight: bold;
        }

        /* Download Section */
        .download {
            padding: 100px 5%;
            background: linear-gradient(45deg, #111, #222);
            text-align: center;
        }

        .download-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
            flex-wrap: wrap;
        }

        .store-btn {
            background-color: white;
            color: black;
            padding: 15px 30px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: opacity 0.3s;
        }

        .store-btn:hover {
            opacity: 0.8;
        }

        .store-btn i {
            font-size: 2rem;
        }

        .store-text {
            text-align: left;
        }

        .store-text small {
            display: block;
            font-size: 0.8rem;
        }

        .store-text strong {
            font-size: 1.2rem;
            font-family: 'Anton', sans-serif;
        }

        /* Footer */
        footer {
            background-color: #111;
            padding: 40px 5%;
            text-align: center;
            border-top: 1px solid #333;
        }

        .social-links {
            margin-bottom: 20px;
        }

        .social-links a {
            color: var(--text-light);
            font-size: 1.5rem;
            margin: 0 15px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--primary-color);
        }

        /* Responsive */
        @media (max-width: 768px) {
            header {
                padding: 15px 5%;
            }
            
            nav ul {
                display: none; /* Ocultar menú en móvil para simplificar */
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">PISS DRUNX KING</div>
        <nav>
            <ul>
                <li><a href="#features">Características</a></li>
                <li><a href="#preview">Preview</a></li>
                <li><a href="#download" class="btn-download-nav">Descargar</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Domina las Calles</h1>
            <p>La app definitiva para skaters. Encuentra misiones, graba tus trucos y demuestra quién es el rey del spot.</p>
            <a href="#download" class="hero-btn">Empieza a Patinar</a>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <h2 class="section-title">¿Qué puedes hacer?</h2>
        <div class="features-grid">
            <div class="feature-card">
                <i class="fa-solid fa-map-location-dot feature-icon"></i>
                <h3>Misiones Reales</h3>
                <p>Encuentra spots legendarios como Plaza de Armas o Parque Los Reyes y completa los trucos sugeridos.</p>
            </div>
            <div class="feature-card">
                <i class="fa-solid fa-video feature-icon"></i>
                <h3>Sube Evidencia</h3>
                <p>Graba tu truco, sube el video directamente desde la app y valida tu misión completada.</p>
            </div>
            <div class="feature-card">
                <i class="fa-solid fa-trophy feature-icon"></i>
                <h3>Gana Recompensas</h3>
                <p>Completa desafíos difíciles y gana premios exclusivos como gorras, tablas y descuentos.</p>
            </div>
        </div>
    </section>

    <!-- App Preview Section (Simulado) -->
    <section id="preview" class="preview">
        <h2 class="section-title">Dentro de la App</h2>
        <div class="phone-mockup">
            <div class="app-screen">
                <div class="app-header">PDK Misiones</div>
                
                <!-- Mision 1 -->
                <div class="mission-item">
                    <div style="width: 100%; height: 120px; background: url('https://images.unsplash.com/photo-1564245645607-4e6988894178?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60') center/cover; margin-bottom: 10px; border-radius: 8px;"></div>
                    <div class="mission-title">Flip 360 en 3 escalones</div>
                    <div class="mission-loc"><i class="fas fa-map-marker-alt"></i> Plaza de Armas, Pudahuel</div>
                    <button class="btn-accept">ACEPTAR MISIÓN</button>
                </div>

                 <!-- Mision 2 -->
                 <div class="mission-item">
                    <div class="mission-title">Boardslide en baranda</div>
                    <div class="mission-loc"><i class="fas fa-map-marker-alt"></i> Parque Los Reyes</div>
                    <div style="font-size: 0.8rem; color: #e63946; font-weight: bold; margin-top: 5px;">Dificultad: Alta</div>
                </div>

            </div>
        </div>
    </section>

    <!-- Download Section -->
    <section id="download" class="download">
        <h2 class="section-title">Descarga PissDrunxKing Hoy</h2>
        <p>Únete a la comunidad y empieza a tachar trucos de tu lista.</p>
        
        <div class="download-buttons">
            <a href="#" class="store-btn">
                <i class="fa-brands fa-google-play"></i>
                <div class="store-text">
                    <small>Disponible en</small>
                    <strong>Google Play</strong>
                </div>
            </a>
            <!-- Opción para descarga directa de APK -->
            <a href="#" class="store-btn" style="background-color: var(--primary-color); color: var(--secondary-color);">
                <i class="fa-solid fa-download"></i>
                <div class="store-text">
                    <small>Descarga Directa</small>
                    <strong>APK (v1.0)</strong>
                </div>
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
            <a href="#"><i class="fa-brands fa-tiktok"></i></a>
            <a href="#"><i class="fa-brands fa-youtube"></i></a>
        </div>
        <p>&copy; 2025 PissDrunxKing. Todos los derechos reservados.</p>
        <p style="font-size: 0.8rem; margin-top: 10px; color: #666;">Desarrollado por Kleber Toledo A.</p>
    </footer>

    <script>
        // Smooth scrolling para los enlaces de navegación
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Simple animación al hacer scroll para las tarjetas
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.feature-card').forEach((el) => {
            el.style.opacity = 0;
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
            observer.observe(el);
        });
    </script>
</body>
</html>
