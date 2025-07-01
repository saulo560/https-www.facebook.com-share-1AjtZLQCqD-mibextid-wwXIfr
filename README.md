<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Three Brothers Construction</title>
  <link rel="stylesheet" href="style.css" />
</head>

<body>
  <!-- ===== ENCABEZADO ===== -->
  <header>
    <h1>Three Brothers Construction</h1>
    <nav>
      <a href="#services" id="nav-services">Servicios</a>
      <a href="#gallery" id="nav-gallery">Galería</a>
      <a href="#contact" id="nav-contact">Contacto</a>
      <button id="lang-toggle">English</button>
    </nav>
  </header>

  <!-- ===== HERO ===== -->
  <section class="hero">
    <h2 id="hero-text">
      Expertos en concreto. Construcción de confianza.
    </h2>
  </section>

  <!-- ===== SERVICIOS ===== -->
  <section id="services">
    <h2 id="services-title">Servicios</h2>
    <ul id="services-list">
      <li>Patios</li>
      <li>Banquetas</li>
      <li>Cocheras</li>
      <li>Escaleras</li>
      <li>Reparaciones</li>
    </ul>
  </section>

  <!-- ===== GALERÍA ===== -->
  <section id="gallery">
    <h2 id="gallery-title">Galería</h2>
    <div class="gallery">
      <img src="images/promo1.png" alt="Concrete Work 1" />
      <img src="images/promo2.png" alt="Concrete Work 2" />
      <img src="images/promo3.png" alt="Concrete Work 3" />
      <img src="images/promo4.png" alt="Concrete Work 4" />
    </div>
  </section>

  <!-- ===== CONTACTO ===== -->
  <section id="contact">
    <h2 id="contact-title">Contacto</h2>
    <p>Louisville, KY</p>
    <a class="whatsapp" href="https://wa.me/15133205238" target="_blank">
      WhatsApp: (513) 320-5238
    </a>
    <p>Email: <a href="mailto:saulotrinidad30@gmail.com">saulotrinidad30@gmail.com</a></p>
  </section>

  <footer>
    &copy; 2025 Three Brothers Construction
  </footer>

  <!-- ===== SCRIPTS ===== -->
  <script>
    /* ----- Texto bilingüe ----- */
    const t = {
      es: {
        hero: "Expertos en concreto. Construcción de confianza.",
        nav: ["Servicios", "Galería", "Contacto", "English"],
        servicesTitle: "Servicios",
        servicesList:
          "<li>Patios</li><li>Banquetas</li><li>Cocheras</li><li>Escaleras</li><li>Reparaciones</li>",
        galleryTitle: "Galería",
        contactTitle: "Contacto",
      },
      en: {
        hero: "Concrete experts. Built on trust.",
        nav: ["Services", "Gallery", "Contact", "Español"],
        servicesTitle: "Services",
        servicesList:
          "<li>Patios</li><li>Sidewalks</li><li>Driveways</li><li>Stairs</li><li>Repairs</li>",
        galleryTitle: "Gallery",
        contactTitle: "Contact",
      },
    };

    let lang = "es";
    const qs = (id) => document.getElementById(id);

    qs("lang-toggle").onclick = () => {
      lang = lang === "es" ? "en" : "es";
      qs("hero-text").textContent = t[lang].hero;
      ["nav-services", "nav-gallery", "nav-contact", "lang-toggle"].forEach(
        (id, i) => (qs(id).textContent = t[lang].nav[i])
      );
      qs("services-title").textContent = t[lang].servicesTitle;
      qs("services-list").innerHTML = t[lang].servicesList;
      qs("gallery-title").textContent = t[lang].galleryTitle;
      qs("contact-title").textContent = t[lang].contactTitle;
    };
  </script>
</body>
</html>
/* ===== RESET BÁSICO ===== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.5;
  color: #333;
}

/* ===== ENCABEZADO ===== */
header {
  background: #222;
  color: #fff;
  padding: 20px;
  text-align: center;
}

nav a,
nav button {
  color: #fff;
  margin: 0 8px;
  text-decoration: none;
  background: none;
  border: none;
  font-size: 1rem;
  cursor: pointer;
}

/* ===== HERO ===== */
.hero {
  background: #f3f3f3;
  padding: 60px 20px;
  text-align: center;
}

.hero h2 {
  font-size: 1.8rem;
  font-weight: 600;
}

/* ===== SECCIONES ===== */
section {
  padding: 40px 20px;
  text-align: center;
}

section h2 {
  margin-bottom: 20px;
  font-size: 1.6rem;
}

ul {
  list-style: none;
  display: inline-block;
  text-align: left;
}

/* ===== GALERÍA ===== */
.gallery {
  display: grid;
  gap: 15px;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  margin-top: 20px;
}

.gallery img {
  width: 100%;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease;
}

.gallery img:hover {
  transform: scale(1.04);
}

/* ===== BOTÓN WHATSAPP ===== */
.whatsapp {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 20px;
  background: #25d366;
  color: #fff;
  border-radius: 5px;
  text-decoration: none;
  font-weight: 600;
  transition: background 0.3s;
}

.whatsapp:hover {
  background: #1da851;
}

/* ===== FOOTER ===== */
footer {
  background: #222;
  color: #fff;
  text-align: center;
  padding: 15px 0;
  margin-top: 40px;
}
/tu-sitio
│
├─ index.html
├─ style.css
└─ images
   ├─ promo1.png
   ├─ promo2.png
   ├─ promo3.png
   └─ promo4.png