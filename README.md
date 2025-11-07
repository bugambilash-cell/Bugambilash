<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Bugambilash — Spa de cejas y pestañas</title>
  <meta name="description" content="Bugambilash — spa especializado en cejas y pestañas. Realza tu mirada con elegancia y confianza. Agenda tu cita por WhatsApp." />

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Dancing+Script:wght@400;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --pink-1: #ffeef0; /* muy suave */
      --pink-2: #f7ccd1; /* medio */
      --accent: #d85967; /* color principal tipo bugambilia */
      --muted: #777777;
      --radius: 14px;
      --container: 1100px;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: 'Poppins', system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color:#222;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      background: linear-gradient(180deg, var(--pink-1) 0%, var(--pink-2) 100%);
      display:flex;
      justify-content:center;
      padding:30px 18px;
    }

    .wrap{
      width:100%;
      max-width:var(--container);
      background: #fff;
      border-radius:20px;
      box-shadow: 0 10px 30px rgba(10,10,10,0.06);
      overflow:hidden;
      min-height:600px;
    }

    /* Header */
    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:22px 34px;
    }
    .logo{
      display:flex;
      align-items:center;
      gap:14px;
    }
    .logo img{height:64px; width:auto;}
    .nav{
      display:flex;
      gap:18px;
      align-items:center;
    }
    .nav a{
      text-decoration:none;
      color:var(--muted);
      font-weight:600;
      font-size:14px;
    }
    .cta{
      background:linear-gradient(90deg,var(--accent),#c84a59);
      color:#fff;
      border:none;
      padding:10px 18px;
      border-radius:10px;
      font-weight:600;
      cursor:pointer;
      text-decoration:none;
    }

    /* Hero */
    .hero{
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:28px;
      align-items:center;
      padding:30px 34px 18px;
    }
    .hero-left{
      padding:18px 6px;
    }
    .tag{
      color:var(--accent);
      font-weight:600;
      letter-spacing:0.6px;
      font-size:14px;
      margin-bottom:14px;
    }
    h1{
      margin:0;
      font-size:38px;
      line-height:1.05;
      color:#222;
    }
    p.lead{
      color:#555;
      margin-top:12px;
      margin-bottom:18px;
      font-size:16px;
      max-width:60ch;
    }

    .hero-actions{
      display:flex;
      gap:12px;
      align-items:center;
      margin-top:18px;
    }
    .secondary{
      background:transparent;
      color:var(--accent);
      border:2px solid var(--accent);
      padding:10px 16px;
      border-radius:10px;
      text-decoration:none;
      font-weight:600;
    }

    /* Hero image / logo focal */
    .hero-right{
      display:flex;
      align-items:center;
      justify-content:center;
      padding:18px;
    }
    .big-logo{
      width:320px;
      height:320px;
      display:flex;
      align-items:center;
      justify-content:center;
      border-radius:16px;
      background: linear-gradient(180deg, rgba(216,89,103,0.06), rgba(216,89,103,0.02));
    }
    .big-logo img{max-width:85%; max-height:85%; object-fit:contain;}

    /* Services */
    .section{
      padding:18px 34px 30px;
      border-top:1px solid #f1f1f1;
    }
    .grid{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:18px;
      margin-top:18px;
    }
    .card{
      background:#fff;
      border-radius:14px;
      padding:16px;
      box-shadow: 0 6px 18px rgba(20,20,20,0.04);
      border:1px solid #fafafa;
    }
    .card h3{margin:6px 0 8px; font-size:17px}
    .card p{margin:0; color:#666; font-size:14px}

    /* About */
    .about{
      display:flex;
      gap:18px;
      align-items:center;
      margin-top:18px;
    }
    .about .text{flex:1}
    .about img{width:220px; height:160px; object-fit:cover; border-radius:12px; box-shadow:0 6px 18px rgba(20,20,20,0.06)}

    /* Gallery */
    .gallery-grid{
      display:grid;
      grid-template-columns: repeat(4, 1fr);
      gap:12px;
      margin-top:14px;
    }
    .placeholder{
      background: linear-gradient(180deg, rgba(216,89,103,0.06), rgba(216,89,103,0.02));
      border:1px dashed rgba(200,80,90,0.18);
      height:150px;
      border-radius:12px;
      display:flex;
      align-items:center;
      justify-content:center;
      color:var(--muted);
      font-size:14px;
    }

    /* Contact */
    .contact{
      display:flex;
      justify-content:space-between;
      gap:18px;
      align-items:center;
      margin-top:18px;
    }
    .contact .info{flex:1}
    .small{
      font-size:13px;
      color:var(--muted);
    }

    footer{
      padding:16px 34px;
      border-top:1px solid #f6f6f6;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:10px;
    }

    /* Floating WhatsApp */
    .whatsapp-fixed{
      position:fixed;
      right:20px;
      bottom:20px;
      z-index:1200;
    }
    .whatsapp-btn{
      display:inline-flex;
      gap:10px;
      align-items:center;
      background:linear-gradient(90deg,#2ecc71,#25d366);
      color:#fff;
      padding:12px 16px;
      border-radius:999px;
      box-shadow: 0 8px 30px rgba(37,211,102,0.18);
      text-decoration:none;
      font-weight:700;
      font-size:15px;
    }

    /* Responsive */
    @media (max-width:960px){
      .hero{grid-template-columns: 1fr; text-align:center}
      .hero-right{order:-1}
      .grid{grid-template-columns: repeat(2, 1fr)}
      .gallery-grid{grid-template-columns: repeat(2, 1fr)}
      .about{flex-direction:column; text-align:center}
      header{padding:16px}
      .wrap{margin:0 8px}
    }
    @media (max-width:520px){
      .grid{grid-template-columns: 1fr}
      .big-logo{width:240px;height:240px}
      .nav{display:none}
    }
  </style>
</head>
<body>
  <div class="wrap" role="main">

    <!-- Header -->
    <header>
      <div class="logo" aria-label="Bugambilash logo">
        <!-- Reemplaza 'logo.png' por la ruta a tu logo. -->
        <img src="logo.png" alt="Bugambilash logo">
        <div style="display:flex;flex-direction:column;line-height:1">
          <strong style="font-size:18px;color:#d85967">Bugambilash</strong>
          <small style="color:var(--muted);font-size:12px">By: Laura Mejía</small>
        </div>
      </div>

      <nav class="nav" aria-label="Navegación principal">
        <a href="#inicio">Inicio</a>
        <a href="#servicios">Servicios</a>
        <a href="#galeria">Galería</a>
        <a href="#contacto">Contacto</a>
        <a class="cta" href="https://wa.me/3151177535" target="_blank" rel="noopener">Agenda tu cita</a>
      </nav>
    </header>

    <!-- Hero -->
    <section id="inicio" class="hero" aria-labelledby="hero-title">
      <div class="hero-left">
        <div class="tag">Spa de cejas y pestañas</div>
        <h1 id="hero-title">Realza tu mirada con elegancia y confianza</h1>
        <p class="lead">En Bugambilash combinamos técnica, detalle y productos de alta calidad para crear resultados personalizados que armonicen con tu rostro. Siéntete radiante, segura y cómoda.</p>

        <div class="hero-actions">
          <a class="cta" href="https://wa.me/3151177535" target="_blank" rel="noopener">Agenda tu cita</a>
          <a class="secondary" href="#servicios">Ver servicios</a>
        </div>
      </div>

      <div class="hero-right" aria
