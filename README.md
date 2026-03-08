# My-Election-Campaign
Vote For Progress Soham Phapale

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vote Soham Phapale | UoB Postgraduate Officer</title>
  <style>
    :root{
      --text:#ffffff;
      --muted:rgba(255,255,255,.88);
      --primary:#111111;
      --accent:#e91e63;
      --accent-2:#ff4f8b;
      --card-bg:rgba(0,0,0,.52);
      --card-border:rgba(255,255,255,.14);
      --shadow:0 20px 50px rgba(0,0,0,.35);
      --max:1180px;
    }

    *{
      box-sizing:border-box;
      scroll-behavior:smooth;
    }

    html, body{
      margin:0;
      padding:0;
    }

    body{
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      color:var(--text);
      background:
        linear-gradient(rgba(12,10,24,.72), rgba(12,10,24,.72)),
        url("https://i.ibb.co/Xk6sqhgw/Whats-App-Image-2026-03-08-at-22-35-08.jpg") center/cover no-repeat fixed;
      overflow-x:hidden;
      min-height:100vh;
    }

    canvas#confetti{
      position:fixed;
      inset:0;
      pointer-events:none;
      z-index:999;
    }

    .container{
      width:min(calc(100% - 32px), var(--max));
      margin:auto;
      position:relative;
      z-index:1;
    }

    .nav{
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:16px;
      padding:20px 0;
    }

    .brand{
      font-weight:900;
      letter-spacing:.3px;
      font-size:1.08rem;
      color:#fff;
    }

    .brand span{
      color:#ff7ab0;
    }

    .nav-links{
      display:flex;
      gap:18px;
      flex-wrap:wrap;
      align-items:center;
    }

    .nav-links a{
      color:var(--muted);
      text-decoration:none;
      font-weight:700;
      font-size:.96rem;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:8px;
      text-decoration:none;
      border:none;
      cursor:pointer;
      padding:14px 20px;
      border-radius:16px;
      font-weight:800;
      font-size:1rem;
      transition:.2s ease;
    }

    .btn-primary{
      color:#fff;
      background:linear-gradient(135deg, var(--accent), var(--accent-2));
      box-shadow:0 14px 28px rgba(233,30,99,.28);
    }

    .btn-secondary{
      color:#fff;
      background:rgba(255,255,255,.08);
      border:1px solid rgba(255,255,255,.18);
      backdrop-filter:blur(8px);
    }

    .btn:hover{
      transform:translateY(-2px);
    }

    .hero{
      display:grid;
      grid-template-columns: 1.05fr .95fr;
      gap:34px;
      align-items:center;
      padding:28px 0 42px;
      min-height:calc(100vh - 90px);
    }

    .badge{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding:10px 14px;
      border-radius:999px;
      background:rgba(255,255,255,.10);
      border:1px solid rgba(255,255,255,.16);
      box-shadow:0 10px 24px rgba(0,0,0,.12);
      font-weight:800;
      color:#fff;
      backdrop-filter:blur(10px);
    }

    .hero h1{
      margin:16px 0 12px;
      font-size:clamp(2.5rem, 5vw, 4.8rem);
      line-height:1.02;
      letter-spacing:-1.4px;
    }

    .hero h1 .grad{
      background:linear-gradient(135deg, #ffffff, #ff9dc3);
      -webkit-background-clip:text;
      background-clip:text;
      color:transparent;
    }

    .hero p{
      margin:0 0 22px;
      max-width:58ch;
      color:var(--muted);
      font-size:1.08rem;
      line-height:1.68;
    }

    .hero-actions{
      display:flex;
      gap:14px;
      flex-wrap:wrap;
      margin-bottom:18px;
    }

    .mini-points{
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      margin-top:12px;
    }

    .pill{
      padding:10px 14px;
      border-radius:999px;
      background:rgba(255,255,255,.08);
      border:1px solid rgba(255,255,255,.16);
      color:#fff;
      font-weight:700;
      font-size:.94rem;
      backdrop-filter:blur(8px);
    }

    .hero-card{
      position:relative;
      background:var(--card-bg);
      border:1px solid var(--card-border);
      border-radius:30px;
      box-shadow:var(--shadow);
      overflow:hidden;
      padding:18px;
      min-height:560px;
      backdrop-filter:blur(10px);
    }

    .candidate-photo{
      width:100%;
      height:100%;
      min-height:510px;
      object-fit:cover;
      object-position:center top;
      border-radius:24px;
      display:block;
      background:#ddd;
    }

    .photo-tag{
      position:absolute;
      left:28px;
      bottom:28px;
      background:rgba(0,0,0,.64);
      color:#fff;
      padding:16px 18px;
      border-radius:18px;
      backdrop-filter:blur(8px);
      box-shadow:0 12px 24px rgba(0,0,0,.18);
      max-width:calc(100% - 56px);
    }

    .photo-tag strong{
      display:block;
      font-size:1.08rem;
      margin-bottom:4px;
    }

    section{
      padding:36px 0 10px;
    }

    .section-head{
      text-align:center;
      max-width:760px;
      margin:0 auto 26px;
    }

    .section-head h2{
      margin:0 0 10px;
      font-size:clamp(1.9rem, 3vw, 2.9rem);
      letter-spacing:-.7px;
    }

    .section-head p{
      margin:0;
      color:var(--muted);
      line-height:1.65;
    }

    .grid{
      display:grid;
      grid-template-columns:repeat(4, 1fr);
      gap:18px;
    }

    .card{
      background:var(--card-bg);
      border:1px solid var(--card-border);
      border-radius:22px;
      padding:22px;
      box-shadow:var(--shadow);
      backdrop-filter:blur(10px);
    }

    .icon{
      width:54px;
      height:54px;
      border-radius:16px;
      display:grid;
      place-items:center;
      font-size:1.35rem;
      background:linear-gradient(135deg, rgba(255,255,255,.18), rgba(255,255,255,.08));
      color:#fff;
      margin-bottom:14px;
    }

    .card h3{
      margin:0 0 8px;
      font-size:1.12rem;
      color:#fff;
    }

    .card p{
      margin:0;
      color:var(--muted);
      line-height:1.6;
      font-size:.98rem;
    }

    .message-card{
      max-width:820px;
      margin:0 auto;
    }

    .cta{
      margin:34px 0 46px;
      padding:28px;
      border-radius:28px;
      background:linear-gradient(135deg, rgba(233,30,99,.92), rgba(17,17,17,.9));
      color:#fff;
      text-align:center;
      box-shadow:0 20px 45px rgba(0,0,0,.34);
      position:relative;
      overflow:hidden;
      border:1px solid rgba(255,255,255,.14);
    }

    .cta h2{
      margin:0 0 10px;
      font-size:clamp(1.8rem, 3vw, 2.7rem);
    }

    .cta p{
      margin:0 auto 18px;
      max-width:58ch;
      line-height:1.65;
      opacity:.95;
    }

    .vote-buttons{
      display:flex;
      justify-content:center;
      gap:14px;
      flex-wrap:wrap;
      min-height:60px;
      position:relative;
    }

    .vote-buttons button{
      border:none;
      cursor:pointer;
      padding:14px 22px;
      border-radius:16px;
      font-weight:800;
      font-size:1rem;
      transition:.2s ease;
    }

    .yes-btn{
      background:#fff;
      color:#111;
      box-shadow:0 10px 24px rgba(0,0,0,.15);
    }

    .no-btn{
      background:rgba(255,255,255,.16);
      color:#fff;
      border:1px solid rgba(255,255,255,.32);
      backdrop-filter:blur(6px);
      position:relative;
    }

    .result{
      margin-top:18px;
      min-height:32px;
      font-weight:900;
      font-size:1.1rem;
      color:#fff;
    }

    footer{
      padding:0 0 34px;
      text-align:center;
      color:rgba(255,255,255,.82);
      font-size:.95rem;
    }

    .fade-up{
      opacity:0;
      transform:translateY(22px);
      transition:all .6s ease;
    }

    .fade-up.show{
      opacity:1;
      transform:translateY(0);
    }

    @media (max-width: 980px){
      .hero,
      .grid{
        grid-template-columns:1fr 1fr;
      }

      .hero-card{
        min-height:auto;
      }

      .candidate-photo{
        min-height:380px;
      }
    }

    @media (max-width: 680px){
      .nav{
        flex-direction:column;
        align-items:flex-start;
      }

      .hero,
      .grid{
        grid-template-columns:1fr;
      }

      .candidate-photo{
        min-height:340px;
      }

      .photo-tag{
        left:18px;
        right:18px;
        bottom:18px;
      }

      .cta{
        padding:24px 18px;
      }
    }
  </style>
</head>
<body>
  <canvas id="confetti"></canvas>

  <div class="container">
    <nav class="nav">
      <div class="brand">Vote <span>SOHAM PHAPALE</span></div>
      <div class="nav-links">
        <a href="#priorities">Priorities</a>
        <a href="#about">Why Me</a>
        <a href="#vote" class="btn btn-primary">Vote Me</a>
      </div>
    </nav>

    <section class="hero">
      <div class="fade-up">
        <div class="badge">UoB Guild Elections • Postgraduate Officer</div>
        <h1>
          <span class="grad">Vote Me</span><br>
          Vote for a stronger postgraduate voice
        </h1>
        <p>
          I’m <strong>SOHAM PHAPALE</strong>, and I’m standing for Postgraduate Officer
          to make sure postgraduate students are heard, supported, and properly represented.
          My focus is simple: practical change, better opportunities, stronger support,
          and a real voice for postgraduates at UoB.
        </p>

        <div class="hero-actions">
          <a href="#vote" class="btn btn-primary">Vote Soham</a>
          <a href="#priorities" class="btn btn-secondary">See My Priorities</a>
        </div>

        <div class="mini-points">
          <span class="pill">Better representation</span>
          <span class="pill">More opportunities</span>
          <span class="pill">Stronger community</span>
          <span class="pill">Postgrad support</span>
        </div>
      </div>

      <div class="hero-card fade-up">
        <img
          class="candidate-photo"
          src="https://i.ibb.co/C58vTXhy/Whats-App-Image-2026-03-08-at-22-35-29.jpg"
          alt="Soham Phapale campaign photo"
        />
        <div class="photo-tag">
          <strong>SOHAM PHAPALE</strong>
          Candidate for UoB Postgraduate Officer
        </div>
      </div>
    </section>

    <section id="priorities">
      <div class="section-head fade-up">
        <h2>My priorities</h2>
        <p>
          A campaign built around what postgraduate students actually need.
        </p>
      </div>

      <div class="grid">
        <div class="card fade-up">
          <div class="icon">🎓</div>
          <h3>Academic support</h3>
          <p>
            Better communication, clearer support systems, and stronger advocacy for postgraduate academic needs.
          </p>
        </div>

        <div class="card fade-up">
          <div class="icon">💼</div>
          <h3>Career opportunities</h3>
          <p>
            More networking, employability events, and useful opportunities for postgraduates after graduation.
          </p>
        </div>

        <div class="card fade-up">
          <div class="icon">🌍</div>
          <h3>International representation</h3>
          <p>
            Stronger support and a louder voice for international postgraduate students across campus.
          </p>
        </div>

        <div class="card fade-up">
          <div class="icon">🤝</div>
          <h3>Community and wellbeing</h3>
          <p>
            A more connected postgraduate experience with better inclusion, events, and wellbeing support.
          </p>
        </div>
      </div>
    </section>

    <section id="about">
      <div class="section-head fade-up">
        <h2>Why vote for me?</h2>
        <p>
          Because postgraduate students deserve representation that is active, visible, and genuinely useful.
        </p>
      </div>

      <div class="card fade-up message-card">
        <h3>My message</h3>
        <p>
          Postgraduates should not feel like an afterthought. Whether you are a taught student,
          researcher, or international student, your voice matters. I’m standing to make sure
          postgraduate issues are heard, acted on, and pushed forward with energy and purpose.
        </p>
      </div>
    </section>

    <section id="vote">
      <div class="cta fade-up">
        <h2>Will you vote for SOHAM PHAPALE?</h2>
        <p>
          For better representation, stronger opportunities, and a postgraduate community that feels heard.
        </p>

        <div class="vote-buttons" id="voteButtons">
          <button class="yes-btn" id="yesBtn">Yes, I’ll vote</button>
          <button class="no-btn" id="noBtn">No</button>
        </div>

        <div class="result" id="result"></div>
      </div>
    </section>

    <footer>
      Built for campaign use • University of Birmingham Postgraduate Officer Election
    </footer>
  </div>

  <script>
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('show');
        }
      });
    }, { threshold: 0.12 });

    document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const result = document.getElementById("result");

    function moveNoButton() {
      const pad = 12;
      const rect = noBtn.getBoundingClientRect();
      const maxX = window.innerWidth - rect.width - pad;
      const maxY = window.innerHeight - rect.height - pad;

      const x = Math.max(pad, Math.random() * maxX);
      const y = Math.max(pad, Math.random() * maxY);

      noBtn.style.position = "fixed";
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
      noBtn.style.zIndex = "1000";
    }

    noBtn.addEventListener("click", (e) => {
      e.preventDefault();
      moveNoButton();
      result.textContent = "Wrong button 😌";
    });

    const canvas = document.getElementById("confetti");
    const ctx = canvas.getContext("2d");
    let confettiPieces = [];
    let running = false;

    function resizeCanvas() {
      canvas.width = window.innerWidth * devicePixelRatio;
      canvas.height = window.innerHeight * devicePixelRatio;
      canvas.style.width = window.innerWidth + "px";
      canvas.style.height = window.innerHeight + "px";
      ctx.setTransform(devicePixelRatio, 0, 0, devicePixelRatio, 0, 0);
    }

    window.addEventListener("resize", resizeCanvas);
    resizeCanvas();

    function rand(min, max) {
      return Math.random() * (max - min) + min;
    }

    function burstConfetti(count = 220) {
      confettiPieces = [];
      const cx = window.innerWidth / 2;
      const cy = window.innerHeight / 3;

      for (let i = 0; i < count; i++) {
        confettiPieces.push({
          x: cx + rand(-60, 60),
          y: cy + rand(-20, 20),
          vx: rand(-7, 7),
          vy: rand(-12, -4),
          g: rand(0.18, 0.34),
          r: rand(3, 7),
          a: rand(0, Math.PI * 2),
          va: rand(-0.2, 0.2),
          life: rand(70, 120),
          hue: rand(0, 360)
        });
      }

      if (!running) {
        running = true;
        requestAnimationFrame(tickConfetti);
      }
    }

    function tickConfetti() {
      ctx.clearRect(0, 0, window.innerWidth, window.innerHeight);

      confettiPieces.forEach(p => {
        p.vy += p.g;
        p.x += p.vx;
        p.y += p.vy;
        p.a += p.va;
        p.life -= 1;

        ctx.save();
        ctx.translate(p.x, p.y);
        ctx.rotate(p.a);
        ctx.fillStyle = `hsl(${p.hue} 90% 55%)`;
        ctx.fillRect(-p.r, -p.r, p.r * 2.2, p.r * 1.4);
        ctx.restore();
      });

      confettiPieces = confettiPieces.filter(p => p.life > 0 && p.y < window.innerHeight + 40);

      if (confettiPieces.length > 0) {
        requestAnimationFrame(tickConfetti);
      } else {
        running = false;
        ctx.clearRect(0, 0, window.innerWidth, window.innerHeight);
      }
    }

    yesBtn.addEventListener("click", () => {
      result.textContent = "Great choice! 🎉";
      burstConfetti(260);
    });
  </script>
</body>
</html>
