<!doctype html>
<html lang="cs">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Honza Novosad — Vědomý pohyb</title>
  <meta name="description" content="Honza Novosad - průvodce vědomým pohybem. Individuální lekce, malé skupiny, facilitace kruhového sdílení a adaptační programy." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#F4F1EB;
      --card:#FFFFFF;
      --text:#253A33;
      --muted:#6B6B6B;
      --accent:#C18F63;
      --sage:#A7C4A0;
      --radius:14px;
      --maxw:1100px;
      --shadow: 0 10px 30px rgba(15,15,15,0.06);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: 'Inter', system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif;
      background:var(--bg);
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.6;
      -webkit-text-size-adjust:100%;
    }
    a{color:inherit}
    .container{max-width:var(--maxw);margin:28px auto;padding:20px}

    /* Header */
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{
      width:64px;height:64px;border-radius:12px;display:flex;align-items:center;justify-content:center;
      font-family:'Playfair Display',serif;font-weight:600;font-size:20px;color:var(--text);
      background:linear-gradient(180deg,var(--sage),#fff);
      box-shadow:var(--shadow);border:1px solid rgba(0,0,0,0.03)
    }
    .brand .meta{line-height:1}
    .nav{display:flex;gap:12px;align-items:center}
    .nav a{padding:8px 10px;border-radius:10px;text-decoration:none;color:var(--muted);font-weight:600}
    .nav a:hover{background:rgba(0,0,0,0.03);color:var(--text)}
    .primary-cta{background:linear-gradient(90deg,var(--accent),#E4C89A);color:white;padding:10px 14px;border-radius:12px;text-decoration:none;font-weight:700}

    /* Hero */
    .hero{
      margin-top:18px;
      display:grid;
      grid-template-columns:1fr 360px;
      gap:24px;
      align-items:center;
    }
    .hero-card{
      background:linear-gradient(180deg,rgba(255,255,255,0.9),rgba(255,255,255,0.8));
      border-radius:16px;padding:28px;box-shadow:var(--shadow)
    }
    h1{font-family:'Playfair Display',serif;font-weight:600;font-size:36px;margin:0}
    .lead {color:var(--muted);margin-top:12px;font-size:17px}
    .hero-cta{margin-top:18px;display:flex;gap:12px;align-items:center}
    .btn{padding:12px 20px;border-radius:999px;border:0;background:var(--accent);color:white;font-weight:700;text-decoration:none}
    .btn-secondary{padding:10px 14px;border-radius:10px;border:1px solid rgba(0,0,0,0.06);background:transparent}

    /* Photo */
    .photo{
      border-radius:12px;overflow:hidden;height:320px;background:linear-gradient(180deg,#fff,#f7f5f2);display:flex;align-items:center;justify-content:center;border:1px solid rgba(0,0,0,0.03);
      box-shadow:0 8px 20px rgba(10,10,10,0.03)
    }
    .photo img{width:100%;height:100%;object-fit:cover;display:block}

    /* Sections */
    section{margin-top:20px;padding:22px;border-radius:12px;background:var(--card);box-shadow:0 8px 20px rgba(10,10,10,0.03)}
    .two-col{display:grid;grid-template-columns:1fr 320px;gap:20px;align-items:start}
    h2{font-family:'Playfair Display',serif;font-size:20px;margin:0 0 10px 0}
    .muted{color:var(--muted)}
    .pill{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(0,0,0,0.03);font-weight:700;font-size:13px}

    .services{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
    .service{padding:12px;border-radius:10px;border:1px solid rgba(0,0,0,0.04);background:linear-gradient(180deg,rgba(167,196,160,0.06),transparent)}

    .timeline{display:flex;flex-direction:column;gap:8px}
    .timeline .item{padding:10px;border-left:3px solid var(--sage);background:rgba(0,0,0,0.01);border-radius:6px}

    .refs blockquote{margin:0;padding:12px;border-left:3px solid var(--accent);color:var(--muted);background:rgba(0,0,0,0.02);border-radius:8px}

    /* Contact */
    form{display:flex;flex-direction:column;gap:10px}
    input,textarea{padding:10px;border-radius:10px;border:1px solid rgba(0,0,0,0.06);font-size:15px}
    button[type="submit"]{padding:12px;border-radius:10px;border:0;background:var(--accent);color:white;font-weight:700}

    footer{margin-top:22px;text-align:center;color:var(--muted);font-size:14px;padding:10px}

    /* Responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr;gap:18px}
      .two-col{grid-template-columns:1fr}
      .services{grid-template-columns:1fr}
      .nav{display:none}
    }
    @media (max-width:420px){
      h1{font-size:28px}
      .photo{height:220px}
    }

    /* Small accessibility helpers */
    a:focus, button:focus, input:focus, textarea:focus{
      outline:3px solid rgba(193,143,99,0.18);outline-offset:3px;border-radius:8px
    }

    /* subtle animations */
    .reveal{opacity:0;transform:translateY(8px);transition:all .6s ease}
    .reveal.show{opacity:1;transform:none}
  </style>
</head>
<body>
  <div class="container" id="page">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden>HN</div>
        <div class="meta">
          <div style="font-weight:800">Honza Novosad</div>
          <div class="muted" style="font-size:13px">Vědomý pohyb · facilitace · průvodce</div>
        </div>
      </div>

      <nav class="nav" aria-label="Hlavní navigace">
        <a href="#o-mne">O mně</a>
        <a href="#sluzby">Služby</a>
        <a href="#projekty">Projekty</a>
        <a href="#kontakt" class="primary-cta">Kontakt</a>
      </nav>
    </header>

    <!-- HERO -->
    <main class="hero" role="main">
      <div class="hero-card reveal" id="heroCard">
        <h1>Vědomý pohyb</h1>
        <p class="lead">Najdi bezpečí v sobě. Návrat k sobě skrze tělo, přírodu a rytmus života. I když „všechno funguje“, mnozí cítí vnitřní prázdno — tady je prostor k návratu k vnímání.</p>

        <div class="hero-cta">
          <a class="btn" href="#kontakt">Domluvit konzultaci</a>
          <a class="btn-secondary" href="#sluzby">Zjistit více</a>
          <div style="margin-left:auto" class="pill">Bezpečí z pohledu nervového systému</div>
        </div>

        <p style="margin-top:14px" class="muted">Jsem průvodce — ne nastavím dlouhodobé rigidní plány. Pracuji v přítomnosti, s respektem k tělu a nervovému systému.</p>
      </div>

      <div class="photo reveal" id="heroPhoto" aria-hidden>
        <!-- Replace src with your photo: e.g. <img src="photo.jpg" alt="Honza Novosad"> -->
        <!-- Placeholder artwork (SVG inline) -->
        <svg width="100%" height="100%" viewBox="0 0 800 600" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Ilustrace přírody">
          <defs>
            <linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="#FDFBF7"/><stop offset="1" stop-color="#EEF3EC"/></linearGradient>
          </defs>
          <rect width="100%" height="100%" fill="url(#g)"/>
          <g transform="translate(40,40)" fill="none" stroke="#A7C4A0" stroke-width="6" stroke-linecap="round" stroke-linejoin="round" opacity="0.9">
            <path d="M20 420 q120 -300 320 -200 q180 80 300 -40" />
            <path d="M10 480 q150 -260 400 -220 q100 10 180 -30" stroke-opacity="0.7"/>
          </g>
          <text x="50%" y="85%" text-anchor="middle" fill="#6B6B6B" font-family="Inter, sans-serif" font-size="14">Fotka / Ilustrace: nahrajte svoji</text>
        </svg>
      </div>
    </main>

    <!-- O MNE -->
    <section id="o-mne" class="reveal">
      <h2>O mně</h2>
      <div class="two-col" style="margin-top:12px">
        <div>
          <p class="muted">Muž, syn svých rodičů, bratr své sestry, otec svých dcer. Působím jako pohybový mentor, terapeut, lektor a facilitátor kruhové komunikace pro děti i dospělé. Nejsem vědec — jsem intuitivní průvodce.</p>
          <p>Prošel jsem cestu od zaměření na výkon k praxi vnímání. Skrze pohyb, dech a respekt k signálům těla vytvářím prostor bezpečí, z něhož může člověk růst. Mým základem je vzdělání FTVS UK a téměř 20 let praxe v pohybu a tréninku.</p>
        </div>

        <aside>
          <div style="font-weight:700;margin-bottom:8px">Moje hodnoty</div>
          <ul style="padding-left:16px;margin:0;color:var(--muted)">
            <li>Důvěra jako východisko</li>
            <li>Bezpečí z hlediska nervového systému</li>
            <li>Respekt k procesu & integritě</li>
          </ul>
        </aside>
      </div>
    </section>

    <!-- Jak pracuji -->
    <section id="how" class="reveal">
      <h2>Jak pracuji</h2>
      <p class="muted">Pracuji v přítomnosti: naslouchám tělu, nabízím nástroje a společně zkoušíme, co funguje. Neplánuji rigidní schémata; vytvářím bezpečný rámec pro samo-regulaci a objevování.</p>

      <div style="margin-top:14px;display:flex;gap:12px;flex-wrap:wrap">
        <div class="pill">Naslouchání</div>
        <div class="pill">Pohyb & Fascie</div>
        <div class="pill">Dech & Rytmus</div>
        <div class="pill">Integrace</div>
      </div>
    </section>

    <!-- Sluzby -->
    <section id="sluzby" class="reveal">
      <h2>Služby & projekty</h2>
      <div class="services" style="margin-top:12px">
        <div class="service">
          <strong>Vědomý pohyb — individuální / párový</strong>
          <p class="muted">60–90 min. Jemné vedení přizpůsobené potřebám těla a mysli.</p>
        </div>

        <div class="service">
          <strong>Malé skupiny (3–6)</strong>
          <p class="muted">Intimní formát, sdílené prožitky, bezpečný rámec.</p>
        </div>

        <div class="service">
          <strong>Týmová práce / kolektivní sporty</strong>
          <p class="muted">Programy zaměřené na koordinaci, rytmus a důvěru v týmu.</p>
        </div>

        <div class="service">
          <strong>Facilitace kruhového sdílení</strong>
          <p class="muted">Mužsko-ženské kruhy, kruhy pro dospívající muže (14–18), kruhy pro muže.</p>
        </div>
      </div>
    </section>

    <!-- Projekty -->
    <section id="projekty" class="reveal">
      <h2>Projekty & adaptační programy</h2>
      <p class="muted">Průvodce adaptačními kurzy pro školy, školy v přírodě a víkendové workshopy vědomého pohybu. Programy jsou interaktivní, bezpečné a koncipované pro věk i potřeby skupiny.</p>
      <ul class="muted" style="margin-top:10px;padding-left:18px">
        <li>Adaptační kurzy: týmová dynamika a komunikace</li>
        <li>Víkendové workshopy: hlubší práce s tělem a dechem</li>
      </ul>
    </section>

    <!-- Zkusenosti -->
    <section id="zkusenosti" class="reveal">
      <h2>Zkušenosti</h2>
      <div class="timeline" style="margin-top:8px">
        <div class="item">
          <strong>FTVS UK</strong> — obor TVS. Téměř 20 let praxe v osobních trénincích a sportovní přípravě (fotbal, moderní gymnastika, závodní aerobik, taneční sporty).
        </div>
        <div class="item">
          <strong>Osobní cesta</strong> — přesun od výkonu k prožívání; komplexní pojetí těla a mysli; práce s fasciemi a nervovým systémem.
        </div>
      </div>
    </section>

    <!-- Reference -->
    <section id="reference" class="refs reveal">
      <h2>Reference</h2>
      <div style="display:grid;gap:10px;margin-top:10px">
        <blockquote>„Díky lekcím jsem poprvé opravdu ucítila své tělo.“ — klientka</blockquote>
        <blockquote>„Cítím se klidnější, jistější a víc sama sebou.“ — klient</blockquote>
      </div>
    </section>

    <!-- FAQ -->
    <section id="faq" class="reveal">
      <h2>Často kladené otázky</h2>
      <p><strong>Musím být sportovec?</strong> Ne. Vědomý pohyb je pro každého — bez ohledu na věk nebo kondici.</p>
      <p><strong>Plánujete dlouhodobě?</strong> Ne. Nepracujeme s rigidními plány; pracuji v přítomnosti a dle toho, co je potřeba.</p>
    </section>

    <!-- Kontakt -->
    <section id="kontakt" class="reveal">
      <h2>Kontakt</h2>
      <p class="muted">Chceš si domluvit konzultaci nebo máš dotaz? Napiš mi — rád se ozvu.</p>

      <div style="display:grid;grid-template-columns:1fr 320px;gap:18px;margin-top:12px">
        <div>
          <form id="contactForm" onsubmit="return handleForm(event)">
            <label class="muted" for="name">Jméno</label>
            <input id="name" placeholder="Vaše jméno" required>

            <label class="muted" for="email">E-mail</label>
            <input id="email" type="email" placeholder="email@example.com" required>

            <label class="muted" for="message">Krátká zpráva</label>
            <textarea id="message" rows="4" placeholder="O co jde?" required></textarea>

            <div style="display:flex;justify-content:space-between;align-items:center">
              <div class="muted" style="font-size:13px">Formulář otevře váš e-mailový klient.</div>
              <button type="submit">Odeslat</button>
            </div>
          </form>
        </div>

        <aside style="padding:12px;border-radius:10px;background:linear-gradient(180deg,rgba(193,143,99,0.06),transparent);border:1px solid rgba(0,0,0,0.03)">
          <div style="font-weight:700;margin-bottom:8px">Kontakt</div>
          <div class="muted">Email</div>
          <div style="margin-bottom:8px"><a href="mailto:YOUR_EMAIL_HERE">YOUR_EMAIL_HERE</a></div>

          <div class="muted">Sociální sítě</div>
          <div style="margin-top:6px"><a href="YOUR_FACEBOOK_OR_IG" target="_blank" rel="noopener">Facebook / Instagram</a></div>

          <div style="margin-top:12px;font-size:13px;color:var(--muted)">Telefon: pokud chceš, doplň sem číslo</div>
        </aside>
      </div>
    </section>

    <footer>
      <div>© <strong>Honza Novosad</strong> — Vědomý pohyb</div>
      <div class="muted">„Naše regenerační schopnost je spojena s hlubokým klidem.“ — Jaroslav Dušek</div>
    </footer>
  </div>

  <script>
    // Smooth reveal on scroll
    function revealOnScroll(){
      document.querySelectorAll('.reveal').forEach(el=>{
        const rect = el.getBoundingClientRect();
        if(rect.top < (window.innerHeight - 80)) el.classList.add('show')
      })
    }
    window.addEventListener('scroll', revealOnScroll);
    window.addEventListener('load', ()=>{
      revealOnScroll();
      // small focus for accessibility: set tabindex on first link
      const firstLink = document.querySelector('.nav a');
      if(firstLink) firstLink.setAttribute('tabindex','0');
    });

    // contact form -> mailto
    function handleForm(e){
      e.preventDefault();
      const name = encodeURIComponent(document.getElementById('name').value.trim());
      const email = encodeURIComponent(document.getElementById('email').value.trim());
      const message = encodeURIComponent(document.getElementById('message').value.trim());
      const subject = encodeURIComponent('Kontakt z webu — ' + (name || 'Neznámý'));
      const body = encodeURIComponent('Jméno: ' + name + '\\nEmail: ' + email + '\\n\\n' + message);
      const mailto = 'mailto:YOUR_EMAIL_HERE?subject=' + subject + '&body=' + body;
      window.location.href = mailto;
      return false;
    }

    // smooth anchor links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', function(e){
        const href = a.getAttribute('href');
        if(href.length>1){
          e.preventDefault();
          const el = document.querySelector(href);
          if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
        }
      })
    });
  </script>
</body>
</html>
