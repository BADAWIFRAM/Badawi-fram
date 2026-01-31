<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Badawi Farm | Supplier Telur Ayam</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <!-- Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    body {
      background: linear-gradient(180deg, #0f172a, #020617);
      color: #fff;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: auto;
    }

    /* HERO */
    .hero {
      text-align: center;
      padding: 100px 0;
    }

    .hero img {
      width: 150px;
      margin-bottom: 25px;
      filter: drop-shadow(0 0 25px rgba(255,193,7,0.6));
      animation: float 4s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    .hero h1 {
      font-size: 3rem;
      font-weight: 700;
      letter-spacing: 2px;
    }

    .hero p {
      margin-top: 15px;
      color: #cbd5f5;
    }

    .btn-group {
      margin-top: 35px;
      display: flex;
      gap: 15px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn {
      padding: 15px 30px;
      border-radius: 14px;
      border: none;
      cursor: pointer;
      font-weight: 600;
      transition: 0.3s;
    }

    .btn-primary {
      background: #facc15;
      color: #000;
    }

    .btn-primary:hover {
      background: #fde047;
    }

    .btn-outline {
      background: transparent;
      border: 1px solid #facc15;
      color: #facc15;
    }

    .btn-outline:hover {
      background: #facc15;
      color: #000;
    }

    /* SECTION */
    section {
      padding: 80px 0;
    }

    h2 {
      text-align: center;
      font-size: 2.2rem;
      margin-bottom: 50px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .card {
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 20px;
      padding: 30px;
      text-align: center;
      backdrop-filter: blur(10px);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-6px);
      border-color: #facc15;
    }

    .card i {
      width: 40px;
      height: 40px;
      color: #facc15;
      margin-bottom: 15px;
    }

    .card h3 {
      margin-bottom: 10px;
    }

    .card p {
      color: #cbd5f5;
      font-size: 0.9rem;
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 50px 0;
      color: #94a3b8;
    }

    footer img {
      width: 80px;
      margin-bottom: 15px;
      opacity: 0.9;
    }

    /* WHATSAPP FLOAT */
    .wa {
      position: fixed;
      bottom: 25px;
      right: 25px;
      background: #22c55e;
      color: #fff;
      padding: 15px 20px;
      border-radius: 50px;
      display: flex;
      align-items: center;
      gap: 10px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.4);
      font-weight: 600;
    }
  </style>
</head>

<body>

  <!-- WHATSAPP -->
  <a class="wa" href="https://wa.me/6282132698172" target="_blank">
    <i data-lucide="message-circle"></i> WhatsApp
  </a>

  <!-- HERO -->
  <div class="hero container">
    <img src="logo-badawi.png" alt="Badawi Farm Logo">
    <h1>BADAWI FARM</h1>
    <p>Supplier Telur Ayam Berkualitas • Grosir & Eceran</p>

    <div class="btn-group">
      <a href="https://wa.me/6282132698172" target="_blank">
        <button class="btn btn-primary">Pesan Sekarang</button>
      </a>
      <a href="https://wa.me/6282132698172" target="_blank">
        <button class="btn btn-outline">Hubungi Kami</button>
      </a>
    </div>
  </div>

  <!-- KEUNGGULAN -->
  <section class="container">
    <h2>Kenapa Pilih Badawi Farm?</h2>
    <div class="grid">
      <div class="card">
        <i data-lucide="egg"></i>
        <h3>Telur Segar</h3>
        <p>Langsung dari peternakan</p>
      </div>
      <div class="card">
        <i data-lucide="shield-check"></i>
        <h3>Kualitas Terjaga</h3>
        <p>Disortir & higienis</p>
      </div>
      <div class="card">
        <i data-lucide="truck"></i>
        <h3>Pengiriman Cepat</h3>
        <p>Area sekitar & tepat waktu</p>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <img src="logo-badawi.png" alt="Badawi Farm">
    <p><strong>BADAWI FARM</strong></p>
    <p>Peternakan & Supplier Telur Ayam</p>
    <p style="margin-top:10px;">© 2026 Badawi Farm</p>
  </footer>

  <script>
    lucide.createIcons();
  </script>

</body>
</html>
