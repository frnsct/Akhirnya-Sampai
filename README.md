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
  --accent:#f7c8d9;
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

.hero-bg{
  position:absolute;
  inset:0;
  background-size:cover;
  background-position:center;
  filter:brightness(0.9) saturate(0.95);
  transition:opacity .8s ease;
  will-change:opacity;
}

.hero-overlay{
  position:absolute;
  inset:0;
  background:linear-gradient(180deg, rgba(247,200,217,0.18), rgba(255,250,250,0.12));
  mix-blend-mode:soft-light;
  pointer-events:none;
}

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

.play-wrap{ display:flex; gap:12px; align-items:center; justify-content:center; margin-top:8px
