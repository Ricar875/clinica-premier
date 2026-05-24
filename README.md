<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clínica Premier · Cartão de Cavaleiro Digital</title>
<link href=" https://fonts.googleapis.com/css2?family= Cormorant +Garamond:ital,wght@ 0,300;0,400;0,600;0,700;1,300; 1,600 &family=Cinzel:wght@400; 600;700&family=DM+Sans:wght@ 300;400;500&display=swap " rel="stylesheet">
<style>
:raiz{
  --ouro: #C9A84C;
  --gold2: #E8C96A;
  --gold3: #F5E6B0;
  --dourado-dim: #8B6914;
  --preto: #080808;
  --preto2: #0F0F0F;
  --preto3: #161616;
  --black4: #1E1E1E;
  --black5: #252525;
  --branco: #FFFFFF;
  --creme: #F5ECD7;
  --silenciado: #7A6E5F;
  --border: rgba(201,168,76,0.18);
  --border2: rgba(201,168,76,0.35);
  --brilho: rgba(201,168,76,0.12);
}

*{margin:0;padding:0;box- sizing:border-box;}
html{scroll-behavior:smooth;}
corpo{
  família de fontes:'DM Sans',sans-serif;
  fundo:var(--preto);cor: var(--creme);
  overflow-x:oculto;
}

/* ── Textura de grão ── */
corpo::após{
  conteúdo:'';posição:fixa; inserção:0;
  background-image:url("data: image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns=' http://www.w3.org/2000/ svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/ filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E" );
  eventos-ponteiro:nenhum;índice-z: 9999;
}

/* ── Divisor de linha dourado ── */
.regra-de-ouro{
  largura:100%;altura:1px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
  margem:0;
}

/* ══════════════════════════════ ══
   HERÓI
══════════════════════════════ ══ */
.herói{
  posição:relativa;
  altura mínima: 100vh;
  exibir:flex;flex-direction: coluna;
  alinhar-itens:centro;justificar- conteúdo:centro;
  preenchimento: 80px 24px 100px;
  fundo:var(--preto);
  overflow:oculto;
}
/* brilhos radiais */
.hero::before{
  conteúdo:'';posição:absoluta;
  topo:-20%;esquerda:50%;transformar: translateX(-50%);
  largura:900px;altura:600px; raio da borda:50%;
  fundo:gradiente radial( elipse,rgba(201,168,76,.09) 0%,transparente 65%);
  eventos-ponteiro:nenhum;
}
/* acento inferior */
.herói::depois{
  conteúdo:'';posição:absoluta;
  inferior:0;esquerda:0;direita:0; altura:1px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
}

/* orbes flutuantes */
.esfera{
  posição:absoluta;borda- raio:50%;
  fundo:gradiente radial( círculo,rgba(201,168,76,.07), transparente 70%);
  animação:orb-float ease-in-out infinita;
}
.orb1{largura:300px;altura: 300px;topo:5%;esquerda:-80px; duração da animação:9s;}
.orb2{largura:200px;altura: 200px;topo:10%;direita:-60px; duração da animação:7s; atraso da animação:-4s;}
.orb3{largura:400px;altura: 400px;inferior:-100px;direita:- 100px;duração da animação:11s; atraso da animação:-2s;}
@keyframes orb-float{0%,100%{transform: translateY(0) scale(1)}50%{transform: translateY(-25px) scale(1.04)}}

/* enfeites de canto */
.corner{position:absolute; width:80px;height:80px;}
.corner svg{largura:100%;altura:100%;}
.c-tl{top:24px;left:24px;}
.c-tr{top:24px;right:24px; transform:scaleX(-1);}
.c-bl{bottom:24px;left:24px; transform:scaleY(-1);}
.c-br{bottom:24px;right:24px; transform:scale(-1);}

.hero-eyebrow{
  família-da-fonte:'Cinzel', serifada;
  tamanho da fonte: 10px; espaçamento entre letras: 6px; cor: var(--dourado);
  text-transform:maiúsculas;
  borda:1px var sólido(--border2);
  preenchimento:7px 24px;raio da borda:50px;
  margem-inferior:28px;
  animação: subida .9s suavizar ambos;
  fundo:rgba(201,168,76,. 04);
}

.título-do-herói{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho-da-fonte:clamp(46px,10vw, 96px);
  peso da fonte: 700;
  cor:var(--branco);
  alinhamento-texto:centrado;
  altura-da-linha:1;
  margem-inferior:10px;
  animação: subida .9s .1s suavização ambos;
}
.hero-title .italic{
  estilo da fonte: itálico; peso da fonte: 300;
  cor:var(--gold2);
  exibir:bloco;
}

.hero-tagline{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte:clamp(14px,3vw,20px) ;
  peso da fonte: 300; estilo da fonte: itálico;
  cor:var(--muted);
  alinhamento-texto:centrado;
  margem-inferior:48px;
  espaçamento entre letras: 1px;
  animação: subida .9s .2s suavização ambos;
}

/* estatísticas */
.hero-stats{
  display:flex;gap:clamp(24px, 5vw,64px);
  margem-inferior:52px;
  animação: subida .9s .3s suavização ambos;
}
.hstat{text-align:center;}
.hstat-n{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte:clamp(28px,6vw,48px) ;peso da fonte:600;
  cor:var(--gold2); altura da linha:1;
}
.hstat-l{
  tamanho da fonte: 10px; espaçamento entre letras: 2px;
  cor:var(--muted);text- transform:maiúsculas;
  margem-superior:5px;
}
.sep{width:1px;background:var( --border);align-self:stretch;}

/* cta */
.hero-cta{
  display:flex;flex-wrap:wrap; gap:16px;justify-content: center;
  animação: subida .9s .4s suavização ambos;
}
.btn-gold{
  plano de fundo: gradiente linear ( 135 graus, var (--gold-dim), var (-- gold), var (--gold2), var (--gold) );
  tamanho-de-fundo:300% 100%;
  cor:var(--preto);
  família-da-fonte:'Cinzel', serifada;
  tamanho da fonte: 11px; espaçamento entre letras: 3px;
  borda:nenhuma;preenchimento:16px 36px;raio da borda:4px;cursor: ponteiro;
  box-shadow:0 8px 32px rgba(201,168,76,.3);
  transição:todos os .35s;transformação de texto:maiúsculas;
  animação:deslocamento dourado 4s linear infinito;
}
@keyframes gold-shift{0%{background- position:0%}100%{background- position:300%}}
.btn-gold:hover{transform: translateY(-3px);box-shadow:0 16px 48px rgba(201,168,76,.45);}

.btn-outline{
  fundo: transparente;
  cor:var(--dourado);
  família-da-fonte:'Cinzel', serifada;
  tamanho da fonte: 11px; espaçamento entre letras: 3px;
  borda:1px var sólido(--border2);
  preenchimento: 16px 36px; raio da borda: 4px; cursor: ponteiro;
  transição:todos os .35s;transformação de texto:maiúsculas;
}
.btn-outline:hover{background: var(--glow);transform: translateY(-3px);}

@keyframes rise{from{opacity:0;transform: translateY(28px)}to{opacity:1; transform:translateY(0)}}

