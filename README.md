<script>
const spotifyLink = "https://open.spotify.com/track/2x3vwXWuecPrRqgEUuSUJA?si=TtoMd6lsQWqItG8DqSEEcA";

const playBtn = document.getElementById('playBtn');
const content = document.getElementById('content');
const poem = document.getElementById('poem');
const heroBg = document.getElementById('heroBg');
const gallery = document.getElementById('gallery');

playBtn.addEventListener('click', (e) => {
  e.preventDefault();

  // 1️⃣ Langsung buka Spotify di tab baru (ini dianggap user gesture)
  const newTab = window.open(spotifyLink, '_blank');

  // 2️⃣ Tampilkan konten setelah sedikit jeda biar tidak ganggu gesture tadi
  setTimeout(() => {
    content.style.display = 'block';
    poem.classList.add('fade-in');

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
  }, 500); // jeda 0.5 detik setelah klik

  // 3️⃣ Fokuskan kembali ke tab ini setelah Spotify terbuka
  if (newTab) newTab.blur();
  window.focus();
});

// Enter juga bisa
playBtn.addEventListener('keyup', (e) => {
  if (e.key === 'Enter') playBtn.click();
});
</script>
