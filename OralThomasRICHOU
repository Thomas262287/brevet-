<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Les Cadets de la Défense</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow:ital,wght@0,300;0,400;0,600;0,700;1,400&family=Barlow+Condensed:wght@400;600;700&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{--navy:#0f1f3d;--navy2:#1a3260;--blue:#1e5fa8;--gold:#c8922a;--gold2:#e8b84b;--white:#f4f0e8;--light:#dde4ef;--gray:#8a9bb5;}
html,body{width:100%;height:100%;overflow:hidden;background:#000;font-family:'Barlow',sans-serif;color:var(--white);cursor:none}
.cursor{position:fixed;width:10px;height:10px;background:var(--gold);border-radius:50%;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);mix-blend-mode:difference}
#progress{position:fixed;top:0;left:0;height:3px;background:linear-gradient(90deg,var(--gold),var(--gold2));transition:width .4s ease;z-index:200}
.slide{position:fixed;inset:0;display:flex;flex-direction:column;opacity:0;pointer-events:none;transition:opacity .5s ease;overflow:hidden}
.slide.active{opacity:1;pointer-events:all}
.goldbar{position:absolute;left:0;top:0;bottom:0;width:7px;background:linear-gradient(180deg,var(--gold),var(--gold2))}
.hbar{display:flex;align-items:center;justify-content:space-between;background:var(--navy);padding:22px 52px;border-bottom:3px solid var(--gold);flex-shrink:0}
.hbar-title{font-family:'Bebas Neue',sans-serif;font-size:32px;letter-spacing:3px}
.hbar-num{font-family:'Bebas Neue',sans-serif;font-size:26px;color:var(--gold);border:2px solid var(--gold);width:46px;height:46px;display:flex;align-items:center;justify-content:center;border-radius:4px}
#nav{position:fixed;bottom:24px;left:50%;transform:translateX(-50%);display:flex;align-items:center;gap:14px;z-index:100;background:rgba(15,31,61,.85);backdrop-filter:blur(12px);border:1px solid rgba(200,146,42,.3);border-radius:50px;padding:8px 22px}
#nav button{background:none;border:none;cursor:pointer;color:var(--gold);font-size:20px;width:34px;height:34px;display:flex;align-items:center;justify-content:center;border-radius:50%;transition:background .2s,transform .15s}
#nav button:hover{background:rgba(200,146,42,.15);transform:scale(1.1)}
#counter{font-family:'Barlow Condensed',sans-serif;font-size:12px;letter-spacing:2px;color:var(--gold2);min-width:52px;text-align:center}
.dots{display:flex;gap:6px;align-items:center}
.dot{width:6px;height:6px;border-radius:50%;background:var(--gray);cursor:pointer;transition:background .2s,transform .2s}
.dot.on{background:var(--gold2);transform:scale(1.4)}
.slide.active .au{animation:fadeUp .45s ease forwards;opacity:0}
.slide.active .au:nth-child(1){animation-delay:.05s}.slide.active .au:nth-child(2){animation-delay:.12s}.slide.active .au:nth-child(3){animation-delay:.19s}.slide.active .au:nth-child(4){animation-delay:.26s}.slide.active .au:nth-child(5){animation-delay:.33s}.slide.active .au:nth-child(6){animation-delay:.40s}
@keyframes fadeUp{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}

/* SLIDE 1 */
#s1{background:var(--navy)}
#s1::before{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(255,255,255,.013) 0,rgba(255,255,255,.013) 1px,transparent 1px,transparent 80px),repeating-linear-gradient(0deg,rgba(255,255,255,.013) 0,rgba(255,255,255,.013) 1px,transparent 1px,transparent 80px)}
.s1-corner{position:absolute;right:0;top:0;width:320px;height:260px;background:var(--navy2);clip-path:polygon(100% 0,0 0,100% 100%)}
.s1-tag{position:absolute;top:38px;left:46px;background:var(--gold);color:var(--navy);font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:12px;letter-spacing:3px;padding:6px 18px;text-transform:uppercase}
.s1-big{position:absolute;top:100px;left:46px;font-family:'Bebas Neue',sans-serif;font-size:clamp(70px,9vw,108px);line-height:.9;letter-spacing:2px}
.s1-big span{color:var(--gold2)}
.s1-q{position:absolute;bottom:130px;left:46px;right:80px;font-size:17px;color:var(--light);font-style:italic;font-weight:300;line-height:1.6;border-left:3px solid var(--gold);padding-left:18px}
.s1-stars{position:absolute;right:46px;top:38px;display:flex;gap:10px}
.s1-star{color:var(--gold);font-size:16px;animation:blink 2s infinite}
.s1-star:nth-child(2){animation-delay:.3s}.s1-star:nth-child(3){animation-delay:.6s}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.35}}