/* pílula de rolagem */
.scroll-pill{
  posição:absoluta;inferior:36px; esquerda:50%;transformação:translateX( -50%);
  display:flex;flex-direction: column;align-items:center;gap: 8px;
  cor:var(--muted);tamanho da fonte: 9px;espaçamento entre letras:3px; transformação do texto:maiúsculas;
}
.scroll-dot{
  largura: 1px; altura: 40px;
  fundo:linear-gradient( 180deg,var(--gold), transparente);
  animação:gotejamento 2s, entrada e saída suaves, infinito;
}
@keyframes drip{0%{transform:scaleY(0); transform-origin:top}50%{ transform:scaleY(1);transform- origin:top}51%{transform- origin:bottom}100%{transform: scaleY(0);transform-origin: bottom}}


/* ══════════════════════════════ ══
   SEÇÃO COMUM
══════════════════════════════ ══ */
.sec{posição:relativa; índice z:1;}
.inner{max-width:1000px; margin:0 auto;padding:80px 24px;}

.sec-eye{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 5px;
  cor:var(--dourado);texto- transform:maiúsculas;margem- inferior:12px;
  display:flex;align-items: center;gap:12px;
}
.sec-eye::before{content:''; width:32px;height:1px; background:var(--gold);}

.sec-h{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: clamp(30px,6vw,52px) ; peso da fonte: 600;
  cor:var(--white); altura da linha:1.1;margem inferior:14px;
}
.sec-h em{font-style:italic;color: var(--gold2);}
.sec-p{font-size:15px;color: var(--muted);line-height:1.9; max-width:520px;font-weight: 300;}


/* ══════════════════════════════ ══
   CLASSES ABCD
══════════════════════════════ ══ */
.classes-sec{background:var(-- black2);}
.classes-grid{
  exibir:grade;
  grid-template-columns:repeat( auto-fill,minmax(220px,1fr));
  espaço: 2px;
  margem-superior:48px;
  borda: 1px var sólido (--borda);
  raio-da-borda:2px;
  overflow:oculto;
}
.cls{
  preenchimento: 36px 28px;
  posição:relativa;overflow: oculto;
  transição: todos os .4s;
  cursor:padrão;
  fundo:var(--black3);
}
.cls::before{
  conteúdo:'';posição:absoluta; inserção:0;
  fundo:linear-gradient( 135deg,rgba(201,168,76,.06), transparente);
  opacidade:0;transição:opacidade .4s;
}
.cls::after{
  contente:'';
  posição:absoluta;topo:0;esquerda: 0;direita:0;altura:3px;
  transição: todos os .4s;
}
.cls:hover{background:var(-- black4);}
.cls:hover::before{opacity:1;}

