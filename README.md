[17_steps_of_you_final.html](https://github.com/user-attachments/files/23003258/17_steps_of_you_final.html)
<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>17 Steps of You — Fransisko for Ankgita</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#fffaf9;
  --card:#ffffff;
  --accent:#f7c8d9; /* soft pink */
  --muted:#7a6f78;
  --text:#2b2b2b;
  --soft:#f3e9e9;
}
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family: 'Montserrat', sans-serif;
  background:linear-gradient(180deg, #fffaf9 0%, #fff 100%);
  color:var(--text);
  display:flex;
  align-items:center;
  justify-content:center;
  padding:20px;
}

.container{
  width:100%;
  max-width:980px;
  background:var(--card);
  border-radius:20px;
  box-shadow: 0 18px 40px rgba(30,20,40,0.06);
  overflow:hidden;
}

.hero{
  position:relative;
  min-height:420px;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:36px;
  background:linear-gradient(180deg, rgba(255,255,255,0.6), rgba(255,250,250,0.6));
}

/* background main image */
.hero-bg{
  position:absolute;
  inset:0;
  background-size:cover;
  background-position:center;
  filter:brightness(0.9) saturate(0.95);
  transition:opacity .8s ease;
  will-change:opacity;
}

/* soft pink overlay */
.hero-overlay{
  position:absolute;
  inset:0;
  background:linear-gradient(180deg, rgba(247,200,217,0.18), rgba(255,250,250,0.12));
  mix-blend-mode:soft-light;
  pointer-events:none;
}

/* floating gentle sparkle */
.sparkle{
  position:absolute;
  inset:0;
  pointer-events:none;
  background-image: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.35) 0px, transparent 40px),
                    radial-gradient(circle at 80% 60%, rgba(255,255,255,0.22) 0px, transparent 30px);
  opacity:0;
  animation: sparkleIn 1.2s forwards .6s;
}
@keyframes sparkleIn{ to{opacity:1} }

.header-content{
  position:relative;
  z-index:3;
  text-align:center;
  max-width:78%;
}
.title{
  font-family:'Playfair Display', serif;
  font-size:34px;
  margin:0;
  color:#3d2f36;
  letter-spacing:0.6px;
}
.subtitle{
  margin:8px 0 18px 0;
  color:var(--muted);
  font-style:italic;
  font-size:15px;
}