/* SLIDE 2 — SOMMAIRE */
#s2{background:#0b1628;flex-direction:row!important}
.s2-left{width:36%;background:var(--navy2);display:flex;flex-direction:column;padding:55px 38px;border-right:4px solid var(--gold);position:relative}
.s2-deco{font-family:'Bebas Neue',sans-serif;font-size:110px;color:rgba(200,146,42,.05);position:absolute;bottom:-10px;left:-5px;line-height:1}
.s2-h{font-family:'Bebas Neue',sans-serif;font-size:40px;color:var(--gold2);letter-spacing:4px;margin-bottom:28px}
.s2-right{flex:1;padding:55px 60px 55px 75px;display:flex;flex-direction:column;justify-content:center;gap:14px}
.pitem{display:flex;align-items:center;gap:18px;padding:14px 18px;border:1px solid rgba(200,146,42,.2);border-left:4px solid var(--gold);background:rgba(255,255,255,.03);transition:background .2s,transform .2s}
.pitem:hover{background:rgba(200,146,42,.08);transform:translateX(5px)}
.pnum{font-family:'Bebas Neue',sans-serif;font-size:30px;color:var(--gold);min-width:32px}
.plabel{font-size:17px;font-weight:600}
.pnote{font-size:11px;color:var(--gray);margin-top:2px}

/* BODY commun */
.body{flex:1;display:flex;padding:30px 46px 80px;gap:22px}

/* SLIDE 3 — INTRO */
#s3 .body{align-items:stretch}
.card3{flex:1;background:rgba(255,255,255,.05);border:1px solid rgba(200,146,42,.2);border-top:4px solid var(--blue);padding:28px 24px;display:flex;flex-direction:column;gap:14px;transition:transform .2s,border-top-color .2s}
.card3:hover{transform:translateY(-4px);border-top-color:var(--gold)}
.c3-icon{font-size:38px}
.c3-title{font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:18px;color:var(--gold2);text-transform:uppercase;letter-spacing:1px}
.c3-kw{display:flex;flex-wrap:wrap;gap:8px;margin-top:4px}
.kw{background:rgba(200,146,42,.15);border:1px solid rgba(200,146,42,.3);color:var(--gold2);font-family:'Barlow Condensed',sans-serif;font-weight:600;font-size:14px;padding:5px 14px;letter-spacing:1px}

/* SLIDE 4 — CADETS (1 seule colonne, pas de valeurs) */
#s4{background:#0b1628}
#s4 .body{flex-direction:column;gap:20px;justify-content:center;max-width:700px;margin:0 auto;width:100%}
.sec-lbl{font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:14px;letter-spacing:2px;color:var(--gold);text-transform:uppercase;border-left:4px solid var(--gold);padding-left:10px;margin-bottom:6px}
.big-year{font-family:'Bebas Neue',sans-serif;font-size:90px;color:var(--gold2);line-height:1}

/* SLIDE 5 — ACTIVITÉS grille 3×3 */
#s5{background:#0b1628}
#s5 .body{display:grid;grid-template-columns:repeat(3,1fr);grid-template-rows:repeat(3,1fr);padding:16px 36px 76px;gap:12px}
.acard{background:rgba(255,255,255,.04);border:1px solid rgba(200,146,42,.18);border-top:3px solid var(--blue);padding:16px 18px;display:flex;flex-direction:column;gap:6px;transition:transform .2s,border-top-color .2s,background .2s;position:relative;overflow:hidden}
.acard::after{content:attr(data-n);position:absolute;right:12px;top:8px;font-family:'Bebas Neue',sans-serif;font-size:40px;color:rgba(255,255,255,.04)}
.acard:hover{transform:translateY(-3px);border-top-color:var(--gold);background:rgba(200,146,42,.06)}
.a-icon{font-size:22px}
.a-title{font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:14px;color:var(--gold2);text-transform:uppercase;letter-spacing:1px}
.a-date{font-size:10px;color:var(--gold);font-style:italic}
.a-kws{display:flex;flex-wrap:wrap;gap:5px;margin-top:2px}
.akw{font-size:11px;color:var(--light);background:rgba(255,255,255,.06);padding:2px 8px;font-weight:600}

