<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SoyaDelight - Empanadas de Harina de Soya</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;800&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <script src="https://kit.fontawesome.com/a2d9b7f3d6.js" crossorigin="anonymous"></script>
    <style>
        :root {
            --green: #00a86b;
            --dark: #112;
            --muted: #6b6b6b;
            --card: #fff;
            --bg: #f6f7f8;
            --orange: #ff8c00;
            --purple: #2d0c3d;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        html, body {
            height: 100%;
            width: 100%;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: var(--bg);
            color: var(--dark);
            line-height: 1.6;
            transition: all 0.5s ease;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        
        /* Modo Halloween */
        body.halloween {
            --green: #ff8c00;
            --dark: #2d0c3d;
            --muted: #b8b8b8;
            --card: #3c1642;
            --bg: #1a0b2e;
            color: #fff;
        }
        
        body.halloween .hero-image {
            filter: sepia(0.5) hue-rotate(-30deg) brightness(0.8);
        }
        
        body.halloween .product img {
            filter: sepia(0.5) hue-rotate(-30deg) brightness(0.7);
        }
        
        body.halloween .promo-banner {
            background: linear-gradient(90deg, #2d0c3d, #5a189a);
        }
        
        body.halloween .btn-outline {
            border-color: #ff8c00;
            color: #ff8c00;
        }
        
        body.halloween .btn-outline:hover {
            background: #ff8c00;
            color: #2d0c3d;
        }
        
        body.halloween .testimonials {
            background: #2d0c3d;
        }
        
        body.halloween .testimonial {
            background: #3c1642;
        }
        
        body.halloween footer {
            background: #2d0c3d;
        }
        
        .halloween-button {
            position: fixed;
            top: 20px;
            right: 20px;
            background: transparent;
            border: none;
            font-size: 1.8rem;
            cursor: pointer;
            z-index: 3000;
            transition: all 0.3s ease;
            padding: 8px;
            border-radius: 50%;
            color: #ff8c00;
            background-color: rgba(255, 255, 255, 0.2);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }
        
        .halloween-button:hover {
            transform: scale(1.2);
            background-color: rgba(255, 140, 0, 0.2);
        }
        
        body.halloween .halloween-button {
            color: #00a86b;
            background-color: rgba(45, 12, 61, 0.7);
        }
        
        header {
            background: var(--green);
            color: white;
            padding: 1rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 1000;
            width: 100%;
        }
        
        .brand {
            display: flex;
            gap: .75rem;
            align-items: center;
        }
        
        .logo {
            width: 50px;
            height: 50px;
            border-radius: 8px;
            background: rgba(255,255,255,0.15);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 800;
        }
        
        nav {
            display: flex;
            gap: 1.5rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 600;
        }
        
        .hero {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            align-items: center;
            padding: 3rem 4%;
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
            flex: 1;
        }
        
        .hero .copy h2 {
            font-size: 2.2rem;
            margin: 0 0 .5rem;
            line-height: 1.2;
        }
        
        .badge {
            display: inline-block;
            background: rgba(255,255,255,0.12);
            padding: .35rem .6rem;
            border-radius: 999px;
            font-weight: 700;
            margin-bottom: 1rem;
            font-size: 0.8rem;
        }
        
        .hero p {
            color: var(--muted);
            line-height: 1.5;
            margin-bottom: 1.5rem;
        }
        
        .cta {
            margin-top: 1.25rem;
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: .7rem 1.5rem;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-family: 'Montserrat', sans-serif;
        }
        
        .btn-primary {
            background: var(--dark);
            color: white;
        }
        
        .btn-primary:hover {
            background: #334;
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--dark);
            color: var(--dark);
        }
        
        .btn-outline:hover {
            background: var(--dark);
            color: white;
        }
        
        .hero-image {
            border-radius: 14px;
            overflow: hidden;
            box-shadow: 0 6px 18px rgba(17,17,34,0.08);
        }
        
        .hero-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .promo-banner {
            background: linear-gradient(90deg, #112, #334);
            color: white;
            padding: 1rem;
            overflow: hidden;
            position: relative;
            margin: 2rem 0;
            border-radius: 0;
            width: 100%;
        }
        
        .promo-content {
            display: flex;
            animation: scrollBanner 20s linear infinite;
            white-space: nowrap;
        }
        
        .promo-text {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 0 2rem;
        }
        
        .promo-tag {
            background: #ff5722;
            color: white;
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-weight: 700;
            font-size: 0.8rem;
        }
        
        .promo-highlight {
            color: #ffeb3b;
            font-weight: 700;
        }
        
        @keyframes scrollBanner {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        
        .section-title {
            text-align: center;
            margin: 3rem 0 1.5rem;
            font-size: 2rem;
            width: 100%;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            padding: 2rem 4%;
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
        }
        
        .product {
            overflow: hidden;
            border-radius: 14px;
            background: white;
            box-shadow: 0 6px 18px rgba(17,17,34,0.08);
            transition: all 0.3s ease;
            position: relative;
        }
        
        .product:hover {
            transform: translateY(-5px);
        }
        
        .product img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            display: block;
        }
        
        .product .info {
            padding: 1.5rem;
        }
        
        .product h3 {
            margin: 0 0 .35rem;
        }
        
        .product p {
            margin: 0 0 .75rem;
            color: var(--muted);
            font-size: .95rem;
        }
        
        .price-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .price {
            font-weight: 800;
            color: var(--green);
            font-size: 1.2rem;
        }
        
        .product-tag {
            position: absolute;
            top: 10px;
            right: 10px;
            background: var(--green);
            color: white;
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: 600;
        }
        
        /* Testimonios */
        .testimonials {
            padding: 3rem 4%;
            background: #f0f0f0;
            margin-top: 2rem;
            width: 100%;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
        }
        
        .testimonial {
            background: white;
            padding: 1.5rem;
            border-radius: 14px;
            box-shadow: 0 6px 18px rgba(17,17,34,0.08);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
            color: var(--muted);
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--green);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .author-info h4 {
            margin-bottom: 0.25rem;
        }
        
        .author-info p {
            margin: 0;
            color: var(--muted);
            font-size: 0.9rem;
        }
        
        /* Modal */
        .modal {
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.5);
            display: none;
            align-items: center;
            justify-content: center;
            padding: 1rem;
            z-index: 2000;
        }
        
        .modal.show {
            display: flex;
        }
        
        .modal .dialog {
            width: 100%;
            max-width: 600px;
            background: white;
            padding: 2rem;
            border-radius: 14px;
            box-shadow: 0 12px 24px rgba(17,17,34,0.15);
            max-height: 90vh;
            overflow-y: auto;
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .modal-title {
            margin: 0;
        }
        
        .close-btn {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--muted);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            border-radius: 10px;
            border: 2px solid #e3e3e3;
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            transition: all 0.3s ease;
            background-color: #f9f9f9;
        }
        
        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--green);
            background-color: white;
            box-shadow: 0 0 0 3px rgba(0, 168, 107, 0.1);
        }
        
        .form-group input::placeholder, .form-group textarea::placeholder {
            color: #a0a0a0;
        }
        
        .form-actions {
            display: flex;
            justify-content: flex-end;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        /* Estilos para la selección de productos */
        .product-selection {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
        
        .product-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem;
            border: 1px solid #e3e3e3;
            border-radius: 8px;
        }
        
        .product-info {
            flex: 1;
        }
        
        .product-name {
            font-weight: 600;
            margin-bottom: 0.25rem;
        }
        
        .product-price {
            color: var(--green);
            font-weight: 700;
        }
        
        .product-quantity {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .quantity-btn {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            border: 1px solid #e3e3e3;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }
        
        .quantity-btn:hover {
            background: var(--green);
            color: white;
        }
        
        .quantity-input {
            width: 50px;
            text-align: center;
            border: 1px solid #e3e3e3;
            border-radius: 4px;
            padding: 0.25rem;
        }
        
        .contact-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            z-index: 1000;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            gap: 15px;
        }
        
        .whatsapp-float, .messenger-float {
            display: flex;
            flex-direction: column;
            align-items: flex-end;
        }
        
        .whatsapp-bubble, .messenger-bubble {
            background: #25D366;
            color: white;
            padding: 12px 18px;
            border-radius: 30px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 10px;
            font-weight: 600;
        }
        
        .messenger-bubble {
            background: #0084FF;
        }
        
        .whatsapp-button, .messenger-button {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            transition: all 0.3s ease;
        }
        
        .whatsapp-button {
            background: #25D366;
        }
        
        .messenger-button {
            background: #0084FF;
        }
        
        .whatsapp-button:hover, .messenger-button:hover {
            transform: scale(1.1);
        }
        
        .whatsapp-button i, .messenger-button i {
            color: white;
            font-size: 32px;
        }
        
        footer {
            padding: 2rem 4%;
            color: var(--muted);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            background: var(--dark);
            color: white;
            margin-top: 3rem;
            width: 100%;
        }
        
        .copyright {
            grid-column: 1 / -1;
            text-align: center;
            padding-top: 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            margin-top: 1rem;
        }
        
        @media (max-width: 768px) {
            .hero {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            nav {
                display: none;
            }
            
            .promo-content {
                animation: scrollBanner 15s linear infinite;
            }
            
            .product-item {
                flex-direction: column;
                align-items: flex-start;
                gap: 1rem;
            }
            
            .product-quantity {
                align-self: flex-end;
            }
            
            .form-row {
                flex-direction: column;
            }
        }
    </style>
</head>

<body>
    <!-- Botón Halloween secreto -->
    <button id="halloween-btn" class="halloween-button">
        <i class="fas fa-ghost"></i>
    </button>

    <!-- Header -->
    <header>
        <div class="brand">
            <div class="logo">SD</div>
            <h1>SoyaDelight</h1>
        </div>
        
        <nav>
            <a href="#productos">Productos</a>
            <a href="#ofertas">Ofertas</a>
            <a href="#testimonios">Testimonios</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="copy">
            <span class="badge">¡Novedad!</span>
            <h2>Deliciosas Empanadas de Harina de Soya</h2>
            <p>Disfruta de nuestras empanadas hechas con harina de soya de alta calidad, ricas en proteínas y bajas en grasas.</p>
            <div class="cta">
                <button class="btn btn-primary" id="order-btn">
                    <i class="fas fa-shopping-cart"></i> Comprar ahora
                </button>
                <a href="#productos" class="btn btn-outline">
                    <i class="fas fa-utensils"></i> Ver Productos
                </a>
            </div>
        </div>
        
        <div class="hero-image">
            <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ca4b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Empanadas de harina de soya">
        </div>
    </section>

    <!-- Banner Promocional -->
    <div class="promo-banner">
        <div class="promo-content">
            <div class="promo-text">
                <span class="promo-tag">STOCK LIMITADO</span>
                <span>¡OFERTA ESPECIAL! 6 empanadas por S/ 14.00 (Ahorras S/ 4.00)</span>
                <span class="promo-highlight">¿REGALO ESPECIAL? ¡PÍDELO COMO REGALO! 💬</span>
                <span>ENVÍOS RÁPIDOS A TODO HUANCAYO ✓</span>
                <span>USA CODIGO "EMPRENDIMIENTO" Y OBTEN 15% DSCTO</span>
            </div>
            <div class="promo-text">
                <span class="promo-tag">STOCK LIMITADO</span>
                <span>¡OFERTA ESPECIAL! 6 empanadas por S/ 14.00 (Ahorras S/ 4.00)</span>
                <span class="promo-highlight">¿REGALO ESPECIAL? ¡PÍDELO COMO REGALO! 💬</span>
                <span>ENVÍOS RÁPIDOS A TODO HUANCAYO ✓</span>
                <span>USA CODIGO "EMPRENDIMIENTO" Y OBTEN 15% DSCTO</span>
            </div>
        </div>
    </div>

    <!-- Productos -->
    <section id="productos">
        <h2 class="section-title">Nuestras Empanadas</h2>
        
        <div class="product-grid">
            <div class="product">
                <span class="product-tag">Más Vendido</span>
                <img src="https://images.unsplash.com/photo-1606755962773-d324e74534a2?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Empanada de soya con vegetales">
                <div class="info">
                    <h3>Empanada de Soya y Vegetales</h3>
                    <p>Relleno de soya texturizada, zanahoria, pimiento y especias naturales.</p>
                    <div class="price-row">
                        <span class="price">S/ 9.00</span>
                        <button class="btn btn-primary btn-sm add-to-cart" data-product="Empanada de Soya y Vegetales" data-price="9.00">
                            Agregar
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="product">
                <img src="https://images.unsplash.com/photo-1541519227354-08fa5d50c44d?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Empanada de soya con champiñones">
                <div class="info">
                    <h3>Empanada de Soya y Champiñones</h3>
                    <p>Combinación perfecta de soya con champiñones salteados y hierbas aromáticas.</p>
                    <div class="price-row">
                        <span class="price">S/ 10.00</span>
                        <button class="btn btn-primary btn-sm add-to-cart" data-product="Empanada de Soya y Champiñones" data-price="10.00">
                            Agregar
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="product">
                <span class="product-tag">Vegana</span>
                <img src="https://images.unsplash.com/photo-1563379091339-03246963d96c?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Empanada de soya vegana">
                <div class="info">
                    <h3>Empanada Vegana de Soya</h3>
                    <p>100% vegana, sin ingredientes de origen animal. Ideal para dietas estrictas.</p>
                    <div class="price-row">
                        <span class="price">S/ 11.00</span>
                        <button class="btn btn-primary btn-sm add-to-cart" data-product="Empanada Vegana de Soya" data-price="11.00">
                            Agregar
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="product">
                <img src="https://images.unsplash.com/photo-1598214886806-c87b84b7078b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Empanada de soya picante">
                <div class="info">
                    <h3>Empanada de Soya Picante</h3>
                    <p>Para los amantes del picante, con ajíes seleccionados y soya marinada.</p>
                    <div class="price-row">
                        <span class="price">S/ 10.00</span>
                        <button class="btn btn-primary btn-sm add-to-cart" data-product="Empanada de Soya Picante" data-price="10.00">
                            Agregar
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Ofertas -->
    <section id="ofertas" style="padding: 2rem 4%; background: #f0f0f0; width: 100%;">
        <h2 class="section-title">Ofertas Especiales</h2>
        
        <div class="product-grid">
            <div class="product">
                <div class="info">
                    <h3>Combo Familiar (6 unidades)</h3>
                    <p>Lleva 6 empanadas de tu elección por un precio especial.</p>
                    <div class="price-row">
                        <span class="price" style="color: #ff5722;">S/ 14.00</span>
                        <button class="btn btn-primary" data-offer="combo6">Comprar Combo</button>
                    </div>
                </div>
            </div>
            
            <div class="product">
                <div class="info">
                    <h3>Combo Fiesta (12 unidades)</h3>
                    <p>Perfecto para eventos y reuniones. 12 empanadas de diferentes sabores.</p>
                    <div class="price-row">
                        <span class="price" style="color: #ff5722;">S/ 25.00</span>
                        <button class="btn btn-primary" data-offer="combo12">Comprar Combo</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonios -->
    <section class="testimonials" id="testimonios">
        <h2 class="section-title">Lo Que Dicen Nuestros Clientes</h2>
        
        <div class="testimonial-grid">
            <div class="testimonial">
                <p class="testimonial-text">"¡Me encantó el color dorado perfecto que tienen las empanadas! Además, su textura es increíblemente crocante por fuera y suave por dentro. ¡Una delicia!"</p>
                <div class="testimonial-author">
                    <div class="author-avatar">JR</div>
                    <div class="author-info">
                        <h4>Juan Ramos</h4>
                        <p>Cliente frecuente</p>
                    </div>
                </div>
            </div>
            
            <div class="testimonial">
                <p class="testimonial-text">"Como vegetariano, es difícil encontrar opciones sabrosas y convenientes. SoyaDelight ha cambiado mi rutina alimentaria completamente. ¡Y esa crocancia es adictiva!"</p>
                <div class="testimonial-author">
                    <div class="author-avatar">CR</div>
                    <div class="author-info">
                        <h4>Carlos Ramos</h4>
                        <p>Vegetariano</p>
                    </div>
                </div>
            </div>
            
            <div class="testimonial">
                <p class="testimonial-text">"Compro regularmente para mi familia. A mis hijos les encanta ese color dorado perfecto y lo crocante que quedan las empanadas. Yo estoy tranquila sabiendo que les doy comida nutritiva y deliciosa."</p>
                <div class="testimonial-author">
                    <div class="author-avatar">AR</div>
                    <div class="author-info">
                        <h4>Ana Ramos</h4>
                        <p>Madre de familia</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contacto">
        <div class="footer-section">
            <h3>SoyaDelight</h3>
            <p>Deliciosas empanadas de harina de soya para una alimentación consciente.</p>
        </div>
        
        <div class="footer-section">
            <h3>Contacto</h3>
            <p><i class="fas fa-map-marker-alt"></i> Av. Principal 123, Huancayo</p>
            <p><i class="fas fa-phone"></i> +51 933 750 473</p>
        </div>
        
        <div class="footer-section">
            <h3>Horario</h3>
            <p>Lunes a Viernes: 9:00 - 20:00</p>
            <p>Sábados: 10:00 - 18:00</p>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 SoyaDelight. Todos los derechos reservados.</p>
        </div>
    </footer>

    <!-- Modal de Pedido -->
    <div class="modal" id="order-modal">
        <div class="dialog">
            <div class="modal-header">
                <h3 class="modal-title">Realizar Pedido</h3>
                <button class="close-btn" id="close-modal">&times;</button>
            </div>
            
            <form id="order-form">
                <div class="form-group">
                    <label>Selecciona tus empanadas</label>
                    <div class="product-selection">
                        <div class="product-item">
                            <div class="product-info">
                                <div class="product-name">Empanada de Soya y Vegetales</div>
                                <div class="product-price">S/ 9.00</div>
                            </div>
                            <div class="product-quantity">
                                <button type="button" class="quantity-btn minus" data-product="vegetales">-</button>
                                <input type="number" class="quantity-input" id="vegetales-qty" min="0" value="0" data-price="9.00">
                                <button type="button" class="quantity-btn plus" data-product="vegetales">+</button>
                            </div>
                        </div>
                        
                        <div class="product-item">
                            <div class="product-info">
                                <div class="product-name">Empanada de Soya y Champiñones</div>
                                <div class="product-price">S/ 10.00</div>
                            </div>
                            <div class="product-quantity">
                                <button type="button" class="quantity-btn minus" data-product="champiñones">-</button>
                                <input type="number" class="quantity-input" id="champiñones-qty" min="0" value="0" data-price="10.00">
                                <button type="button" class="quantity-btn plus" data-product="champiñones">+</button>
                            </div>
                        </div>
                        
                        <div class="product-item">
                            <div class="product-info">
                                <div class="product-name">Empanada Vegana de Soya</div>
                                <div class="product-price">S/ 11.00</div>
                            </div>
                            <div class="product-quantity">
                                <button type="button" class="quantity-btn minus" data-product="vegana">-</button>
                                <input type="number" class="quantity-input" id="vegana-qty" min="0" value="0" data-price="11.00">
                                <button type="button" class="quantity-btn plus" data-product="vegana">+</button>
                            </div>
                        </div>
                        
                        <div class="product-item">
                            <div class="product-info">
                                <div class="product-name">Empanada de Soya Picante</div>
                                <div class="product-price">S/ 10.00</div>
                            </div>
                            <div class="product-quantity">
                                <button type="button" class="quantity-btn minus" data-product="picante">-</button>
                                <input type="number" class="quantity-input" id="picante-qty" min="0" value="0" data-price="10.00">
                                <button type="button" class="quantity-btn plus" data-product="picante">+</button>
                            </div>
                        </div>
                    </div>
                    
                    <div class="total-price" style="text-align: right; margin-top: 1rem; font-weight: 700; font-size: 1.2rem;">
                        Total: S/ <span id="total-amount">0.00</span>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="name">Nombre completo</label>
                    <input type="text" id="name" required placeholder="Ingresa tu nombre completo">
                </div>
                
                <div class="form-group">
                    <label for="phone">Teléfono</label>
                    <input type="tel" id="phone" required placeholder="Ingresa tu número de teléfono">
                </div>
                
                <div class="form-group">
                    <label for="address">Dirección de entrega</label>
                    <input type="text" id="address" required placeholder="Ingresa tu dirección completa para la entrega">
                </div>
                
                <div class="form-group">
                    <label for="discount-code">Código de descuento (opcional)</label>
                    <input type="text" id="discount-code" placeholder="Ej: EMPRENDIMIENTO">
                </div>
                
                <div class="form-actions">
                    <button type="button" class="btn btn-outline" id="cancel-order">Cancelar</button>
                    <button type="submit" class="btn btn-primary">Realizar Pedido</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal del Cupón Secreto -->
    <div class="modal" id="coupon-modal">
        <div class="dialog">
            <div class="modal-header">
                <h3 class="modal-title">¡Felicidades!</h3>
                <button class="close-btn" id="close-coupon-modal">&times;</button>
            </div>
            <p>¡Encontraste el botón secreto de Halloween! Has desbloqueado un cupón especial.</p>
            <div style="background: #f0f0f0; padding: 1rem; border-radius: 8px; margin: 1rem 0; text-align: center;">
                <h3 style="color: #ff5722; margin-bottom: 0.5rem;">CUPÓN: EMPRENDEDOR</h3>
                <p style="margin: 0;">Obtén un 20% de descuento adicional en tu pedido</p>
            </div>
            <p>Usa este código junto con "EMPRENDIMIENTO" para obtener un descuento total del 35%.</p>
            <div class="form-actions">
                <button class="btn btn-primary" id="accept-coupon">Aceptar</button>
            </div>
        </div>
    </div>

    <!-- Botones de contacto flotantes -->
    <div class="contact-float">
        <div class="whatsapp-float">
            <div class="whatsapp-bubble">
                <i class="fab fa-whatsapp"></i>
                +51 933 750 473
            </div>
            <a href="https://wa.me/51933750473" class="whatsapp-button" target="_blank">
                <i class="fab fa-whatsapp"></i>
            </a>
        </div>
        
        <div class="messenger-float">
            <div class="messenger-bubble">
                <i class="fab fa-facebook-messenger"></i>
                Envíanos un mensaje
            </div>
            <a href="https://m.me/SoyaDelight" class="messenger-button" target="_blank">
                <i class="fab fa-facebook-messenger"></i>
            </a>
        </div>
    </div>

    <script>
        // Elementos del DOM
        const orderBtn = document.getElementById('order-btn');
        const orderModal = document.getElementById('order-modal');
        const closeModal = document.getElementById('close-modal');
        const cancelOrder = document.getElementById('cancel-order');
        const orderForm = document.getElementById('order-form');
        const totalAmount = document.getElementById('total-amount');
        const discountCode = document.getElementById('discount-code');
        const halloweenBtn = document.getElementById('halloween-btn');
        const couponModal = document.getElementById('coupon-modal');
        const closeCouponModal = document.getElementById('close-coupon-modal');
        const acceptCoupon = document.getElementById('accept-coupon');
        
        // Variables para el carrito
        let cart = {
            vegetales: 0,
            champiñones: 0,
            vegana: 0,
            picante: 0
        };
        
        // Precios de productos en soles (terminados en .00)
        const prices = {
            vegetales: 9.00,
            champiñones: 10.00,
            vegana: 11.00,
            picante: 10.00
        };
        
        // Control del modo Halloween
        let halloweenMode = false;
        let couponShown = false;
        
        // Botón Halloween
        halloweenBtn.addEventListener('click', () => {
            document.body.classList.toggle('halloween');
            halloweenMode = !halloweenMode;
            
            // Mostrar modal del cupón solo la primera vez
            if (halloweenMode && !couponShown) {
                couponModal.classList.add('show');
                couponShown = true;
            }
        });
        
        // Cerrar modal del cupón
        closeCouponModal.addEventListener('click', () => {
            couponModal.classList.remove('show');
        });
        
        acceptCoupon.addEventListener('click', () => {
            couponModal.classList.remove('show');
        });
        
        // Cerrar modal del cupón al hacer clic fuera
        couponModal.addEventListener('click', (e) => {
            if (e.target === couponModal) {
                couponModal.classList.remove('show');
            }
        });
        
        // Abrir modal de pedido
        orderBtn.addEventListener('click', () => {
            orderModal.classList.add('show');
            updateTotal();
        });
        
        // Cerrar modal de pedido
        closeModal.addEventListener('click', () => {
            orderModal.classList.remove('show');
        });
        
        cancelOrder.addEventListener('click', () => {
            orderModal.classList.remove('show');
        });
        
        // Cerrar modal al hacer clic fuera
        orderModal.addEventListener('click', (e) => {
            if (e.target === orderModal) {
                orderModal.classList.remove('show');
            }
        });
        
        // Actualizar total
        function updateTotal() {
            let total = 0;
            for (const product in cart) {
                total += cart[product] * prices[product];
            }
            
            // Aplicar descuentos
            let discount = 0;
            if (discountCode.value.toUpperCase() === 'EMPRENDIMIENTO') {
                discount += 0.15; // 15% de descuento
            }
            
            // Aplicar descuento adicional si se usa el cupón secreto
            if (discountCode.value.toUpperCase().includes('EMPRENDEDOR')) {
                discount += 0.20; // 20% adicional
            }
            
            if (discount > 0) {
                total = total * (1 - discount);
            }
            
            totalAmount.textContent = total.toFixed(2);
        }
        
        // Manejar botones de cantidad
        document.querySelectorAll('.quantity-btn').forEach(button => {
            button.addEventListener('click', (e) => {
                const product = e.target.dataset.product;
                const input = document.getElementById(`${product}-qty`);
                
                if (e.target.classList.contains('plus')) {
                    input.value = parseInt(input.value) + 1;
                } else if (e.target.classList.contains('minus') && input.value > 0) {
                    input.value = parseInt(input.value) - 1;
                }
                
                cart[product] = parseInt(input.value);
                updateTotal();
            });
        });
        
        // Manejar cambios en inputs de cantidad
        document.querySelectorAll('.quantity-input').forEach(input => {
            input.addEventListener('change', (e) => {
                const product = e.target.id.replace('-qty', '');
                cart[product] = parseInt(e.target.value) || 0;
                updateTotal();
            });
        });
        
        // Aplicar descuento cuando cambia el código
        discountCode.addEventListener('input', updateTotal);
        
        // Agregar productos desde la página principal
        document.querySelectorAll('.add-to-cart').forEach(button => {
            button.addEventListener('click', (e) => {
                const productName = e.target.dataset.product;
                let productKey;
                
                // Determinar la clave del producto según el nombre
                if (productName.includes('Vegetales')) productKey = 'vegetales';
                else if (productName.includes('Champiñones')) productKey = 'champiñones';
                else if (productName.includes('Vegana')) productKey = 'vegana';
                else if (productName.includes('Picante')) productKey = 'picante';
                
                // Abrir modal y actualizar cantidad
                orderModal.classList.add('show');
                const input = document.getElementById(`${productKey}-qty`);
                input.value = parseInt(input.value) + 1;
                cart[productKey] = parseInt(input.value);
                updateTotal();
            });
        });
        
        // Manejar ofertas especiales
        document.querySelectorAll('[data-offer]').forEach(button => {
            button.addEventListener('click', (e) => {
                const offer = e.target.dataset.offer;
                
                // Abrir modal
                orderModal.classList.add('show');
                
                // Resetear carrito
                for (const product in cart) {
                    cart[product] = 0;
                    document.getElementById(`${product}-qty`).value = 0;
                }
                
                // Agregar productos según la oferta
                if (offer === 'combo6') {
                    // Combo familiar: 6 empanadas (2 vegetales, 2 champiñones, 1 vegana, 1 picante)
                    document.getElementById('vegetales-qty').value = 2;
                    document.getElementById('champiñones-qty').value = 2;
                    document.getElementById('vegana-qty').value = 1;
                    document.getElementById('picante-qty').value = 1;
                    
                    cart.vegetales = 2;
                    cart.champiñones = 2;
                    cart.vegana = 1;
                    cart.picante = 1;
                } else if (offer === 'combo12') {
                    // Combo fiesta: 12 empanadas (3 de cada sabor)
                    document.getElementById('vegetales-qty').value = 3;
                    document.getElementById('champiñones-qty').value = 3;
                    document.getElementById('vegana-qty').value = 3;
                    document.getElementById('picante-qty').value = 3;
                    
                    cart.vegetales = 3;
                    cart.champiñones = 3;
                    cart.vegana = 3;
                    cart.picante = 3;
                }
                
                updateTotal();
            });
        });
        
        // Manejar envío del formulario
        orderForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // Verificar que se haya seleccionado al menos un producto
            const totalItems = Object.values(cart).reduce((a, b) => a + b, 0);
            if (totalItems === 0) {
                alert('Por favor, selecciona al menos una empanada.');
                return;
            }
            
            // Construir mensaje para WhatsApp
            let message = "¡Hola! Quiero hacer un pedido:\n\n";
            
            // Agregar productos seleccionados
            if (cart.vegetales > 0) {
                message += `${cart.vegetales} x Empanada de Soya y Vegetales - S/ ${(cart.vegetales * 9.00).toFixed(2)}\n`;
            }
            if (cart.champiñones > 0) {
                message += `${cart.champiñones} x Empanada de Soya y Champiñones - S/ ${(cart.champiñones * 10.00).toFixed(2)}\n`;
            }
            if (cart.vegana > 0) {
                message += `${cart.vegana} x Empanada Vegana de Soya - S/ ${(cart.vegana * 11.00).toFixed(2)}\n`;
            }
            if (cart.picante > 0) {
                message += `${cart.picante} x Empanada de Soya Picante - S/ ${(cart.picante * 10.00).toFixed(2)}\n`;
            }
            
            message += `\nTotal: S/ ${totalAmount.textContent}\n`;
            
            // Aplicar descuento si corresponde
            if (discountCode.value.toUpperCase() === 'EMPRENDIMIENTO') {
                message += `(Descuento aplicado: 15% con código EMPRENDIMIENTO)\n`;
            } else if (discountCode.value.toUpperCase().includes('EMPRENDEDOR')) {
                message += `(Descuento aplicado: 35% con códigos EMPRENDIMIENTO y EMPRENDEDOR)\n`;
            }
            
            message += `\nNombre: ${document.getElementById('name').value}\n`;
            message += `Teléfono: ${document.getElementById('phone').value}\n`;
            message += `Dirección: ${document.getElementById('address').value}\n`;
            
            // Codificar mensaje para URL
            const encodedMessage = encodeURIComponent(message);
            const whatsappURL = `https://wa.me/51933750473?text=${encodedMessage}`;
            
            // Abrir WhatsApp
            window.open(whatsappURL, '_blank');
            
            // Cerrar modal y resetear formulario
            orderModal.classList.remove('show');
            orderForm.reset();
            
            // Resetear carrito
            for (const product in cart) {
                cart[product] = 0;
                document.getElementById(`${product}-qty`).value = 0;
            }
            updateTotal();
        });
    </script>
</body>
</html>
