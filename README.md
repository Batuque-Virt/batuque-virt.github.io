<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Kylria Melissa — Seus Olhos, Meu Tudo</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500;1,600&family=Playfair+Display:ital,wght@0,600;0,800;1,600;1,800&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-deep:#0a2c2e;
    --bg-mid:#103e41;
    --turquoise:#3fd9d3;
    --turquoise-soft:#a8ece8;
    --turquoise-dim: rgba(63,217,211,0.18);
    --cream:#fbf5ea;
    --ink:#163433;
    --red:#e63950;
    --gold:#e6c98f;
  }

  *{ margin:0; padding:0; box-sizing:border-box; }

  html{ scroll-behavior:smooth; }

  body{
    font-family:'Jost', sans-serif;
    background:var(--bg-deep);
    color:var(--cream);
    overflow-x:hidden;
  }

  /* ============ FLOATING HEARTS ============ */
  .hearts-field{
    position:fixed; inset:0; pointer-events:none; z-index:50; overflow:hidden;
  }
  .floating-heart{
    position:absolute; bottom:-10vh; color:var(--red);
    animation: floatUp linear infinite;
    filter: drop-shadow(0 0 6px rgba(230,57,80,0.35));
  }
  @keyframes floatUp{
    0%{ transform: translateY(0) translateX(0) rotate(0deg); opacity:0; }
    8%{ opacity:.75; }
    85%{ opacity:.6; }
    100%{ transform: translateY(-115vh) translateX(40px) rotate(25deg); opacity:0; }
  }

  /* ============ HERO ============ */
  .hero{
    position:relative; min-height:100vh; padding: 4rem 0;
    display:flex; align-items:center; justify-content:center;
    overflow:hidden;
    background: radial-gradient(circle at center, var(--bg-mid) 0%, var(--bg-deep) 100%);
  }
  .hero-overlay{
    position:absolute; inset:0; z-index: 1;
    background:
      linear-gradient(180deg, rgba(10,44,46,0.2) 0%, rgba(10,44,46,0.4) 55%, rgba(10,44,46,0.95) 100%),
      radial-gradient(ellipse at center, rgba(63,217,211,0.12) 0%, rgba(10,44,46,0.4) 70%);
    pointer-events: none;
  }
  .hero-content{
    position:relative; z-index:2; text-align:center; padding:0 24px;
    display:flex; flex-direction:column; align-items:center; gap:18px;
    width: 100%;
    max-width: 900px;
  }
  .hero-ballerina{
    width:64px; height:64px; opacity:.85;
    filter: drop-shadow(0 0 10px rgba(63,217,211,0.5));
  }
  .eyebrow{
    font-family:'Jost', sans-serif; font-weight:400; letter-spacing:0.35em;
    text-transform:uppercase; font-size:0.78rem; color:var(--turquoise-soft);
  }
  .hero-content h1{
    font-family:'Playfair Display', serif; font-weight:800;
    font-size:clamp(2.8rem, 9vw, 6.2rem); line-height:1.05;
    color:var(--cream); text-shadow:0 4px 30px rgba(0,0,0,0.4);
  }
  .hero-content h1 em{
    font-style:italic; font-weight:600; color:var(--turquoise);
  }
  .hero-sub{
    font-family:'Cormorant Garamond', serif; font-style:italic; font-weight:500;
    font-size:clamp(1.05rem, 2.4vw, 1.45rem); color:var(--turquoise-soft);
    max-width:520px; letter-spacing:0.02em;
  }

  /* Container do vídeo com a altura controlada e responsiva */
  .video-container {
    width: 100%;
    max-width: 800px;
    margin: 1.5rem 0;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 20px 50px rgba(0,0,0,0.5);
    border: 1px solid var(--turquoise-dim);
    aspect-ratio: 16 / 9;
  }
  .video-container iframe {
    width: 100% !important;
    height: 100% !important;
  }

  .hero-divider{
    width:1px; height:40px; background:linear-gradient(180deg, var(--turquoise), transparent);
    margin-top:8px; animation: pulseLine 2.6s ease-in-out infinite;
  }
  @keyframes pulseLine{ 0%,100%{opacity:.3;} 50%{opacity:1;} }

  .scroll-cue{
    margin-top: 10px;
    font-family:'Jost', sans-serif;
    font-size:0.7rem; letter-spacing:0.3em; text-transform:uppercase;
    color:var(--turquoise-soft);
    animation: bob 2.4s ease-in-out infinite;
    text-shadow: 0 2px 8px rgba(0,0,0,0.8);
  }
  @keyframes bob{ 0%,100%{ transform:translateY(0); } 50%{ transform:translateY(6px); } }

  /* ============ POEM SECTION ============ */
  .poem-section{
    position:relative; background:
      radial-gradient(ellipse at 18% 12%, rgba(63,217,211,0.10) 0%, transparent 45%),
      radial-gradient(ellipse at 85% 80%, rgba(230,57,80,0.08) 0%, transparent 40%),
      var(--bg-mid);
    padding:7rem 1.5rem 8rem; display:flex; flex-direction:column; align-items:center;
    overflow:hidden;
  }
  .stardust{ position:absolute; inset:0; pointer-events:none; }
  .star{
    position:absolute; width:3px; height:3px; border-radius:50%;
    background:var(--turquoise-soft); animation: twinkle ease-in-out infinite;
  }
  @keyframes twinkle{ 0%,100%{opacity:.15; transform:scale(1);} 50%{opacity:1; transform:scale(1.6);} }

  .ribbon{ position:absolute; top:0; left:50%; transform:translateX(-50%);
    height:100%; width:min(900px, 100%); opacity:.5; pointer-events:none; }

  .section-head{
    text-align:center; margin-bottom:3.2rem; position:relative; z-index:2;
  }
  .section-head .eyebrow{ color:var(--turquoise); }
  .section-head h2{
    font-family:'Playfair Display', serif; font-style:italic; font-weight:600;
    font-size:clamp(1.8rem, 4.5vw, 3rem); color:var(--cream); margin-top:0.6rem;
  }

  .poem-card{
    position:relative; z-index:2; max-width:680px; width:100%;
    background:var(--cream); color:var(--ink);
    border-radius:6px 28px 6px 28px;
    padding:clamp(2.2rem, 5vw, 4rem);
    box-shadow:0 30px 70px -25px rgba(0,0,0,0.55), 0 0 0 1px rgba(63,217,211,0.15);
    transform:rotate(-0.6deg);
  }
  .poem-card::before{
    content:'“';
    position:absolute; top:-2.6rem; left:1.6rem;
    font-family:'Playfair Display', serif; font-size:6.5rem; font-weight:800;
    color:var(--turquoise); opacity:.5; line-height:1;
  }
  .poem-title{
    font-family:'Playfair Display', serif; font-style:italic; font-weight:700;
    font-size:clamp(1.6rem, 4vw, 2.4rem); color:var(--red);
    margin-bottom:1.4rem; letter-spacing:0.01em;
  }
  .poem-text{
    font-family:'Cormorant Garamond', serif; font-size:clamp(1.08rem, 2.1vw, 1.32rem);
    line-height:1.85; color:var(--ink); text-align:justify;
  }
  .poem-text + .poem-text{ margin-top:1.3rem; }
  .poem-closing{
    margin-top:2.2rem; padding-top:1.6rem; border-top:1px solid var(--turquoise-dim);
    font-family:'Playfair Display', serif; font-style:italic; font-weight:800;
    font-size:clamp(1.3rem, 3vw, 1.8rem); color:var(--turquoise); text-align:right;
  }
  .poem-closing span{ color:var(--red); }
  .poem-signoff{
    margin-top:1.6rem; text-align:right; font-family:'Cormorant Garamond', serif;
    font-style:italic; font-size:1.05rem; color:#5a8c8a;
  }

  /* ============ GALLERY ============ */
  .gallery-section{
    position:relative; background:var(--bg-deep);
    padding:6.5rem 1.5rem 7.5rem;
    display:flex; flex-direction:column; align-items:center;
  }
  .mosaic{
    width:100%; max-width:1040px;
    display:grid; grid-template-columns: 1.4fr 1fr; grid-template-rows: 1fr 1fr;
    gap:1.1rem; height:min(640px, 80vw);
  }
  .frame{
    position:relative; overflow:hidden; border-radius:4px;
    border:1px solid var(--turquoise-dim);
    box-shadow:0 25px 60px -30px rgba(0,0,0,0.7);
  }
  .frame::after{
    content:''; position:absolute; inset:0; pointer-events:none;
    border:1px solid rgba(251,245,234,0.08); border-radius:4px;
    box-shadow: inset 0 0 0 10px rgba(10,44,46,0.0);
  }
  .frame-1{ grid-row: 1 / 3; grid-column: 1; }
  .frame-2{ grid-row: 1; grid-column: 2; }
  .frame-3{ grid-row: 2; grid-column: 2; }

  .mosaic-img{
    position:absolute; inset:0; width:100%; height:100%; object-fit:cover;
    opacity:0; filter:blur(0); transform:scale(1) translateX(0); transition:none;
    will-change: opacity, filter, transform;
  }
  .mosaic-img.active{
    opacity:1; filter:blur(0px); transform:scale(1) translateX(0);
    transition: opacity 1s ease-in-out, filter 1s ease-in-out, transform 1s ease-in-out;
  }
  .mosaic-img.exiting{
    opacity:0; filter:blur(26px); transform:scale(1.08) translateX(-6%);
    transition: opacity 1s ease-in-out, filter 1s ease-in-out, transform 1s ease-in-out;
  }
  .mosaic-img.prep{
    opacity:0; filter:blur(26px); transform:scale(1.08) translateX(6%);
    transition:none;
  }
  .frame-label{
    position:absolute; bottom:14px; left:16px; z-index:3;
    font-family:'Cormorant Garamond', serif; font-style:italic; font-size:0.95rem;
    color:var(--cream); letter-spacing:0.05em; opacity:.85;
    text-shadow:0 2px 10px rgba(0,0,0,0.6);
    display:flex; align-items:center; gap:6px;
  }
  .frame-label svg{ width:14px; height:14px; flex-shrink:0; }

  /* ============ FOOTER ============ */
  .site-footer{
    position:relative; background:
      linear-gradient(180deg, var(--bg-deep), #062021);
    text-align:center; padding:5rem 1.5rem 4rem;
  }
  .footer-mark{ width:46px; height:46px; margin:0 auto 1.4rem; opacity:.9; }
  .site-footer h3{
    font-family:'Playfair Display', serif; font-style:italic; font-weight:700;
    font-size:clamp(1.4rem, 3.4vw, 2.1rem); color:var(--turquoise-soft);
    margin-bottom:0.6rem;
  }
  .site-footer p{
    font-family:'Cormorant Garamond', serif; font-size:1.05rem; color:#9fc9c7;
    max-width:420px; margin:0 auto;
  }
  .footer-date{
    margin-top:1.6rem; font-family:'Jost', sans-serif; font-size:0.7rem;
    letter-spacing:0.35em; text-transform:uppercase; color:var(--turquoise);
    opacity:.7;
  }

  @media (max-width: 700px){
    .mosaic{
      grid-template-columns: 1fr; grid-template-rows: repeat(3, 220px);
      height:auto;
    }
    .frame-1{ grid-row:1; grid-column:1; }
    .frame-2{ grid-row:2; grid-column:1; }
    .frame-3{ grid-row:3; grid-column:1; }
    .poem-card{ border-radius:6px 18px 6px 18px; }
  }

  @media (prefers-reduced-motion: reduce){
    .floating-heart, .star, .scroll-cue, .hero-divider{ animation:none !important; }
    .mosaic-img{ transition:none !important; }
  }
</style>
</head>
<body>

<!-- floating hearts -->
<div class="hearts-field" id="heartsField"></div>

<!-- ============ HERO ============ -->
<section class="hero">
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <svg class="hero-ballerina" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
      <circle cx="50" cy="18" r="8" stroke="#3fd9d3" stroke-width="3"/>
      <path d="M50 26 V52" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round"/>
      <path d="M50 32 C32 28, 22 14, 16 10" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
      <path d="M50 32 C68 28, 80 16, 86 14" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
      <path d="M50 52 C40 64, 34 78, 30 92" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
      <path d="M50 52 C66 58, 80 70, 88 60" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
      <path d="M44 53 C50 60, 56 60, 60 53" stroke="#3fd9d3" stroke-width="30.4" fill="none"/>
    </svg>
    <span class="eyebrow">Feliz dia dos Namorados</span>
    <h1>Kylria <em>Melissa</em></h1>
    
    <!-- Texto Superior -->
    <p class="hero-sub">Para a bailarina que transformou meus dias em tons de castanho — esta página é sua.</p>
    
    <!-- Vídeo com a URL corrigida usando youtube-nocookie + a ID do seu vídeo -->
    <div class="video-container">
      <iframe 
        width="100%" 
        height="600" 
        src="https://www.youtube-nocookie.com/embed/aheql99E4EQ" 
        title="KYEME" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
        referrerpolicy="strict-origin-when-cross-origin" 
        allowfullscreen>
      </iframe >
    </div>

    <!-- Divisor Visual Dinâmico -->
    <div class="hero-divider"></div>
    
    <!-- Texto Inferior -->
    <div class="scroll-cue">AMASSEI NESSE PRESENTE</div>
  </div>
</section>

<!-- ============ poeminha ============ -->
<section class="poem-section">
  <div class="stardust" id="stardust"></div>
  <svg class="ribbon" viewBox="0 0 400 1000" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="ribbonGrad" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0" stop-color="#3fd9d3" stop-opacity="0"/>
        <stop offset="0.15" stop-color="#3fd9d3" stop-opacity="0.55"/>
        <stop offset="0.85" stop-color="#3fd9d3" stop-opacity="0.55"/>
        <stop offset="1" stop-color="#3fd9d3" stop-opacity="0"/>
      </linearGradient>
    </defs>
    <path d="M40 0 C 360 120, 40 260, 360 420 C 80 600, 380 760, 60 1000"
          stroke="url(#ribbonGrad)" stroke-width="2" fill="none"/>
  </svg>

  <div class="section-head">
    <span class="eyebrow">Para você</span>
    <h2>um poema, em tons de castanho</h2>
  </div>

  <article class="poem-card">
    <h3 class="poem-title">Seus olhos...</h3>

    <p class="poem-text">Como neutrinos vindos da mais distante estrela me atravessa com tanta facilidade quanto você tem de me fazer viajar em suas palavras. Eu em meio a cidade de pedra que bane o sol de minhas vistas, que é lar de tão solitários e dolorosos lamentos. Encontrei em você a luz refletida como uma noite estrelada, repleta de magia e poesia. Mostrando me as mais lindas cores no mundo em tons castanhos.</p>

    <p class="poem-text">Trazendo com seus aos meus, aquela que não sei mais enxergar. Tirando me de dias em tons de sombras e iluminando lugares que há muito não reconheço mas chamo de lar. Fuligem sob minhas roupas formam uma verdadeira armadura moderna que não são capazes de sequer tornar minhas vestes tão pesadas quanto meus dias longe de seus olhos.</p>

    <p class="poem-text">Moro sozinho pois quem me enxerga está tão longe quanto as montanhas. E nesse mundo de pessoas cegas para o que há de importante, sorte tive um dia. De ser castanho, de me enxergar castanho, de me ver no universe único dentro de seus olhos.</p>

    <p class="poem-text">Pois nesse mundo repleto de cegos para o que há de importante, viver o poema de nossas histórias e escolhas refletidas e iluminadas pela luz da fogueira, que aquece nossos corpos e nossa noite repleta de dança com palavras de amor que ninguém além de nós seria capaz de ouvir de nossas bocas caladas, é vida, é castanho.</p>

    <p class="poem-text">A maior e melhor aventura. Incapaz de riscar o amor em meu peito.</p>

    <div class="poem-closing">Seus olhos. <span>Meu tudo.</span></div>
    <div class="poem-signoff">— para Kylria Melissa</div>
  </article>
</section>

<!-- ============ GALLERY ============ -->
<section class="gallery-section">
  <div class="section-head">
    <span class="eyebrow">Memórias em movimento</span>
    <h2>cada giro, um instante seu</h2>
  </div>

  <div class="mosaic">
    <div class="frame frame-1" id="frame1">
      <span class="frame-label">
        <svg viewBox="0 0 24 24" fill="#e63950"><path d="M12 21s-7.5-4.5-9.6-9.1C1 8.7 2.7 6 5.6 6c1.7 0 3.1.9 4 2.2C10.5 6.9 11.9 6 13.6 6c2.9 0 4.6 2.7 3.2 5.9C19.5 16.5 12 21 12 21z"/></svg>
        primeira luz
      </span>
    </div>
    <div class="frame frame-2" id="frame2">
      <span class="frame-label">
        <svg viewBox="0 0 24 24" fill="#e63950"><path d="M12 21s-7.5-4.5-9.6-9.1C1 8.7 2.7 6 5.6 6c1.7 0 3.1.9 4 2.2C10.5 6.9 11.9 6 13.6 6c2.9 0 4.6 2.7 3.2 5.9C19.5 16.5 12 21 12 21z"/></svg>
        passos de dança
      </span>
    </div>
    <div class="frame frame-3" id="frame3">
      <span class="frame-label">
        <svg viewBox="0 0 24 24" fill="#e63950"><path d="M12 21s-7.5-4.5-9.6-9.1C1 8.7 2.7 6 5.6 6c1.7 0 3.1.9 4 2.2C10.5 6.9 11.9 6 13.6 6c2.9 0 4.6 2.7 3.2 5.9C19.5 16.5 12 21 12 21z"/></svg>
        olhos castanhos
      </span>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer class="site-footer">
  <svg class="footer-mark" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
    <circle cx="50" cy="18" r="8" stroke="#3fd9d3" stroke-width="3"/>
    <path d="M50 26 V52" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round"/>
    <path d="M50 32 C32 28, 22 14, 16 10" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
    <path d="M50 32 C68 28, 80 16, 86 14" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
    <path d="M50 52 C40 64, 34 78, 30 92" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
    <path d="M50 52 C66 58, 80 70, 88 60" stroke="#3fd9d3" stroke-width="3" stroke-linecap="round" fill="none"/>
  </svg>
  <h3>Feliz Dia dos Namorados, meu amor.</h3>
  <p>Em cada cidade de pedra, você é a luz refletida</p>
  <p>castanho, turquesa e amor pelo meu caminho...</p>

  <div class="footer-date">para Kylria Melissa por Ygor...</div>
</footer>

<script>
  // ---------- corações ----------
  const heartsField = document.getElementById('heartsField');
  const HEART_COUNT = 16;
  for(let i=0;i<HEART_COUNT;i++){
    const h = document.createElement('div');
    h.className = 'floating-heart';
    h.innerHTML = '&#10084;';
    const size = 10 + Math.random()*22;
    h.style.left = (Math.random()*100) + 'vw';
    h.style.fontSize = size + 'px';
    h.style.opacity = (0.25 + Math.random()*0.4).toFixed(2);
    const duration = 14 + Math.random()*16;
    h.style.animationDuration = duration + 's';
    h.style.animationDelay = (-Math.random()*duration) + 's';
    heartsField.appendChild(h);
  }

  // ---------- poeira estelar ----------
  const stardust = document.getElementById('stardust');
  const STAR_COUNT = 50;
  for(let i=0;i<STAR_COUNT;i++){
    const s = document.createElement('div');
    s.className = 'star';
    s.style.left = (Math.random()*100) + '%';
    s.style.top = (Math.random()*100) + '%';
    const dur = 2 + Math.random()*4;
    s.style.animationDuration = dur + 's';
    s.style.animationDelay = (-Math.random()*dur) + 's';
    const scale = 0.5 + Math.random()*1.5;
    s.style.transform = 'scale(' + scale + ')';
    stardust.appendChild(s);
  }

  // ---------- LINKS DO IMGUR ----------
  const IMAGES = [
    "https://i.imgur.com/PuRHrci.jpeg",
    "https://i.imgur.com/szbF6Qt.jpeg",
    "https://i.imgur.com/ayUwiDQ.jpeg",
    "https://i.imgur.com/5Xsimv3.jpeg",
    "https://i.imgur.com/im3zJny.jpeg",
    "https://i.imgur.com/B4KLkRq.jpeg",
    "https://i.imgur.com/4wk7NmW.jpeg",
    "https://i.imgur.com/sen0jgt.jpeg",
    "https://i.imgur.com/V4Ciwvj.jpeg",
    "https://i.imgur.com/TKfqXjL.jpeg"
  ];

  const FRAME_SETS = [
    [IMAGES[0], IMAGES[3], IMAGES[6], IMAGES[9]],
    [IMAGES[1], IMAGES[4], IMAGES[7]],
    [IMAGES[2], IMAGES[5], IMAGES[8]]
  ];

  const TRANSITION_MS = 1000;
  const DISPLAY_MS = 5000;
  const CYCLE_MS = TRANSITION_MS + DISPLAY_MS;

  function buildFrame(frameEl, urls){
    urls.forEach((url, i) => {
      const img = document.createElement('img');
      img.className = 'mosaic-img';
      img.src = url;
      img.alt = 'Kylria Melissa';
      img.loading = 'lazy';
      if(i === 0) img.classList.add('active');
      frameEl.appendChild(img);
    });
  }

  function runFrame(frameEl, urls, startDelay){
    if(urls.length < 2) return;
    let idx = 0;
    const imgs = frameEl.querySelectorAll('.mosaic-img');

    function cycle(){
      const current = idx;
      const next = (idx + 1) % imgs.length;
      const curEl = imgs[current];
      const nextEl = imgs[next];

      nextEl.classList.add('prep');
      void nextEl.offsetWidth;

      requestAnimationFrame(() => {
        curEl.classList.remove('active');
        curEl.classList.add('exiting');
        nextEl.classList.remove('prep');
        nextEl.classList.add('active');
      });

      setTimeout(() => {
        curEl.classList.remove('exiting');
      }, TRANSITION_MS);

      idx = next;
    }

    setTimeout(() => {
      cycle();
      setInterval(cycle, CYCLE_MS);
    }, startDelay);
  }

  ['frame1','frame2','frame3'].forEach((id, i) => {
    const el = document.getElementById(id);
    const urls = FRAME_SETS[i];
    buildFrame(el, urls);
    runFrame(el, urls, i * 2000);
  });
</script>
</body>
</html>