/* SLIDE 6 — CAMP */
#s6{background:linear-gradient(135deg,#080f1f,#0f1f3d)}
#s6 .body{gap:0;padding:0}
.camp-l{width:40%;padding:32px 46px 80px;display:flex;flex-direction:column;justify-content:space-between;border-right:2px solid rgba(200,146,42,.3)}
.camp-big{font-family:'Bebas Neue',sans-serif;font-size:clamp(50px,6vw,78px);color:var(--gold2);line-height:.9}
.cstat{display:flex;align-items:center;gap:14px;padding:13px 16px;background:rgba(200,146,42,.08);border:1px solid rgba(200,146,42,.2);margin-bottom:10px}
.cstat-n{font-family:'Bebas Neue',sans-serif;font-size:34px;color:var(--gold2);min-width:56px}
.cstat-l{font-size:12px;color:var(--light)}
.camp-r{flex:1;padding:32px 46px 80px;display:flex;flex-direction:column;gap:14px}
.camp-tag{display:inline-block;background:var(--gold);color:var(--navy);font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:11px;letter-spacing:2px;padding:5px 14px;text-transform:uppercase;margin-bottom:8px}
.camp-kws{display:flex;flex-direction:column;gap:10px}
.ckw{display:flex;align-items:center;gap:12px;padding:12px 16px;background:rgba(255,255,255,.04);border-left:4px solid var(--gold);font-family:'Barlow Condensed',sans-serif;font-weight:600;font-size:16px;letter-spacing:.5px}
.ckw-icon{font-size:20px}

/* SLIDE 7 — CÉRÉMONIES */
#s7{background:#080f1f}
#s7 .body{align-items:stretch;gap:18px}
.cere-main{flex:1.3;display:flex;flex-direction:column;gap:14px}
.cere-side{flex:1;display:flex;flex-direction:column;gap:12px}
.cere-dc{background:var(--navy);border-left:4px solid var(--gold);padding:16px 18px;flex:1;display:flex;flex-direction:column;gap:5px}
.cere-d{font-family:'Bebas Neue',sans-serif;font-size:20px;color:var(--gold2)}
.cere-p{font-size:12px;color:var(--gray)}
.cere-kws{display:flex;flex-wrap:wrap;gap:7px;margin-top:6px}
.ckwsmall{font-size:12px;color:var(--light);background:rgba(255,255,255,.06);padding:3px 10px;font-weight:600}
.geo-box{background:rgba(30,95,168,.12);border:1px solid rgba(30,95,168,.35);padding:16px 18px;display:flex;gap:12px;align-items:flex-start}
.geo-lbl{font-family:'Barlow Condensed',sans-serif;font-weight:700;color:var(--blue);font-size:13px;letter-spacing:1px;text-transform:uppercase;margin-bottom:5px}
.geo-kws{display:flex;flex-wrap:wrap;gap:6px}
.quote{border-left:3px solid var(--gold);padding-left:16px;font-style:italic;font-size:15px;color:var(--gold2);line-height:1.6}

/* SLIDE 8 — CE QUE ÇA M'A APPORTÉ (4 cartes 2×2) */
#s8{background:#0b1628}
#s8 .body{display:grid;grid-template-columns:repeat(2,1fr);grid-template-rows:repeat(2,1fr);padding:24px 46px 80px;gap:18px}
.vcard{background:var(--navy);border:1px solid rgba(200,146,42,.15);border-top:4px solid var(--gold);padding:26px 24px;display:flex;flex-direction:column;gap:12px;transition:transform .2s,background .2s}
.vcard:hover{transform:translateY(-4px);background:var(--navy2)}
.vc-num{font-family:'Bebas Neue',sans-serif;font-size:48px;color:var(--gold);line-height:1}
.vc-title{font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:20px;color:var(--gold2);text-transform:uppercase;letter-spacing:1px}
.vc-kws{display:flex;flex-wrap:wrap;gap:7px;margin-top:4px}
.vkw{font-size:13px;color:var(--light);background:rgba(255,255,255,.07);padding:4px 12px;font-weight:600}