/* play button */
.play-wrap{ display:flex; gap:12px; align-items:center; justify-content:center; margin-top:8px; }
.play-btn{
  background:linear-gradient(180deg, #fffbfd, var(--accent));
  border:1px solid rgba(200,160,180,0.18);
  padding:12px 16px;
  border-radius:999px;
  cursor:pointer;
  box-shadow: 0 8px 20px rgba(155,124,168,0.06);
  font-weight:600;
  display:inline-flex;
  gap:10px;
  align-items:center;
  transition:transform .18s ease, box-shadow .18s ease;
}
.play-btn:active{ transform:translateY(2px); }
.play-cta{ font-size:14px; color:#3c2b2f; }
.play-sub{ font-size:12px; color:var(--muted); opacity:0.9; }

/* main content */
.content{
  padding:28px;
  display:flex;
  gap:28px;
  align-items:flex-start;
  flex-direction:column;
}

/* photo gallery slide */
.gallery{ display:flex; gap:16px; align-items:center; justify-content:center; flex-wrap:wrap; }
.thumb{
  width:220px; height:150px; border-radius:12px; overflow:hidden;
  box-shadow:0 10px 30px rgba(30,20,40,0.06);
  background:#eee; display:flex; align-items:center; justify-content:center;
  transition:transform .6s cubic-bezier(.2,.9,.3,1), opacity .6s;
}
.thumb img{ width:100%; height:100%; object-fit:cover; display:block; }

.caption{ color:var(--muted); font-size:14px; text-align:center; margin-top:8px; }

/* typewriter text */
.poem{
  max-width:720px;
  margin:14px auto 6px auto;
  font-size:16px;
  line-height:1.7;
  color:#3b2f34;
  min-height:84px;
  opacity:0;
  transform:translateY(6px);
  transition:opacity .6s ease, transform .6s ease;
  white-space:pre-line;
}

/* closing polaroid */
.polaroid-wrap{ display:flex; gap:12px; align-items:center; justify-content:center; margin-top:18px; }
.polaroid{
  width:260px; border-radius:12px; overflow:hidden; background:#fff; padding:12px; box-shadow:0 16px 40px rgba(30,20,40,0.07);
  text-align:center;
}
.polaroid img{ width:100%; height:180px; object-fit:cover; display:block; border-radius:8px; }
.footer-note{ font-size:13px; color:var(--muted); margin-top:10px; text-align:center; }

/* small responsive */
@media (max-width:720px){
  .title{ font-size:26px; }
  .thumb{ width:48%; height:140px; }
  .polaroid{ width:95%; }
}

/* entry animations */
.fade-in{ animation:fadeUp .8s ease forwards; }
@keyframes fadeUp{ to{ opacity:1; transform:none } }

</style>
</head>
<body>
<div class="container" role="main" aria-label="17 Steps of You">
  <header class="hero" id="hero">
    <div class="hero-bg" id="heroBg" style="background-image:url('IMG_5865.jpeg');"></div>
    <div class="hero-overlay"></div>
    <div class="sparkle"></div>

    <div class="header-content">
      <h1 class="title">17 Steps of You</h1>
      <p class="subtitle">Tujuh belas langkah yang menjadikanmu lembut seperti cahaya.</p>

      <div class="play-wrap">
        <button class="play-btn" id="playBtn" aria-label="Tap to play">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" style="transform:translateX(2px)"><path d="M5 3v18l15-9L5 3z" fill="#3b2b2f"/></svg>
          <div style="text-align:left">
            <div class="play-cta">Tap to listen • Semua Aku Dirayakan</div>
            <div class="play-sub">by Nadin Amizah — tap once to open Spotify</div>
          </div>
        </button>
      </div>
    </div>
  </header>

  <section class="content" id="content" style="display:none">
    <div class="poem" id="poem">
Tujuh belas tahun kau menari dalam semesta,
menyalakan lembut cahaya di tiap tapak langkahmu.

Dunia barangkali tak pernah siap menyambut indahnya keberadaanmu,
tapi aku—aku bersyukur semesta sempat mempertemukan kita.

Hari ini bukan sekadar ulang tahunmu,
tapi perayaan kecil atas bagaimana kau membuat dunia terasa lebih tenang.
    </div>

    <div class="gallery" id="gallery">
      <div class="thumb"><img src="866C9A92-C232-4B3F-8235-6701E0C83902.jpeg" alt="photo1"></div>
      <div class="thumb"><img src="809733C2-7F69-4F7F-9D9C-675E0E154F7E.jpeg" alt="photo2"></div>
      <div class="thumb"><img src="729054C0-8DAB-4797-B818-932EABDB05AC.jpeg" alt="photo3"></div>
      <div class="thumb"><img src="B0AA8983-A9ED-4BFB-AC20-67FCDBE6D2B4.jpeg" alt="photo4"></div>
    </div>

    <div class="caption">Dari pagi yang terang, sampai senyum yang diam-diam nyala di matamu.</div>

    <div class="polaroid-wrap">
      <div class="polaroid">
        <img src="IMG_5865.jpeg" alt="polaroid">
        <div class="footer-note">
          Selamat ulang tahun, Ankgita Oktora.<br>
          Tujuh belas tahun, tujuh belas cara dunia jatuh cinta padamu.<br>
          <strong>crafted by Fransisko Totti</strong>
        </div>
      </div>
    </div>
  </section>
</div>

<script>
<script>
const spotifyLink = "https://open.spotify.com/track/2x3vwXWuecPrRqgEUuSUJA?si=TtoMd6lsQWqItG8DqSEEcA";

const playBtn = document.getElementById('playBtn');
const content = document.getElementById('content');
const poem = document.getElementById('poem');
const heroBg = document.getElementById('heroBg');
const gallery = document.getElementById('gallery');

playBtn.addEventListener('click', (e) => {
  e.preventDefault();

  // buka Spotify dulu (karena butuh interaksi langsung biar ga diblok)
  window.open(spotifyLink, '_blank');

  // tampilkan konten setelah jeda kecil biar animasi tetap smooth
  content.style.display = 'block';

  setTimeout(() => {
    poem.classList.add('fade-in');
  }, 300);

  const thumbs = Array.from(gallery.querySelectorAll('.thumb'));
  thumbs.forEach((t, i) => {
    t.style.opacity = 0;
    t.style.transform = 'translateY(8px)';
    setTimeout(() => {
      t.style.opacity = 1;
      t.style.transform = 'none';
      t.style.transition = 'all .7s cubic-bezier(.2,.9,.3,1)';
    }, 400 + i * 200);
  });

  heroBg.style.opacity = 0.24;
});

// accessibility: biar bisa tekan Enter juga
playBtn.addEventListener('keyup', (e) => {
  if (e.key === 'Enter') playBtn.click();
});
</script>


</script>

</body>
</html>
