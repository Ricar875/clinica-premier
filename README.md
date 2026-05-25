
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clínica Premier · Multiespecialidades</title>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700;800&family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,600;0,9..144,700;1,9..144,300;1,9..144,600&display=swap" rel="stylesheet">
<style>
:root{
  --mint:#00C9A7;--mint2:#00B896;--mint3:#80EDD9;--mint-pale:#E6FBF7;
  --teal:#0097A7;--teal2:#00838F;
  --white:#FFFFFF;--off:#F7FFFE;
  --dark:#0D2B2A;--dark2:#163330;
  --text:#1A3A38;--text2:#4A6E6B;--text3:#8AADAA;
  --gray:#F0F9F8;--gray2:#E4F4F2;--gray3:#C8E6E3;
  --shadow:0 4px 30px rgba(0,201,167,.12);
  --shadow2:0 12px 60px rgba(0,201,167,.18);
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'Sora',sans-serif;background:var(--white);color:var(--text);overflow-x:hidden;}
nav{position:fixed;top:0;left:0;right:0;z-index:200;padding:0 5vw;background:rgba(255,255,255,.92);backdrop-filter:blur(20px);border-bottom:1px solid var(--gray2);}
.nav-i{max-width:1200px;margin:0 auto;height:66px;display:flex;align-items:center;justify-content:space-between;}
.logo{display:flex;align-items:center;gap:12px;}
.logo-mark{width:40px;height:40px;background:linear-gradient(135deg,var(--mint),var(--teal));border-radius:12px;display:grid;place-items:center;font-size:20px;box-shadow:0 4px 16px rgba(0,201,167,.35);}
.logo-name{font-size:17px;font-weight:700;color:var(--dark);letter-spacing:-.3px;}
.logo-name span{color:var(--mint2);}
.nav-links{display:flex;gap:32px;}
.nav-links a{font-size:13px;font-weight:500;color:var(--text2);text-decoration:none;transition:color .2s;}
.nav-links a:hover{color:var(--mint2);}
.nav-cta{background:var(--dark);color:#fff;font-size:13px;font-weight:600;padding:10px 22px;border-radius:50px;border:none;cursor:pointer;transition:all .25s;}
.nav-cta:hover{background:var(--mint2);transform:translateY(-1px);}
@media(max-width:700px){.nav-links{display:none;}}
.hero{min-height:100vh;padding:100px 5vw 80px;background:linear-gradient(135deg,#E8FDF9 0%,#F5FFFE 40%,#E0FAF5 100%);position:relative;display:flex;align-items:center;overflow:hidden;}
.hero-blob1{position:absolute;top:-180px;right:-180px;width:700px;height:700px;background:radial-gradient(circle,rgba(0,201,167,.12),transparent 65%);pointer-events:none;}
.hero-blob2{position:absolute;bottom:-200px;left:-100px;width:500px;height:500px;background:radial-gradient(circle,rgba(0,151,167,.10),transparent 65%);pointer-events:none;}
.hero-inner{max-width:1200px;margin:0 auto;display:grid;grid-template-columns:1fr 480px;gap:80px;align-items:center;width:100%;}
@media(max-width:900px){.hero-inner{grid-template-columns:1fr;}.hero-visual{display:none;}}
.hero-tag{display:inline-flex;align-items:center;gap:8px;background:var(--mint-pale);border:1px solid var(--mint3);color:var(--mint2);font-size:11px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;padding:7px 16px;border-radius:50px;margin-bottom:24px;}
.hero-tag-dot{width:8px;height:8px;background:var(--mint);border-radius:50%;animation:live 2s ease-in-out infinite;}
@keyframes live{0%,100%{box-shadow:0 0 0 0 rgba(0,201,167,.5)}70%{box-shadow:0 0 0 8px rgba(0,201,167,0)}}
h1{font-family:'Fraunces',serif;font-size:clamp(42px,5.5vw,68px);font-weight:700;color:var(--dark);line-height:1.1;letter-spacing:-1px;margin-bottom:20px;}
h1 em{font-style:italic;color:var(--mint2);}
.hero-desc{font-size:17px;color:var(--text2);line-height:1.75;margin-bottom:40px;max-width:500px;font-weight:300;}
.btns{display:flex;gap:14px;flex-wrap:wrap;}
.btn-main{background:linear-gradient(135deg,var(--mint2),var(--teal));color:#fff;font-size:14px;font-weight:600;padding:16px 32px;border-radius:50px;border:none;cursor:pointer;transition:all .3s;box-shadow:0 8px 30px rgba(0,201,167,.35);display:flex;align-items:center;gap:9px;}
.btn-main:hover{transform:translateY(-3px);}
.btn-ghost{background:transparent;color:var(--dark);font-size:14px;font-weight:600;padding:16px 32px;border-radius:50px;border:2px solid var(--gray3);cursor:pointer;transition:all .3s;}
.btn-ghost:hover{border-color:var(--mint2);color:var(--mint2);}
.hero-nums{display:flex;gap:40px;margin-top:48px;flex-wrap:wrap;}
.hnum-n{font-family:'Fraunces',serif;font-size:36px;font-weight:700;color:var(--dark);line-height:1;}
.hnum-n span{color:var(--mint2);}
.hnum-l{font-size:11px;color:var(--text3);margin-top:4px;letter-spacing:.5px;}
.hero-visual{position:relative;}
.hcard{background:var(--white);border-radius:24px;padding:28px;box-shadow:var(--shadow2);border:1px solid var(--gray2);}
.hcard-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:20px;}
.hcard-title{font-size:12px;font-weight:700;color:var(--text3);letter-spacing:1px;text-transform:uppercase;}
.hcard-live{display:flex;align-items:center;gap:6px;font-size:11px;font-weight:700;color:var(--mint2);}
.dot-live{width:7px;height:7px;border-radius:50%;background:var(--mint);animation:live 1.5s infinite;}
.esp-mini{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;}
.em-item{background:var(--gray);border-radius:14px;padding:16px 10px;text-align:center;transition:all .3s;}
.em-item:hover{background:var(--mint-pale);transform:translateY(-2px);}
.em-icon{font-size:24px;margin-bottom:6px;}
.em-name{font-size:10px;font-weight:600;color:var(--text2);}
.hcard-foot{margin-top:16px;padding-top:16px;border-top:1px solid var(--gray2);display:flex;justify-content:space-between;align-items:center;}
.hcard-avail{font-size:12px;font-weight:600;color:var(--mint2);}
.hcard-link{font-size:12px;font-weight:700;color:var(--dark);text-decoration:none;}
.hcard-link:hover{color:var(--mint2);}
.float-badge{position:absolute;top:-20px;right:-20px;background:var(--dark);color:#fff;border-radius:16px;padding:14px 18px;box-shadow:0 8px 30px rgba(13,43,42,.3);animation:float 4s ease-in-out infinite;}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-8px)}}
.fb-num{font-family:'Fraunces',serif;font-size:28px;font-weight:700;color:var(--mint3);line-height:1;}
.fb-lbl{font-size:10px;color:rgba(255,255,255,.6);}
.sec{padding:90px 5vw;}
.si{max-width:1200px;margin:0 auto;}
.sec-kicker{font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--mint2);margin-bottom:10px;}
.sec-h{font-family:'Fraunces',serif;font-size:clamp(30px,4vw,48px);font-weight:700;color:var(--dark);line-height:1.15;margin-bottom:14px;letter-spacing:-.5px;}
.sec-h em{font-style:italic;color:var(--mint2);}
.sec-p{font-size:15px;color:var(--text2);line-height:1.85;max-width:520px;font-weight:300;}
.classes-sec{background:var(--gray);}
.cls-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:20px;margin-top:52px;}
.cls-card{background:var(--white);border-radius:20px;padding:30px;border:1.5px solid var(--gray2);transition:all .3s;position:relative;overflow:hidden;}
.cls-card:hover{transform:translateY(-5px);box-shadow:var(--shadow2);border-color:var(--mint3);}
.cls-card::after{content:'';position:absolute;top:0;left:0;right:0;height:3px;border-radius:20px 20px 0 0;}
.cls-a::after{background:linear-gradient(90deg,var(--mint),var(--mint3));}
.cls-b::after{background:linear-gradient(90deg,var(--teal),#4DD0E1);}
.cls-c::after{background:linear-gradient(90deg,#43A047,#A5D6A7);}
.cls-d::after{background:linear-gradient(90deg,#FB8C00,#FFCC80);}
.cls-tag{display:inline-block;font-size:10px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;padding:5px 14px;border-radius:50px;margin-bottom:16px;}
.cls-a .cls-tag{background:var(--mint-pale);color:var(--mint2);}
.cls-b .cls-tag{background:#E0F7FA;color:var(--teal);}
.cls-c .cls-tag{background:#F1F8E9;color:#43A047;}
.cls-d .cls-tag{background:#FFF3E0;color:#FB8C00;}
.cls-name{font-family:'Fraunces',serif;font-size:22px;font-weight:700;color:var(--dark);margin-bottom:8px;}
.cls-desc{font-size:13px;color:var(--text2);line-height:1.65;margin-bottom:18px;font-weight:300;}
.cls-list{list-style:none;}
.cls-list li{font-size:12px;color:var(--text2);padding:5px 0;border-bottom:1px solid var(--gray2);display:flex;align-items:center;gap:8px;}
.cls-list li:last-child{border:none;}
.cls-list li::before{content:'';width:6px;height:6px;border-radius:50%;flex-shrink:0;}
.cls-a .cls-list li::before{background:var(--mint2);}
.cls-b .cls-list li::before{background:var(--teal);}
.cls-c .cls-list li::before{background:#43A047;}
.cls-d .cls-list li::before{background:#FB8C00;}
.esp-sec{background:var(--white);}
.esp-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(135px,1fr));gap:12px;margin-top:52px;}
.esp-item{background:var(--gray);border-radius:16px;padding:22px 14px;text-align:center;transition:all .3s;cursor:default;border:1.5px solid transparent;}
.esp-item:hover{background:var(--mint-pale);border-color:var(--mint3);transform:translateY(-3px);}
.esp-ico{font-size:28px;margin-bottom:8px;}
.esp-nm{font-size:11px;font-weight:600;color:var(--text2);line-height:1.4;}
.flow-sec{background:var(--dark);padding:90px 5vw;}
.flow-sec .sec-kicker{color:var(--mint3);}
.flow-sec .sec-h{color:#fff;}
.flow-sec .sec-h em{color:var(--mint3);}
.flow-sec .sec-p{color:rgba(255,255,255,.55);}
.flow-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(190px,1fr));gap:2px;margin-top:52px;}
.fstep{padding:30px 24px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.08);transition:all .3s;}
.fstep:first-child{border-radius:16px 0 0 16px;}
.fstep:last-child{border-radius:0 16px 16px 0;}
.fstep:hover{background:rgba(0,201,167,.08);}
.fstep-n{font-family:'Fraunces',serif;font-size:52px;font-weight:700;color:rgba(255,255,255,.07);line-height:1;margin-bottom:14px;}
.fstep-ico{font-size:26px;margin-bottom:12px;}
.fstep-t{font-size:15px;font-weight:600;color:#fff;margin-bottom:6px;}
.fstep-d{font-size:12px;color:rgba(255,255,255,.5);line-height:1.7;}
.plans-sec{background:var(--gray);}
.plans-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(290px,1fr));gap:20px;margin-top:52px;}
.plan-card{background:var(--white);border-radius:20px;padding:32px;border:1.5px solid var(--gray2);transition:all .3s;}
.plan-card:hover{transform:translateY(-4px);box-shadow:var(--shadow2);}
.plan-card.feat{border-color:var(--mint2);background:linear-gradient(160deg,var(--mint-pale),var(--white));}
.plan-tag{display:inline-flex;align-items:center;gap:6px;font-size:11px;font-weight:700;letter-spacing:1px;text-transform:uppercase;padding:6px 14px;border-radius:50px;margin-bottom:18px;}
.plan-card:not(.feat) .plan-tag{background:var(--gray);color:var(--text2);}
.plan-card.feat .plan-tag{background:var(--mint2);color:#fff;}
.plan-name{font-family:'Fraunces',serif;font-size:24px;font-weight:700;color:var(--dark);margin-bottom:8px;}
.plan-desc{font-size:13px;color:var(--text2);line-height:1.65;margin-bottom:22px;font-weight:300;}
.plan-list{list-style:none;}
.plan-list li{font-size:13px;color:var(--text2);padding:8px 0;border-bottom:1px solid var(--gray2);display:flex;align-items:center;gap:10px;}
.plan-list li:last-child{border:none;}
.plan-list li::before{content:'✓';font-size:11px;font-weight:800;color:var(--mint2);flex-shrink:0;}
.wa-sec{background:var(--white);}
.wa-inner{max-width:1200px;margin:0 auto;display:grid;grid-template-columns:1fr 420px;gap:70px;align-items:center;}
@media(max-width:900px){.wa-inner{grid-template-columns:1fr;}}
.wa-list{margin-top:30px;display:flex;flex-direction:column;gap:12px;}
.wa-row{display:flex;gap:16px;padding:16px 18px;background:var(--gray);border-radius:14px;transition:background .2s;}
.wa-row:hover{background:var(--mint-pale);}
.wa-ico-box{width:44px;height:44px;border-radius:12px;display:grid;place-items:center;font-size:20px;flex-shrink:0;}
.wa-row:nth-child(1) .wa-ico-box{background:var(--mint-pale);}
.wa-row:nth-child(2) .wa-ico-box{background:#E0F7FA;}
.wa-row:nth-child(3) .wa-ico-box{background:#FFF8E1;}
.wa-row:nth-child(4) .wa-ico-box{background:#F3E5F5;}
.wa-rt{font-size:14px;font-weight:600;color:var(--dark);margin-bottom:3px;}
.wa-rd{font-size:12px;color:var(--text2);line-height:1.55;font-weight:300;}
.wa-box{background:var(--dark);border-radius:24px;padding:36px;color:#fff;}
.wa-box-title{font-family:'Fraunces',serif;font-size:26px;font-weight:700;margin-bottom:6px;}
.wa-box-sub{font-size:13px;color:rgba(255,255,255,.55);line-height:1.65;margin-bottom:26px;font-weight:300;}
.wa-num-row{background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.1);border-radius:12px;padding:14px 18px;display:flex;align-items:center;gap:10px;font-size:14px;color:rgba(255,255,255,.6);margin-bottom:10px;}
.wa-num-row strong{color:var(--mint3);font-weight:700;}
.btn-wa{width:100%;margin-top:6px;background:linear-gradient(135deg,#1B5E20,#43A047,#00C853);color:#fff;border:none;border-radius:12px;padding:17px;font-size:13px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:10px;transition:all .3s;box-shadow:0 6px 24px rgba(0,200,83,.3);}
.btn-wa:hover{transform:translateY(-2px);}
.wa-chips{display:flex;flex-wrap:wrap;gap:8px;margin-top:16px;}
.wa-chip{font-size:10px;font-weight:600;padding:5px 13px;border-radius:50px;background:rgba(0,201,167,.15);color:var(--mint3);border:1px solid rgba(0,201,167,.25);}
footer{background:var(--dark2);color:rgba(255,255,255,.5);padding:52px 5vw 36px;text-align:center;}
.ft-logo{font-family:'Fraunces',serif;font-size:22px;font-weight:700;color:#fff;margin-bottom:8px;}
.ft-logo span{color:var(--mint3);}
.ft-text{font-size:13px;line-height:1.9;margin-bottom:24px;}
.ft-copy{font-size:11px;color:rgba(255,255,255,.2);}
@media(max-width:600px){.cls-grid,.flow-grid,.plans-grid{grid-template-columns:1fr;}.fstep:first-child,.fstep:last-child{border-radius:12px;}}
</style>
</head>
<body>
<nav>
  <div class="nav-i">
    <div class="logo"><div class="logo-mark">🏥</div><div class="logo-name">Clínica <span>Premier</span></div></div>
    <div class="nav-links"><a href="#especialidades">Especialidades</a><a href="#classes">Planos</a><a href="#como-funciona">Como Funciona</a><a href="#whatsapp">Contato</a></div>
    <button class="nav-cta" onclick="document.getElementById('whatsapp').scrollIntoView({behavior:'smooth'})">📱 Agendar Consulta</button>
  </div>
</nav>
<section class="hero">
  <div class="hero-blob1"></div><div class="hero-blob2"></div>
  <div class="hero-inner">
    <div>
      <div class="hero-tag"><span class="hero-tag-dot"></span>Atendimento disponível agora</div>
      <h1>Saúde de <em>qualidade</em> para toda a família</h1>
      <p class="hero-desc">Mais de 20 especialidades médicas, agendamento rápido pelo WhatsApp, convênio ou particular.</p>
      <div class="btns">
        <button class="btn-main" onclick="document.getElementById('whatsapp').scrollIntoView({behavior:'smooth'})">💬 Agendar pelo WhatsApp</button>
        <button class="btn-ghost" onclick="document.getElementById('especialidades').scrollIntoView({behavior:'smooth'})">Ver Especialidades →</button>
      </div>
      <div class="hero-nums">
        <div class="hnum"><div class="hnum-n"><span>+</span>20</div><div class="hnum-l">Especialidades</div></div>
        <div class="hnum"><div class="hnum-n">4</div><div class="hnum-l">Planos</div></div>
        <div class="hnum"><div class="hnum-n">24<span>h</span></div><div class="hnum-l">WhatsApp</div></div>
        <div class="hnum"><div class="hnum-n">7<span>×</span></div><div class="hnum-l">Dias/semana</div></div>
      </div>
    </div>
    <div class="hero-visual">
      <div class="float-badge"><div class="fb-num">+20</div><div class="fb-lbl">especialidades</div></div>
      <div class="hcard">
        <div class="hcard-header"><div class="hcard-title">Especialidades em destaque</div><div class="hcard-live"><span class="dot-live"></span>Ao vivo</div></div>
        <div class="esp-mini">
          <div class="em-item"><div class="em-icon">🫀</div><div class="em-name">Cardiologia</div></div>
          <div class="em-item"><div class="em-icon">🧠</div><div class="em-name">Neurologia</div></div>
          <div class="em-item"><div class="em-icon">🦴</div><div class="em-name">Ortopedia</div></div>
          <div class="em-item"><div class="em-icon">👁️</div><div class="em-name">Oftalmologia</div></div>
          <div class="em-item"><div class="em-icon">🌸</div><div class="em-name">Ginecologia</div></div>
          <div class="em-item"><div class="em-icon">🍼</div><div class="em-name">Pediatria</div></div>
        </div>
        <div class="hcard-foot"><div class="hcard-avail">● Médicos disponíveis hoje</div><a href="especialidades-hoje.html" class="hcard-link">Ver todos →</a></div>
      </div>
    </div>
  </div>
</section>
<section class="sec classes-sec" id="classes">
  <div class="si">
    <div class="sec-kicker">Planos de Atendimento</div>
    <h2 class="sec-h">Escolha o plano <em>ideal</em> para você</h2>
    <p class="sec-p">Quatro opções pensadas para cada perfil.</p>
    <div class="cls-grid">
      <div class="cls-card cls-a"><div class="cls-tag">⭐ Classe A</div><div class="cls-name">Premier Gold</div><div class="cls-desc">Atendimento exclusivo com médicos selecionados.</div><ul class="cls-list"><li>Especialista selecionado</li><li>Análises prioritárias</li><li>Canal VIP WhatsApp</li><li>Agendamento em 24h</li><li>Plano premium incluído</li></ul></div>
      <div class="cls-card cls-b"><div class="cls-tag">Classe B</div><div class="cls-name">Executivo Prata</div><div class="cls-desc">Qualidade e agilidade com conforto diferenciado.</div><ul class="cls-list"><li>Especialista disponível</li><li>Análises completas</li><li>WhatsApp dedicado</li><li>Agendamento em 48h</li><li>Convênio aceito</li></ul></div>
      <div class="cls-card cls-c"><div class="cls-tag">Classe C</div><div class="cls-name">Essencial Plus</div><div class="cls-desc">Acesso completo com atendimento humano eficiente.</div><ul class="cls-list"><li>Consultas por especialidade</li><li>Análises básicas</li><li>Chatbot + Humano</li><li>Agendamento flexível</li><li>Convênios populares</li></ul></div>
      <div class="cls-card cls-d"><div class="cls-tag">Classe D</div><div class="cls-name">Acesso Básico</div><div class="cls-desc">Saúde acessível e de qualidade para todos.</div><ul class="cls-list"><li>Consulta clínica geral</li><li>Análises básicas</li><li>Agendamento pelo chatbot</li><li>Convênios básicos</li><li>Triagem e encaminhamento</li></ul></div>
    </div>
  </div>
</section>
<section class="sec esp-sec" id="especialidades">
  <div class="si">
    <div class="sec-kicker">Especialidades Médicas</div>
    <h2 class="sec-h">Mais de 20 <em>especialidades</em> disponíveis</h2>
    <p class="sec-p">Rotatividade planejada de especialistas ao longo da semana.</p>
    <div class="esp-grid">
      <div class="esp-item"><div class="esp-ico">🫀</div><div class="esp-nm">Cardiologia</div></div>
      <div class="esp-item"><div class="esp-ico">🧠</div><div class="esp-nm">Neurologia</div></div>
      <div class="esp-item"><div class="esp-ico">🦴</div><div class="esp-nm">Ortopedia</div></div>
      <div class="esp-item"><div class="esp-ico">👁️</div><div class="esp-nm">Oftalmologia</div></div>
      <div class="esp-item"><div class="esp-ico">🌸</div><div class="esp-nm">Ginecologia</div></div>
      <div class="esp-item"><div class="esp-ico">🍼</div><div class="esp-nm">Pediatria</div></div>
      <div class="esp-item"><div class="esp-ico">🦷</div><div class="esp-nm">Odontologia</div></div>
      <div class="esp-item"><div class="esp-ico">🧪</div><div class="esp-nm">Análises Clínicas</div></div>
      <div class="esp-item"><div class="esp-ico">🩻</div><div class="esp-nm">Radiologia</div></div>
      <div class="esp-item"><div class="esp-ico">💊</div><div class="esp-nm">Clínica Geral</div></div>
      <div class="esp-item"><div class="esp-ico">🧬</div><div class="esp-nm">Endocrinologia</div></div>
      <div class="esp-item"><div class="esp-ico">🫁</div><div class="esp-nm">Pneumologia</div></div>
      <div class="esp-item"><div class="esp-ico">🩸</div><div class="esp-nm">Hematologia</div></div>
      <div class="esp-item"><div class="esp-ico">🦠</div><div class="esp-nm">Infectologia</div></div>
      <div class="esp-item"><div class="esp-ico">🧘</div><div class="esp-nm">Psiquiatria</div></div>
      <div class="esp-item"><div class="esp-ico">🏃</div><div class="esp-nm">Med. Esportiva</div></div>
      <div class="esp-item"><div class="esp-ico">🧴</div><div class="esp-nm">Dermatologia</div></div>
      <div class="esp-item"><div class="esp-ico">👂</div><div class="esp-nm">Otorrinol.</div></div>
      <div class="esp-item"><div class="esp-ico">🦵</div><div class="esp-nm">Fisioterapia</div></div>
      <div class="esp-item"><div class="esp-ico">💉</div><div class="esp-nm">Urologia</div></div>
    </div>
  </div>
</section>
<section class="flow-sec" id="como-funciona">
  <div class="si">
    <div class="sec-kicker">Como Funciona</div>
    <h2 class="sec-h">Do agendamento ao <em>resultado</em></h2>
    <p class="sec-p">Processo simples e rápido, integrado ao WhatsApp.</p>
    <div class="flow-grid">
      <div class="fstep"><div class="fstep-n">01</div><div class="fstep-ico">💬</div><div class="fstep-t">WhatsApp</div><div class="fstep-d">Chatbot ou atendente humano. Resposta em minutos.</div></div>
      <div class="fstep"><div class="fstep-n">02</div><div class="fstep-ico">🏅</div><div class="fstep-t">Escolha o Plano</div><div class="fstep-d">Classes A, B, C ou D.</div></div>
      <div class="fstep"><div class="fstep-n">03</div><div class="fstep-ico">📅</div><div class="fstep-t">Agendamento</div><div class="fstep-d">Escolha especialista e horário.</div></div>
      <div class="fstep"><div class="fstep-n">04</div><div class="fstep-ico">🩺</div><div class="fstep-t">Consulta</div><div class="fstep-d">Atendimento personalizado.</div></div>
      <div class="fstep"><div class="fstep-n">05</div><div class="fstep-ico">📋</div><div class="fstep-t">Resultados</div><div class="fstep-d">Laudos direto no WhatsApp.</div></div>
    </div>
  </div>
</section>
<section class="sec plans-sec">
  <div class="si">
    <div class="sec-kicker">Formas de Pagamento</div>
    <h2 class="sec-h">Particular, Convênio <em>ou Plano</em></h2>
    <p class="sec-p">Atendemos todas as formas. Ninguém fica sem cuidado.</p>
    <div class="plans-grid">
      <div class="plan-card"><div class="plan-tag">💳 Particular</div><div class="plan-name">Atendimento Particular</div><div class="plan-desc">Agilidade máxima, sem burocracia.</div><ul class="plan-list"><li>Todas as especialidades</li><li>Análises completas</li><li>Agendamento imediato</li><li>Resultados digitais</li></ul></div>
      <div class="plan-card feat"><div class="plan-tag">⭐ Convênio</div><div class="plan-name">Convênios Aceitos</div><div class="plan-desc">Aceitamos os principais convênios.</div><ul class="plan-list"><li>Principais convênios aceitos</li><li>Todas as especialidades</li><li>Verificação rápida pelo chat</li><li>Sem cobrança adicional</li></ul></div>
      <div class="plan-card"><div class="plan-tag">❤️ Plano de Saúde</div><div class="plan-name">Planos da Clínica</div><div class="plan-desc">Cobertura nas 4 classes de atendimento.</div><ul class="plan-list"><li>Cobertura total por classe</li><li>Análises incluídas</li><li>Atendimento prioritário</li><li>Canal exclusivo WhatsApp</li></ul></div>
    </div>
  </div>
</section>
<section class="sec wa-sec" id="whatsapp">
  <div class="wa-inner">
    <div>
      <div class="sec-kicker">Atendimento Digital</div>
      <h2 class="sec-h">WhatsApp com <em>Chatbot + Humano</em></h2>
      <p class="sec-p">Inteligência artificial e atendimento humano juntos.</p>
      <div class="wa-list">
        <div class="wa-row"><div class="wa-ico-box">🤖</div><div><div class="wa-rt">Chatbot 24 horas</div><div class="wa-rd">Agendamento automático a qualquer hora.</div></div></div>
        <div class="wa-row"><div class="wa-ico-box">👩‍⚕️</div><div><div class="wa-rt">Atendente Humano Real</div><div class="wa-rd">Nossa equipe assume quando necessário.</div></div></div>
        <div class="wa-row"><div class="wa-ico-box">📋</div><div><div class="wa-rt">Resultados pelo WhatsApp</div><div class="wa-rd">Análises enviadas direto no chat.</div></div></div>
        <div class="wa-row"><div class="wa-ico-box">🏅</div><div><div class="wa-rt">Canal VIP Classe A</div><div class="wa-rd">Resposta prioritária em minutos.</div></div></div>
      </div>
    </div>
    <div class="wa-box">
      <div class="wa-box-title">💬 Fale Conosco Agora</div>
      <div class="wa-box-sub">Agende sua consulta em menos de 2 minutos.</div>
      <div class="wa-num-row">📱 <strong>(75) 3281-3632</strong></div>
      <div class="wa-num-row">📱 <strong>(75) 2018-0098</strong></div>
      <button class="btn-wa" onclick="window.open('https://wa.me/5575328136322','_blank')"><span style="font-size:20px">💬</span> AGENDAR CONSULTA AGORA</button>
      <div class="wa-chips"><span class="wa-chip">✓ Resposta rápida</span><span class="wa-chip">✓ 24h disponível</span><span class="wa-chip">✓ Bot + Humano</span></div>
    </div>
  </div>
</section>
<footer>
  <div class="ft-logo">🏥 Clínica <span>Premier</span></div>
  <div class="ft-text">Multiespecialidades · Particular · Convênio · Planos A · B · C · D</div>
  <div class="ft-copy">© 2026 · Clínica Premier · Todos os direitos reservados</div>
</footer>
</body>
</html>