/* SLIDE 10 — MERCI */
#s10{background:var(--navy)}
#s10::before{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(255,255,255,.013) 0,rgba(255,255,255,.013) 1px,transparent 1px,transparent 80px),repeating-linear-gradient(0deg,rgba(255,255,255,.013) 0,rgba(255,255,255,.013) 1px,transparent 1px,transparent 80px)}
.merci-in{position:relative;z-index:1;flex:1;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;gap:28px;padding:60px}
.merci-big{font-family:'Bebas Neue',sans-serif;font-size:clamp(60px,9vw,110px);color:var(--white);line-height:.9}
.merci-big span{color:var(--gold2)}
.merci-line{width:120px;height:4px;background:linear-gradient(90deg,var(--gold),var(--gold2))}
.merci-sub{font-size:20px;color:var(--light);font-style:italic;font-weight:300;max-width:600px;line-height:1.7}

/* SLIDE 9 — CONCLUSION */
#s9{background:var(--navy)}
#s9::before{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(255,255,255,.012) 0,rgba(255,255,255,.012) 1px,transparent 1px,transparent 80px),repeating-linear-gradient(0deg,rgba(255,255,255,.012) 0,rgba(255,255,255,.012) 1px,transparent 1px,transparent 80px)}
.s10-in{position:relative;z-index:1;flex:1;display:flex;flex-direction:column;justify-content:center;padding:50px 72px;gap:28px}
.s10-lbl{font-family:'Barlow Condensed',sans-serif;font-size:13px;letter-spacing:5px;color:var(--gold);text-transform:uppercase}
.s10-big{font-family:'Bebas Neue',sans-serif;font-size:clamp(50px,7vw,88px);line-height:.9;color:var(--white)}
.s10-line{width:100px;height:4px;background:linear-gradient(90deg,var(--gold),var(--gold2))}
.s10-kws{display:flex;flex-wrap:wrap;gap:12px}
.s10kw{background:rgba(200,146,42,.12);border:1px solid rgba(200,146,42,.3);color:var(--gold2);font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:16px;padding:8px 20px;letter-spacing:1px}
.s10-cards{display:flex;gap:20px;margin-top:4px}
.s10c{flex:1;background:rgba(255,255,255,.05);border:1px solid rgba(200,146,42,.2);padding:20px;display:flex;flex-direction:column;align-items:center;gap:8px;text-align:center}
.s10c-icon{font-size:32px}
.s10c-txt{font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:16px;color:var(--gold2);text-transform:uppercase;letter-spacing:1px}
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div id="progress"></div>

<!-- ═══ SLIDE 1 — TITRE ═══ -->
<div class="slide active" id="s1">
  <div class="goldbar"></div>
  <div class="s1-corner"></div>
  <div class="s1-stars"><span class="s1-star">★</span><span class="s1-star">★</span><span class="s1-star">★</span></div>
  <div class="s1-tag">Oral de Brevet — 3ème</div>
  <div class="s1-big">Les <span>Cadets</span><br>de la Défense</div>
  <div class="s1-q">En quoi cette formation contribue-t-elle<br>à la formation de la personne et du citoyen ?</div>
</div>

<!-- ═══ SLIDE 2 — SOMMAIRE ═══ -->
<div class="slide" id="s2">
  <div class="s2-left">
    <div class="s2-deco">PLAN</div>
    <div class="s2-h">Sommaire</div>
  </div>
  <div class="s2-right">
    <div class="pitem au"><div class="pnum">01</div><div><div class="plabel">Introduction</div><div class="pnote">Pourquoi je me suis porté volontaire</div></div></div>
    <div class="pitem au"><div class="pnum">02</div><div><div class="plabel">Les Cadets de la Défense</div><div class="pnote">Origine du programme</div></div></div>
    <div class="pitem au"><div class="pnum">03</div><div><div class="plabel">Les activités</div><div class="pnote">Sorties · Camp Canjuers · Cérémonies</div></div></div>
    <div class="pitem au"><div class="pnum">04</div><div><div class="plabel">Ce que ça m'a apporté</div><div class="pnote">4 grands apprentissages</div></div></div>
    <div class="pitem au"><div class="pnum">05</div><div><div class="plabel">Conclusion</div><div class="pnote">Réponse à la problématique</div></div></div>
  </div>
