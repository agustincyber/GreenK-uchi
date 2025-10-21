<!--
Archivo: index.html
Proyecto: SoyaDelight - Página de venta de empanadas de soya
Instrucciones:
1. Copia este archivo como index.html en la raíz de tu repo de GitHub.
2. Añade imágenes en la carpeta /assets (ej: assets/empanada1.jpg) o cambia las rutas a imágenes online.
3. Publicar: en GitHub -> Settings -> Pages -> branch: main / folder: root -> Save.
-->
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SoyaDelight - Empanadas de Soya</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;800&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
  <script src="https://kit.fontawesome.com/a2d9b7f3d6.js" crossorigin="anonymous"></script>
  <style>
    :root{
      --green:#00a86b;
      --dark:#112;
      --muted:#6b6b6b;
      --card:#fff;
      --bg:#f6f7f8;
      --glass: rgba(255,255,255,0.85);
    }
    *{box-sizing:border-box}
    body{font-family: 'Montserrat', sans-serif;margin:0;background:linear-gradient(180deg,var(--bg),#eef2f4);color:var(--dark)}
    header{background:var(--green);color:white;padding:1.25rem 1rem;display:flex;align-items:center;justify-content:space-between}
    .brand{display:flex;gap:.75rem;align-items:center}
    .logo{width:56px;height:56px;border-radius:8px;background:rgba(255,255,255,0.15);display:flex;align-items:center;justify-content:center;font-weight:800;font-size:1.1rem}
    .brand h1{margin:0;font-family:'Playfair Display',serif;font-weight:700;font-size:1.25rem}
    nav a{color:white;text-decoration:none;margin-left:1rem;font-weight:600}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:2rem;align-items:center;padding:3rem 4%}
    .hero .copy h2{font-size:2rem;margin:0 0 .5rem}
    .badge{display:inline-block;background:rgba(255,255,255,0.12);padding:.35rem .6rem;border-radius:999px;font-weight:700;margin-bottom:1rem}
    .hero p{color:var(--muted);line-height:1.5}
    .cta{margin-top:1.25rem}
    .btn{display:inline-block;padding:.7rem 1rem;border-radius:10px;text-decoration:none;font-weight:700}
    .btn-primary{background:var(--dark);color:white}
    .btn-outline{background:transparent;border:2px solid var(--dark);color:var(--dark);margin-left:.5rem}

    .card{background:var(--card);border-radius:14px;box-shadow:0 6px 18px rgba(17,17,34,0.08);padding:1rem}
    .product-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1rem;padding:2rem 4%}
    .product{overflow:hidden;border-radius:12px;background:linear-gradient(180deg,var(--glass),#fff);padding:0}
    .product img{width:100%;height:180px;object-fit:cover;display:block}
    .product .info{padding:1rem}
    .product h3{margin:0 0 .35rem}
    .product p{margin:0 0 .75rem;color:var(--muted);font-size:.95rem}
    .price-row{display:flex;justify-content:space-between;align-items:center}
    .price{font-weight:800;color:var(--green)}

    .features{display:flex;gap:1rem;padding:1.5rem 4%;flex-wrap:wrap}
    .feature{flex:1 1 200px;background:linear-gradient(180deg,#fff,var(--glass));padding:1rem;border-radius:10px}

    footer{padding:1.25rem 4%;color:var(--muted);display:flex;justify-content:space-between;align-items:center}

    /* Modal */
    .modal{position:fixed;inset:0;background:rgba(0,0,0,0.5);display:none;align-items:center;justify-content:center;padding:1rem}
    .modal.show{display:flex}
    .modal .dialog{width:100%;max-width:520px;background:white;padding:1rem;border-radius:12px}
    .form-row{display:flex;gap:.5rem;margin-bottom:.5rem}
    .form-row input,.form-row select{flex:1;padding:.6rem;border-radius:8px;border:1px solid #e3e3e3}

    /* responsive */
    @media (max-width:880px){
      .hero{grid-template-columns:1fr}
      .hero img{display:none}
      header{padding:.8rem}
    }
  </style>
</head>
<body>
  <header>
    <div class="brand">
      <div class="logo">SD</div>
      <div>
        <h1>SoyaDelight</h1>
        <div style="font-size:.8rem;color:rgba(255,255,255,0.9);margin-top:.15rem">Empanadas de soya - saludables y sabrosas</div>
      </div>
    </div>
    <nav>
      <a href="#productos">Productos</a>
      <a href="#promos">Promociones</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <section class="hero">
    <div class="copy">
      <span class="badge">Nuevo • Lanzamiento</span>
      <h2>Empanadas artesanales de soya, crujientes por fuera, sabrosas por dentro</h2>
      <p>Alternativa vegetariana con proteína de soya y verduras frescas. Hechas a mano y con ingredientes locales. Perfectas para snack, almuerzo o venta callejera.</p>
      <div class="cta">
        <a class="btn btn-primary" href="#productos">Ver productos</a>
        <a class="btn btn-outline" href="https://wa.me/51900000000?text=Hola%20SoyaDelight%20quiero%20hacer%20un%20pedido" target="_blank">Pedir por WhatsApp</a>
      </div>
    </div>
    <div>
      <div class="card">
        <img src="assets/empanada-hero.jpg" alt="Empanada de soya" style="width:100%;height:240px;object-fit:cover;border-radius:10px">
        <div style="padding:1rem">
          <h3 style="margin:0">Pack de lanzamiento - 6 unidades</h3>
          <p style="margin:.5rem 0;color:var(--muted)">Congeladas para recalentar o entregadas calientes en la zona urbana.</p>
          <div class="price-row">
            <div class="price">S/ 20.00</div>
            <div>
              <button class="btn btn-primary" onclick="openOrder('Pack 6')">Ordenar</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="productos" class="product-grid">
    <div class="product">
      <img src="assets/empanada1.jpg" alt="Empanada tradicional de soya">
      <div class="info">
        <h3>Empanada tradicional</h3>
        <p>Relleno de soya sazonada con cebolla, perejil y toque de comino.</p>
        <div class="price-row">
          <div class="price">S/ 4.00</div>
          <button class="btn btn-outline" onclick="openOrder('Empanada tradicional')">Pedir</button>
        </div>
      </div>
    </div>

    <div class="product">
      <img src="assets/empanada2.jpg" alt="Empanada ají de soya">
      <div class="info">
        <h3>Empanada ají</h3>
        <p>Con un toque de ají amarillo y ají panca, estilo criollo.</p>
        <div class="price-row">
          <div class="price">S/ 4.50</div>
          <button class="btn btn-outline" onclick="openOrder('Empanada ají')">Pedir</button>
        </div>
      </div>
    </div>

    <div class="product">
      <img src="assets/empanada3.jpg" alt="Empanada champiñones y soya">
      <div class="info">
        <h3>Empanada champiñones</h3>
        <p>Relleno mixto de champiñones y soya, textura suculenta.</p>
        <div class="price-row">
          <div class="price">S/ 5.00</div>
          <button class="btn btn-outline" onclick="openOrder('Empanada champiñones')">Pedir</button>
        </div>
      </div>
    </div>
  </section>

  <section class="features">
    <div class="feature card">
      <h4>Ingredientes</h4>
      <p>Proteína de soya hidratada, masa de harina de trigo, cebolla, ají, aceite de oliva, sal y especias.</p>
    </div>
    <div class="feature card">
      <h4>Conservación</h4>
      <p>Recomendado congelar para venta por packs. Recalentar en horno 12-15 min a 180°C o freír 3-4 min por lado.</p>
    </div>
    <div class="feature card">
      <h4>Envíos</h4>
      <p>Delivery local con motorizado propio o entrega mediante apps de reparto. Pedidos en 24h en packs.</p>
    </div>
  </section>

  <footer id="contacto">
    <div>© <strong>SoyaDelight</strong> 2025 • Hecho en Perú</div>
    <div style="display:flex;gap:.6rem;align-items:center">
      <a href="https://www.instagram.com" target="_blank" aria-label="instagram"><i class="fab fa-instagram"></i></a>
      <a href="https://www.facebook.com" target="_blank" aria-label="facebook"><i class="fab fa-facebook"></i></a>
      <a href="mailto:ventas@soya-delight.com">ventas@soya-delight.com</a>
    </div>
  </footer>

  <!-- Modal de pedido simple -->
  <div id="modal" class="modal" onclick="closeModal(event)">
    <div class="dialog card" role="dialog" aria-modal="true">
      <h3 id="modal-title">Realizar pedido</h3>
      <div style="margin:.5rem 0;color:var(--muted)">Completa tus datos y confirma el pedido por WhatsApp.</div>
      <div class="form-row">
        <input id="cust-name" placeholder="Tu nombre">
        <input id="cust-phone" placeholder="Teléfono (ej: 9XXXXXXXX)">
      </div>
      <div class="form-row">
        <select id="item-select">
          <option>Empanada tradicional - S/4.00</option>
        </select>
      </div>
      <div class="form-row">
        <input id="qty" type="number" value="1" min="1">
        <input id="address" placeholder="Dirección de entrega">
      </div>
      <div style="display:flex;gap:.5rem;justify-content:flex-end">
        <button class="btn btn-outline" onclick="closeModal()">Cancelar</button>
        <button class="btn btn-primary" onclick="sendWhatsApp()">Confirmar y enviar por WhatsApp</button>
      </div>
    </div>
  </div>

  <script>
    const products = ['Empanada tradicional - S/4.00','Empanada ají - S/4.50','Empanada champiñones - S/5.00','Pack 6 - S/20.00'];
    const itemSelect = document.getElementById('item-select');
    products.forEach(p=>{const o=document.createElement('option');o.textContent=p;itemSelect.appendChild(o)});

    function openOrder(item){
      document.getElementById('modal-title').textContent = 'Pedido: '+item;
      // seleccionar opción que contenga el nombre
      for(let i=0;i<itemSelect.options.length;i++){
        if(itemSelect.options[i].textContent.includes(item.split(' - ')[0])){itemSelect.selectedIndex=i;break}
      }
      document.getElementById('modal').classList.add('show');
    }
    function closeModal(e){
      if(e && e.target && e.target.id!=='modal') return; // click dentro del dialog
      document.getElementById('modal').classList.remove('show');
    }
    function sendWhatsApp(){
      const name = encodeURIComponent(document.getElementById('cust-name').value || 'Cliente');
      const phone = document.getElementById('cust-phone').value || '';
      const item = encodeURIComponent(document.getElementById('item-select').value);
      const qty = encodeURIComponent(document.getElementById('qty').value);
      const addr = encodeURIComponent(document.getElementById('address').value || 'Recojo en tienda');
      const message = `Hola%20SoyaDelight%20soy%20${name}%20-%20Quiero%20${qty}%20de%20${item}%20Direccion:%20${addr}`;
      // numero de empresa en formato internacional (ej: 51 + celular)
      const waNumber = '51900000000';
      const url = `https://wa.me/${waNumber}?text=${message}`;
      if(!phone){
        // redirigir igual para confirmacion, el usuario añadiría su numero
        window.open(url,'_blank');
      } else {
        window.open(url,'_blank');
      }
    }
  </script>
</body>
</html>
