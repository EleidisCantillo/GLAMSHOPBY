<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mis Catálogos - Productos de Belleza y Moda</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            color: white;
            margin-bottom: 40px;
            padding: 30px 20px;
        }

        header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .section {
            margin-bottom: 50px;
        }

        .section-title {
            color: white;
            font-size: 1.8em;
            margin-bottom: 20px;
            text-align: center;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }

        .catalogs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-bottom: 20px;
        }

        .catalog-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .catalog-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
        }

        .catalog-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2em;
            color: white;
        }

        .catalog-card.beauty .catalog-icon {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        }

        .catalog-card.fashion .catalog-icon {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        }

        .catalog-card.home .catalog-icon {
            background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
        }

        .catalog-card h3 {
            font-size: 1.5em;
            color: #333;
            margin-bottom: 10px;
        }

        .catalog-card p {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .catalog-btn {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1em;
        }

        .catalog-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .contact-section {
            background: white;
            border-radius: 15px;
            padding: 40px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .contact-section h2 {
            color: #333;
            margin-bottom: 20px;
            font-size: 2em;
        }

        .contact-section p {
            color: #666;
            font-size: 1.1em;
            margin-bottom: 25px;
        }

        .contact-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .contact-btn {
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1em;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .whatsapp-btn {
            background: #25D366;
            color: white;
        }

        .whatsapp-btn:hover {
            background: #20ba5a;
            transform: scale(1.05);
        }

        .email-btn {
            background: #EA4335;
            color: white;
        }

        .email-btn:hover {
            background: #d33426;
            transform: scale(1.05);
        }

        .services-info {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 25px 0;
        }

        .service-item {
            display: flex;
            align-items: center;
            gap: 8px;
            background: #f8f9fa;
            padding: 12px 20px;
            border-radius: 20px;
            color: #333;
            font-weight: 500;
        }

        .service-icon {
            font-size: 1.2em;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }

            .section-title {
                font-size: 1.5em;
            }

            .catalogs-grid {
                grid-template-columns: 1fr;
            }
        }

        footer {
            text-align: center;
            color: white;
            padding: 20px;
            margin-top: 40px;
            opacity: 0.8;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>✨ Mis Catálogos ✨</h1>
            <p>Descubre las mejores marcas de belleza y moda</p>
        </header>

        <!-- Sección de Productos de Belleza -->
        <div class="section">
            <h2 class="section-title">💄 Productos de Belleza y Cuidado Personal</h2>
            <div class="catalogs-grid">
                <div class="catalog-card beauty">
                    <div class="catalog-icon">💋</div>
                    <h3>Esika, L'BEL y Zyzone</h3>
                    <p>Maquillaje, cosméticos premium y productos de cuidado personal innovadores</p>
                    <button class="catalog-btn" onclick="openCatalog('esika-lbel-zyzone')">Ver Catálogos</button>
                </div>

                <div class="catalog-card beauty">
                    <div class="catalog-icon">🌿</div>
                    <h3>Natura</h3>
                    <p>Productos naturales para el cuidado personal y bienestar</p>
                    <button class="catalog-btn" onclick="openCatalog('natura')">Ver Catálogo</button>
                </div>

                <div class="catalog-card beauty">
                    <div class="catalog-icon">🛍️</div>
                    <h3>Novaventa Prestigio</h3>
                    <p>Belleza y cuidado personal para toda la familia</p>
                    <button class="catalog-btn" onclick="openCatalog('novaventa')">Ver Catálogo</button>
                </div>

                <div class="catalog-card beauty">
                    <div class="catalog-icon">💎</div>
                    <h3>Avon</h3>
                    <p>Cosméticos y fragancias reconocidas mundialmente</p>
                    <button class="catalog-btn" onclick="openCatalog('avon')">Ver Catálogo</button>
                </div>
            </div>
        </div>

        <!-- Sección de Moda -->
        <div class="section">
            <h2 class="section-title">👗 Moda y Vestuario</h2>
            <div class="catalogs-grid">
                <div class="catalog-card fashion">
                    <div class="catalog-icon">👔</div>
                    <h3>Carmel</h3>
                    <p>Moda elegante y versátil para toda ocasión</p>
                    <button class="catalog-btn" onclick="openCatalog('carmel')">Ver Catálogo</button>
                </div>

                <div class="catalog-card fashion">
                    <div class="catalog-icon">👚</div>
                    <h3>Loguin</h3>
                    <p>Ropa moderna y confortable con estilo único</p>
                    <button class="catalog-btn" onclick="openCatalog('loguin')">Ver Catálogo</button>
                </div>

                <div class="catalog-card fashion">
                    <div class="catalog-icon">🌊</div>
                    <h3>Pacifika</h3>
                    <p>Colecciones frescas y contemporáneas para tu guardarropa</p>
                    <button class="catalog-btn" onclick="openCatalog('pacifica')">Ver Catálogo</button>
                </div>
            </div>
        </div>

        <!-- Sección de Productos para la Casa -->
        <div class="section">
            <h2 class="section-title">🏠 Productos para la Casa y Más</h2>
            <div class="catalogs-grid">
                <div class="catalog-card home">
                    <div class="catalog-icon">🏡</div>
                    <h3>Novaventa Tradicional</h3>
                    <p>Artículos para el hogar, cocina, decoración y más</p>
                    <button class="catalog-btn" onclick="openCatalog('novaventa-tradicional')">Ver Catálogo</button>
                </div>

                <div class="catalog-card home">
                    <div class="catalog-icon">🏠</div>
                    <h3>Avon Casa</h3>
                    <p>Productos para el hogar, decoración y bienestar familiar</p>
                    <button class="catalog-btn" onclick="openCatalog('avon-casa')">Ver Catálogo</button>
                </div>
            </div>
        </div>

        <!-- Sección de Contacto -->
        <div class="contact-section">
            <h2>📱 ¿Te interesa algún producto?</h2>
            <p>Contáctame para más información, pedidos o consultas sobre los catálogos</p>
            <div class="services-info">
                <div class="service-item">
                    <span class="service-icon">✅</span>
                    <span>Disponibilidad de productos</span>
                </div>
                <div class="service-item">
                    <span class="service-icon">💰</span>
                    <span>Cotización personalizada</span>
                </div>
                <div class="service-item">
                    <span class="service-icon">🚚</span>
                    <span>Información de entrega</span>
                </div>
            </div>
            <div class="contact-buttons">
                <a href="https://wa.me/573122567593" class="contact-btn whatsapp-btn" target="_blank">
                    📱 WhatsApp
                </a>
                <a href="mailto:tu-email@ejemplo.com" class="contact-btn email-btn">
                    📧 Email
                </a>
            </div>
        </div>

        <footer>
            <p>&copy; 2024 - Todos los derechos reservados | Distribuidor Autorizado</p>
        </footer>
    </div>

    <script>
        function openCatalog(catalog) {
            // Aquí puedes agregar los enlaces reales de cada catálogo
            const catalogLinks = {
                'esika-lbel-zyzone': 'https://catalogo.somosbelcorp.com/co/EleidisCantillo1/lbel/pages/1',
                'natura': 'https://co.natura.digital-catalogue.com/co/2026/03/revista/ciclo-3/view/index.html?id_consultora=1137252&utm_term=web&info=eyJ1c2VyIjp7ImN5Y2xlIjoiMjAyNjAzIiwic2Vzc2lvbklkIjoiOTAxNTQ1N2EtMTgzMS00ZWQ4LTkwZjktNmUwZDUwNWI4NWY0Iiwic2hvcElkIjpudWxsfSwibWFnYXppbmUiOnsieWVhciI6IjIwMjYiLCJjeWNsZSI6IjIwMjYwMyIsImlkIjoib2xmc3U2cDgzcmswdmc0MXF3dXV4aXluM3B0d3ZxY2FjNTl2a2JtMSJ9fQ==&page=1',
                'novaventa': 'https://catalogo.novaventa.com/novaventa/2026/prestigio/c3/prestigio-c3/',
                'avon': 'https://short.natura.com/jYOdl0e',
                'carmel': 'https://catalogo.carmel.com.co/2026c03/c03ed02-2026/?utm_source=paginaPedidosCarmel&utm_medium=organico&utm_campaign=pdfOfertas1_Ed2&utm_content=ver_catalogo',
                'loguin': 'https://catalogo.loguin.com.co/2026c03/c03ed02-2026/?utm_source=paginaPedidosLoguin&utm_medium=organico&utm_campaign=pdfOfertas1_Ed2&utm_content=ver_catalogo',
                'pacifica': 'https://catalogo.pacifika.com.co/2026c03/c03ed02-2026/?utm_source=paginaPedidosPacifikaRH&utm_medium=organico&utm_campaign=pdfOfertas1_Ed2&utm_content=ver_catalogo',
                'novaventa-tradicional': 'https://catalogo.novaventa.com/novaventa/2026/tradicional/c3/tradicional-c3/',
                'avon-casa': 'https://short.natura.com/rWeXUSr'
            };

            // Si el enlace está configurado, abrir en nueva pestaña
            if (catalogLinks[catalog] && catalogLinks[catalog] !== '#') {
                window.open(catalogLinks[catalog], '_blank');
            } else {
                // Si no hay enlace, mostrar mensaje
                alert(`¡Gracias por tu interés en ${catalog.toUpperCase()}!\n\nPróximamente: Aquí podrás ver el catálogo completo.\n\nPor ahora, contáctame directamente para enviarte el catálogo digital.`);
            }
        }

        // Animación de entrada
        window.addEventListener('load', () => {
            const cards = document.querySelectorAll('.catalog-card');
            cards.forEach((card, index) => {
                setTimeout(() => {
                    card.style.opacity = '0';
                    card.style.transform = 'translateY(20px)';
                    card.style.transition = 'all 0.5s ease';
                    
                    setTimeout(() => {
                        card.style.opacity = '1';
                        card.style.transform = 'translateY(0)';
                    }, 50);
                }, index * 100);
            });
        });
    </script>
</body>
</html>