</div>

<!-- ═══ SLIDE 3 — INTRO ═══ -->
<div class="slide" id="s3">
  <div class="hbar"><div class="hbar-title">Introduction</div><div class="hbar-num">01</div></div>
  <div class="body">
    <div class="card3 au">
      <div class="c3-icon">❓</div>
      <div class="c3-title">La problématique</div>
      <div class="c3-kw"><span class="kw">Personne</span><span class="kw">Citoyen</span><span class="kw">Formation</span></div>
    </div>
    <div class="card3 au">
      <div class="c3-icon">🙋</div>
      <div class="c3-title">Pourquoi moi ?</div>
      <div class="c3-kw"><span class="kw">Volontaire en 4ème</span><span class="kw">Se dépasser</span><span class="kw">Curiosité</span></div>
    </div>
    <div class="card3 au">
      <div class="c3-icon">🗺️</div>
      <div class="c3-title">Mon plan</div>
      <div class="c3-kw"><span class="kw">Présentation</span><span class="kw">Activités</span><span class="kw">Apports</span></div>
    </div>
  </div>
</div>

<!-- ═══ SLIDE 4 — LES CADETS (origine seulement) ═══ -->
<div class="slide" id="s4">
  <div class="hbar"><div class="hbar-title">Les Cadets de la Défense</div><div class="hbar-num">02</div></div>
  <div class="body">
    <div style="display:flex;flex-direction:column;gap:20px;justify-content:center;width:100%">
      <div class="sec-lbl">Origine</div>
      <div class="big-year">2008</div>
      <div class="c3-kw">
        <span class="kw">Ministère des Armées</span>
        <span class="kw">Lien jeunesse & armée</span>
        <span class="kw">Volontariat</span>
        <span class="kw">Collégiens</span>
        <span class="kw">Éducation nationale</span>
      </div>
    </div>
  </div>
</div>

<!-- ═══ SLIDE 5 — ACTIVITÉS grille 3×3 ═══ -->
<div class="slide" id="s5">
  <div class="hbar"><div class="hbar-title">Les activités de l'année</div><div class="hbar-num">03</div></div>
  <div class="body">
    <div class="acard au" data-n="1">
      <div class="a-icon">⚓</div>
      <div class="a-title">Arsenal & Marine</div>
      <div class="a-kws"><span class="akw">Toulon</span><span class="akw">Musée Marine</span><span class="akw">Matériel</span></div>
    </div>
    <div class="acard au" data-n="2">
      <div class="a-icon">🎖️</div>
      <div class="a-title">Musée artillerie</div>
      <div class="a-kws"><span class="akw">Hyères 1918</span><span class="akw">Cimetière US</span><span class="akw">Ste-Barbe</span></div>
    </div>
    <div class="acard au" data-n="3">
      <div class="a-icon">✈️</div>
      <div class="a-title">SIAé</div>
      <div class="a-kws"><span class="akw">Cuers</span><span class="akw">Aéronautique</span></div>
    </div>
    <div class="acard au" data-n="4">
      <div class="a-icon">🐕</div>
      <div class="a-title">Combat Sol Air (C4)</div>
      <div class="a-kws"><span class="akw">Hyères</span><span class="akw">Blockhaus</span><span class="akw">Chenil</span></div>
    </div>
   
    <div class="acard au" data-n="6">
      <div class="a-icon">🏕️</div>
      <div class="a-title">Survie & Bivouac</div>
      <div class="a-kws"><span class="akw">Nature</span><span class="akw">Bivouac</span><span class="akw">Arsenal</span></div>
    </div>
    <div class="acard au" data-n="6">
      <div class="a-icon">🏔️</div>
      <div class="a-title">Camp Canjuers</div>
      <div class="a-kws"><span class="akw">Camp militaire</span><span class="akw">Collectivité</span><span class="akw">Discipline</span></div>
    </div>
    <div class="acard au" data-n="7">
      <div class="a-icon">🏝️</div>
      <div class="a-title">Porquerolles</div>
      <div class="a-kws"><span class="akw">Île</span><span class="akw">Aquatique</span><span class="akw">Carmignac</span></div>
    </div>
    <div class="acard au" data-n="8">
      <div class="a-icon">🎖️</div>
      <div class="a-title">Cérémonies</div>
      <div class="a-kws"><span class="akw">Devoir de mémoire</span><span class="akw">Commémoration</span></div>
    </div>
  </div>
