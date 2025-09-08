# Barbie
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Identidad Visual de Barbie — Guía Interactiva</title>
  <meta name="description" content="Página interactiva que explica los elementos visuales de la identidad de Barbie: color, logo, tipografía, packaging, patrones y tono visual." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <!-- Fuentes: cursiva estilo logotipo + sans y display -->
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;600;800&family=Playfair+Display:wght@600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --barbie-pink:#E0218A; /* tono principal icónico */
      --barbie-pink-2:#FF5BBE; /* acento luminoso */
      --barbie-pink-3:#FF8AD6; /* claro */
      --barbie-magenta:#C6007E; /* profundidad para contraste */
      --barbie-black:#111;
      --barbie-white:#fff;
      --ink:#2b2b2b;
      --bg:#fff8fd;
      --card:#ffffff;
      --shadow:0 10px 30px rgba(0,0,0,.08);
      --radius:18px;
      --radius-lg:28px;
    }
    *{box-sizing:border-box}
    html,body{margin:0}
    body{
      font-family:Poppins,system-ui,-apple-system,Segoe UI,Roboto,Arial,Helvetica,sans-serif;
      color:var(--ink);
      background:radial-gradient(1200px 600px at 10% -10%, rgba(255,138,214,.20), transparent),
                 radial-gradient(1000px 500px at 90% 10%, rgba(224,33,138,.15), transparent),
                 var(--bg);
      line-height:1.6;
    }
    a{color:var(--barbie-pink);text-decoration:none}
    header{
      position:sticky;top:0;z-index:50;backdrop-filter:saturate(150%) blur(8px);
      background:linear-gradient(180deg, rgba(255,255,255,.9), rgba(255,255,255,.65));
      border-bottom:1px solid rgba(0,0,0,.06)
    }
    .nav{max-width:1200px;margin:auto;display:flex;gap:20px;align-items:center;padding:12px 20px}
    .brand{font-family:Pacifico,cursive;font-size:30px;color:var(--barbie-pink);letter-spacing:.4px;white-space:nowrap}
    .pill{margin-left:auto;display:flex;gap:8px}
    .pill button{border:0;padding:10px 14px;border-radius:999px;background:var(--card);box-shadow:var(--shadow);cursor:pointer}
    .pill button[aria-pressed="true"]{background:var(--barbie-pink);color:#fff}

    .hero{max-width:1200px;margin:24px auto 40px;display:grid;grid-template-columns:1.2fr .8fr;gap:24px;align-items:center;padding:0 20px}
    .hero-card{background:linear-gradient(135deg, var(--barbie-pink), var(--barbie-pink-2));border-radius:var(--radius-lg);color:#fff;position:relative;overflow:hidden;box-shadow:0 20px 60px rgba(224,33,138,.35)}
    .hero-card::after{content:"";position:absolute;inset:-20% -10%;background:radial-gradient(closest-side, rgba(255,255,255,.35), transparent 70%);transform:rotate(8deg)}
    .hero-content{position:relative;padding:46px}
    .hero h1{font-family:"Playfair Display",serif;font-weight:800;font-size:48px;line-height:1.05;margin:0 0 10px}
    .badge{display:inline-flex;align-items:center;gap:8px;background:rgba(255,255,255,.18);backdrop-filter:blur(6px);border:1px solid rgba(255,255,255,.35);padding:8px 12px;border-radius:999px;font-weight:600}
    .spark{width:8px;height:8px;background:#fff;border-radius:50%;box-shadow:0 0 20px #fff, 0 0 40px #fff}
    .hero p{margin:8px 0 0;font-size:18px;opacity:.95}
    .hero-visual{display:grid;gap:16px}
    .tile{background:var(--card);border-radius:var(--radius);padding:18px;box-shadow:var(--shadow);position:relative;overflow:hidden}
    .tile .label{font-weight:700;font-size:13px;letter-spacing:.5px;text-transform:uppercase;color:#9a3a75}

    .section{max-width:1200px;margin:28px auto;padding:0 20px}
    .section h2{font-family:"Playfair Display",serif;font-size:34px;margin:6px 0 14px}
    .section p.lead{margin-top:0;color:#6b2560}

    /* Tarjetas */
    .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:16px}
    .card{background:var(--card);border-radius:var(--radius);box-shadow:var(--shadow);padding:18px;transition:transform .25s ease, box-shadow .25s ease}
    .card:hover{transform:translateY(-4px);box-shadow:0 14px 34px rgba(0,0,0,.12)}

    /* Paleta */
    .swatches{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:14px;margin-top:12px}
    .swatch{border-radius:14px;overflow:hidden;border:1px solid rgba(0,0,0,.06);cursor:pointer;isolation:isolate}
    .swatch-top{height:90px}
    .swatch-meta{display:flex;justify-content:space-between;align-items:center;padding:10px 12px;background:#fff}
    .copy{font-size:12px;padding:6px 10px;border-radius:999px;border:1px solid rgba(0,0,0,.1);background:#fff;cursor:pointer}
    .copied{background:var(--barbie-pink);color:#fff;border-color:transparent}

    /* Logo: do/don't */
    .logo-show{font-family:Pacifico,cursive;font-size:48px;color:var(--barbie-pink);letter-spacing:.5px;text-shadow:0 6px 20px rgba(224,33,138,.25)}
    .dosdonts{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:16px;margin-top:12px}
    .do{border:2px solid #29a36a}
    .dont{border:2px solid #cc3b3b}
    .flag{font-size:12px;font-weight:700;padding:4px 10px;border-radius:999px}
    .flag.do{background:#29a36a22;color:#10754b}
    .flag.dont{background:#cc3b3b22;color:#a42222}

    /* Tipografías */
    .type-grid{display:grid;grid-template-columns:1.2fr .8fr;gap:18px}
    .sample h3{margin:0}
    .toggle{display:flex;gap:8px;margin-bottom:6px}
    .toggle button{border:0;padding:8px 12px;border-radius:999px;background:#f6e0f0;cursor:pointer}
    .toggle button.active{background:var(--barbie-pink);color:#fff}

    /* Packaging cards con tilt */
    .pack-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
    .pack{perspective:900px}
    .pack .inner{background:linear-gradient(145deg, #fff, #ffe7f5);border:1px solid rgba(0,0,0,.06);border-radius:20px;padding:18px;transform-style:preserve-3d;transition:transform .15s ease, box-shadow .15s ease;box-shadow:var(--shadow)}
    .pack .window{height:130px;border-radius:14px;box-shadow:inset 0 0 0 2px rgba(0,0,0,.06), inset 0 10px 30px rgba(0,0,0,.08);background:repeating-linear-gradient(45deg, #ffd1ea 0 10px, #fff1fa 10px 20px)}
    .pack .cta{display:inline-block;margin-top:10px;padding:8px 12px;border-radius:999px;background:var(--barbie-pink);color:#fff;font-weight:700}

    /* Patrones */
    .pattern-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:12px}
    .pattern{height:120px;border-radius:14px;border:1px solid rgba(0,0,0,.06);background-size:22px 22px}
    .p-hearts{background-image:radial-gradient(circle at 8px 8px, var(--barbie-pink) 5px, transparent 6px)}
    .p-stripes{background-image:repeating-linear-gradient(45deg, var(--barbie-pink) 0 10px, var(--barbie-pink-3) 10px 20px)}
    .p-stars{background-image:radial-gradient(var(--barbie-pink) 2px, transparent 3px), radial-gradient(var(--barbie-pink-2) 2px, transparent 3px);background-position:0 0,11px 11px}

    /* Timeline */
    .timeline{display:grid;grid-auto-flow:column;grid-auto-columns:minmax(260px, 1fr);gap:16px;overflow:auto;padding-bottom:6px}
    .t-card{background:var(--card);border-radius:16px;padding:14px;border:1px solid rgba(0,0,0,.06)}
    .t-year{font-weight:800;color:var(--barbie-magenta)}

    /* Modal */
    dialog{border:0;border-radius:20px;padding:0;box-shadow:0 30px 60px rgba(0,0,0,.25)}
    dialog::backdrop{background:rgba(0,0,0,.4)}
    .modal{padding:16px 18px}
    .modal h3{margin:0 0 8px}

    /* Footer */
    footer{max-width:1200px;margin:40px auto 80px;padding:0 20px;color:#7a5771}

    /* Botón flotante */
    .float{position:fixed;right:16px;bottom:16px;border:0;border-radius:999px;padding:12px 14px;background:var(--barbie-pink);color:#fff;box-shadow:0 14px 34px rgba(224,33,138,.35);cursor:pointer}

    @media (max-width: 880px){
      .hero{grid-template-columns:1fr}
      .type-grid{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <header>
    <nav class="nav" aria-label="Barra de navegación">
      <div class="brand" aria-label="Logotipo estilizado">Barbie</div>
      <div class="pill" role="group" aria-label="Temas de color">
        <button id="themeDefault" aria-pressed="true">Clásico</button>
        <button id="themePop">Pop</button>
        <button id="themeNoir">Noir</button>
      </div>
    </nav>
  </header>

  <main>
    <!-- HERO -->
    <section class="hero" aria-labelledby="tit-hero">
      <article class="hero-card" role="img" aria-label="Gradiente rosa con destellos">
        <div class="hero-content">
          <span class="badge"><span class="spark"></span> Guía interactiva</span>
          <h1 id="tit-hero">Identidad Visual de Barbie</h1>
          <p>Explora los pilares visuales que hacen reconocible a Barbie: color icónico, logotipo, tipografías, packaging, patrones y tono visual. Interactúa con los componentes para ver <em>do’s & don’ts</em>, copiar paletas y probar contrastes.</p>
        </div>
      </article>
      <div class="hero-visual">
        <div class="tile">
          <div class="label">Color Primario</div>
          <div style="height:120px;border-radius:12px;background:linear-gradient(135deg, var(--barbie-pink), var(--barbie-pink-2));box-shadow:inset 0 -20px 40px rgba(0,0,0,.1)"></div>
        </div>
        <div class="tile">
          <div class="label">Tipografía display</div>
          <div style="font-family:Pacifico,cursive;font-size:40px;color:var(--barbie-pink);">Barbie</div>
          <div style="font-size:13px;color:#7a5771">Uso inspiracional del estilo cursivo para titulares.</div>
        </div>
      </div>
    </section>

    <!-- COLOR -->
    <section class="section" aria-labelledby="sec-color">
      <h2 id="sec-color">1) Color: el rosa icónico</h2>
      <p class="lead">La paleta se centra en un rosa vibrante con acentos luminosos y magenta profundo para contraste. Haz clic en cada muestra para <strong>copiar el HEX</strong> y usa el comprobador rápido de contraste.</p>
      <div class="swatches" id="swatches"></div>
      <div class="card" aria-live="polite" style="margin-top:12px">
        <strong>Comprobador rápido WCAG</strong>
        <div style="display:flex;gap:12px;align-items:center;margin-top:8px;flex-wrap:wrap">
          <label>Fondo:
            <select id="bgSelect"></select>
          </label>
          <label>Texto:
            <select id="fgSelect">
              <option value="#000">Negro</option>
              <option value="#fff">Blanco</option>
            </select>
          </label>
          <button id="checkContrast" class="copy">Calcular</button>
          <span id="contrastResult" aria-live="polite"></span>
          <span id="contrastPreview" style="margin-left:auto;padding:6px 12px;border-radius:10px;border:1px solid rgba(0,0,0,.1)">Vista previa</span>
        </div>
      </div>
    </section>

    <!-- LOGO -->
    <section class="section" aria-labelledby="sec-logo">
      <h2 id="sec-logo">2) Logotipo: rasgos y usos</h2>
      <div class="cards">
        <div class="card">
          <div class="logo-show" aria-label="Estilo de logotipo cursivo">Barbie</div>
          <p>El logotipo se percibe <strong>amable, juguetón y femenino</strong>, con curvas fluidas y terminaciones redondeadas. Mantén suficiente respiración alrededor y usa preferentemente el rosa corporativo sobre fondo claro.</p>
          <button class="copy" data-modal="modalLogo">Ver especificaciones</button>
        </div>
        <div class="card do">
          <span class="flag do">Do ✅</span>
          <p style="margin:.5rem 0 0"><strong>Contraste correcto</strong> y tamaño legible. Evita distorsionar la forma del trazo.</p>
          <div style="display:flex;gap:12px;margin-top:10px">
            <div class="tile" style="flex:1;text-align:center"><div class="logo-show">Barbie</div></div>
          </div>
        </div>
        <div class="card dont">
          <span class="flag dont">Don't 🚫</span>
          <p style="margin:.5rem 0 0">No apliques <strong>contornos agresivos</strong>, <strong>degradados oscuros</strong> o deformaciones horizontales.</p>
          <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:10px">
            <div class="tile" style="filter:drop-shadow(0 0 0 #000)"><div class="logo-show" style="-webkit-text-stroke:3px #222;color:transparent">Barbie</div></div>
            <div class="tile"><div class="logo-show" style="transform:skewX(18deg)">Barbie</div></div>
          </div>
        </div>
      </div>
    </section>

    <!-- TIPO -->
    <section class="section" aria-labelledby="sec-type">
      <h2 id="sec-type">3) Tipografías y tono editorial</h2>
      <p class="lead">Titulares expresivos + textos cercanos. Cambia el <em>mood</em> para ver combinaciones sugeridas.</p>
      <div class="type-grid">
        <div class="card sample">
          <div class="toggle" role="tablist" aria-label="Conjuntos tipográficos">
            <button role="tab" class="active" data-pair="playfair">Glam</button>
            <button role="tab" data-pair="poppins">Pop</button>
          </div>
          <div id="typeSample">
            <h3 style="font-family:'Playfair Display',serif;font-size:40px;line-height:1.1">Sueña en rosa</h3>
            <p>Una voz optimista, confiable y divertida. Evita tecnicismos; prioriza mensajes claros, empoderadores y directos.</p>
            <a class="copy" href="#" id="ctaEjemplo">Comprar muñeca</a>
          </div>
        </div>
        <div class="card">
          <strong>Guías rápidas</strong>
          <ul>
            <li>Jerarquía marcada: titulares llamativos + párrafos de 14–18px.</li>
            <li>Botones con esquinas redondeadas y alto contraste.</li>
            <li>Espacios generosos; evita saturar con demasiados gráficos.</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- PACKAGING -->
    <section class="section" aria-labelledby="sec-pack">
      <h2 id="sec-pack">4) Packaging & presentación</h2>
      <p class="lead">Ventana visible del producto, predominio del rosa, brillo sutil y gráficos alegres. Mueve el mouse sobre las cajas.</p>
      <div class="pack-grid">
        <div class="pack">
          <div class="inner" data-tilt>
            <div class="window"></div>
            <h3 style="margin:10px 0 4px">Clásico</h3>
            <p>Fondo claro con acentos rosa y tipografía friendly.</p>
            <span class="cta">Ver detalles</span>
          </div>
        </div>
        <div class="pack">
          <div class="inner" data-tilt>
            <div class="window" style="background:repeating-linear-gradient(135deg,#ffd1ea 0 12px,#fff 12px 24px)"></div>
            <h3 style="margin:10px 0 4px">Edición Pop</h3>
            <p>Patrones diagonales y tonos vibrantes para colecciones.</p>
            <span class="cta">Ver detalles</span>
          </div>
        </div>
        <div class="pack">
          <div class="inner" data-tilt>
            <div class="window" style="background:repeating-linear-gradient(90deg,#ffe3f2 0 8px,#fff 8px 16px)"></div>
            <h3 style="margin:10px 0 4px">Firma</h3>
            <p>Acabados premium y mayor respiración visual.</p>
            <span class="cta">Ver detalles</span>
          </div>
        </div>
      </div>
    </section>

    <!-- PATRONES -->
    <section class="section" aria-labelledby="sec-patterns">
      <h2 id="sec-patterns">5) Patrones e iconografía</h2>
      <p class="lead">Elementos repetitivos alegres: corazones, estrellas, diagonales. Úsalos en fondos o <em>stickers</em> con baja opacidad.</p>
      <div class="pattern-grid">
        <div class="pattern p-hearts" title="Corazones"></div>
        <div class="pattern p-stripes" title="Rayas"></div>
        <div class="pattern p-stars" title="Estrellas"></div>
        <div class="pattern" style="background-image:radial-gradient(circle at 10px 10px, var(--barbie-pink-2) 6px, transparent 7px);"></div>
      </div>
    </section>

    <!-- TIMELINE -->
    <section class="section" aria-labelledby="sec-time">
      <h2 id="sec-time">6) Hitos e interpretación simbólica</h2>
      <p class="lead">Un ícono cultural: moda, diversidad y empoderamiento. Desliza para ver.</p>
      <div class="timeline" id="timeline"></div>
    </section>

    <!-- MODAL ESPECIFICACIONES LOGO -->
    <dialog id="modalLogo">
      <div class="modal">
        <h3>Especificaciones recomendadas</h3>
        <ul>
          <li>Uso preferente: <strong>Rosa principal</strong> sobre fondo claro.</li>
          <li>Área de respeto: altura de la “B” alrededor del logotipo.</li>
          <li>No aplicar contornos pesados, sombras duras ni deformaciones.</li>
          <li>Versiones monocromas: rosa, blanco o negro según contraste.</li>
        </ul>
        <div style="display:flex;gap:8px;justify-content:flex-end;margin-top:8px">
          <button class="copy" data-close>Listo</button>
        </div>
      </div>
    </dialog>
  </main>

  <footer>
    <p><small>Esta es una guía educativa inspirada en la identidad visual de Barbie. “Barbie” es una marca de Mattel. Este recurso no es oficial.</small></p>
  </footer>

  <button class="float" id="toTop" aria-label="Volver arriba">↑</button>

  <script>
    // ===== Utilidades =====
    const $ = (sel, ctx=document) => ctx.querySelector(sel);
    const $$ = (sel, ctx=document) => Array.from(ctx.querySelectorAll(sel));

    // ===== Paleta interactiva =====
    const palette = [
      {name:'Barbie Pink', hex:getComputedStyle(document.documentElement).getPropertyValue('--barbie-pink').trim()},
      {name:'Acento', hex:getComputedStyle(document.documentElement).getPropertyValue('--barbie-pink-2').trim()},
      {name:'Claro', hex:getComputedStyle(document.documentElement).getPropertyValue('--barbie-pink-3').trim()},
      {name:'Magenta Profundo', hex:getComputedStyle(document.documentElement).getPropertyValue('--barbie-magenta').trim()},
      {name:'Blanco', hex:'#ffffff'},
      {name:'Negro', hex:'#111111'},
    ];

    const swatchesEl = $('#swatches');
    const bgSelect = $('#bgSelect');
    const fgSelect = $('#fgSelect');
    const contrastBtn = $('#checkContrast');
    const contrastResult = $('#contrastResult');
    const contrastPreview = $('#contrastPreview');

    function renderSwatches(){
      swatchesEl.innerHTML = '';
      palette.forEach(p=>{
        const sw = document.createElement('div');
        sw.className='swatch';
        sw.innerHTML = `
          <div class="swatch-top" style="background:${p.hex}"></div>
          <div class="swatch-meta"><span>${p.name}</span><button class="copy" data-hex="${p.hex}">${p.hex}</button></div>
        `;
        swatchesEl.appendChild(sw);
      });
      // selects
      bgSelect.innerHTML = palette.map(p=>`<option value="${p.hex}">${p.name}</option>`).join('');
    }

    function copyHex(hex, btn){
      navigator.clipboard.writeText(hex).then(()=>{
        btn.classList.add('copied');
        btn.textContent='Copiado';
        setTimeout(()=>{btn.classList.remove('copied');btn.textContent=hex},1200);
      });
    }

    swatchesEl.addEventListener('click', (e)=>{
      const btn = e.target.closest('button[data-hex]');
      if(btn){ copyHex(btn.dataset.hex, btn); }
    });

    renderSwatches();

    // ===== Contraste rápido (WCAG aprox.) =====
    function luminance(rgb){
      const a = rgb.map(v=>{
        v/=255;return v<=0.03928? v/12.92 : ((v+0.055)/1.055)**2.4;
      });
      return 0.2126*a[0]+0.7152*a[1]+0.0722*a[2];
    }
    function hexToRgb(hex){
      const h = hex.replace('#','');
      return [parseInt(h.substring(0,2),16), parseInt(h.substring(2,4),16), parseInt(h.substring(4,6),16)];
    }
    function contrast(bg, fg){
      const L1 = luminance(hexToRgb(bg));
      const L2 = luminance(hexToRgb(fg));
      const ratio = (Math.max(L1,L2)+0.05)/(Math.min(L1,L2)+0.05);
      return Math.round(ratio*100)/100;
    }
    contrastBtn.addEventListener('click', ()=>{
      const bg = bgSelect.value; const fg = fgSelect.value;
      const ratio = contrast(bg, fg);
      let level = ratio>=7? 'AAA' : ratio>=4.5? 'AA' : 'Insuficiente';
      contrastResult.textContent = `Contraste: ${ratio}:1 — ${level}`;
      contrastPreview.style.background = bg;
      contrastPreview.style.color = fg;
      contrastPreview.textContent = 'Texto de ejemplo';
    });

    // ===== Modal logo =====
    $$('#modalLogo [data-close]').forEach(b=> b.addEventListener('click', ()=> $('#modalLogo').close()));
    $$('[data-modal]').forEach(b=> b.addEventListener('click', ()=> $(`#${b.dataset.modal}`).showModal()));

    // ===== Tipografía: pares =====
    const typePairs = {
      playfair:{titleFont:"'Playfair Display',serif", bodyFont:'Poppins, sans-serif', cta:'¡Lo quiero!'},
      poppins:{titleFont:'Poppins, sans-serif', bodyFont:'Poppins, sans-serif', cta:'Comprar ahora'},
    };
    $$('.toggle button').forEach(btn=>{
      btn.addEventListener('click', ()=>{
        $$('.toggle button').forEach(b=>b.classList.remove('active'));
        btn.classList.add('active');
        const key = btn.dataset.pair; const conf = typePairs[key];
        const sample = $('#typeSample');
        sample.querySelector('h3').style.fontFamily = conf.titleFont;
        sample.querySelector('p').style.fontFamily = conf.bodyFont;
        $('#ctaEjemplo').textContent = conf.cta;
      });
    });

    // ===== Tarjetas con tilt =====
    $$('.pack .inner').forEach(card=>{
      card.addEventListener('mousemove', (e)=>{
        const r = card.getBoundingClientRect();
        const x = e.clientX - r.left; const y = e.clientY - r.top;
        const rx = ((y/r.height)-0.5)*-10; // rotateX
        const ry = ((x/r.width)-0.5)*10;  // rotateY
        card.style.transform = `rotateX(${rx}deg) rotateY(${ry}deg)`;
        card.style.boxShadow = `0 20px 50px rgba(224,33,138,.25)`;
      });
      card.addEventListener('mouseleave', ()=>{
        card.style.transform = 'rotateX(0) rotateY(0)';
        card.style.boxShadow = '';
      });
    });

    // ===== Timeline =====
    const events = [
      {year:1959, text:'Nacimiento de la muñeca Barbie.'},
      {year:1965, text:'Barbie astronauta — aspiracional y de futuro.'},
      {year:1980, text:'Se amplía la diversidad de muñecas.'},
      {year:2016, text:'Cuerpos, tonos de piel y estilos más diversos.'},
      {year:2023, text:'Película impulsa un resurgir del rosa en cultura pop.'}
    ];
    const tl = $('#timeline');
    events.forEach(ev=>{
      const el = document.createElement('div');
      el.className='t-card';
      el.innerHTML = `<div class="t-year">${ev.year}</div><div>${ev.text}</div>`;
      tl.appendChild(el);
    });

    // ===== Modo de color (temas) =====
    const themes = {
      default:{bg:'#fff8fd', ink:'#2b2b2b'},
      pop:{bg:'#fff0f8', ink:'#241225'},
      noir:{bg:'#0e0b0d', ink:'#f3e7f1'}
    };
    function setTheme(key){
      document.documentElement.style.setProperty('--bg', themes[key].bg);
      document.documentElement.style.setProperty('--ink', themes[key].ink);
      $('#themeDefault').setAttribute('aria-pressed', key==='default');
      $('#themePop').setAttribute('aria-pressed', key==='pop');
      $('#themeNoir').setAttribute('aria-pressed', key==='noir');
    }
    $('#themeDefault').addEventListener('click', ()=>setTheme('default'));
    $('#themePop').addEventListener('click', ()=>setTheme('pop'));
    $('#themeNoir').addEventListener('click', ()=>setTheme('noir'));

    // ===== Volver arriba =====
    $('#toTop').addEventListener('click', ()=> window.scrollTo({top:0,behavior:'smooth'}));
  </script>
</body>
</html>
