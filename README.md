 # gua-digital-story-mapping essay



<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gua Digital Story Experience</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --bg: #071426;
  --card: #10243b;
  --blue: #42c8ff;
  --purple: #9b72ff;
  --text: #f3f7ff;
  --muted: #a9bad0;
}

body {
  font-family: Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

header {
  position: sticky;
  top: 0;
  z-index: 10;
  padding: 16px;
  background: #071426f2;
  border-bottom: 1px solid #29415d;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-weight: bold;
  font-size: 18px;
}

.logo span {
  color: var(--blue);
}

nav a {
  color: white;
  text-decoration: none;
  margin-left: 12px;
  font-size: 13px;
}

main {
  max-width: 800px;
  margin: auto;
  padding: 16px;
}

.hero {
  min-height: 460px;
  padding: 25px;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  background:
    linear-gradient(0deg, #020812 5%, transparent 100%),
    radial-gradient(ellipse at 50% 60%,
      #26bfff 0%, #183d6b 30%,
      #071426 75%);
  border: 1px solid #315477;
}

.tag {
  display: inline-block;
  color: #9eeaff;
  background: #0c2c49;
  border: 1px solid #42c8ff;
  border-radius: 30px;
  padding: 5px 12px;
  font-size: 12px;
  width: fit-content;
}

h1 {
  font-size: clamp(32px, 8vw, 50px);
  line-height: 1.1;
  margin: 18px 0;
}

h1 span {
  color: var(--blue);
}

p {
  color: var(--muted);
  margin: 12px 0;
}

.btn {
  display: inline-block;
  padding: 12px 18px;
  margin: 6px 5px 6px 0;
  border-radius: 12px;
  border: none;
  cursor: pointer;
  font-weight: bold;
  text-decoration: none;
  font-size: 14px;
}

.primary {
  background: linear-gradient(100deg,
    var(--blue), #9c8aff);
  color: #071426;
}

.secondary {
  background: #17304c;
  color: white;
  border: 1px solid #34516e;
}

section {
  margin-top: 35px;
  scroll-margin-top: 80px;
}

h2 {
  font-size: 25px;
  margin-bottom: 15px;
}

h3 {
  margin-bottom: 10px;
}

.card {
  background: var(--card);
  border: 1px solid #29435f;
  border-radius: 20px;
  padding: 20px;
  margin-bottom: 15px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
}

.feature {
  background: var(--card);
  padding: 18px;
  border-radius: 18px;
  border: 1px solid #29435f;
  color: white;
  text-decoration: none;
}

.feature span {
  font-size: 25px;
  display: block;
}

.feature b {
  display: block;
  margin-top: 8px;
}

.feature small {
  color: var(--muted);
}

/* PETA */

.map {
  height: 250px;
  border-radius: 20px;
  background:
    linear-gradient(35deg,
      transparent 45%, #4d9a7955 46% 49%,
      transparent 50%),
    radial-gradient(ellipse,
      #265f58, #102b3a);
  position: relative;
  overflow: hidden;
  border: 1px solid #355575;
}

.pin {
  position: absolute;
  top: 40%;
  left: 48%;
  font-size: 35px;
}

.map-label {
  position: absolute;
  bottom: 12px;
  left: 12px;
  background: #071426e8;
  padding: 10px;
  border-radius: 10px;
  font-size: 13px;
}

/* STORYTELLING */

.story-image {
  height: 180px;
  border-radius: 15px;
  margin-bottom: 15px;
  background:
    radial-gradient(ellipse at 50% 80%,
      #28caffaa, transparent 50%),
    linear-gradient(145deg,
      #183b64, #071426);
}

.progress {
  height: 5px;
  background: #29435f;
  margin-top: 15px;
  border-radius: 10px;
  overflow: hidden;
}

#bar {
  width: 33%;
  height: 100%;
  background: var(--blue);
  transition: width .3s;
}

/* DIGITAL MAPPING */

.mapping {
  height: 220px;
  border-radius: 15px;
  background:
    radial-gradient(ellipse at 50% 80%,
      #42c8ffcc, transparent 45%),
    linear-gradient(145deg,
      #183b64, #071426);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-weight: bold;
  font-size: 18px;
  transition: background .5s;
  animation: glow 4s infinite alternate;
}

@keyframes glow {
  from { filter: brightness(.8); }
  to { filter: brightness(1.4); }
}

.quiz button {
  display: block;
  width: 100%;
  text-align: left;
  margin: 10px 0;
}

footer {
  text-align: center;
  color: #7890a9;
  padding: 35px 15px 100px;
  font-size: 13px;
}

.bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: #071426f5;
  border-top: 1px solid #29415d;
  display: flex;
  justify-content: space-around;
  padding: 12px 3px;
  z-index: 20;
}

.bottom-nav a {
  color: #b6c9df;
  text-decoration: none;
  font-size: 12px;
  text-align: center;
}

@media (min-width: 650px) {
  main {
    padding: 25px;
  }

  .grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">🌌 GUA <span>DIGITAL</span></div>
  <nav>
    <a href="#beranda">Home</a>
    <a href="#peta">Peta</a>
  </nav>
</header>

<main>

<!-- BERANDA -->

<div class="hero" id="beranda">
  <span class="tag">WISATA • CERITA • TEKNOLOGI</span>

  <h1>
    Jelajahi Dunia<br>
    <span>di Balik Gua</span>
  </h1>

  <p>
    Rasakan pengalaman wisata digital melalui
    cerita, peta, animasi, dan visual digital mapping
    yang memukau.
  </p>

  <div>
    <a href="#jelajah" class="btn primary">
      Mulai Jelajah ↗
    </a>

    <a href="#cerita" class="btn secondary">
      ▶ Dengarkan Cerita
    </a>
  </div>
</div>

<!-- MENU -->

<section id="jelajah">
  <h2>Jelajah Digital</h2>

  <div class="grid">
    <a class="feature" href="#peta">
      <span>📍</span>
      <b>Peta Gua</b>
      <small>Lokasi wisata</small>
    </a>

    <a class="feature" href="#cerita">
      <span>🎧</span>
      <b>Storytelling</b>
      <small>Kisah gua</small>
    </a>

    <a class="feature" href="#mapping">
      <span>✨</span>
      <b>Digital Mapping</b>
      <small>Visual interaktif</small>
    </a>

    <a class="feature" href="#kuis">
      <span>🧭</span>
      <b>Kuis Jelajah</b>
      <small>Uji pengetahuan</small>
    </a>
  </div>
</section>

<!-- PETA -->

<section id="peta">
  <h2>Peta Wisata Gua</h2>

  <div class="map">
    <div class="pin">📍</div>

    <div class="map-label">
      Gua Wisata - Lokasi Demo
    </div>
  </div>

  <p>
    Peta ini masih berupa ilustrasi prototype.
    Kamu dapat menggantinya dengan lokasi gua
    yang sebenarnya.
  </p>

  <a class="btn secondary"
     href="https://www.openstreetmap.org/"
     target="_blank">
    Buka Peta Online ↗
  </a>
</section>

<!-- STORYTELLING -->

<section id="cerita">
  <h2>Kisah di Balik Gua</h2>

  <div class="card">
    <div class="story-image"></div>

    <h3 id="judulCerita">
      Awal Sebuah Petualangan
    </h3>

    <p id="narasi">
      Di antara rimbunnya alam, tersembunyi
      sebuah gua yang menyimpan keindahan dan
      kisah masa lalu. Mari menjelajah dengan
      rasa ingin tahu dan tetap menjaga alam.
    </p>

    <button class="btn primary" onclick="audio()">
      ▶ Putar Narasi
    </button>

    <button class="btn secondary" onclick="nextStory()">
      Cerita Berikutnya →
    </button>

    <div class="progress">
      <div id="bar"></div>
    </div>

    <p id="nomor">Cerita 1 dari 3</p>
  </div>
</section>

<!-- DIGITAL MAPPING -->

<section id="mapping">
  <h2>Digital Mapping</h2>

  <div class="card">

    <div class="mapping" id="visual">
      GUA DIGITAL<br>
      <small id="mode">Cahaya Biru</small>
    </div>

    <p>
      Pilih warna untuk melihat simulasi
      visual digital mapping pada gua.
    </p>

    <button class="btn secondary"
      onclick="setMode('blue')">
      🔵 Biru
    </button>

    <button class="btn secondary"
      onclick="setMode('purple')">
      🟣 Ungu
    </button>

    <button class="btn secondary"
      onclick="setMode('green')">
      🟢 Aurora
    </button>

    <p>
      Simulasi ini merupakan efek visual
      website, bukan proyeksi fisik.
    </p>

  </div>
</section>

<!-- KUIS -->

<section id="kuis">
  <h2>Kuis Penjelajah</h2>

  <div class="card quiz">
    <h3>
      Apa yang harus dilakukan saat
      berwisata ke gua?
    </h3>

    <button class="btn secondary"
      onclick="jawab(false)">
      A. Membuang sempah di area gua
    </button>

    <button class="btn secondary"
      onclick="jawab(true)">
      B. Merusak ornamen gua
    </button>

    <button class="btn secondary"
      onclick="jawab(false)">
      C. Mencoret ornamen gua
    </button>

    <p id="hasil"></p>
  </div>
</section>

<!-- PENUTUP -->

<section>
  <div class="card" style="text-align:center">
    <h2>Jaga Gua, Jaga Cerita 🌿</h2>

    <p>
      Keindahan alam adalah warisan bersama.
      Jelajahi dengan bijak dan jaga
      kelestarian gua.
    </p>

    <a href="#beranda" class="btn primary">
      Kembali ke Atas ↑
    </a>
  </div>
</section>

</main>

<footer>
  Gua Digital Story Experience<br>
  Prototype Website Wisata Digital
</footer>

<!-- NAVIGASI HP -->

<div class="bottom-nav">
  <a href="#beranda">🏠<br>Home</a>
  <a href="#peta">📍<br>Peta</a>
  <a href="#cerita">🎧<br>Cerita</a>
  <a href="#mapping">✨<br>Mapping</a>
  <a href="#kuis">🧭<br>Kuis</a>
</div>

<script>
const cerita = [
  {
    judul: "Awal Sebuah Petualangan",
    teks: "Di antara rimbunnya alam, tersembunyi sebuah gua yang menyimpan keindahan dan kisah masa lalu. Mari menjelajah dengan rasa ingin tahu dan tetap menjaga alam."
  },
  {
    judul: "Rahasia Formasi Batu",
    teks: "Selama waktu yang sangat panjang, air dan proses alam membentuk lorong serta ornamen batu yang unik. Setiap lekuk menjadi bukti keajaiban alam."
  },
  {
    judul: "Warisan yang Harus Dijaga",
    teks: "Gua adalah rumah bagi makhluk hidup dan bagian dari warisan alam. Jangan membuang sampah atau merusak formasi batu. Keindahannya harus dijaga bersama."
  }
];

let indexCerita = 0;

function audio() {
  if (!("speechSynthesis" in window)) {
    alert("Browser tidak mendukung fitur audio.");
    return;
  }

  speechSynthesis.cancel();

  const suara = new SpeechSynthesisUtterance(
    cerita[indexCerita].teks
  );

  suara.lang = "id-ID";
  suara.rate = 0.9;

  speechSynthesis.speak(suara);
}

function nextStory() {
  indexCerita = (indexCerita + 1) % cerita.length;

  document.getElementById("judulCerita").textContent =
    cerita[indexCerita].judul;

  document.getElementById("narasi").textContent =
    cerita[indexCerita].teks;

  document.getElementById("nomor").textContent =
    "Cerita " + (indexCerita + 1) + " dari 3";

  document.getElementById("bar").style.width =
    ((indexCerita + 1) / 3 * 100) + "%";

  speechSynthesis.cancel();
}

function setMode(mode) {
  const visual = document.getElementById("visual");
  const label = document.getElementById("mode");

  if (mode === "blue") {
    visual.style.background =
      "radial-gradient(ellipse at 50% 80%, #42c8ff, transparent 60%), #071426";
    label.textContent = "Cahaya Biru";
  }

  if (mode === "purple") {
    visual.style.background =
      "radial-gradient(ellipse at 50% 80%, #b45cff, transparent 60%), #071426";
    label.textContent = "Cahaya Ungu";
  }

  if (mode === "green") {
    visual.style.background =
      "radial-gradient(ellipse at 50% 80%, #3fffd0, transparent 60%), #071426";
    label.textContent = "Aurora";
  }
}

function jawab(benar) {
  const hasil = document.getElementById("hasil");

  if (benar) {
    hasil.textContent =
      "Benar! 🌟 Selalu jaga kelestarian gua.";
    hasil.style.color = "#79f2bd";
  } else {
    hasil.textContent =
      "Belum tepat. Coba pilih tindakan yang menjaga alam.";
    hasil.style.color = "#ffb3a7";
  }
}
</script>

</body>
</html>