</div>

<!-- ═══ SLIDE 6 — CAMP CANJUERS ═══ -->
<div class="slide" id="s6">
  <div class="hbar"><div class="hbar-title">Camp militaire de Canjuers</div><div class="hbar-num">03</div></div>
  <div class="body" style="padding:0;gap:0">
    <div class="camp-l">
      <div>
        <div class="camp-big">CAMP<br>CANJUERS</div>
        <div style="font-size:12px;color:var(--gray);margin-top:10px;font-weight:300">Avril 2026</div>
      </div>
      <div>
        <div class="cstat"><div class="cstat-n">5J</div><div class="cstat-l">jours au camp</div></div>
        <div class="cstat"><div class="cstat-n">24h</div><div class="cstat-l">vie en collectivité</div></div>
      </div>
    </div>
    <div class="camp-r">
      <div class="camp-tag">✦ Moment fort de l'année</div>
      <div class="camp-kws">
        <div class="ckw au"><span class="ckw-icon">⏰</span> Réveil tôt</div>
        <div class="ckw au"><span class="ckw-icon">📋</span> Discipline</div>
        <div class="ckw au"><span class="ckw-icon">🏕️</span> Bivouac</div>
        <div class="ckw au"><span class="ckw-icon">🎵</span> Chants militaires</div>
        <div class="ckw au"><span class="ckw-icon">🤝</span> Cohésion</div>
        <div class="ckw au"><span class="ckw-icon">💪</span> Dépassement de soi</div>
      </div>
    </div>
  </div>
</div>

<!-- ═══ SLIDE 7 — CÉRÉMONIES ═══ -->
<div class="slide" id="s7">
  <div class="hbar"><div class="hbar-title">Cérémonies — Devoir de mémoire</div><div class="hbar-num">03</div></div>
  <div class="body">
    <div class="cere-main">
      <div class="quote">"Se souvenir, c'est s'engager."</div>
      <div class="sec-lbl" style="margin-top:6px">Lien Histoire-Géo</div>
      <div class="geo-box au">
        <div style="font-size:26px;flex-shrink:0">📚</div>
        <div>
          <div class="geo-lbl">Programmes de 3ème</div>
          <div class="geo-kws">
            <span class="kw" style="font-size:12px">Guerres mondiales</span>
            <span class="kw" style="font-size:12px">Monuments aux morts</span>
            <span class="kw" style="font-size:12px">Lieux de mémoire</span>
            <span class="kw" style="font-size:12px">Construction de la paix</span>
          </div>
        </div>
      </div>
    </div>
    <div class="cere-side">
      <div class="cere-dc au">
        <div class="cere-d">11 Novembre 2025</div>
        <div class="cere-p">📍 Hyères</div>
        <div class="cere-kws"><span class="ckwsmall">Gerbes</span><span class="ckwsmall">Marseillaise</span><span class="ckwsmall">Silence</span></div>
      </div>
      <div class="cere-dc au">
        <div class="cere-d">8 Mai 2026</div>
        <div class="cere-p">📍 Hyères</div>
        <div class="cere-kws"><span class="ckwsmall">Victoire 1945</span><span class="ckwsmall">Commémoration</span></div>
      </div>
      <div class="cere-dc au">
        <div class="cere-d">Cérémonie d'installation</div>
        <div class="cere-p">📍 Toulon</div>
        <div class="cere-kws"><span class="ckwsmall">Fanion</span><span class="ckwsmall">Carnet</span><span class="ckwsmall">Ordre serré</span></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══ SLIDE 8 — CE QUE ÇA M'A APPORTÉ (4 cartes) ═══ -->
