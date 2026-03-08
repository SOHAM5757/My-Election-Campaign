# My-Election-Campaign
Vote For Progress Soham Phapale
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vote Soham Phapale | UoB Guild of students Postgraduate Officer</title>
  <style>
    :root{
      --bg:#f7f4ff;
      --bg-soft:#efe8ff;
      --card:#ffffffde;
      --text:#171326;
      --muted:#5f5877;
      --primary:#6d28d9;
      --accent:#ec4899;
      --line:rgba(109,40,217,.14);
      --shadow:0 18px 45px rgba(36,18,80,.14);
      --max:1180px;
    }

    *{ box-sizing:border-box; scroll-behavior:smooth; }

    body{
      margin:0;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      color:var(--text);
      background:linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)),
    url("https://i.ibb.co/h1rWSPjq/your-image.jpg");
        radial-gradient(circle at 12% 10%, #ffffff, transparent 30%),
        radial-gradient(circle at 88% 18%, #f7d9ff, transparent 25%),
        linear-gradient(135deg, var(--bg), var(--bg-soft));
      overflow-x:hidden;
    }

    .orb{
      position:fixed;
      border-radius:50%;
      filter:blur(60px);
      opacity:.28;
      pointer-events:none;
      z-index:0;
    }
    .orb.one{
      width:260px;height:260px;
      background:#d8c0ff;
      top:-60px; left:-80px;
    }
    .orb.two{
      width:320px;height:320px;
      background:#ffc7dd;
      bottom:-110px; right:-90px;
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
      letter-spacing:.2px;
      font-size:1.05rem;
    }

    .brand span{
      color:var(--primary);
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
      background:linear-gradient(135deg, var(--primary), var(--accent));
      box-shadow:0 14px 28px rgba(109,40,217,.24);
    }

    .btn-secondary{
      color:var(--primary);
      background:#fff;
      border:1px solid rgba(109,40,217,.18);
      box-shadow:0 10px 24px rgba(0,0,0,.06);
    }

    .btn:hover{
      transform:translateY(-2px);
    }

    .hero{
      display:grid;
      grid-template-columns: 1.08fr .92fr;
      gap:34px;
      align-items:center;
      padding:26px 0 36px;
      min-height:calc(100vh - 90px);
    }

    .badge{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding:10px 14px;
      border-radius:999px;
      background:#fff;
      border:1px solid var(--line);
      box-shadow:0 10px 24px rgba(0,0,0,.05);
      font-weight:800;
      color:var(--primary);
    }

    .hero h1{
      margin:16px 0 12px;
      font-size:clamp(2.4rem, 5vw, 4.7rem);
      line-height:1.02;
      letter-spacing:-1.4px;
    }

    .hero h1 .grad{
      background:linear-gradient(135deg, var(--primary), var(--accent));
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
      background:#fff;
      border:1px solid var(--line);
      color:var(--muted);
      font-weight:700;
      font-size:.94rem;
    }

    .hero-card{
      position:relative;
      background:linear-gradient(180deg, rgba(255,255,255,.92), rgba(255,255,255,.76));
      border:1px solid rgba(255,255,255,.78);
      border-radius:30px;
      box-shadow:var(--shadow);
      overflow:hidden;
      padding:18px;
      min-height:560px;
    }

    .candidate-photo{
      width:100%;
      height:100%;
      min-height:510px;
      object-fit:cover;
      object-position:center top;
      border-radius:24px;
      display:block;
      background:#ece8f8;
    }

    .photo-tag{
      position:absolute;
      left:28px;
      bottom:28px;
      background:rgba(23,19,38,.84);
      color:#fff;
      padding:16px 18px;
      border-radius:18px;
      backdrop-filter:blur(8px);
      box-shadow:0 12px 24px rgba(0,0,0,.18);
      max-width:calc(100% - 56px);
    }

    .photo-tag strong{
      display:block;
      font-size:1.06rem;
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
      background:var(--card);
      border:1px solid rgba(255,255,255,.75);
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
      background:linear-gradient(135deg, rgba(109,40,217,.14), rgba(236,72,153,.12));
      color:var(--primary);
      margin-bottom:14px;
    }

    .card h3{
      margin:0 0 8px;
      font-size:1.12rem;
    }

    .card p{
      margin:0;
      color:var(--muted);
      line-height:1.6;
      font-size:.98rem;
    }

    .cta{
      margin:34px 0 46px;
      padding:28px;
      border-radius:28px;
      background:linear-gradient(135deg, rgba(109,40,217,.96), rgba(236,72,153,.92));
      color:#fff;
      text-align:center;
      box-shadow:0 20px 45px rgba(109,40,217,.28);
      position:relative;
      overflow:hidden;
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
      color:var(--primary);
      box-shadow:0 10px 24px rgba(0,0,0,.08);
    }

    .no-btn{
      background:rgba(255,255,255,.18);
      color:#fff;
      border:1px solid rgba(255,255,255,.35);
      backdrop-filter:blur(6px);
      position:relative;
    }

    .result{
      margin-top:18px;
      min-height:30px;
      font-weight:900;
      font-size:1.1rem;
    }

    footer{
      padding:0 0 34px;
      text-align:center;
      color:var(--muted);
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
  <div class="orb one"></div>
  <div class="orb two"></div>

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
          src="https://i.ibb.co/Y7Q8qKpS/your-photo.jpg"
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

      <div class="card fade-up" style="max-width:820px; margin:0 auto;">
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
          hue: rand(0, 360),
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