/* cores da barra superior específicas da classe */
.cls-a::after{background: linear-gradient(90deg,#C9A84C, #F5E6B0,#C9A84C);}
.cls-b::after{background: linear-gradient(90deg,#94A3B8, #CBD5E1,#94A3B8);}
.cls-c::after{background: linear-gradient(90deg,#78716C, #A8A29E,#78716C);}
.cls-d::after{background: linear-gradient(90deg,#44403C, #78716C,#44403C);}

.cls-letter{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 64px; peso da fonte: 700; estilo da fonte: itálico;
  altura da linha: 1; margem inferior: 8px;
  opacidade: 0,15; posição: absoluta; topo: 16px; direita: 20px;
}
.cls-a .cls-letter{color:var(--gold2) ;}
.cls-b .cls-letter{color:#94A3B8;}
.cls-c .cls-letter{color:#78716C;}
.cls-d .cls-letter{color:#44403C;}

.cls-badge{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 3px;
  text-transform:uppercase; padding:4px 12px;border-radius:2px;
  display:inline-block;margin- bottom:16px;
}
.cls-a .cls-badge{background:rgba( 201,168,76,.15);color:var(-- gold2);border:1px solid rgba(201,168,76,.3);}
.cls-b .cls-badge{background:rgba( 148,163,184,.1);color:#CBD5E1; border:1px solid rgba(148,163,184,.25);}
.cls-c .cls-badge{background:rgba( 120,113,108,.1);color:#A8A29E; border:1px solid rgba(120,113,108,.25);}
.cls-d .cls-badge{background:rgba(68, 64,60,.15);color:#78716C; border:1px solid rgba(68,64,60,.3);}

.cls-name{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 22px; peso da fonte: 600; cor: var(--white);
  margem-inferior:6px;
}
.cls-sub{font-size:11px;color: var(--muted);line-height:1.6; margin-bottom:20px;}
.cls-items{list-style:none;}
.cls-items li{
  tamanho da fonte: 12px; cor: rgba(255, 255, 255, 0,6);
  padding:5px 0;border-bottom:1px solid rgba(255,255,255,.04);
  display:flex;align-items: center;gap:8px;
}
.cls-items li::before{content:'◆';font- size:5px;flex-shrink:0;}
.cls-a .cls-items li::before{color:var(--gold);}
.cls-b .cls-items li::before{color:#94A3B8;}
.cls-c .cls-items li::before{color:#78716C;}
.cls-d .cls-items li::before{color:#44403C;}

.cls-price{
  margem-superior:20px;
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 13px; estilo da fonte: itálico;
  cor:var(--muted);
}
.cls-a .cls-price{color:var(--gold);}


/* ══════════════════════════════ ══
   ESPECIALIDADES
══════════════════════════════ ══ */
.esp-sec{background:var(-- black);}
.esp-grid{
  exibir:grade;
  grid-template-columns:repeat( auto-fill,minmax(120px,1fr));
  espaço:1px;
  margem-superior:48px;
  borda: 1px var sólido (--borda);
}
.esp{
  preenchimento: 20px 14px;
  alinhamento-texto:centrado;
  fundo:var(--black2);
  transição:todos .3s;cursor:padrão;
  posição:relativa;overflow: oculto;
}
.esp::antes{
  conteúdo:'';posição:absoluta; inferior:0;esquerda:0;direita:0; altura:1px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
  transformar:escalaX(0); transição:transformar .4s;
}
.esp:hover{background:var(-- black3);}
.esp:hover::before{transform: scaleX(1);}
.esp-icon{font-size:24px; margin-bottom:8px;filter: grayscale(30%);}
.esp-name{font-size:11px; color:rgba(255,255,255,.6); line-height:1.3;}

.live-badge{
  display:inline-flex;align- items:center;gap:8px;
  fundo:rgba(201,168,76,. 08);borda:1px sólida var(--border2);
  preenchimento:6px 18px;raio da borda:2px;
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 3px;
  cor:var(--dourado);margem-superior: 20px;
}
.live-dot{largura:6px;altura: 6px;borda-raio:50%; fundo:var(--gold2);
  box-shadow:0 0 6px var(--gold2);animation:pulse 1.5s ease-in-out infinite;}
@keyframes pulse{0%,100%{opacity:1; transform:scale(1)}50%{ opacity:.4;transform:scale(.8) }}


/* ══════════════════════════════ ══
   FLUXO (COMO FUNCIONA)
══════════════════════════════ ══ */
.flow-sec{
  fundo:var(--black2);
  border-top:1px var sólido(--border);
  border-bottom:1px var sólido(--border);
}
.flow-steps{
  exibir:grade;
  grid-template-columns:repeat( auto-fill,minmax(200px,1fr));
  lacuna:0;
  margem-superior:48px;
  borda: 1px var sólido (--borda);
}
.fstep{
  preenchimento: 32px 24px;
  borda-direita:1px sólida var(--borda);
  posição:relativa;transição: fundo .3s;
}
.fstep:last-child{border- right:none;}
.fstep:hover{background:rgba( 201,168,76,.03);}
.fstep-n{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 56px; peso da fonte: 700; estilo da fonte: itálico;
  cor:rgba(201,168,76,.12); altura da linha:1; margem inferior: 16px;
}
.fstep-icon{font-size:22px; margin-bottom:10px;}
.fstep-title{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 18px; peso da fonte: 600; cor: var(--white);
  margem-inferior:6px;
}
.fstep-desc{font-size:12px; color:var(--muted);line- height:1.7;}
/* seta de conexão na área de trabalho */
.fstep::after{
  conteúdo:'→';
  posição:absoluta;topo:50%; direita:-12px;transformação: translateY(-50%);
  cor:var(--gold-dim); tamanho da fonte:14px;índice z:2;
}
.fstep:last-child::after{ display:none;}


/* ══════════════════════════════ ══
   PLANOS / FORMAS DE ATENDIMENTO
══════════════════════════════ ══ */
.plans-sec{background:var(-- black);}
.planos-grade{
  exibir:grade;
  grid-template-columns:repeat( auto-fill,minmax(260px,1fr));
  espaço:1px;
  margem-superior:48px;
  borda: 1px var sólido (--borda);
}
.plano{
  preenchimento: 36px 28px;
  fundo:var(--black2);
  posição:relativa;overflow: oculto;
  transição: todos os .4s;
}
.plano::antes{
  conteúdo:'';posição:absoluta; topo:0;esquerda:0;direita:0;altura: 1px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
  opacidade:0;transição:opacidade .4s;
}
.plan:hover{background:var(-- black3);}
.plan:hover::before{opacity:1; }

.plan.featured{
  fundo:linear-gradient( 160deg,#1A1400,#120F00,var(-- black2));
  borda:1px sólida rgba(201,168,76,.3);
}
.plan.featured::after{
  conteúdo:'✦ DESTAQUE';
  posição:absoluta;topo:16px; direita:16px;
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:8px;espaçamento-entre-letras: 2px;
  cor:var(--gold);fundo: rgba(201,168,76,.1);
  preenchimento:3px 10px;raio da borda:2px;
}

.plan-type{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 4px;
  cor:var(--gold-dim);texto- transform:maiúsculas;margem- inferior:16px;
}
.plan-name{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 26px; peso da fonte: 600; cor: var(--white);
  margem-inferior:6px;
}
.plan-sub{font-size:12px; color:var(--muted);line- height:1.6;margin-bottom:24px; }
.plan-items{list-style:none;}
.plan-items li{
  tamanho da fonte: 13px; cor: rgba(255, 255, 255, 0,65);
  preenchimento:8px 0;
  borda-inferior:1px sólida rgba(255,255,255,.05);
  display:flex;align-items: center;gap:10px;
}
.plan-items li::before{content:'✦';font- size:7px;color:var(--gold); flex-shrink:0;}


/* ══════════════════════════════ ══
   WHATSAPP
══════════════════════════════ ══ */
.wa-sec{
  fundo:var(--black2);
  border-top:1px var sólido(--border);
}
.wa-grid{
  exibir:grade;modelo-de-grade- colunas:1fr 1fr;
  espaço:48px;alinhamento-itens:centro;
}
@media(max-width:680px){.wa- grid{grid-template-columns: 1fr;}}

.wa-features{margin-top:32px; display:flex;flex-direction: column;gap:1px;}
.wa-feat{
  display:flex;align-items:flex- start;gap:16px;
  preenchimento: 18px 20px;
  fundo:var(--black3);
  borda: 1px var sólido (--borda);
  borda-inferior:nenhuma;
  transição:fundo .3s;
}
.wa-feat:first-child{border- radius:2px 2px 0 0;}
.wa-feat:last-child{border- bottom:1px solid var(--border);border-radius:0 0 2px 2px;}
.wa-feat:hover{background:var( --black4);}
.wa-feat-icon{font-size:22px; flex-shrink:0;margin-top:2px;}
.wa-feat-t{font-size:13px; font-weight:500;color:var(-- white);margin-bottom:3px;}
.wa-feat-d{font-size:12px; color:var(--muted);line- height:1.6;}

/* painel de cartão */
.wa-painel{
  fundo:var(--preto);
  borda:1px var sólido(--border2);
  raio-da-borda:2px;
  preenchimento:36px;
  posição:relativa;overflow: oculto;
}
.wa-panel::before{
  conteúdo:'';posição:absoluta; topo:0;esquerda:0;direita:0;altura: 1px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
}
.wa-panel-title{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 24px; peso da fonte: 600; cor: var(--white); margem inferior: 4px;
}
.wa-panel-sub{font-size:12px; color:var(--muted);line- height:1.7;margin-bottom:24px; }
.wa-number-box{
  plano de fundo:var(--preto2); borda: 1px var sólido (--borda);
  preenchimento:14px 16px;raio da borda:2px;margem inferior:20px;
  display:flex;align-items: center;gap:12px;
  tamanho da fonte: 13px; cor: var(-- mudo);
}
.wa-number-box strong{color:var(--gold2);}

.btn-wa{
  largura: 100%;
  fundo:linear-gradient( 135deg,#128C7E,#25D366,# 128C7E);
  tamanho-de-fundo:200% 100%;
  cor:var(--white);borda: nenhuma;raio-da-borda:2px;
  preenchimento:16px;fonte:' Cinzel',serif;
  tamanho da fonte: 10px; espaçamento entre letras: 3px;
  cursor:ponteiro;
  display:flex;align-items: center;justify-content:center; gap:10px;
  box-shadow:0 8px 32px rgba(37,211,102,.25);
  transição: todos os .35s;
  animação:wa-shift 4s linear infinito;
}
@keyframes wa-shift{0%{background- position:0%}100%{background- position:200%}}
.btn-wa:hover{transform: translateY(-3px);box-shadow:0 16px 48px rgba(37,211,102,.35);}

.wa-chips{display:flex;flex- wrap:wrap;gap:8px;margin-top: 16px;}
.wa-chip{
  tamanho da fonte: 10px; preenchimento: 4px 12px; raio da borda: 2px;
  fundo:rgba(37,211,102,. 08);
  borda:1px sólida rgba(37,211,102,.2);cor:# 4ADE80;
  espaçamento entre letras: 0,5px;
}


/* ══════════════════════════════ ══
   CARTÃO DE CAVALEIRO DIGITAL
══════════════════════════════ ══ */
.card-sec{
  fundo:var(--preto);
  border-top:1px var sólido(--border);
  alinhamento-texto:centrado;
}
.dcard{
  largura máxima: 500px; margem: 48px automática 0;
  fundo:gradiente-linear( 145deg,#0A0800 0%,#1A1200 35%,#0D0B00 70%,#0A0800 100%);
  borda:1px sólida rgba(201,168,76,.35);
  raio-da-borda:4px;
  sombra de caixa:
    0 0 0 1px rgba(201,168,76,.06),
    0 40px 80px rgba(0,0,0,.9),
    0 0 60px rgba(201,168,76,.06) inset;
  preenchimento:36px;
  posição:relativa;overflow: oculto;
}
/* brilho */
.dcard::before{
  conteúdo:'';posição:absoluta;
  topo:0;esquerda:-100%;largura:50%; altura:100%;
  fundo:linear-gradient( 105deg,transparent 35%,rgba(201,168,76,.08) 50%,transparent 65%);
  animação: brilho-de-cartão 5s entrada-saída infinita;
}
@keyframes card-shine{0%,100%{left:-100%} 60%{left:150%}}
/* borda interna */
.dcard::after{
  conteúdo:'';posição:absoluta; inserção:8px;
  borda:1px sólida rgba(201,168,76,.07);
  border-radius:2px;pointer- events:none;
}

.dcard-top{display:flex; justify-content:space-between; align-items:flex-start;margin- bottom:32px;}
.dcard-logo{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 4px;
  cor:var(--dourado);
}
.dcard-crown{font-size:22px; filter:drop-shadow(0 0 8px rgba(201,168,76,.6));}

.dcard-class{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 4px;
  cor:var(--gold-dim);texto- transform:maiúsculas;margem- inferior:8px;
}
.dcard-title{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 38px; peso da fonte: 700; cor: var(--white);
  altura da linha: 1; margem inferior: 4px;
}
.dcard-title em{font-style:italic;color: var(--gold2);}
.dcard-sub{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 12px; estilo da fonte: itálico;
  cor:var(--muted); espaçamento entre letras:2px;margem inferior: 28px;
}

.dcard-tags{display:flex;flex- wrap:wrap;gap:8px;margin- bottom:32px;justify-content: center;}
.dcard-tag{
  tamanho da fonte: 10px; preenchimento: 5px 14px; raio da borda: 2px;
  fundo:rgba(201,168,76,. 07);
  borda:1px sólida rgba(201,168,76,.2);cor:var( --gold);
  display:flex;align-items: center;gap:5px;
}

.dcard-foot{
  exibir:flex;justificar-conteúdo: espaço-entre;alinhar-itens: flex-end;
  borda-superior:1px sólida rgba(201,168,76,.1);preenchimento- superior:20px;
}
.dcard-member-info{}
.dcard-member-lbl{font-size: 9px;color:var(--muted);letter- spacing:2px;text-transform: uppercase;}
.dcard-member-val{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 15px; cor: var(-- gold2); espaçamento entre letras: 1px; margem superior: 2px;
}
.dcard-chip{
  largura:48px;altura:36px;
  fundo:gradiente-linear( 135deg,#C9A84C 0%,#8B6914 40%,#F5E6B0 60%,#C9A84C 100%);
  raio-da-borda:4px;
  box-shadow:inset 0 1px 0 rgba(255,255,255,.25),0 3px 8px rgba(0,0,0,.6);
}
.dcard-num{
  família-da-fonte:'Cormorant Garamond', serifada;
  tamanho da fonte: 14px; cor: var(-- mudo); espaçamento entre letras: 4px;
  estilo-da-fonte: itálico;
}


/* ══════════════════════════════ ══
   RODAPÉ
══════════════════════════════ ══ */
rodapé{
  fundo:var(--preto);
  border-top:1px var sólido(--border);
  preenchimento: 48px 24px 36px;
  alinhamento-texto:centrado;
}
.footer-logo{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:12px;espaçamento-entre-letras: 5px;
  cor:var(--dourado);margem- inferior:12px;
}
.footer-sep{
  largura:60px;altura:1px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
  margem:14px automática;
}
.footer-text{font-size:12px; color:var(--muted);line- height:1.8;}
.footer-copy{
  margem superior: 24px; tamanho da fonte: 10px; cor: rgba(255,255,255,. 15); espaçamento entre letras: 1px;
}

/* ─ responsivo ─ */
@media(max-width:600px){
  .classes-grid,.flow-steps,. plans-grid{grid-template- columns:1fr;}
  .fstep{border-right:none; border-bottom:1px solid var(--border);}
  .fstep::after{content:'↓'; right:50%;top:auto;bottom:- 14px;transform:none;}
  .hero-stats{gap:20px;}
  .sep{display:none;}
}
</style>
</head>
<body>

<!-- Definição de canto SVG -->
<svg style="display:none">
  <symbol id="corner-svg" viewBox="0 0 80 80">
    <path d="M4 4 L4 40" stroke="#C9A84C" stroke-width="1" fill="none" opacity="0.5"/>
    <path d="M4 4 L40 4" stroke="#C9A84C" stroke-width="1" fill="none" opacity="0.5"/>
    <circle cx="4" cy="4" r="2" fill="#C9A84C" opacity="0.6"/>
  </symbol>
</svg>

<!-- ══ HERÓI ══ -->
<section class="hero">
  <div class="orb orb1"></div>
  <div class="orb orb2"></div>
  <div class="orb orb3"></div>
  <div class="corner c-tl"><svg><use href="#corner-svg"/></svg></ div>
  <div class="corner c-tr"><svg><use href="#corner-svg"/></svg></ div>
  <div class="corner c-bl"><svg><use href="#corner-svg"/></svg></ div>
  <div class="corner c-br"><svg><use href="#corner-svg"/></svg></ div>

  <div class="hero-eyebrow">✦ Cartão de Cavaleiro Digital · Apresenta</div>

  <h1 class="hero-title">
    Clínica
    <span class="italic">Premier</span>
  </h1>

  <p class="hero-tagline"> Multiespecialidades · Excelência em cada atendimento</p>

  <div class="hero-stats">
    <div class="hstat">
      <div class="hstat-n">+30</div>
      <div class="hstat-l"> Especialidades</div>
    </div>
    <div class="sep"></div>
    <div class="hstat">
      <div class="hstat-n">4</div>
      <div class="hstat-l">Classes A·B·C·D</div>
    </div>
    <div class="sep"></div>
    <div class="hstat">
      <div class="hstat-n">24h</div>
      <div class="hstat-l">WhatsApp</div>
    </div>
    <div class="sep"></div>
    <div class="hstat">
      <div class="hstat-n">7×</div>
      <div class="hstat-l">Dias/semana</ div>
    </div>
  </div>

  <div class="hero-cta">
    <button class="btn-gold" onclick="document.getElementById ('classes'). scrollIntoView({behavior:' smooth'})">
      ✦ Ver Aulas de Atendimento
    </button>
    <button class="btn-outline" onclick="document.getElementById ('whatsapp'). scrollIntoView({behavior:' smooth'})">
      💬Agenda via WhatsApp
    </button>
  </div>

  <div class="scroll-pill">
    <span>Descrever</span>
    <div class="scroll-dot"></div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ══ CLASSES ABCD ══ -->
<section class="sec classes-sec" id="classes">
  <div class="inner">
    <div class="sec-eye">Níveis de Atendimento</div>
    <h2 class="sec-h">Escolha sua <em>Classe</em><br>de Atendimento</h2>
    <p class="sec-p">Quatro níveis pensados ​​para cada perfil de paciente — do atendimento essencial ao mais exclusivo e personalizado.</p>

    <div class="classes-grid">

      <!-- CLASSE A -->
      <div class="cls cls-a">
        <div class="cls-letter">A</div>
        <div class="cls-badge">✦ Classe A</div>
        <div class="cls-name">Premier Gold</div>
        <div class="cls-sub">Atendimento máximo. Exclusividade total com médicos selecionados e análises prioritárias.</div>
        <ul class="cls-items">
          <li>Consulta com especialista selecionado</li>
          <li>Análises clínicas completas prioritárias</li>
          <li>Canal VIP sem WhatsApp</li>
          <li>Agendamento em até 24h</li>
          <li>Plano de saúde premium incluído</li>
          <li>Acompanhamento personalizado</li>
        </ul>
        <div class="cls-price">✦ Particular · Plano Ouro · Convênio Premium</div>
      </div>

      <!-- CLASSE B -->
      <div class="cls cls-b">
        <div class="cls-letter">B</div>
        <div class="cls-badge">Classe B</div>
        <div class="cls-name">Executivo Prata</div>
        <div class="cls-sub">Equilíbrio entre qualidade e agilidade. Atendimento completo com conforto diferenciado.</div>
        <ul class="cls-items">
          <li>Consulta com especialista disponível</li>
          <li>Análises clínicas completas</li>
          <li>Atendimento WhatsApp dedicado</li>
          <li>Agendamento em até 48h</li>
          <li>Convênio e particulares aceitos</li>
          <li>Resultados digitais rápidos</li>
        </ul>
        <div class="cls-price" style="color:#94A3B8"> Particular · Convênio · Plano Prata</div>
      </div>

      <!-- CLASSE C -->
      <div class="cls cls-c">
        <div class="cls-letter">C</div>
        <div class="cls-badge">Classe C</div>
        <div class="cls-name">Essencial Plus</div>
        <div class="cls-sub">Acesso completo às especialidades com atendimento humano e eficiente via WhatsApp.</div>
        <ul class="cls-items">
          <li>Consultas por especialidade</li>
          <li>Análises básicas e quantitativas</li>
          <li>Chatbot + Atendimento humano</li>
          <li>Agendamento flexível</li>
          <li>Convênios populares aceitos</li>
          <li>Acompanhamento padrão</li>
        </ul>
        <div class="cls-price" style="color:#78716C">Convênio · Particular com desconto</div>
      </div>

      <!-- CLASSE D -->
      <div class="cls cls-d">
        <div class="cls-letter">D</div>
        <div class="cls-badge">Classe D</div>
        <div class="cls-name">Acesso Básico</div>
        <div class="cls-sub">Atendimento essencial de qualidade. Saúde acessível para todos os perfis de paciente.</div>
        <ul class="cls-items">
          <li>Consulta clínica geral</li>
          <li>Análises básicas</li>
          <li>Agendamento pelo chatbot</li>
          <li>Convênios básicos aceitos</li>
          <li>Triagem e encaminhamento</li>
          <li>Suporte WhatsApp padrão</li>
        </ul>
        <div class="cls-price" style="color:#57534E">Convênio básico · Gratuidade parcial</div>
      </div>

    </div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ══ ESPECIALIDADES ══ -->
<section class="sec esp-sec" id="especialidades">
  <div class="inner">
    <div class="sec-eye">Especialidades Médicas</div>
    <h2 class="sec-h">Cada dia um <em>especialista</em><br> diferente para você</h2>
    <p class="sec-p">Rotatividade planejada de médicos especialistas para cobrir todas as áreas da saúde ao longo da semana.</p>
    <div class="live-badge">
      <span class="live-dot"></span>
      Médicos disponíveis hoje
    </div>

    <div class="esp-grid">
      <div class="esp"><div class="esp-icon"> 🫀</div><div class="esp-name">Cardiologia</ div></div>
      <div class="esp"><div class="esp-icon"> 🧠</div><div class="esp-name">Neurologia</ div></div>
      <div class="esp"><div class="esp-icon"> 🦴</div><div class="esp-name">Ortopedia</ div></div>
      <div class="esp"><div class="esp-icon"> 👁️</div><div class="esp-name">Oftalmologia </div></div>
      <div class="esp"><div class="esp-icon"> 🌸</div><div class="esp-name">Ginecologia</ div></div>
      <div class="esp"><div class="esp-icon"> 🍼</div><div class="esp-name">Pediatria</ div></div>
      <div class="esp"><div class="esp-icon"> 🦷</div><div class="esp-name">Odontologia</ div></div>
      <div class="esp"><div class="esp-icon"> 🧪</div><div class="esp-name">Análises Clínicas</div></div>
      <div class="esp"><div class="esp-icon"> 🩻</div><div class="esp-name">Radiologia</ div></div>
      <div class="esp"><div class="esp-icon"> 💊</div><div class="esp-name">Clínica Geral</div></div>
      <div class="esp"><div class="esp-icon"> 🧬</div><div class="esp-name"> Endocrinologia</div></div>
      <div class="esp"><div class="esp-icon"> 🫁</div><div class="esp-name">Pneumologia</ div></div>
      <div class="esp"><div class="esp-icon"> 🩸</div><div class="esp-name">Hematologia</ div></div>
      <div class="esp"><div class="esp-icon"> 🦠</div><div class="esp-name">Infectologia </div></div>
      <div class="esp"><div class="esp-icon"> 🧘</div><div class="esp-name">Psiquiatria</ div></div>
      <div class="esp"><div class="esp-icon"> 🏃</div><div class="esp-name">Medicina Esportiva</div></div>
    </div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ══ FLUXO ══ -->
<section class="sec flow-sec">
  <div class="inner">
    <div class="sec-eye">Como Funciona</div>
    <h2 class="sec-h">Do agendamento<br>ao <em>resultado</em></h2>
    <p class="sec-p">Processo simples, rápido e totalmente integrado ao WhatsApp com chatbot inteligente e atendimento humano.</p>

    <div class="flow-steps">
      <div class="fstep">
        <div class="fstep-n">01</div>
        <div class="fstep-icon"> 💬</div>
        <div class="fstep-title">WhatsApp </div>
        <div class="fstep-desc">Fale com nosso Chatbot Oi ou atendente humano. Resposta imediata 24h.</div>
      </div>
      <div class="fstep">
        <div class="fstep-n">02</div>
        <div class="fstep-icon"> 🏅</div>
        <div class="fstep-title">Escolha sua Classe</div>
        <div class="fstep-desc">Selecione entre as classes A, B, C ou D conforme seu plano ou convênio.</div>
      </div>
      <div class="fstep">
        <div class="fstep-n">03</div>
        <div class="fstep-icon"> 📅</div>
        <div class="fstep-title"> Agendamento</div>
        <div class="fstep-desc">Escolha o especialista e o dia disponível. Confirmação automática pelo chat.</div>
      </div>
      <div class="fstep">
        <div class="fstep-n">04</div>
        <div class="fstep-icon"> 🩺</div>
        <div class="fstep-title">Consulta </div>
        <div class="fstep-desc">Atendimento personalizado na clínica com o especialista agendado.</div>
      </div>
      <div class="fstep">
        <div class="fstep-n">05</div>
        <div class="fstep-icon"> 🧪</div>
        <div class="fstep-title">Análises</ div>
        <div class="fstep-desc">Laboratório completo no local. Resultados enviados direto no WhatsApp.</div>
      </div>
    </div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ══ PLANOS ══ -->
<section class="sec plans-sec">
  <div class="inner">
    <div class="sec-eye">Formas de Atendimento</div>
    <h2 class="sec-h">Particular, Convênio<br>ou <em>Plano de Saúde</em></h2>
    <p class="sec-p">Atendemos todas as formas de pagamento. Ninguém fica sem cuidado.</p>

    <div class="plans-grid">
      <div class="plan">
        <div class="plan-type">Particular </div>
        <div class="plan-name">Atendimento Particular</div>
        <div class="plan-sub">Agilidade máxima, sem burocracia. Você escolhe o especialista a cada hora.</div>
        <ul class="plan-items">
          <li>Todas as especialidades disponíveis</li>
          <li>Análises clínicas completas</li>
          <li>Agendamento imediato</li>
          <li>Resultados digitais</li>
        </ul>
      </div>

      <div class="plan featured">
        <div class="plan-type">Convênio</ div>
        <div class="plan-name">Convênios Aceitos</div>
        <div class="plan-sub">Aceitamos os principais convênios. Verifique seu pelo WhatsApp em segundos.</div>
        <ul class="plan-items">
          <li>Principais Convênios Aceitos</li>
          <li>Todas as especialidades cobertas</li>
          <li>Verificação rápida pelo chat</li>
          <li>Sem cobrança adicional</li>
        </ul>
      </div>

      <div class="plan">
        <div class="plan-type">Plano de Saúde</div>
        <div class="plan-name">Planos da Clínica</div>
        <div class="plan-sub">Planos próprios com ampla cobertura nas 4 classes de atendimento A, B, C e D.</div>
        <ul class="plan-items">
          <li>Cobertura total por aula</li>
          <li>Análises laboratoriais incluídas</li>
          <li>Atendimento prioritário</li>
          <li>Canal exclusivo no WhatsApp</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ══ WHATSAPP ══ -->
<section class="sec wa-sec" id="whatsapp">
  <div class="inner">
    <div class="wa-grid">
      <div>
        <div class="sec-eye">Atendimento Digital</div>
        <h2 class="sec-h">WhatsApp com<br><em>Chatbot + Humano</em></h2>
        <p class="sec-p">Inteligência artificial e atendimento humano juntos. Você nunca fica sem resposta.</p>

        <div class="wa-features">
          <div class="wa-feat">
            <div class="wa-feat-icon"> 🤖</div>
            <div>
              <div class="wa-feat-t">Chatbot Oi — 24 horas</div>
              <div class="wa-feat-d">Agendamento, dúvidas e informações automáticas a qualquer hora.</div>
            </div>
          </div>
          <div class="wa-feat">
            <div class="wa-feat-icon" > 👩‍⚕️</div>
            <div>
              <div class="wa-feat-t">Atendente Humano Real</div>
              <div class="wa-feat-d">Sempre que um humano precisar, nossa equipe assume o atendimento.</div>
            </div>
          </div>
          <div class="wa-feat">
            <div class="wa-feat-icon"> 📋</div>
            <div>
              <div class="wa-feat-t">Resultados pelo WhatsApp</div>
              <div class="wa-feat-d">Análises clínicas enviadas diretamente no seu chat com segurança.</div>
            </div>
          </div>
          <div class="wa-feat">
            <div class="wa-feat-icon"> 🏅</div>
            <div>
              <div class="wa-feat-t">Canal VIP Classe A</div>
              <div class="wa-feat-d">Pacientes Classe A têm canal prioritário com resposta em minutos.</div>
            </div>
          </div>
        </div>
      </div>

      <div>
        <div class="wa-panel">
          <div class="wa-panel-title"> 💬Fale Conosco Agora</div>
          <div class="wa-panel-sub">Agende sua consulta em menos de 2 minutos. Nosso chatbot ou atendente responde na hora.</div>
          <div class="wa-number-box">
            <span> 📱</span>
            WhatsApp: (XX) XXXXX-XXXX
          </div>
          <button class="btn-wa" onclick="window.open(' https:// wa.me/55XXXXXXXXXXX ','_blank') ">
            <span style="font-size:18px" > 💬</span>
            AGENDAR CONSULTA AGORA
          </button>
          <div class="wa-chips">
            <span class="wa-chip">✓ Resposta rápida</span>
            <span class="wa-chip">✓ 24h disponível</span>
            <span class="wa-chip">✓ Bot + Humano</span>
            <span class="wa-chip">✓th online</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ══ CARTÃO DE CAVALEIRO DIGITAL ══ -->
<section class="sec card-sec">
  <div class="inner">
    <div class="sec-eye" style="justify-content:center" >Identidade Digital Premium</div>
    <h2 class="sec-h" style="text-align:center; margin:0 auto">O <em>Cartão Chevalier Digital</em><br>da sua Clínica</h2>
    <p class="sec-p" style="margin:12px auto 0;text-align:center">Uma apresentação única e diferenciada que posiciona sua clínica no mais alto padrão do mercado.</p>

    <div class="dcard">
      <div class="dcard-top">
        <div class="dcard-logo">✦ CARTÃO DE CAVALEIRO DIGITAL</div>
        <div class="dcard-crown">♛</div>
      </div>

      <div class="dcard-class">Classe Premier · Multiespecialidades</div>
      <div class="dcard-title">Clínica <em>Premier</em></div>
      <div class="dcard-sub">Saúde · Bem-estar · Excelência</div>

      <div class="dcard-tags">
        <span class="dcard-tag"> 🩺Consultas</span>
        <span class="dcard-tag"> 🧪Análises</span>
        <span class="dcard-tag"> 📅Agenda</span>
        <span class="dcard-tag"> 💬WhatsApp</span>
        <span class="dcard-tag"> 🏅A · B · C · D</span>
        <span class="dcard-tag"> 🤝Convênio</span>
        <span class="dcard-tag"> ❤️Plano de Saúde</span>
      </div>

      <div class="dcard-foot">
        <div class="dcard-member-info">
          <div class="dcard-member-lbl">Nível de Acesso</div>
          <div class="dcard-member-val">✦ Classe Premier A</div>
        </div>
        <div class="dcard-chip"></div>
        <div class="dcard-num">**** 2026</div>
      </div>
    </div>
  </div>
</section>

<!-- ══ RODAPÉ ══ -->
<rodapé>
  <div class="footer-logo">✦ CARTÃO DE CAVALEIRO DIGITAL</div>
  <div class="footer-sep"></div>
  <div class="footer-text">
    Clínica Premier Multiespecialidades<br>
    Particular · Convênio · Planos A · B · C · D<br>
    Agendamento via WhatsApp · Chatbot Oi + Atendimento Humano
  </div>
  <div class="footer-copy">© 2026 · Cartão Digital Chevalier · Todos os direitos reservados</div>
</footer>

</body>!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Especialidades · Hoje na Clínica</title>
<link href=" https://fonts.googleapis.com/css2?family= Cormorant +Garamond:ital,wght@ 0,400;0,600;0,700;1,400& family=Cinzel:wght@400;600& family=DM+Sans:wght@300;400; 500&display=swap " rel="stylesheet">
<style>
:raiz{
  --ouro:#C9A84C;--ouro2:# E8C96A;--ouro3:#F5E6B0;
  --gold-dim:#8B6914;
  --preto:#080808;--preto2:# 0F0F0F;--preto3:#161616;-- preto4:#1E1E1E;
  --creme:#F5ECD7;--silencioso:# 7A6E5F;
  --border:rgba(201,168,76,0.18) ;--border2:rgba(201,168,76,0. 35);
  --verde:#22C55E;--vermelho:#6B7280;
}
*{margin:0;padding:0;box- sizing:border-box;}
body{background:var(--black); color:var(--cream);font- family:'DM Sans',sans-serif;min-height: 100vh;padding:40px 20px;}

/* ── cabeçalho ── */
.page-head{text-align:center; margin-bottom:48px;}
.eyebrow{font-family:'Cinzel', serif;font-size:9px;letter- spacing:5px;color:var(--gold);
  borda:1px sólida var(--border2);preenchimento:6px 20px;raio-da-borda:2px;
  display:inline-block;margin- bottom:16px;}
.page-title{font-family:' Cormorant Garamond',serif;font-size: clamp(32px,7vw,56px);
  peso da fonte:700;cor:#fff; altura da linha:1;}
.page-title em{font-style:italic;color: var(--gold2);}
.page-sub{font-size:14px; color:var(--muted);margin-top: 10px;line-height:1.7;}

/* ── barra de data ── */
.date-bar{
  display:flex;align-items: center;justify-content:center; gap:16px;
  margem-inferior:32px;flex-wrap: envolver;
}
.date-pill{
  plano de fundo:var(--preto3); borda:1px var sólido(--border2);
  raio da borda: 2px; preenchimento: 10px 20px;
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:10px;espaçamento-entre-letras: 3px;cor:var(--gold);
  display:flex;align-items: center;gap:8px;
}
.live-dot{largura:7px;altura: 7px;borda-raio:50%; fundo:var(--verde);
  box-shadow:0 0 6px var(--green);animation:blink 1.5s ease-in-out infinite;}
@keyframes blink{0%,100%{opacity:1}50%{ opacity:.3}}

.contador{
  tamanho da fonte: 12px; cor: var(-- mudo);
  display:flex;align-items: center;gap:6px;
}
.counter strong{color:var(--gold2);}

/* ── PAINEL DE ALTERNÂNCIA DO ADMINISTRADOR ── */
.admin-panel{
  largura máxima: 800px; margem: 0 auto 40px;
  fundo:var(--black2); borda:1px sólida var(--border);raio-da-borda: 2px;
  overflow:oculto;
}
.admin-header{
  exibir:flex;alinhar-itens: centro;justificar-conteúdo:espaço- entre;
  padding:14px 20px;border-bottom:1px solid var(--border);cursor:pointer;
  seleção do usuário:nenhum;
}
.admin-title{font-family:' Cinzel',serif;font-size:9px; letter-spacing:3px;color:var(- -gold);}
.admin-arrow{color:var(--gold) ;transition:transform .3s;font-size:12px;}
.admin-arrow.open{transform: rotate(180deg);}
.admin-body{padding:20px; display:none;}
.admin-body.open{display: block;}

.admin-note{font-size:11px; color:var(--muted);margin- bottom:16px;line-height:1.6;
  padding:10px 14px;background:rgba(201,168, 76,.05);border-left:2px solid var(--gold);}

.admin-grid{
  display:grid;grid-template- columns:repeat(auto-fill, minmax(160px,1fr));gap:8px;
}
.toggle-item{
  display:flex;align-items: center;gap:10px;
  plano de fundo:var(--preto3); borda: 1px var sólido (--borda);
  raio da borda: 2px; preenchimento: 10px 12px; cursor: ponteiro;
  transição:todos .25s;seleção do usuário:nenhuma;
}
.toggle-item:hover{border- color:var(--border2);}
.toggle-item.active{border- color:rgba(34,197,94,.3); background:rgba(34,197,94,.05) ;}
.toggle-icon{font-size:18px; flex-shrink:0;}
.toggle-name{font-size:11px; color:rgba(255,255,255,.7); line-height:1.3;}
.toggle-item.active .toggle-name{color:#fff;}
.toggle-check{
  margem-esquerda:automática;largura:16px; altura:16px;raio-da-borda:2px; flex-shrink:0;
  borda: 1px var sólido (--silenciado);
  exibir:flex;alinhar-itens: centro;justificar-conteúdo:centro;
  tamanho da fonte: 9px; cor: transparente; transição: todas .2s;
}
.toggle-item.active .toggle-check{
  fundo:var(--verde); cor-da-borda:var(--verde); cor:#fff;
}

.admin-actions{display:flex; gap:10px;margin-top:16px;flex- wrap:wrap;}
.btn-sm{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 2px;
  preenchimento:8px 16px;raio da borda:2px;cursor: ponteiro;transição:tudo .25s;
}
.btn-all{background:rgba(201, 168,76,.1);border:1px solid var(--border2);color:var(-- gold);}
.btn-all:hover{background: rgba(201,168,76,.2);}
.btn-none{background:var(-- black3);border:1px solid var(--border);color:var(-- muted);}
.btn-none:hover{border-color: var(--border2);color:var(-- cream);}
.btn-apply{
  fundo: gradiente linear ( 135 graus, var (--gold-dim), var (- gold));
  borda:nenhuma;cor:var(--preto) ;peso da fonte:500;margem esquerda: automática;
}
.btn-apply:hover{box-shadow:0 4px 16px rgba(201,168,76,.3);transform: translateY(-1px);}

/* ── EXIBIR GRADE ── */
.esp-wrap{max-width:800px; margin:0 auto;}

.filter-tabs{display:flex;gap: 8px;margin-bottom:24px;flex- wrap:wrap;}
.ftab{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:9px;espaçamento-entre-letras: 2px;
  preenchimento:7px 16px;raio da borda:2px;cursor: ponteiro;
  border:1px solid var(--border);color:var(-- muted);
  fundo:transparente; transição:tudo .25s;
}
.ftab.active{background:rgba( 201,168,76,.1);border-color: var(--border2);color:var(-- gold);}

.esp-grid{
  exibir:grade;
  grid-template-columns:repeat( auto-fill,minmax(130px,1fr));
  espaço:1px;
  borda: 1px var sólido (--borda);
}

.esp-card{
  preenchimento: 20px 14px; alinhamento de texto: centro;
  fundo:var(--black2);
  posição:relativa;overflow: oculto;
  transição: todos os .35s;
}

/* disponível */
.esp-card.available{cursor: default;}
.esp-card.available::after{
  conteúdo:'';posição:absoluta; inferior:0;esquerda:0;direita:0; altura:2px;
  fundo:linear-gradient( 90deg,transparent,var(--gold), transparent);
}
.esp-card.available:hover{ background:var(--black3);}

/* indisponível */
.esp-card.unavailable{
  fundo:rgba(8,8,8,.8);
  opacidade: 0,45;
  filtro: escala de cinza (1);
}
.esp-card.unavailable .esp-badge{display:flex;}

/* oculto pelo filtro */
.esp-card.hidden{display:none; }

.esp-icon{font-size:26px; margin-bottom:8px;}
.esp-name{font-size:11px; color:rgba(255,255,255,.75); line-height:1.4;margin-bottom: 6px;}

.esp-status{
  família-da-fonte:'Cinzel',serif; tamanho-da-fonte:8px;espaçamento-entre-letras: 1px;
  preenchimento: 3px 8px; raio da borda: 2px; exibição: bloco em linha;
}
.disponível .esp-status{
  fundo:rgba(34,197,94,.1); borda:1px sólida rgba(34,197,94,.25);cor:var( --verde);
}
.indisponível .esp-status{
  fundo:rgba(107,114,128,. 1);borda:1px sólida rgba(107,114,128,.2);cor:# 6B7280;
}

.esp-badge{
  posição:absoluta;topo:8px; direita:8px;
  fundo:rgba(107,114,128,. 15);borda:1px sólida rgba(107,114,128,.2);
  raio da borda: 2px; preenchimento: 2px 6px;
  tamanho da fonte: 8px; cor: #6B7280; espaçamento entre letras: 1px;
  exibir:nenhum;alinhar itens: centro;espaçamento:3px;
}

/* ── estado vazio ── */
.vazio{
  grid-column:1/-1;padding:40px; text-align:center;
  cor:var(--muted);tamanho da fonte: 13px;estilo da fonte: itálico;
}

/* ── regra de ouro ── */
.rule{height:1px;background: linear-gradient(90deg, transparent,var(--gold), transparent);margin:40px 0;}
</style>
</head>
<body>

<div class="page-head">
  <div class="eyebrow">✦ Cartão de Cavaleiro Digital</div>
  <h1 class="page-title"> Especialidades <em>Hoje</em></h1>
  <p class="page-sub">Veja quais médicos especialistas estão atendendo hoje na clínica</p>
</div>

<!-- data + contador -->
<div style="max-width:800px;margin: 0 auto;">
  <div class="date-bar">
    <div class="date-pill">
      <span class="live-dot"></span>
      <span id="today-label">Carregando... </span>
    </div>
    <div class="counter">
      <strong id="available-count">0</strong> disponível hoje  · 
      <span id="unavailable-count">0</span> indisponíveis
    </div>
  </div>

  <!-- PAINEL DE ADMINISTRAÇÃO -->
  <div class="admin-panel">
    <div class="admin-header" onclick="toggleAdmin()">
      <span class="admin-title"> ⚙PAINEL DA CLÍNICA — DEFINIR DISPONIBILIDADE DE HOJE</span>
      <span class="admin-arrow" id="admin-arrow">▼</span>
    </div>
    <div class="admin-body" id="admin-body">
      <div class="admin-note">
        Marque as especialidades que estão atendendo <strong>hoje</strong>. As demarcadas aparecem como “Indisponível hoje” para os pacientes.
      </div>
      <div class="admin-grid" id="admin-grid"></div>
      <div class="admin-actions">
        <button class="btn-sm btn-all" onclick="selectAll()">✦ MARCAR TODOS</button>
        <button class="btn-sm btn-none" onclick="selectNone()"> DESMARCAR TODOS</button>
        <button class="btn-sm btn-apply" onclick="applyChanges()">✦ APLICAR AGORA</button>
      </div>
    </div>
  </div>

  <!-- FILTRAR ABAS -->
  <div class="filter-tabs">
    <button class="ftab active" onclick="filterCards('all', this)">Todos</button>
    <button class="ftab" onclick="filterCards(' available',this)">✦ Disponíveis hoje</button>
    <button class="ftab" onclick="filterCards(' unavailable',this)"> Indisponíveis</button>
  </div>

  <!-- EXIBIR GRADE -->
  <div class="esp-grid" id="esp-grid"></div>

  <div class="regra"></div>
  <p style="text-align:center;font- size:11px;color:var(--muted); font-style:italic;">
    ✦ Disponibilidade atualizada diariamente · Agendamentos via WhatsApp
  </p>
</div>

<script>
const especialidades = [
  {icon:' 🫀', name:'Cardiologia', available:false},
  {ícone:' 🧠', nome:'Neurologia', disponível:false},
  {ícone:' 🦴', nome:'Ortopedia', disponível:true},
  {icon:' 👁️', name:'Oftalmologia', available:false},
  {icon:' 🌸', name:'Ginecologia', available:true},
  {icon:' 🍼', name:'Pediatria', available:true},
  {ícone:' 🦷', nome:'Odontologia', disponível:false},
  {ícone:' 🧪', nome:'Análises Clínicas', disponível:true},
  {icon:' 🩻', name:'Radiologia', available:false},
  {ícone:' 💊', nome:'Clínica Geral', disponível:true},
  {icon:' 🧬', name:'Endocrinologia', available:false},
  {ícone:' 🫁', nome:'Pneumologia', disponível:true},
  {icon:' 🩸', name:'Hematologia', available:false},
  {icon:' 🦠', nome:'Infectologia', disponível:false},
  {ícone:' 🧘', nome:'Psiquiatria / Psicologia', disponível:true},
  {ícone:' 🏃', nome:'Medicina Esportiva', disponível:false},
  {icon:' 🧴', name:'Dermatologia', available:true},
  {ícone:' 👂', nome:'Otorrinolaringologia', disponível:false},
  {icon:' 🦵', name:'Fisioterapia', available:true},
  {ícone:' 💉', nome:'Urologia', disponível:false},
];

// Defina o rótulo da data de hoje
const dias = ['Domingo','Segunda-feira',' Terça-feira','Quarta-feira',' Quinta-feira','Sexta-feira',' Sábado'];
const meses = ['Janeiro','Fevereiro','Março' ,'Abril','Maio','Junho',' Julho','Agosto','Setembro',' Outubro','Novembro','Dezembro' ];
const now = new Date();
document.getElementById(' today-label').textContent =
  `${days[now.getDay()]}, ${now.getDate()} de ${months[now.getMonth()]} de ${now.getFullYear()}`;

let currentFilter = 'todos';

função renderizarAdminGrid(){
  const g = document.getElementById(' admin-grid');
  g.innerHTML = specialities.map((s,i)=>`
    <div class="toggle-item ${s.available?'active':''}" onclick="toggleItem(${i})">
      <span class="toggle-icon">${s.icon}< /span>
      <span class="toggle-name">${ s.name }< /span>
      <span class="toggle-check">${s. disponível?'✓':''}</span>
    </div>
  `).join('');
}

função toggleItem(i){
  especialidades[i].disponíveis = !especialidades[i].disponíveis;
  renderAdminGrid();
}

function selectAll(){specialties.forEach (s=>s.available=true); renderAdminGrid();}
function selectNone(){specialties.forEach (s=>s.available=false); renderAdminGrid();}

função aplicarAlterações(){
  renderDisplayGrid();
  atualizarContador();
  // confirmação por flash
  const btn = document.querySelector('.btn- apply');
  btn.textContent = '✓ APLICADO!';
  setTimeout(()=>btn. textContent='✦ APLICAR AGORA',2000);
}

função renderDisplayGrid(){
  const g = document.getElementById('esp- grid');
  g.innerHTML = specialities.map((s,i)=>{
    const cls = s.available ? 'disponível' : 'indisponível';
    const hidden = (currentFilter==='available' && !s.available) ||
                   (currentFilter===' indisponível' && s.disponível) ? 'oculto' : '';
    retornar `
      <div class="esp-card ${cls} ${hidden}">
        <div class="esp-badge">— Hoje não</div>
        <div class="esp-icon">${s.icon} </div>
        <div class="esp-name">${ s.name } </div>
        <div class="esp-status">${s. disponível ? '● Hoje' : '○ Indisponível'}</div>
      </div>`;
  }).juntar('');

  // estado vazio
  const visible = g.querySelectorAll('.esp-card: not(.hidden)').length;
  se(visível===0){
    g.innerHTML += '<div class="empty">Nenhuma especialidade nesta categoria hoje.</div>';
  }
}

função atualizarContador(){
  const av = specialties.filter(s=>s.available ).length;
  document.getElementById(' contagem disponível').textContent = av;
  document.getElementById(' unavailable-count'). textContent = specialties.length - av;
}

função filterCards(tipo, btn){
  currentFilter = tipo;
  document.querySelectorAll('. ftab').forEach(b=>b.classList. remove('active'));
  btn.classList.add('ativo');
  renderDisplayGrid();
}

função toggleAdmin(){
  const body = document.getElementById(' admin-body');
  const arrow = document.getElementById(' admin-arrow');
  body.classList.toggle('aberto');
  arrow.classList.toggle('aberto') ;
}

// inicialização
renderAdminGrid();
renderDisplayGrid();
atualizarContador();
</script>
</body>
</html>


</html>