<div class="slide" id="s8">
  <div class="hbar"><div class="hbar-title">Ce que les Cadets m'ont apporté</div><div class="hbar-num">04</div></div>
  <div class="body">
    <div class="vcard au">
      <div class="vc-num">1</div>
      <div class="vc-title">Discipline & Rigueur</div>
      <div class="vc-kws"><span class="vkw">Règles</span><span class="vkw">Ponctualité</span><span class="vkw">Sérieux</span></div>
    </div>
    <div class="vcard au">
      <div class="vc-num">2</div>
      <div class="vc-title">Esprit d'équipe & Cohésion</div>
      <div class="vc-kws"><span class="vkw">Ensemble</span><span class="vkw">Liens forts</span><span class="vkw">Appartenance</span></div>
    </div>
    <div class="vcard au">
      <div class="vc-num">3</div>
      <div class="vc-title">Autonomie & Prendre sur soi</div>
      <div class="vc-kws"><span class="vkw">Responsable</span><span class="vkw">Se dépasser</span><span class="vkw">Tenir</span></div>
    </div>
    <div class="vcard au">
      <div class="vc-num">4</div>
      <div class="vc-title">Sens civique & Devoir de mémoire</div>
      <div class="vc-kws"><span class="vkw">Citoyen</span><span class="vkw">Mémoire</span><span class="vkw">Engagement</span></div>
    </div>
  </div>
</div>

<!-- ═══ SLIDE 9 — CONCLUSION ═══ -->
<div class="slide" id="s9">
  <div class="goldbar"></div>
  <div class="s10-in">
    <div class="s10-lbl">05 — Conclusion</div>
    <div class="s10-big">Ce que je retiens<br>des Cadets</div>
    <div class="s10-line"></div>
    <div class="s10-kws au">
      <span class="s10kw">🌟 Expérience unique</span>
      <span class="s10kw">🤝 Valeurs pour la vie</span>
      <span class="s10kw">🇫🇷 Citoyen responsable</span>
      <span class="s10kw">📖 Lien avec les cours</span>
      <span class="s10kw">💪 Plus fort qu'avant</span>
    </div>
    <div class="s10-cards">
      <div class="s10c au"><div class="s10c-icon">👤</div><div class="s10c-txt">La personne</div></div>
      <div class="s10c au"><div class="s10c-icon">🏛️</div><div class="s10c-txt">Le citoyen</div></div>
      <div class="s10c au"><div class="s10c-icon">🎯</div><div class="s10c-txt">Réponse à la problématique</div></div>
    </div>
  </div>
</div>


<!-- ═══ SLIDE 10 — MERCI ═══ -->
<div class="slide" id="s10">
  <div class="goldbar"></div>
  <div class="merci-in">
    <div class="merci-big">Merci de<br>m'avoir <span>écouté</span></div>
    <div class="merci-line"></div>
    <div class="merci-sub">Je suis disponible pour répondre à vos questions.</div>
  </div>
</div>

<!-- NAV -->
<div id="nav">
  <button onclick="go(-1)">&#8592;</button>
  <div class="dots" id="dots"></div>
  <div id="counter">1 / 10</div>
  <button onclick="go(1)">&#8594;</button>
</div>

<script>
const slides=document.querySelectorAll('.slide'),total=slides.length;
let cur=0;
const dotsEl=document.getElementById('dots');
for(let i=0;i<total;i++){const d=document.createElement('div');d.className='dot'+(i===0?' on':'');d.onclick=()=>goTo(i);dotsEl.appendChild(d);}
function goTo(n){slides[cur].classList.remove('active');dotsEl.children[cur].classList.remove('on');cur=(n+total)%total;slides[cur].classList.add('active');dotsEl.children[cur].classList.add('on');document.getElementById('counter').textContent=(cur+1)+' / '+total;document.getElementById('progress').style.width=((cur+1)/total*100)+'%';}
function go(d){goTo(cur+d)}
document.addEventListener('keydown',e=>{if(e.key==='ArrowRight'||e.key===' ')go(1);if(e.key==='ArrowLeft')go(-1);});
let tx=0;
document.addEventListener('touchstart',e=>tx=e.touches[0].clientX);
document.addEventListener('touchend',e=>{const dx=e.changedTouches[0].clientX-tx;if(Math.abs(dx)>50)go(dx<0?1:-1)});
const cur2=document.getElementById('cursor');
document.addEventListener('mousemove',e=>{cur2.style.left=e.clientX+'px';cur2.style.top=e.clientY+'px'});
document.getElementById('progress').style.width=(1/total*100)+'%';
</script>
</body>
</html>
