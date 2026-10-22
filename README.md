<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UzAuto Motors</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f5f8;
      color: #172033;
    }
    header {
      background: #101827;
      color: white;
      padding: 22px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 12px;
    }
    header h2 { margin: 0; color: #ffca28; }
    nav a {
      color: white;
      text-decoration: none;
      margin-left: 18px;
    }
    .hero {
      padding: 65px 8%;
      background: linear-gradient(120deg, #172033, #334d72);
      color: white;
    }
    .hero h1 { font-size: 42px; margin-bottom: 12px; }
    .hero p { line-height: 1.7; }
    .cars {
      padding: 35px 8%;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }
    .car {
      background: white;
      padding: 22px;
      border-radius: 12px;
      box-shadow: 0 4px 16px #00000012;
    }
    .car h3 { color: #203c65; }
    .car button {
      background: #d71920;
      color: white;
      border: 0;
      padding: 11px 16px;
      border-radius: 6px;
      cursor: pointer;
    }
    #info { margin-top: 14px; line-height: 1.6; }
    footer {
      padding: 25px;
      background: #101827;
      color: white;
      text-align: center;
    }
    a { cursor: pointer; }
  </style>
</head>
<body>

  <header>
    <h2>UzAuto Motors</h2>
    <nav>
      <a href="#home">Bosh sahifa</a>
      <a href="#cars">Avtomobillar</a>
      <a href="#contact">Aloqa</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <h1>O‘zbekiston avtomobillari</h1>
    <p>UzAuto Motors va Chevrolet avtomobillari haqida
      ma'lumot beruvchi o‘quv sayti.</p>
    <a href="#cars" style="color:#ffca28">
      Avtomobillarni ko‘rish ↓
    </a>
  </section>

  <section class="cars" id="cars">
    <h2>Bizning avtomobillar</h2>
    <div class="grid">
      <article class="car">
        <h3>Chevrolet Cobalt</h3>
        <p>Qulay va kundalik foydalanish uchun sedan.</p>
        <button onclick="showInfo('Cobalt')">Batafsil</button>
      </article>

      <article class="car">
        <h3>Chevrolet Onix</h3>
        <p>Zamonaviy dizaynga ega sedan.</p>
        <button onclick="showInfo('Onix')">Batafsil</button>
      </article>

      <article class="car">
        <h3>Chevrolet Tracker</h3>
        <p>Shahar va sayohat uchun krossover.</p>
        <button onclick="showInfo('Tracker')">Batafsil</button>
      </article>

      <article class="car">
        <h3>Chevrolet Damas</h3>
        <p>Yuk va yo‘lovchi tashishga mo‘ljallangan avtomobil.</p>
        <button onclick="showInfo('Damas')">Batafsil</button>
      </article>
    </div>
    <div id="info"></div>
  </section>

  <footer id="contact">
    <h3>Aloqa</h3>
    <p>UzAuto Motors haqida o‘quv loyihasi</p>
    <a href="https://uzautomotors.com/"
       style="color:#ffca28">
      Rasmiy sayt
    </a>
  </footer>

  <script>
    function showInfo(car) {
      const descriptions = {
        Cobalt: "Cobalt — kundalik foydalanishga mos sedan.",
        Onix: "Onix — zamonaviy sedan modeli.",
        Tracker: "Tracker — ixcham krossover.",
        Damas: "Damas — amaliy, ixcham avtomobil."
      };

      document.getElementById("info").innerHTML =
        "<h3>" + car + "</h3><p>" +
        descriptions[car] + "</p>";
    }
  </script>

</body>
</html>
