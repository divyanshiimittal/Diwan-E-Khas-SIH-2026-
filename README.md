<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NEVYRA — The Northeast, Unhurried</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,600;1,9..144,400;1,9..144,500&family=Manrope:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@400;500;600&family=Space+Grotesk:wght@500;600;700&display=swap" rel="stylesheet">
<style>
/* ============ TOKENS ============ */
:root{
  --mist:#F5F8F1;
  --paper:#FFFFFF;
  --pine:#1E3A2F;
  --pine-2:#2F5745;
  --teal:#2E6B72;
  --marigold:#D9A441;
  --terracotta:#B85A3E;
  --sage:#E9F0E3;
  --sage-2:#DCE7D5;
  --ink:#20302A;
  --ink-soft:#4B5D54;
  --line:#D7E1CF;
  --shadow: 0 8px 30px -12px rgba(30,58,47,0.25);
  --radius: 14px;

  /* ---- vivid accents (colour pass) ---- */
  --coral:#E8604C;
  --sky:#2E8FA6;
  --violet:#7B5EA7;
  --sun:#F2B705;
  --rose:#D6537D;
  --mint:#2FB286;
  --royal:#3E6FB0;
  --amber:#D9752E;

  /* ---- per-state accent colours ---- */
  --c-assam:#2F8F5B;
  --c-meghalaya:#2E8FA6;
  --c-arunachal:#7B5EA7;
  --c-nagaland:#D9752E;
  --c-manipur:#C2447A;
  --c-mizoram:#2FB286;
  --c-tripura:#B85A3E;
  --c-sikkim:#3E6FB0;

  /* ---- gen-z pass: extra juice ---- */
  --hot:#FF4D8D;
  --zap:#7C5CFF;
  --lime:#B4F03C;
  --cyber:#00D9C0;
  --sun2:#FFC629;
  --ink-hard:#0F1710;
  --pop-shadow: 5px 5px 0 var(--ink-hard);
  --pop-shadow-sm: 3px 3px 0 var(--ink-hard);
  --grot: 'Space Grotesk', sans-serif;
}

*{box-sizing:border-box;}
html{scroll-behavior:smooth;}
@media (prefers-reduced-motion: reduce){
  html{scroll-behavior:auto;}
  *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important;}
}
body{
  margin:0;
  background:var(--mist);
  color:var(--ink);
  font-family:'Manrope',sans-serif;
  font-size:16px;
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
}
h1,h2,h3,h4{
  font-family:'Fraunces',serif;
  color:var(--pine);
  margin:0;
  font-weight:500;
  letter-spacing:-0.01em;
}
.mono{font-family:'IBM Plex Mono',monospace;}
a{color:inherit;}
img,svg{display:block;max-width:100%;}
button{font-family:inherit;cursor:pointer;}
:focus-visible{outline:3px solid var(--marigold); outline-offset:3px;}

.wrap{max-width:1180px; margin:0 auto; padding:0 28px;}
.eyebrow{
  font-family:'IBM Plex Mono',monospace;
  text-transform:uppercase;
  letter-spacing:0.14em;
  font-size:12px;
  color:var(--teal);
  font-weight:600;
}
.section{padding:96px 0;}
.section-head{max-width:680px; margin-bottom:48px;}
.section-head h2{font-size:clamp(28px,4vw,42px); margin-top:10px;}
.section-head p{color:var(--ink-soft); font-size:17px; margin-top:14px;}

/* ============ NAV ============ */
header.site-nav{
  position:sticky; top:0; z-index:50;
  background:rgba(245,248,241,0.86);
  backdrop-filter:blur(10px);
  border-bottom:1px solid var(--line);
}
.nav-inner{
  max-width:1180px; margin:0 auto; padding:16px 28px;
  display:flex; align-items:center; justify-content:space-between;
}
.brand{display:flex; align-items:baseline; gap:10px;}
.brand-mark{font-family:'Fraunces',serif; font-weight:600; font-size:22px; letter-spacing:0.02em; color:var(--pine);}
.brand-sub{font-family:'IBM Plex Mono',monospace; font-size:10px; letter-spacing:0.16em; color:var(--teal); text-transform:uppercase;}
.nav-links{display:flex; gap:28px; list-style:none; margin:0; padding:0;}
.nav-links a{
  font-size:14px; font-weight:600; text-decoration:none; color:var(--ink-soft);
  padding-bottom:3px; border-bottom:2px solid transparent; transition:color .2s, border-color .2s;
}
.nav-links a:hover{color:var(--pine); border-color:var(--marigold);}
.nav-toggle{display:none; background:none; border:1px solid var(--line); border-radius:8px; padding:8px 10px;}
@media (max-width:860px){
  .nav-links{
    position:absolute; top:100%; left:0; right:0; background:var(--paper);
    flex-direction:column; padding:18px 28px; gap:16px; border-bottom:1px solid var(--line);
    display:none;
  }
  .nav-links.open{display:flex;}
  .nav-toggle{display:block;}
}

/* ============ HERO ============ */
.hero{
  position:relative; overflow:hidden;
  min-height:92vh;
  display:flex; flex-direction:column; justify-content:flex-end;
  background:linear-gradient(180deg,#FCEFD6 0%, #F7DCC6 22%, #DCEAE2 55%, var(--mist) 100%);
}
.hero-sky{
  position:absolute; inset:0; z-index:0;
}
.hero-content{
  position:relative; z-index:3;
  padding:0 28px 64px;
  max-width:1180px; margin:0 auto; width:100%;
}
.hero-quote{
  font-family:'Fraunces',serif; font-style:italic; font-weight:400;
  font-size:clamp(26px,4.4vw,48px);
  color:var(--pine);
  max-width:840px;
  line-height:1.28;
}
.hero-quote-src{
  margin-top:16px;
  font-family:'IBM Plex Mono',monospace;
  font-size:13px; color:var(--ink-soft); letter-spacing:0.02em;
}
.hero-tagline{
  margin-top:34px; display:flex; gap:14px; align-items:center; flex-wrap:wrap;
}
.pill{
  font-family:'IBM Plex Mono',monospace; font-size:12px; letter-spacing:0.06em;
  background:var(--paper); border:1px solid var(--line); border-radius:100px;
  padding:8px 16px; color:var(--pine-2);
}
.pill:nth-of-type(1){background:linear-gradient(120deg,#FDE9C8,#FBD3A9); border-color:#F0C089; color:#8A4A12;}
.pill:nth-of-type(2){background:linear-gradient(120deg,#DCEEE8,#CDE6E0); border-color:var(--sky); color:#1D5D6B;}
.scroll-cue{
  position:absolute; bottom:26px; right:28px; z-index:3;
  display:flex; flex-direction:column; align-items:center; gap:8px;
  font-family:'IBM Plex Mono',monospace; font-size:11px; letter-spacing:0.14em;
  color:var(--pine-2); text-transform:uppercase;
}
.scroll-cue .line{width:1px; height:38px; background:var(--pine-2); position:relative; overflow:hidden;}
.scroll-cue .line::after{
  content:''; position:absolute; top:-40px; left:0; width:100%; height:40%;
  background:var(--marigold); animation:dropline 2.4s ease-in-out infinite;
}
@keyframes dropline{
  0%{top:-40%;} 60%{top:100%;} 100%{top:100%;}
}
@media (prefers-reduced-motion: reduce){ .scroll-cue .line::after{ animation:none; top:60%; } }

.ridge{display:block; width:100%; height:auto;}

/* ============ STEP INDEX ============ */
.step-index{
  background:linear-gradient(90deg,var(--pine) 0%, var(--pine-2) 45%, var(--sky) 100%); color:var(--mist);
  padding:14px 0;
}
.step-index .wrap{display:flex; gap:0; overflow-x:auto; scrollbar-width:none;}
.step-index .wrap::-webkit-scrollbar{display:none;}
.step-index a{
  font-family:'IBM Plex Mono',monospace; font-size:12px; white-space:nowrap;
  text-decoration:none; color:#CFE0D4; padding:8px 22px 8px 0; display:flex; align-items:center; gap:8px;
}
.step-index a b{color:var(--marigold); font-weight:600;}
.step-index a:hover{color:#fff;}

/* ============ SEASON ADVISORY ============ */
.season-panel{
  background:var(--paper); border:1px solid var(--line); border-radius:var(--radius);
  box-shadow:var(--shadow); padding:36px; margin-bottom:28px;
}
.month-strip{
  display:grid; grid-template-columns:repeat(12,1fr); gap:6px; margin-top:22px;
}
.month-btn{
  border:1px solid var(--line); background:var(--sage); border-radius:8px;
  padding:12px 4px; text-align:center; font-family:'IBM Plex Mono',monospace; font-size:11px;
  color:var(--ink-soft); transition:transform .15s, box-shadow .15s;
}
.month-btn:hover{transform:translateY(-3px);}
.month-btn.best{background:#DCEEDC; border-color:#B7DAB8; color:var(--pine-2);}
.month-btn.good{background:#F5EBD2; border-color:var(--marigold); color:#8A6512;}
.month-btn.flood{background:#F5DCD2; border-color:var(--terracotta); color:#8A3A22;}
.month-btn.selected{box-shadow:0 0 0 3px var(--pine) inset;}
.season-detail{
  margin-top:24px; padding:22px; border-radius:10px; background:var(--sage); border:1px solid var(--sage-2);
  display:grid; grid-template-columns:1fr 1fr 1fr; gap:20px;
}
@media (max-width:760px){.season-detail{grid-template-columns:1fr;}}
.season-detail .stat-label{font-family:'IBM Plex Mono',monospace; font-size:11px; text-transform:uppercase; letter-spacing:0.08em; color:var(--teal);}
.season-detail .stat-value{font-family:'Fraunces',serif; font-size:20px; color:var(--pine); margin-top:6px;}

.legend{display:flex; gap:18px; margin-top:18px; flex-wrap:wrap; font-size:13px; color:var(--ink-soft);}
.legend span{display:inline-flex; align-items:center; gap:7px;}
.legend i{width:12px; height:12px; border-radius:3px; display:inline-block;}
.legend .b{background:#DCEEDC; border:1px solid #B7DAB8;}
.legend .g{background:#F5EBD2; border:1px solid var(--marigold);}
.legend .f{background:#F5DCD2; border:1px solid var(--terracotta);}

.flood-alert{
  display:flex; gap:16px; align-items:flex-start;
  background:#FBEFE9; border:1px solid var(--terracotta); border-radius:var(--radius);
  padding:22px 24px;
}
.flood-alert .icon{
  flex:0 0 auto; width:38px; height:38px; border-radius:50%; background:var(--terracotta);
  display:flex; align-items:center; justify-content:center; color:#fff; font-family:'IBM Plex Mono',monospace; font-weight:700;
}
.flood-alert h4{color:#8A3A22; font-size:17px;}
.flood-alert p{margin:8px 0 0; color:#7A4331; font-size:14.5px;}

/* ============ STICKERS / MARQUEE / GEN-Z BITS ============ */
.sticker{
  display:inline-flex; align-items:center; gap:6px;
  font-family:var(--grot); font-weight:700; font-size:12px; letter-spacing:0.02em;
  background:var(--lime); color:var(--ink-hard); border:2px solid var(--ink-hard);
  border-radius:100px; padding:6px 14px; box-shadow:var(--pop-shadow-sm);
  transform:rotate(-2deg);
}
.sticker.pink{background:var(--hot); color:#fff;}
.sticker.zap{background:var(--zap); color:#fff;}
.sticker.sun{background:var(--sun2); color:var(--ink-hard);}

.marquee{
  background:var(--ink-hard); color:var(--lime); overflow:hidden; white-space:nowrap;
  padding:9px 0; border-top:2px solid var(--ink-hard); border-bottom:2px solid var(--ink-hard);
}
.marquee-track{display:inline-flex; gap:36px; animation:marquee 28s linear infinite; padding-left:36px;}
.marquee-track span{
  font-family:var(--grot); font-weight:600; font-size:13px; letter-spacing:0.04em; text-transform:uppercase;
  display:inline-flex; align-items:center; gap:10px;
}
@keyframes marquee{ 0%{transform:translateX(0);} 100%{transform:translateX(-50%);} }
@media (prefers-reduced-motion: reduce){ .marquee-track{animation:none;} }

/* ---- photo banners + credit ---- */
.photo-credit{
  font-family:var(--grot); font-size:11px; color:var(--ink-soft);
  display:flex; align-items:center; gap:6px; margin-top:6px;
}
.photo-credit a{color:var(--teal); text-decoration:none; border-bottom:1px dashed var(--teal);}
.photo-credit a:hover{color:var(--pine);}
.photo-credit .cc-badge{
  font-family:var(--grot); font-weight:700; font-size:10px; letter-spacing:0.03em;
  background:var(--sage); border:1px solid var(--sage-2); color:var(--pine-2);
  padding:2px 7px; border-radius:100px; white-space:nowrap;
}
.state-card-photo{
  height:130px; margin:-22px -22px 16px; border-radius:var(--radius) var(--radius) 0 0;
  background-size:cover; background-position:center; position:relative; overflow:hidden;
  border-bottom:3px solid var(--ink-hard);
}
.state-card-photo::after{
  content:''; position:absolute; inset:0;
  background:linear-gradient(180deg, rgba(0,0,0,0) 40%, rgba(0,0,0,0.55) 100%);
}
.state-card-photo .icon-chip{
  position:absolute; bottom:10px; left:12px; z-index:2;
  width:34px; height:34px; border-radius:9px; background:rgba(255,255,255,0.92);
  display:flex; align-items:center; justify-content:center; color:var(--accent, var(--pine-2));
  box-shadow:var(--pop-shadow-sm);
}
.state-card-photo .icon-chip svg{width:20px; height:20px;}
.state-panel-hero{
  position:relative; border-radius:10px; overflow:hidden; margin-bottom:20px;
  height:220px; background-size:cover; background-position:center;
  border:2px solid var(--ink-hard);
}
.state-panel-hero .caption{
  position:absolute; left:0; right:0; bottom:0; padding:10px 14px;
  background:linear-gradient(0deg, rgba(0,0,0,0.7), rgba(0,0,0,0));
  display:flex; justify-content:space-between; align-items:flex-end; gap:10px; flex-wrap:wrap;
}
.state-panel-hero .caption span.place-name{
  font-family:var(--grot); font-weight:600; color:#fff; font-size:14px;
}
.state-panel-hero .caption a{
  font-family:var(--grot); font-size:11px; color:#EAF2E4; text-decoration:none;
  border-bottom:1px dashed rgba(255,255,255,0.6);
}

/* ============ ASK NEVYRA — CHAT WIZARD ============ */
.chat-shell{
  background:var(--ink-hard); border-radius:20px; border:2px solid var(--ink-hard);
  box-shadow:var(--pop-shadow); overflow:hidden;
}
.chat-topbar{
  display:flex; align-items:center; gap:10px; padding:16px 20px;
  background:linear-gradient(120deg, var(--zap), var(--hot));
}
.chat-topbar .dot{width:9px; height:9px; border-radius:50%; background:rgba(255,255,255,0.55);}
.chat-topbar .who{
  font-family:var(--grot); font-weight:700; color:#fff; font-size:14px; margin-left:4px;
}
.chat-topbar .status{
  margin-left:auto; font-family:var(--grot); font-size:11px; color:rgba(255,255,255,0.85);
  display:flex; align-items:center; gap:6px;
}
.chat-topbar .status i{width:7px; height:7px; border-radius:50%; background:var(--lime); display:inline-block;}
.chat-body{
  background:#0F1710 url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="60" height="60"><circle cx="2" cy="2" r="1.4" fill="%23223026"/></svg>');
  padding:22px 20px; min-height:120px; max-height:520px; overflow-y:auto;
  display:flex; flex-direction:column; gap:14px;
}
.bubble{
  max-width:82%; padding:12px 16px; border-radius:16px; font-size:14.5px; line-height:1.5;
  animation:pop-in .35s ease;
}
@keyframes pop-in{ from{opacity:0; transform:translateY(8px) scale(.98);} to{opacity:1; transform:translateY(0) scale(1);} }
.bubble.bot{
  align-self:flex-start; background:#1B271E; color:#EAF2E4; border-bottom-left-radius:4px;
  font-family:'Manrope',sans-serif;
}
.bubble.user{
  align-self:flex-end; background:var(--lime); color:var(--ink-hard); border-bottom-right-radius:4px;
  font-family:var(--grot); font-weight:600;
}
.bubble.result{
  align-self:stretch; max-width:100%; background:linear-gradient(135deg, #1B271E, #23342A);
  border:1px solid #33473A;
}
.bubble.result h4{color:var(--lime); font-size:16px; margin-bottom:6px; font-family:var(--grot);}
.bubble.result p{color:#CFE0D4; margin:0 0 10px; font-size:13.5px;}
.typing{
  align-self:flex-start; display:flex; gap:4px; padding:14px 16px; background:#1B271E; border-radius:16px; border-bottom-left-radius:4px;
}
.typing span{width:6px; height:6px; border-radius:50%; background:#7A9384; animation:blink 1.2s infinite ease-in-out;}
.typing span:nth-child(2){animation-delay:.15s;}
.typing span:nth-child(3){animation-delay:.3s;}
@keyframes blink{ 0%,80%,100%{opacity:.25;} 40%{opacity:1;} }
.chat-choices{
  display:flex; flex-wrap:wrap; gap:8px; padding:4px 20px 20px; background:#0F1710;
}
.chat-choices button{
  font-family:var(--grot); font-weight:600; font-size:13px; color:#EAF2E4;
  background:#1B271E; border:1.5px solid #33473A; border-radius:100px; padding:9px 16px;
  transition:transform .15s, background .15s, border-color .15s;
}
.chat-choices button:hover{background:var(--lime); color:var(--ink-hard); border-color:var(--lime); transform:translateY(-2px);}
.chat-choices .go-btn{
  background:linear-gradient(120deg, var(--hot), var(--zap)); border:none; color:#fff;
  padding:11px 22px; box-shadow:var(--pop-shadow-sm);
}
.chat-choices .go-btn:hover{transform:translateY(-2px) rotate(-1deg); color:#fff;}
.chat-restart{
  display:flex; justify-content:flex-end; padding:0 20px 18px; background:#0F1710;
}
.chat-restart button{
  font-family:var(--grot); font-size:11.5px; color:#7A9384; background:none; border:none;
  text-decoration:underline; text-underline-offset:3px;
}
.chat-restart button:hover{color:var(--lime);}

/* ============ ITINERARY BUILDER ============ */
.builder{
  background:var(--paper); border:1px solid var(--line); border-radius:var(--radius);
  box-shadow:var(--shadow); padding:40px;
}
.builder-form{
  display:grid; grid-template-columns:1fr 1fr 1.2fr auto; gap:24px; align-items:end;
}
@media (max-width:900px){.builder-form{grid-template-columns:1fr 1fr; }}
@media (max-width:560px){.builder-form{grid-template-columns:1fr;}}
.field label{
  display:block; font-family:'IBM Plex Mono',monospace; font-size:11px; text-transform:uppercase;
  letter-spacing:0.08em; color:var(--teal); margin-bottom:10px;
}
.field .days-row{display:flex; align-items:center; gap:14px;}
input[type=range]{-webkit-appearance:none; width:100%; height:4px; background:var(--line); border-radius:4px; outline:none;}
input[type=range]::-webkit-slider-thumb{-webkit-appearance:none; width:20px; height:20px; border-radius:50%; background:var(--pine); border:3px solid var(--marigold); cursor:pointer;}
input[type=range]::-moz-range-thumb{width:20px; height:20px; border-radius:50%; background:var(--pine); border:3px solid var(--marigold); cursor:pointer;}
.days-value{font-family:'Fraunces',serif; font-size:26px; color:var(--pine); min-width:52px;}
select{
  width:100%; padding:12px 14px; border-radius:8px; border:1px solid var(--line); background:var(--sage);
  font-family:'Manrope',sans-serif; font-size:14px; font-weight:600; color:var(--ink);
}
.btn-primary{
  background:linear-gradient(120deg,var(--pine-2),var(--sky)); color:#fff; border:none; padding:14px 26px; border-radius:8px;
  font-weight:700; font-size:14px; letter-spacing:0.02em; transition:background .2s, transform .15s, box-shadow .2s;
  white-space:nowrap; box-shadow:0 6px 18px -6px rgba(46,139,166,0.55);
}
.btn-primary:hover{background:linear-gradient(120deg,var(--pine),var(--teal)); transform:translateY(-2px);}
.btn-ghost{
  background:transparent; border:1px solid var(--line); color:var(--pine-2); padding:10px 18px;
  border-radius:8px; font-weight:600; font-size:13px;
}
.btn-ghost.active, .btn-ghost:hover{border-color:var(--pine); background:var(--sage);}

.itinerary-output{margin-top:36px;}
.itinerary-summary{
  display:flex; gap:36px; flex-wrap:wrap; padding:20px 0 28px; border-bottom:1px dashed var(--line); margin-bottom:28px;
}
.itinerary-summary .box .stat-label{font-family:'IBM Plex Mono',monospace; font-size:11px; text-transform:uppercase; color:var(--teal); letter-spacing:.08em;}
.itinerary-summary .box .stat-value{font-family:'Fraunces',serif; font-size:24px; color:var(--pine); margin-top:4px;}
.day-card{
  display:grid; grid-template-columns:64px 1fr auto; gap:18px; align-items:start;
  padding:18px 0; border-bottom:1px solid var(--line);
}
.day-card:last-child{border-bottom:none;}
.day-num{
  font-family:'IBM Plex Mono',monospace; font-size:12px; color:var(--teal); font-weight:600;
  background:var(--sage); border-radius:8px; text-align:center; padding:10px 0;
}
.day-body h4{font-size:17px;}
.day-body .day-state{font-family:'IBM Plex Mono',monospace; font-size:11px; color:var(--marigold); text-transform:uppercase; letter-spacing:.06em; margin-bottom:4px; display:block;}
.day-body p{margin:6px 0 0; color:var(--ink-soft); font-size:14.5px;}
.day-cost{font-family:'IBM Plex Mono',monospace; font-size:14px; color:var(--pine); white-space:nowrap; text-align:right;}

/* ============ STATE GRID ============ */
.state-grid{
  display:grid; grid-template-columns:repeat(4,1fr); gap:18px;
}
@media (max-width:960px){.state-grid{grid-template-columns:repeat(2,1fr);}}
@media (max-width:560px){.state-grid{grid-template-columns:1fr;}}
.state-card{
  background:var(--paper); border:1px solid var(--line); border-radius:var(--radius);
  padding:22px; cursor:pointer; transition:box-shadow .2s, transform .2s, border-color .2s;
  position:relative;
}
.state-card:hover{box-shadow:var(--shadow); transform:translateY(-4px); border-color:var(--pine-2);}
.state-card{border-top:4px solid var(--accent, var(--pine-2));}
.state-card .icon{width:34px; height:34px; color:var(--accent, var(--pine-2)); margin-bottom:14px;}
.state-card h3{font-size:19px;}
.state-card .tag{font-family:'IBM Plex Mono',monospace; font-size:11px; color:var(--accent, var(--teal)); margin-top:6px; display:block;}
.state-card .expand{position:absolute; top:20px; right:20px; font-family:'IBM Plex Mono',monospace; color:var(--ink-soft); font-size:18px; transition:transform .2s;}
.state-card.open .expand{transform:rotate(45deg); color:var(--marigold);}

/* ---- place photo banner ---- */
.place{padding:0; overflow:hidden;}
.place .photo{
  height:108px; display:flex; align-items:center; justify-content:center;
  font-size:40px; position:relative; color:#fff;
}
.place .photo::after{
  content:''; position:absolute; inset:0;
  background:radial-gradient(circle at 30% 20%, rgba(255,255,255,0.28), transparent 60%);
}
.place .body{padding:14px 16px 16px;}
.place .photo-link{
  display:inline-flex; align-items:center; gap:5px; margin-top:8px;
  font-family:'IBM Plex Mono',monospace; font-size:11px; text-decoration:none;
  color:var(--teal); border-bottom:1px dashed var(--teal); padding-bottom:1px;
}
.place .photo-link:hover{color:var(--pine);}

/* ---- GUIDES ---- */
.guide-grid{display:grid; grid-template-columns:repeat(4,1fr); gap:18px;}
@media (max-width:960px){.guide-grid{grid-template-columns:repeat(2,1fr);}}
@media (max-width:560px){.guide-grid{grid-template-columns:1fr;}}
.guide-card{
  background:var(--paper); border:1px solid var(--line); border-radius:var(--radius);
  overflow:hidden; box-shadow:0 1px 0 var(--line); display:flex; flex-direction:column;
}
.guide-card .head{
  padding:18px 18px 16px; color:#fff; background:var(--accent, var(--pine));
}
.guide-card .head h4{color:#fff; font-size:17px;}
.guide-card .head .spec{font-family:'IBM Plex Mono',monospace; font-size:11px; opacity:0.9; margin-top:5px; display:block;}
.guide-card .body{padding:16px 18px 18px; flex:1; display:flex; flex-direction:column; gap:10px;}
.guide-rate{display:flex; justify-content:space-between; font-size:13px; border-bottom:1px dashed var(--line); padding-bottom:8px;}
.guide-rate b{display:block; font-family:'Fraunces',serif; font-size:15px; color:var(--pine); font-weight:600;}
.guide-rate span.who{color:var(--ink-soft); font-family:'IBM Plex Mono',monospace; font-size:10.5px; text-transform:uppercase; letter-spacing:.05em;}
.guide-link{
  margin-top:auto; display:inline-flex; align-items:center; justify-content:center; gap:6px;
  background:var(--sage); border:1px solid var(--sage-2); border-radius:8px; padding:9px 12px;
  font-size:12.5px; font-weight:700; color:var(--pine-2); text-decoration:none; transition:background .2s;
}
.guide-link:hover{background:var(--accent, var(--pine)); color:#fff; border-color:transparent;}
.guide-note{
  grid-column:1/-1; background:var(--paper); border:1px dashed var(--line); border-radius:var(--radius);
  padding:20px 22px; font-size:13.5px; color:var(--ink-soft); margin-top:4px;
}
.guide-note b{color:var(--pine-2);}
.guide-note a{color:var(--teal); font-weight:600; text-decoration:none; border-bottom:1px dashed var(--teal);}

.state-panel{
  grid-column:1/-1; background:var(--sage); border:1px solid var(--sage-2); border-radius:var(--radius);
  padding:0; max-height:0; overflow:hidden; transition:max-height .4s ease, padding .4s ease;
}
.state-panel.open{padding:28px; max-height:900px;}
.state-panel .places{display:grid; grid-template-columns:repeat(3,1fr); gap:18px; margin-top:16px;}
@media (max-width:820px){.state-panel .places{grid-template-columns:1fr 1fr;}}
@media (max-width:560px){.state-panel .places{grid-template-columns:1fr;}}
.place{background:var(--paper); border:1px solid var(--line); border-radius:10px; padding:16px;}
.place h5{font-family:'Fraunces',serif; font-size:15.5px; font-weight:600; color:var(--pine); margin:0 0 6px;}
.place p{margin:0; font-size:13.5px; color:var(--ink-soft);}
.state-panel-meta{display:flex; gap:28px; flex-wrap:wrap; font-size:13.5px; color:var(--ink-soft);}
.state-panel-meta b{color:var(--pine-2); font-family:'IBM Plex Mono',monospace; font-size:11px; text-transform:uppercase; letter-spacing:.06em; display:block; margin-bottom:4px;}

/* ============ HOTELS ============ */
.hotel-controls{display:flex; gap:28px; flex-wrap:wrap; align-items:center; margin-bottom:28px;}
.tier-toggle{display:flex; gap:8px;}
.hotel-grid{display:grid; grid-template-columns:repeat(3,1fr); gap:20px;}
@media (max-width:900px){.hotel-grid{grid-template-columns:1fr 1fr;}}
@media (max-width:600px){.hotel-grid{grid-template-columns:1fr;}}
.hotel-card{
  background:var(--paper); border:1px solid var(--line); border-radius:var(--radius); overflow:hidden;
  box-shadow:0 1px 0 var(--line);
}
.hotel-card .swatch{height:96px; }
.hotel-card .body{padding:18px;}
.hotel-card h4{font-size:16.5px;}
.hotel-card .loc{font-family:'IBM Plex Mono',monospace; font-size:11px; color:var(--teal); margin-top:4px; display:block;}
.hotel-card p{font-size:13.5px; color:var(--ink-soft); margin:10px 0 0;}
.hotel-card .price{
  margin-top:14px; padding-top:14px; border-top:1px dashed var(--line);
  display:flex; justify-content:space-between; align-items:baseline;
}
.hotel-card .price .amt{font-family:'Fraunces',serif; font-size:19px; color:var(--pine);}
.hotel-card .price .per{font-family:'IBM Plex Mono',monospace; font-size:10.5px; color:var(--ink-soft);}
.tier-badge{
  font-family:'IBM Plex Mono',monospace; font-size:10px; text-transform:uppercase; letter-spacing:.08em;
  padding:4px 9px; border-radius:100px; display:inline-block;
}
.tier-badge.budget{background:#DCEEDC; color:#2F5745;}
.tier-badge.mid{background:#F5EBD2; color:#8A6512;}
.tier-badge.luxury{background:#EADFF5; color:#5C3A8A;}

/* ============ PRICE TABLE ============ */
.price-groups{display:grid; grid-template-columns:1fr 1fr; gap:28px;}
@media (max-width:800px){.price-groups{grid-template-columns:1fr;}}
.price-group{background:var(--paper); border:1px solid var(--line); border-radius:var(--radius); padding:26px; border-top:4px solid var(--pine-2);}
.price-group:nth-child(4n+1){border-top-color:var(--coral);}
.price-group:nth-child(4n+2){border-top-color:var(--sky);}
.price-group:nth-child(4n+3){border-top-color:var(--amber);}
.price-group:nth-child(4n+4){border-top-color:var(--violet);}
.price-group h4{font-size:15px; text-transform:uppercase; letter-spacing:.06em; font-family:'IBM Plex Mono',monospace; color:var(--teal); font-weight:600; margin-bottom:16px;}
.price-row{display:flex; justify-content:space-between; align-items:center; padding:10px 0; border-bottom:1px solid var(--line); gap:12px;}
.price-row:last-child{border-bottom:none;}
.price-row .item{font-size:14.5px; color:var(--ink);}
.price-row .item small{display:block; color:var(--ink-soft); font-size:12px; margin-top:2px;}
.price-row .amount{font-family:'IBM Plex Mono',monospace; font-size:14px; color:var(--pine); white-space:nowrap;}
.price-note{margin-top:18px; font-size:12.5px; color:var(--ink-soft); font-style:italic;}

/* ============ CULTURE ============ */
.culture-grid{display:grid; grid-template-columns:repeat(3,1fr); gap:20px;}
@media (max-width:900px){.culture-grid{grid-template-columns:1fr 1fr;}}
@media (max-width:600px){.culture-grid{grid-template-columns:1fr;}}
.culture-card{background:var(--paper); border:1px solid var(--line); border-radius:var(--radius); padding:24px; border-left:4px solid var(--pine-2);}
.culture-card:nth-child(6n+1){border-left-color:var(--coral);}
.culture-card:nth-child(6n+2){border-left-color:var(--sky);}
.culture-card:nth-child(6n+3){border-left-color:var(--violet);}
.culture-card:nth-child(6n+4){border-left-color:var(--sun);}
.culture-card:nth-child(6n+5){border-left-color:var(--rose);}
.culture-card:nth-child(6n+6){border-left-color:var(--mint);}
.culture-card .eyebrow{margin-bottom:8px; display:block;}
.culture-card h4{font-size:17px;}
.culture-card p{font-size:13.5px; color:var(--ink-soft); margin-top:10px;}

/* ============ FOOTER ============ */
footer{
  background:var(--pine); color:var(--mist); padding:64px 0 32px; margin-top:40px;
}
.footer-top{display:flex; justify-content:space-between; gap:40px; flex-wrap:wrap; padding-bottom:40px; border-bottom:1px solid rgba(255,255,255,0.14);}
.footer-quote{font-family:'Fraunces',serif; font-style:italic; font-size:22px; max-width:520px; color:#EAF2E4;}
.footer-brand{font-family:'Fraunces',serif; font-size:26px; font-weight:600;}
.footer-cols{display:flex; gap:60px; flex-wrap:wrap;}
.footer-col h5{font-family:'IBM Plex Mono',monospace; font-size:11px; text-transform:uppercase; letter-spacing:.1em; color:var(--marigold); margin-bottom:12px;}
.footer-col a{display:block; color:#CFE0D4; text-decoration:none; font-size:13.5px; margin-bottom:8px;}
.footer-bottom{
  display:flex; justify-content:space-between; padding-top:24px; flex-wrap:wrap; gap:10px;
  font-family:'IBM Plex Mono',monospace; font-size:12px; color:#9BB3A5;
}

/* reveal-on-scroll */
.reveal{opacity:0; transform:translateY(18px); transition:opacity .7s ease, transform .7s ease;}
.reveal.in{opacity:1; transform:translateY(0);}
</style>
</head>
<body>

<header class="site-nav">
  <div class="nav-inner">
    <div class="brand">
      <span class="brand-mark">NEVYRA</span>
      <span class="brand-sub">Northeast &amp; Sikkim</span>
    </div>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle menu">☰</button>
    <ul class="nav-links" id="navLinks">
      <li><a href="#ask">Ask Nevyra</a></li>
      <li><a href="#when">When to go</a></li>
      <li><a href="#plan">Plan a trip</a></li>
      <li><a href="#states">The eight</a></li>
      <li><a href="#stay">Stay</a></li>
      <li><a href="#costs">Prices</a></li>
      <li><a href="#culture">Culture</a></li>
      <li><a href="#guides">Local guides</a></li>
    </ul>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero" id="hero">
  <svg class="hero-sky" viewBox="0 0 1440 760" preserveAspectRatio="xMidYMax slice" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <defs>
      <linearGradient id="skyGrad" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stop-color="#F7C873"/>
        <stop offset="35%" stop-color="#F2A66B"/>
        <stop offset="70%" stop-color="#E9DDC6"/>
        <stop offset="100%" stop-color="#DCEAE2"/>
      </linearGradient>
    </defs>
    <rect width="1440" height="760" fill="url(#skyGrad)"/>
    <circle cx="1180" cy="180" r="90" fill="#F6D77A" opacity="0.85"/>
    <!-- far ridge -->
    <path d="M0,420 L100,380 L220,410 L340,340 L460,400 L600,320 L740,390 L860,330 L1000,400 L1140,350 L1280,410 L1440,370 L1440,760 L0,760 Z" fill="#9FC3C7" opacity="0.8"/>
    <!-- mid ridge -->
    <path d="M0,480 L140,430 L260,470 L400,400 L520,460 L660,400 L800,470 L940,410 L1080,470 L1220,420 L1440,460 L1440,760 L0,760 Z" fill="#5F9E82" opacity="0.9"/>
    <!-- near ridge -->
    <path d="M0,560 L120,510 L260,555 L380,490 L520,550 L640,500 L780,560 L920,505 L1080,555 L1220,510 L1440,545 L1440,760 L0,760 Z" fill="#3E8F5E"/>
    <!-- foreground tea-garden band -->
    <path d="M0,640 C240,610 320,660 560,635 C800,610 900,655 1140,630 C1300,614 1380,628 1440,622 L1440,760 L0,760 Z" fill="#2A6B45"/>
    <!-- mist layers -->
    <g id="mist1" opacity="0.55">
      <ellipse cx="220" cy="470" rx="260" ry="26" fill="#F5F8F1"/>
      <ellipse cx="760" cy="500" rx="320" ry="30" fill="#F5F8F1"/>
      <ellipse cx="1220" cy="460" rx="240" ry="24" fill="#F5F8F1"/>
    </g>
    <g id="mist2" opacity="0.4">
      <ellipse cx="60" cy="555" rx="220" ry="22" fill="#F5F8F1"/>
      <ellipse cx="620" cy="580" rx="300" ry="26" fill="#F5F8F1"/>
      <ellipse cx="1180" cy="560" rx="260" ry="22" fill="#F5F8F1"/>
    </g>
  </svg>

  <div class="hero-content">
    <p class="eyebrow reveal in">NEVYRA · a slow guide to India's far corner</p>
    <p class="hero-quote">"Here the mountains keep their heads in the cloud, and the rivers never remember the same shape twice."</p>
    <p class="hero-quote-src">— carried across the hills, as the old villages tell it</p>
    <div class="hero-tagline">
      <span class="pill">8 states, one green wilderness</span>
      <span class="pill">Living root bridges · monasteries · tea gardens · rice-beer harvests</span>
      <span class="sticker">certified underrated era ✦</span>
    </div>
  </div>

  <div class="scroll-cue"><span>Begin</span><span class="line"></span></div>
</section>

<div class="marquee" aria-hidden="true">
  <div class="marquee-track">
    <span>✦ no cap, this is the most underrated trip in india</span>
    <span>✦ living root bridges &gt; any bridge you've seen</span>
    <span>✦ tap "ask nevyra" and let the bot plan it</span>
    <span>✦ real photos, real sources, zero stock images</span>
    <span>✦ no cap, this is the most underrated trip in india</span>
    <span>✦ living root bridges &gt; any bridge you've seen</span>
    <span>✦ tap "ask nevyra" and let the bot plan it</span>
    <span>✦ real photos, real sources, zero stock images</span>
  </div>
</div>

<nav class="step-index">
  <div class="wrap">
    <a href="#ask"><b>00</b> Ask Nevyra</a>
    <a href="#when"><b>01</b> When to go</a>
    <a href="#plan"><b>02</b> Plan your days</a>
    <a href="#states"><b>03</b> Explore the eight</a>
    <a href="#stay"><b>04</b> Where to stay</a>
    <a href="#costs"><b>05</b> What things cost</a>
    <a href="#culture"><b>06</b> Culture &amp; feasts</a>
    <a href="#guides"><b>07</b> Local guides</a>
  </div>
</nav>

<!-- ============ 00 ASK NEVYRA — CHAT WIZARD ============ -->
<section class="section" id="ask">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="sticker pink">new · talk to the site</span>
      <h2 style="margin-top:14px;">Don't feel like scrolling? Just tell Nevyra.</h2>
      <p>Answer a few quick taps and it'll build your trip for you — no forms, just vibes. Prefer to browse yourself? Everything below still works.</p>
    </div>

    <div class="chat-shell reveal">
      <div class="chat-topbar">
        <span class="dot"></span><span class="dot"></span><span class="dot"></span>
        <span class="who">NEVYRA bot</span>
        <span class="status"><i></i>online, always down to plan a trip</span>
      </div>
      <div class="chat-body" id="chatBody"></div>
      <div class="chat-choices" id="chatChoices"></div>
      <div class="chat-restart"><button id="chatRestart" type="button">start over</button></div>
    </div>
  </div>
</section>

<!-- ============ 01 SEASON / FLOOD ============ -->
<section class="section" id="when">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 01</span>
      <h2>First, know the sky</h2>
      <p>The Northeast runs on the monsoon's schedule, not the calendar's. Tap a month to see what travelling there actually looks like — and where the Brahmaputra has the final word.</p>
    </div>

    <div class="season-panel reveal">
      <div class="legend">
        <span><i class="b"></i> Best window — clear skies, open parks, festivals</span>
        <span><i class="g"></i> Economical — thinner crowds, softer prices, some rain</span>
        <span><i class="f"></i> Flood &amp; landslide risk — plains and hill roads affected</span>
      </div>
      <div class="month-strip" id="monthStrip"></div>
      <div class="season-detail" id="seasonDetail">
        <div class="box"><span class="stat-label">Status</span><div class="stat-value" id="statStatus">—</div></div>
        <div class="box"><span class="stat-label">What to expect</span><div class="stat-value" id="statExpect" style="font-size:15px; font-family:Manrope; font-weight:500; color:var(--ink-soft);">Select a month above</div></div>
        <div class="box"><span class="stat-label">Good for</span><div class="stat-value" id="statGood" style="font-size:15px; font-family:Manrope; font-weight:500; color:var(--ink-soft);">—</div></div>
      </div>
    </div>

    <div class="flood-alert reveal">
      <div class="icon">!</div>
      <div>
        <h4>Flood advisory — June through September</h4>
        <p>The Brahmaputra and its tributaries flood the Assam plains most monsoons, and Kaziranga National Park closes to visitors (roughly mid-May to late October) as its grasslands go under water. Hill roads in Meghalaya, Sikkim, Arunachal Pradesh and Mizoram see landslides during heavy spells. It's the cheapest and greenest time to travel — just build in flexible dates, avoid low-lying river routes, and check district administration and IMD bulletins before you commit to a itinerary in this window.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ 02 ITINERARY BUILDER ============ -->
<section class="section" id="plan" style="background:var(--sage);">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 02</span>
      <h2>Then, shape the days</h2>
      <p>Tell NEVYRA how long you have and how you like to spend, and it will lay out a day-by-day route across the region's real geography — not a generic checklist.</p>
    </div>

    <div class="builder reveal">
      <div class="builder-form">
        <div class="field">
          <label for="daysRange">Length of trip</label>
          <div class="days-row">
            <input type="range" id="daysRange" min="3" max="16" value="7">
            <span class="days-value"><span id="daysValue">7</span>d</span>
          </div>
        </div>
        <div class="field">
          <label for="budgetSelect">Daily budget style</label>
          <select id="budgetSelect">
            <option value="budget">Backpacker — homestays &amp; local food</option>
            <option value="mid" selected>Mid-range — comfort without excess</option>
            <option value="luxury">Luxury — resorts &amp; private transport</option>
          </select>
        </div>
        <div class="field">
          <label for="circuitSelect">Circuit</label>
          <select id="circuitSelect">
            <option value="classic">Classic — Assam &amp; Meghalaya</option>
            <option value="sikkim">Himalayan — Sikkim</option>
            <option value="tribal">Tribal Trail — Nagaland &amp; Manipur</option>
            <option value="grand">Grand Northeast — a bit of everything</option>
          </select>
        </div>
        <button class="btn-primary" id="generateBtn">Build my itinerary</button>
      </div>

      <div class="itinerary-output" id="itineraryOutput"></div>
    </div>
  </div>
</section>

<!-- ============ 03 STATES ============ -->
<section class="section" id="states">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 03</span>
      <h2>Explore the eight</h2>
      <p>Seven sisters, and Sikkim standing beside them. Open a state to see the places that define it.</p>
    </div>
    <div class="state-grid" id="stateGrid"></div>
  </div>
</section>

<!-- ============ 04 HOTELS ============ -->
<section class="section" id="stay" style="background:var(--sage);">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 04</span>
      <h2>Where to stay</h2>
      <p>From family homestays to Himalayan resorts. Pick a state and a tier — categories and price bands are indicative; always confirm current rates before booking.</p>
    </div>

    <div class="hotel-controls reveal">
      <select id="hotelState"></select>
      <div class="tier-toggle" id="tierToggle">
        <button class="btn-ghost active" data-tier="budget">Affordable</button>
        <button class="btn-ghost" data-tier="mid">Mid-range</button>
        <button class="btn-ghost" data-tier="luxury">Luxury</button>
      </div>
    </div>

    <div class="hotel-grid reveal" id="hotelGrid"></div>
  </div>
</section>

<!-- ============ 05 PRICES ============ -->
<section class="section" id="costs">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 05</span>
      <h2>What things cost</h2>
      <p>A rough feel for everyday spending — street food, transport, permits and the crafts worth carrying home. Ranges are typical and will move with season and bargaining.</p>
    </div>
    <div class="price-groups reveal" id="priceGroups"></div>
  </div>
</section>

<!-- ============ 06 CULTURE ============ -->
<section class="section" id="culture" style="background:var(--sage);">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 06</span>
      <h2>Culture &amp; feasts</h2>
      <p>The region's calendar of festivals, its kitchens, and the weaves worth learning to recognise.</p>
    </div>
    <div class="culture-grid reveal" id="cultureGrid"></div>
  </div>
</section>

<!-- ============ 07 LOCAL GUIDES ============ -->
<section class="section" id="guides">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="eyebrow">Step 07</span>
      <h2>Hire a local guide</h2>
      <p>A good local guide is the difference between passing through and actually understanding a place — and in Arunachal, Nagaland and Mizoram, a licensed guide or agent is how your Inner Line/Protected Area Permit gets arranged at all. Rates below are typical per-day ranges for Indian and foreign travellers; book or verify through each state's official tourism department.</p>
    </div>
    <div class="guide-grid reveal" id="guideGrid"></div>
    <div class="guide-note reveal">
      <b>For visitors from outside India:</b> foreign nationals need a Protected Area Permit (PAP) for Arunachal Pradesh, and restricted-area formalities can apply in parts of Nagaland, Manipur, Mizoram and Sikkim near the international border — a registered local agent typically arranges this alongside the guide booking. <b>For Indian nationals:</b> an Inner Line Permit (ILP), obtainable online or on arrival, is required for Arunachal Pradesh, Nagaland and Mizoram; no permit is needed for Assam, Meghalaya, Manipur (interior), Tripura or Sikkim's main circuit. Two pan-India resources worth bookmarking: the Ministry of Tourism's guide directory at <a href="https://www.incredibleindia.gov.in" target="_blank" rel="noopener">incredibleindia.gov.in</a>, and the <a href="https://www.iato.in" target="_blank" rel="noopener">Indian Association of Tour Operators (iato.in)</a>, which lists accredited member agencies across every state on this page.
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div class="footer-top">
      <div>
        <div class="footer-brand">NEVYRA</div>
        <p class="footer-quote">"Go slow through the hills — they were never in a hurry, and they won't wait for the ones who are."</p>
      </div>
      <div class="footer-cols">
        <div class="footer-col">
          <h5>Guide</h5>
          <a href="#when">When to go</a>
          <a href="#plan">Plan your days</a>
          <a href="#states">The eight states</a>
        </div>
        <div class="footer-col">
          <h5>Practical</h5>
          <a href="#stay">Where to stay</a>
          <a href="#costs">What things cost</a>
          <a href="#culture">Culture &amp; feasts</a>
          <a href="#guides">Local guides</a>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 NEVYRA — a slow travel guide to Northeast India &amp; Sikkim</span>
      <span>Crafted by Team Diwan-E-Khas</span>
    </div>
  </div>
</footer>

<script>
/* ============================================================
   DATA
   ============================================================ */
const MONTHS = [
  {m:"Jan", status:"best", expect:"Cold, clear, dry across the plains", good:"Kaziranga, Majuli, Tawang snow"},
  {m:"Feb", status:"best", expect:"Crisp mornings, blooming rhododendrons begin", good:"Sikkim treks, Nagaland villages"},
  {m:"Mar", status:"good", expect:"Warming up, rhododendrons peak in the hills", good:"Ziro, Sikkim, Cherrapunji"},
  {m:"Apr", status:"best", expect:"Bihu season — vivid, warm, festive", good:"Assam culture, Majuli"},
  {m:"May", status:"good", expect:"Pre-monsoon showers begin, humid in the plains", good:"Meghalaya waterfalls filling up"},
  {m:"Jun", status:"flood", expect:"Monsoon breaks — heavy rain in Assam & Meghalaya", good:"Cherrapunji rainfall spectacle, budget travel"},
  {m:"Jul", status:"flood", expect:"Peak monsoon, Brahmaputra swells", good:"Lush landscapes if you can stay flexible"},
  {m:"Aug", status:"flood", expect:"Continued flood risk on the plains", good:"Off-season rates, quiet hill towns"},
  {m:"Sep", status:"flood", expect:"Rain tapering, rivers still high", good:"Late-monsoon greenery"},
  {m:"Oct", status:"best", expect:"Skies clear, Kaziranga reopens", good:"Wildlife safaris, Durga Puja in Assam"},
  {m:"Nov", status:"best", expect:"Cool, dry, Hornbill Festival season", good:"Nagaland, Manipur, Meghalaya"},
  {m:"Dec", status:"best", expect:"Cold and clear, Christmas markets in the hills", good:"Shillong, Sikkim, Mizoram, Manipur"}
];

const STATES = [
  {id:"assam", name:"Assam", tag:"Rivers, tea and one-horned rhinos", icon:"leaf", accent:"var(--c-assam)",
    best:"Nov – Apr", knownFor:"Tea gardens, the Brahmaputra, wildlife",
    places:[
      {n:"Kaziranga National Park", e:"🦏", g:"linear-gradient(135deg,#2F8F5B,#6FB37E)", d:"Grasslands along the Brahmaputra, home to the greatest concentration of one-horned rhinos left on earth."},
      {n:"Majuli Island", e:"🛶", g:"linear-gradient(135deg,#2E8FA6,#7FC1CE)", d:"The world's largest river island, its Neo-Vaishnavite monasteries (satras) unchanged for centuries."},
      {n:"Kamakhya Temple, Guwahati", e:"🛕", g:"linear-gradient(135deg,#D9752E,#F2B705)", d:"A Shakti Peetha perched on Nilachal Hill, one of the oldest and most significant temples in the east."},
      {n:"Jorhat Tea Estates", e:"🍃", g:"linear-gradient(135deg,#3E8F5E,#9BC98A)", d:"Colonial-era gardens where you can walk the rows and taste orthodox Assam tea at source."},
      {n:"Sivasagar", e:"🏯", g:"linear-gradient(135deg,#B85A3E,#E29A6E)", d:"Ahom-dynasty tanks, temples and palaces from six centuries of a kingdom the Mughals never conquered."},
      {n:"Sualkuchi", e:"🧵", g:"linear-gradient(135deg,#C2447A,#E88FB0)", d:"The 'Manchester of Assam' — a village of looms weaving muga and eri silk by hand."}
    ]},
  {id:"meghalaya", name:"Meghalaya", tag:"Abode of clouds", icon:"bridge", accent:"var(--c-meghalaya)",
    best:"Oct – May", knownFor:"Living root bridges, waterfalls, the wettest place on earth",
    places:[
      {n:"Living Root Bridges, Nongriat", e:"🌉", g:"linear-gradient(135deg,#2E8FA6,#5FC7B8)", d:"Rubber-tree roots trained across streams by the Khasi over generations — living infrastructure, still growing."},
      {n:"Cherrapunji (Sohra)", e:"🌧️", g:"linear-gradient(135deg,#3E6FB0,#7FA9D6)", d:"Among the wettest places on the planet, ringed by waterfalls that roar in the monsoon."},
      {n:"Dawki & the Umngot River", e:"🚣", g:"linear-gradient(135deg,#2FB2A6,#8FE0D4)", d:"Water so clear that boats appear to float in mid-air above the riverbed."},
      {n:"Mawlynnong", e:"🌿", g:"linear-gradient(135deg,#2F8F5B,#8FCB9E)", d:"Asia's cleanest village, a bamboo-fenced settlement with a living-root skywalk."},
      {n:"Shillong", e:"🎸", g:"linear-gradient(135deg,#7B5EA7,#B79BDB)", d:"The 'Scotland of the East' — pine hills, lakes, and a lively music scene."},
      {n:"Mawsmai Caves", e:"🕳️", g:"linear-gradient(135deg,#4B5D54,#8CA79A)", d:"Limestone caverns you can walk straight through, lit and cool year-round."}
    ]},
  {id:"arunachal", name:"Arunachal Pradesh", tag:"Land of the dawn-lit mountains", icon:"mountain", accent:"var(--c-arunachal)",
    best:"Oct – Apr (permit required)", knownFor:"High passes, monasteries, tribal diversity",
    places:[
      {n:"Tawang Monastery", e:"🛕", g:"linear-gradient(135deg,#7B5EA7,#B79BDB)", d:"The largest monastery in India, and the birthplace of the 6th Dalai Lama's legend — high, cold, and serene."},
      {n:"Sela Pass", e:"🚩", g:"linear-gradient(135deg,#3E6FB0,#A7C4E8)", d:"A 13,700-ft crossing draped in prayer flags, gateway to the Tawang valley."},
      {n:"Ziro Valley", e:"🌾", g:"linear-gradient(135deg,#D9752E,#F2C56B)", d:"Home of the Apatani, terraced rice-fish fields and the Ziro Music Festival."},
      {n:"Dirang", e:"🍎", g:"linear-gradient(135deg,#C2447A,#E88FB0)", d:"Apple orchards and hot springs tucked in a quiet valley on the way to Tawang."},
      {n:"Bomdila", e:"⛩️", g:"linear-gradient(135deg,#6B5FA8,#9E8FD1)", d:"Monastery town with sweeping views of the Kameng valley."}
    ]},
  {id:"nagaland", name:"Nagaland", tag:"Land of festivals", icon:"bird", accent:"var(--c-nagaland)",
    best:"Oct – Mar", knownFor:"Konyak villages, Hornbill Festival, green valleys",
    places:[
      {n:"Kohima War Cemetery", e:"🕊️", g:"linear-gradient(135deg,#4B5D54,#8CA79A)", d:"A quiet, immaculately kept memorial to the WWII battle that turned the tide in the East."},
      {n:"Dzükou Valley", e:"🌸", g:"linear-gradient(135deg,#D6537D,#F0A6C0)", d:"A high alpine valley carpeted with wildflowers each monsoon — a multi-day trek reward."},
      {n:"Kisama Heritage Village", e:"🥁", g:"linear-gradient(135deg,#D9752E,#F2B705)", d:"Hosts the Hornbill Festival every December, gathering all of Nagaland's tribes under one roof."},
      {n:"Mon District", e:"🪶", g:"linear-gradient(135deg,#B85A3E,#E29A6E)", d:"Konyak villages once known for headhunting, now known for their morungs and tattooed elders."},
      {n:"Khonoma", e:"🌾", g:"linear-gradient(135deg,#2F8F5B,#8FCB9E)", d:"A pioneering green village built around terrace farming and conservation."}
    ]},
  {id:"manipur", name:"Manipur", tag:"Jewel of India", icon:"lake", accent:"var(--c-manipur)",
    best:"Oct – Mar", knownFor:"Floating islands, classical dance, women's markets",
    places:[
      {n:"Loktak Lake", e:"🌊", g:"linear-gradient(135deg,#2E8FA6,#7FC1CE)", d:"The largest freshwater lake in the Northeast, dotted with phumdis — floating islands of vegetation."},
      {n:"Keibul Lamjao National Park", e:"🦌", g:"linear-gradient(135deg,#2F8F5B,#8FCB9E)", d:"The world's only floating national park, last refuge of the endangered sangai deer."},
      {n:"Ima Keithel, Imphal", e:"🧺", g:"linear-gradient(135deg,#C2447A,#E88FB0)", d:"A market run entirely by women for centuries — thousands of stalls, one long tradition."},
      {n:"Kangla Fort", e:"🏰", g:"linear-gradient(135deg,#B85A3E,#E29A6E)", d:"Seat of Manipur's ancient kings, on the banks of the Imphal River."},
      {n:"Andro & Sendra villages", e:"🏺", g:"linear-gradient(135deg,#D9752E,#F2C56B)", d:"Pottery traditions and views over Loktak from a lakeside hill."}
    ]},
  {id:"mizoram", name:"Mizoram", tag:"Land of the highlanders", icon:"waterfall", accent:"var(--c-mizoram)",
    best:"Nov – Mar", knownFor:"Bamboo hills, waterfalls, warm hospitality",
    places:[
      {n:"Aizawl", e:"🏙️", g:"linear-gradient(135deg,#2FB286,#8FE0C4)", d:"A city built on a ridge, its streets climbing and dropping between bamboo-covered hills."},
      {n:"Reiek", e:"🏕️", g:"linear-gradient(135deg,#2F8F5B,#8FCB9E)", d:"A peak with sweeping views and a recreated traditional Mizo village."},
      {n:"Vantawng Falls", e:"💦", g:"linear-gradient(135deg,#2E8FA6,#7FC1CE)", d:"The state's tallest waterfall, dropping through dense forest."},
      {n:"Champhai", e:"🌾", g:"linear-gradient(135deg,#D9752E,#F2C56B)", d:"Border town ringed by terraced paddy fields, often called the 'rice bowl of Mizoram'."}
    ]},
  {id:"tripura", name:"Tripura", tag:"Palaces in the hills", icon:"palace", accent:"var(--c-tripura)",
    best:"Oct – Mar", knownFor:"Royal palaces, rock-cut carvings, lakeside retreats",
    places:[
      {n:"Ujjayanta Palace", e:"🏛️", g:"linear-gradient(135deg,#B85A3E,#E29A6E)", d:"The former royal residence, now a museum, with Mughal-style gardens in the heart of Agartala."},
      {n:"Neermahal", e:"🛶", g:"linear-gradient(135deg,#2E8FA6,#7FC1CE)", d:"A lake palace built in the middle of Rudrasagar Lake, reachable only by boat."},
      {n:"Unakoti", e:"🗿", g:"linear-gradient(135deg,#4B5D54,#8CA79A)", d:"Giant rock-cut carvings of Shiva and other deities, dated to roughly the 7th–9th century, half-swallowed by jungle."},
      {n:"Jampui Hills", e:"🍊", g:"linear-gradient(135deg,#D9752E,#F2B705)", d:"Orange orchards and Mizo-Chin villages along Tripura's highest ridge."}
    ]},
  {id:"sikkim", name:"Sikkim", tag:"Where the mountains meet the sky", icon:"snow", accent:"var(--c-sikkim)",
    best:"Mar – Jun & Oct – Dec", knownFor:"Kanchenjunga views, monasteries, alpine lakes",
    places:[
      {n:"Gangtok", e:"🏔️", g:"linear-gradient(135deg,#3E6FB0,#8FB2E0)", d:"Sikkim's capital, strung along a ridge with monastery bells and momo stalls in equal measure."},
      {n:"Tsomgo (Changu) Lake", e:"🏞️", g:"linear-gradient(135deg,#2E8FA6,#7FC1CE)", d:"A glacial lake at 12,400 ft, often edged with snow well into spring."},
      {n:"Nathu La Pass", e:"🚩", g:"linear-gradient(135deg,#7B5EA7,#B79BDB)", d:"A high Himalayan trade route to Tibet, one of the few open border crossings in the region."},
      {n:"Yumthang Valley", e:"🌷", g:"linear-gradient(135deg,#D6537D,#F0A6C0)", d:"The 'Valley of Flowers' — rhododendrons in bloom against snow peaks each spring."},
      {n:"Pelling", e:"⛰️", g:"linear-gradient(135deg,#3E6FB0,#8FB2E0)", d:"Unbroken views of Kanchenjunga, the world's third-highest peak, from your breakfast table."},
      {n:"Rumtek Monastery", e:"🛕", g:"linear-gradient(135deg,#D9752E,#F2B705)", d:"Seat-in-exile of the Karmapa, one of Tibetan Buddhism's grandest monasteries outside Tibet."}
    ]}
];

/* ---- real photos, one per state, sourced from Wikimedia Commons ---- */
const STATE_PHOTOS = {
  assam:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/3/3b/One-Horned_Rhino_at_the_Kaziranga_National_Park,_Assam.jpg/640px-One-Horned_Rhino_at_the_Kaziranga_National_Park,_Assam.jpg",
    place:"Indian rhinoceros, Kaziranga National Park", license:"CC BY-SA 4.0",
    src:"https://commons.wikimedia.org/wiki/File:One-Horned_Rhino_at_the_Kaziranga_National_Park,_Assam.jpg" },
  meghalaya:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/6/65/Hanging_root_bridge_shillong.jpg/640px-Hanging_root_bridge_shillong.jpg",
    place:"A living root bridge near Shillong", license:"CC BY-SA 4.0",
    src:"https://commons.wikimedia.org/wiki/File:Hanging_root_bridge_shillong.jpg" },
  arunachal:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Tawang_Monastery_(Tibetan_Buddhist).jpg/640px-Tawang_Monastery_(Tibetan_Buddhist).jpg",
    place:"Tawang Monastery", license:"CC BY-SA 4.0",
    src:"https://commons.wikimedia.org/wiki/File:Tawang_Monastery_(Tibetan_Buddhist).jpg" },
  nagaland:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/Inu_Etc_in_Dzukou_Valley,_Nagaland.jpg/640px-Inu_Etc_in_Dzukou_Valley,_Nagaland.jpg",
    place:"Dzükou Valley", license:"CC BY 4.0",
    src:"https://commons.wikimedia.org/wiki/File:Inu_Etc_in_Dzukou_Valley,_Nagaland.jpg" },
  manipur:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/7/70/Loktak_Lake_View.jpg/640px-Loktak_Lake_View.jpg",
    place:"Loktak Lake", license:"CC BY-SA 4.0",
    src:"https://commons.wikimedia.org/wiki/File:Loktak_Lake_View.jpg" },
  mizoram:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/View_of_the_ridgetop_city_of_Aizawl,_state_capital_of_Mizoram.jpg/640px-View_of_the_ridgetop_city_of_Aizawl,_state_capital_of_Mizoram.jpg",
    place:"Aizawl, ridgetop capital of Mizoram", license:"CC BY-SA 3.0",
    src:"https://commons.wikimedia.org/wiki/File:View_of_the_ridgetop_city_of_Aizawl,_state_capital_of_Mizoram.jpg" },
  tripura:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Ujjayanta_Palace_Agartala_Tripura_Front.jpg/640px-Ujjayanta_Palace_Agartala_Tripura_Front.jpg",
    place:"Ujjayanta Palace, Agartala", license:"Wikimedia Commons",
    src:"https://commons.wikimedia.org/wiki/File:Ujjayanta_Palace_Agartala_Tripura_Front.jpg" },
  sikkim:{ url:"https://upload.wikimedia.org/wikipedia/commons/thumb/b/b3/Sunrise_over_Kangchenjunga.jpg/640px-Sunrise_over_Kangchenjunga.jpg",
    place:"Kangchenjunga at sunrise, seen from Pelling", license:"CC BY-SA 4.0",
    src:"https://commons.wikimedia.org/wiki/File:Sunrise_over_Kangchenjunga.jpg" }
};

/* ---- pan-Northeast local guide directory ---- */
const GUIDES = [
  {state:"Assam", accent:"var(--c-assam)", spec:"Wildlife safaris, river culture & tea-estate walks",
   indian:"₹1,500 – ₹3,000 /day", foreign:"₹3,000 – ₹6,000 /day",
   note:"Kaziranga jeep-safari guides are booked at the park gate; river & Majuli guides through registered operators.",
   url:"https://assamtourism.gov.in", label:"assamtourism.gov.in"},
  {state:"Meghalaya", accent:"var(--c-meghalaya)", spec:"Root-bridge treks, caving & waterfall trails",
   indian:"₹1,200 – ₹2,500 /day", foreign:"₹2,500 – ₹5,000 /day",
   note:"Nongriat & Mawlynnong village guide associations set fixed local rates — hire on arrival or in advance.",
   url:"https://meghalayatourism.in", label:"meghalayatourism.in"},
  {state:"Arunachal Pradesh", accent:"var(--c-arunachal)", spec:"High-altitude passes & monastery circuits — arranges permits",
   indian:"₹2,000 – ₹4,000 /day", foreign:"₹4,500 – ₹9,000 /day",
   note:"A registered agent is required to secure the Protected Area Permit (foreigners) or ILP (Indians) — guide fee usually bundled in.",
   url:"https://arunachaltourism.com", label:"arunachaltourism.com"},
  {state:"Nagaland", accent:"var(--c-nagaland)", spec:"Konyak & tribal-village visits, Hornbill Festival",
   indian:"₹1,800 – ₹3,500 /day", foreign:"₹3,500 – ₹7,000 /day",
   note:"Village-entry etiquette varies by tribe — a local guide is strongly advised for Mon district homestays.",
   url:"https://tourism.nagaland.gov.in", label:"tourism.nagaland.gov.in"},
  {state:"Manipur", accent:"var(--c-manipur)", spec:"Loktak Lake boating & Imphal heritage walks",
   indian:"₹1,200 – ₹2,500 /day", foreign:"₹2,500 – ₹5,000 /day",
   note:"Boatman-guides for Loktak's floating islands are hired directly at Sendra/Karang jetty.",
   url:"https://manipurtourism.gov.in", label:"manipurtourism.gov.in"},
  {state:"Mizoram", accent:"var(--c-mizoram)", spec:"Bamboo-hill treks & waterfall hikes",
   indian:"₹1,500 – ₹3,000 /day", foreign:"₹3,000 – ₹6,000 /day",
   note:"An Inner Line Permit is needed by Indian and foreign visitors alike — most guides help process it.",
   url:"https://mizotourism.mizoram.gov.in", label:"mizotourism.mizoram.gov.in"},
  {state:"Tripura", accent:"var(--c-tripura)", spec:"Palace history & Unakoti rock-carving tours",
   indian:"₹1,000 – ₹2,200 /day", foreign:"₹2,200 – ₹4,500 /day",
   note:"Government-approved guides can be booked directly through the state tourism corporation counter in Agartala.",
   url:"https://tripuratourism.gov.in", label:"tripuratourism.gov.in"},
  {state:"Sikkim", accent:"var(--c-sikkim)", spec:"Himalayan treks, monastery & high-pass routes",
   indian:"₹2,000 – ₹4,000 /day", foreign:"₹4,000 – ₹8,000 /day",
   note:"Nathu La & Tsomgo Lake require a registered Sikkim guide/agency to obtain the restricted-area permit.",
   url:"https://sikkimtourism.gov.in", label:"sikkimtourism.gov.in"}
];

const ICONS = {
  leaf:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8 32C8 16 24 8 34 8C34 20 26 32 8 32Z" stroke="currentColor" stroke-width="2"/><path d="M9 31C16 24 22 18 33 9" stroke="currentColor" stroke-width="2"/></svg>',
  bridge:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M4 28C4 16 12 10 20 10C28 10 36 16 36 28" stroke="currentColor" stroke-width="2"/><path d="M4 28H36" stroke="currentColor" stroke-width="2"/><path d="M12 28V21M20 28V17M28 28V21" stroke="currentColor" stroke-width="2"/></svg>',
  mountain:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M3 32L15 12L22 22L27 15L37 32H3Z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/><path d="M12 24L15 20L18 24" stroke="currentColor" stroke-width="2"/></svg>',
  bird:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M5 24C11 16 17 16 20 22C23 16 29 16 35 24" stroke="currentColor" stroke-width="2"/><circle cx="20" cy="14" r="3" stroke="currentColor" stroke-width="2"/></svg>',
  lake:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><ellipse cx="20" cy="26" rx="16" ry="6" stroke="currentColor" stroke-width="2"/><path d="M10 26C10 18 16 12 20 12C24 12 30 18 30 26" stroke="currentColor" stroke-width="2"/></svg>',
  waterfall:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M10 6H30V16C30 16 26 20 26 26C26 30 30 32 30 32" stroke="currentColor" stroke-width="2"/><path d="M14 16V32M20 16V32" stroke="currentColor" stroke-width="2" stroke-dasharray="1 4"/></svg>',
  palace:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6 32V18L20 8L34 18V32" stroke="currentColor" stroke-width="2"/><path d="M6 32H34M14 32V22H26V32" stroke="currentColor" stroke-width="2"/><circle cx="20" cy="6" r="1.6" fill="currentColor"/></svg>',
  snow:'<svg viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M20 4L26 30L6 14H34L14 30L20 4Z" stroke="currentColor" stroke-width="1.6" stroke-linejoin="round"/></svg>'
};

const CIRCUITS = {
  classic:[
    {state:"Assam", place:"Guwahati", act:"Arrive; sunset boat ride on the Brahmaputra, Kamakhya Temple at dawn."},
    {state:"Assam", place:"Kaziranga", act:"Jeep and elephant-back safari through the rhino grasslands."},
    {state:"Assam", place:"Kaziranga", act:"Second safari zone at first light; afternoon transfer toward Shillong."},
    {state:"Meghalaya", place:"Shillong", act:"Ward's Lake, Laitlum canyon viewpoint, local music café in the evening."},
    {state:"Meghalaya", place:"Cherrapunji", act:"Nohkalikai and Seven Sisters falls, Mawsmai limestone caves."},
    {state:"Meghalaya", place:"Nongriat", act:"Trek down to the double-decker living root bridge; swim in the pools below."},
    {state:"Meghalaya", place:"Dawki", act:"Glass-clear Umngot river by boat, Mawlynnong's cleanest village en route back."},
    {state:"Assam", place:"Majuli", act:"Ferry to the river island; visit a Vaishnavite satra and watch mask-making."},
    {state:"Assam", place:"Jorhat", act:"Walk a working tea estate, orthodox tea tasting."},
    {state:"Assam", place:"Sivasagar", act:"Ahom-era tanks and temples before the final transfer to Guwahati."}
  ],
  sikkim:[
    {state:"Sikkim", place:"Gangtok", act:"Arrive; MG Marg evening stroll and momo dinner."},
    {state:"Sikkim", place:"Gangtok", act:"Rumtek Monastery and Banjhakri Falls."},
    {state:"Sikkim", place:"Tsomgo Lake", act:"Drive up to the glacial lake and Baba Mandir, altitude permitting Nathu La."},
    {state:"Sikkim", place:"Pelling", act:"Transfer west; sunset over Kanchenjunga from Pelling's ridge."},
    {state:"Sikkim", place:"Pelling", act:"Khecheopalri Lake, Pemayangtse Monastery, Rabdentse ruins."},
    {state:"Sikkim", place:"Yuksom", act:"Start of the old trekking trail; quiet monastery town for the night."},
    {state:"Sikkim", place:"Lachung", act:"Drive north through pine forest to the high valley town."},
    {state:"Sikkim", place:"Yumthang Valley", act:"Rhododendron valley and Zero Point snowline, weather permitting."},
    {state:"Sikkim", place:"Gangtok", act:"Return south; Tashi View Point and handicraft centre."}
  ],
  tribal:[
    {state:"Nagaland", place:"Kohima", act:"War Cemetery, state museum, arrival evening."},
    {state:"Nagaland", place:"Khonoma", act:"Green village walk, terrace farms, community conservation area."},
    {state:"Nagaland", place:"Kisama", act:"Heritage village — Hornbill Festival grounds and tribal morungs."},
    {state:"Nagaland", place:"Dzükou Valley", act:"Day trek into the valley, wildflowers if in season."},
    {state:"Nagaland", place:"Mon", act:"Long transfer north to Konyak country; village homestay."},
    {state:"Nagaland", place:"Longwa", act:"A village that straddles the India–Myanmar border; meet the Angh's family."},
    {state:"Manipur", place:"Imphal", act:"Transfer south; Kangla Fort and the Ima Keithel women's market."},
    {state:"Manipur", place:"Loktak Lake", act:"Boat among the floating phumdis; Keibul Lamjao park at dawn."},
    {state:"Manipur", place:"Moirang", act:"INA memorial and lakeside villages before departure."}
  ],
  grand:[
    {state:"Assam", place:"Guwahati", act:"Arrive; Kamakhya Temple and river cruise."},
    {state:"Assam", place:"Kaziranga", act:"Rhino safari across the grasslands."},
    {state:"Meghalaya", place:"Shillong", act:"Waterfalls and viewpoints en route from Assam."},
    {state:"Meghalaya", place:"Cherrapunji", act:"Living root bridges and the wettest hills in the world."},
    {state:"Meghalaya", place:"Dawki", act:"Glass-water river, Mawlynnong village."},
    {state:"Nagaland", place:"Kohima", act:"War Cemetery, transfer into the hills."},
    {state:"Nagaland", place:"Kisama", act:"Tribal heritage village and morungs."},
    {state:"Sikkim", place:"Gangtok", act:"Fly/transfer to the Himalaya; monastery town evening."},
    {state:"Sikkim", place:"Tsomgo Lake", act:"High-altitude glacial lake day trip."},
    {state:"Sikkim", place:"Pelling", act:"Kanchenjunga views and Pemayangtse Monastery."},
    {state:"Sikkim", place:"Yumthang Valley", act:"Rhododendron valley finale before departure."}
  ]
};

const BUDGET_META = {
  budget:{label:"Backpacker", perDay:1900, factor:0.62, note:"dorms, homestays, shared sumo taxis, street food"},
  mid:{label:"Mid-range", perDay:3600, factor:1, note:"boutique stays, private cabs between towns, sit-down meals"},
  luxury:{label:"Luxury", perDay:8200, factor:1.9, note:"resorts & heritage stays, private vehicle throughout, guided experiences"}
};

const HOTELS = {
  assam:{
    budget:[
      {n:"Riverside Homestay", loc:"Near Kaziranga, Assam", d:"Family-run rooms on stilts, home-cooked Assamese thali, bicycle hire.", range:"₹900 – ₹1,600 / night"},
      {n:"Backpacker's Nest", loc:"Guwahati", d:"Dorms and simple doubles a short walk from the Brahmaputra ghats.", range:"₹500 – ₹1,200 / night"}
    ],
    mid:[
      {n:"Tea Garden Bungalow", loc:"Jorhat, Assam", d:"Converted planter's bungalow set inside a working tea estate.", range:"₹3,200 – ₹5,500 / night"},
      {n:"Wild Grass Lodge", loc:"Kaziranga fringe", d:"Garden cottages with safari desks and an in-house naturalist.", range:"₹3,500 – ₹6,000 / night"}
    ],
    luxury:[
      {n:"Brahmaputra Riverfront Resort", loc:"Guwahati", d:"River-view suites, spa, and sunset cruise included.", range:"₹9,000 – ₹16,000 / night"},
      {n:"Kaziranga Wilderness Camp", loc:"Kaziranga", d:"Luxury tented suites, private safaris, multi-course dining.", range:"₹12,000 – ₹22,000 / night"}
    ]
  },
  meghalaya:{
    budget:[
      {n:"Root Bridge Homestay", loc:"Nongriat village", d:"Basic rooms steps from the double-decker bridge; candlelit dinners.", range:"₹700 – ₹1,400 / night"},
      {n:"Ward's Lake Guesthouse", loc:"Shillong", d:"Simple central rooms, walking distance to Police Bazar.", range:"₹900 – ₹1,800 / night"}
    ],
    mid:[
      {n:"Cloud Ridge Cottages", loc:"Cherrapunji (Sohra)", d:"Glass-walled rooms facing the valley and waterfalls.", range:"₹3,000 – ₹5,200 / night"},
      {n:"Pinewood Boutique Stay", loc:"Shillong", d:"Colonial-style rooms with fireplace and mountain views.", range:"₹3,400 – ₹5,800 / night"}
    ],
    luxury:[
      {n:"Ri Kynjai Lakeside Resort", loc:"Umiam Lake, near Shillong", d:"Khasi-inspired cottages over the lake, full-service spa.", range:"₹10,000 – ₹18,000 / night"}
    ]
  },
  arunachal:{
    budget:[
      {n:"Monastery Guest Rooms", loc:"Tawang", d:"Basic heated rooms run by a local family near the monastery.", range:"₹800 – ₹1,600 / night"}
    ],
    mid:[
      {n:"Dirang Valley Resort", loc:"Dirang", d:"Wood cottages by the river, hot spring access nearby.", range:"₹3,200 – ₹5,600 / night"},
      {n:"Ziro Apatani Homestay", loc:"Ziro Valley", d:"Stay inside an Apatani family compound amid rice-fish fields.", range:"₹2,200 – ₹4,000 / night"}
    ],
    luxury:[
      {n:"Sela Heights Lodge", loc:"Near Sela Pass", d:"High-altitude lodge with heated suites and mountain-facing decks.", range:"₹9,500 – ₹15,000 / night"}
    ]
  },
  nagaland:{
    budget:[
      {n:"Konyak Village Homestay", loc:"Longwa / Mon", d:"Stay with a local family in a traditional morung-style home.", range:"₹700 – ₹1,300 / night"}
    ],
    mid:[
      {n:"Heritage Kohima Inn", loc:"Kohima", d:"Comfortable rooms near the War Cemetery with valley views.", range:"₹2,800 – ₹4,800 / night"}
    ],
    luxury:[
      {n:"Hornbill Festival Camp", loc:"Kisama (Dec only)", d:"Premium tented camp during festival season, close to the grounds.", range:"₹8,000 – ₹14,000 / night"}
    ]
  },
  manipur:{
    budget:[
      {n:"Loktak Floating Homestay", loc:"Loktak Lake", d:"Simple stilt rooms on the lake edge among the phumdis.", range:"₹800 – ₹1,500 / night"}
    ],
    mid:[
      {n:"Imphal Garden Hotel", loc:"Imphal", d:"Central, comfortable rooms near Kangla Fort and Ima Keithel.", range:"₹2,600 – ₹4,500 / night"}
    ],
    luxury:[
      {n:"Sangai Lakeview Resort", loc:"Moirang, Loktak Lake", d:"Premium lake-facing rooms with private boat access.", range:"₹7,500 – ₹13,000 / night"}
    ]
  },
  mizoram:{
    budget:[
      {n:"Aizawl Ridge Homestay", loc:"Aizawl", d:"Family home on the hillside with home-cooked Mizo meals.", range:"₹700 – ₹1,400 / night"}
    ],
    mid:[
      {n:"Reiek Hill Resort", loc:"Reiek", d:"Cottages with views over the surrounding peaks.", range:"₹2,600 – ₹4,600 / night"}
    ],
    luxury:[
      {n:"Champhai Valley Retreat", loc:"Champhai", d:"Premium rooms overlooking terraced paddy fields.", range:"₹6,500 – ₹11,000 / night"}
    ]
  },
  tripura:{
    budget:[
      {n:"Agartala City Lodge", loc:"Agartala", d:"Simple rooms close to Ujjayanta Palace.", range:"₹700 – ₹1,300 / night"}
    ],
    mid:[
      {n:"Neermahal View Cottages", loc:"Melaghar, near Neermahal", d:"Lakeside rooms with a boat ride to the palace included.", range:"₹2,600 – ₹4,500 / night"}
    ],
    luxury:[
      {n:"Jampui Hills Orchard Resort", loc:"Jampui Hills", d:"Premium cottages amid orange orchards on Tripura's highest ridge.", range:"₹6,000 – ₹10,500 / night"}
    ]
  },
  sikkim:{
    budget:[
      {n:"MG Marg Backpackers", loc:"Gangtok", d:"Simple dorms and doubles a short walk from the main promenade.", range:"₹900 – ₹1,700 / night"},
      {n:"Pelling Ridge Homestay", loc:"Pelling", d:"Family-run rooms with unobstructed Kanchenjunga views.", range:"₹1,200 – ₹2,200 / night"}
    ],
    mid:[
      {n:"Yumthang Valley Lodge", loc:"Lachung", d:"Heated wood cottages ahead of the rhododendron valley drive.", range:"₹3,800 – ₹6,500 / night"},
      {n:"Pemayangtse View Cottages", loc:"Pelling", d:"Comfortable rooms facing the monastery ridge and peak beyond.", range:"₹3,200 – ₹5,800 / night"}
    ],
    luxury:[
      {n:"Kanchenjunga Heights Resort", loc:"Pelling", d:"Premium suites with floor-to-ceiling peak views and full spa.", range:"₹11,000 – ₹20,000 / night"},
      {n:"Gangtok Heritage Palace Hotel", loc:"Gangtok", d:"Former royal guest house, now a five-star heritage property.", range:"₹13,000 – ₹24,000 / night"}
    ]
  }
};

const PRICE_GROUPS = [
  {title:"Food & drink", rows:[
    {item:"Cup of tea (roadside stall)", note:"Assam/Sikkim/Darjeeling blends", price:"₹10 – ₹20"},
    {item:"Plate of momos (8 pcs)", note:"steamed or fried, veg or pork", price:"₹60 – ₹120"},
    {item:"Local thali", note:"rice, dal, sabzi, fish or meat", price:"₹100 – ₹200"},
    {item:"Bamboo-shoot fish curry meal", note:"Assamese/Naga-style", price:"₹150 – ₹280"},
    {item:"Thukpa / noodle soup", note:"Sikkim & Arunachal staple", price:"₹80 – ₹150"},
    {item:"Rice beer (zutho / chhaang)", note:"tribal home-brew, per serving", price:"₹40 – ₹100"}
  ]},
  {title:"Getting around", rows:[
    {item:"Shared sumo/taxi, inter-town", note:"per seat, 2–4 hr routes", price:"₹250 – ₹700"},
    {item:"Private cab, full day", note:"sightseeing with driver", price:"₹2,500 – ₹4,500"},
    {item:"City auto-rickshaw ride", note:"short hop within town", price:"₹40 – ₹100"},
    {item:"Boat ride (Umngot / Loktak)", note:"per person, shared boat", price:"₹300 – ₹600"},
    {item:"Kaziranga jeep safari", note:"per person, shared jeep", price:"₹1,200 – ₹2,500"}
  ]},
  {title:"Permits & entry", rows:[
    {item:"Inner Line Permit", note:"Arunachal / Nagaland / Mizoram, Indian nationals", price:"₹100 – ₹300"},
    {item:"Protected Area Permit", note:"foreign nationals, varies by state", price:"₹500 – ₹2,000"},
    {item:"Kaziranga park entry", note:"per person, plus camera fee", price:"₹100 – ₹650"},
    {item:"Nathu La Pass permit", note:"Sikkim, arranged via agent", price:"₹600 – ₹1,000"}
  ]},
  {title:"Crafts to bring home", rows:[
    {item:"Naga / Manipuri handwoven shawl", note:"cotton or wool", price:"₹1,500 – ₹6,000"},
    {item:"Assam muga silk (per metre)", note:"natural golden silk", price:"₹3,000 – ₹8,000"},
    {item:"Assam orthodox tea, 250g", note:"single-estate", price:"₹150 – ₹500"},
    {item:"Khasi bamboo handicraft", note:"baskets, mats, trays", price:"₹200 – ₹1,200"},
    {item:"Sikkimese thangka print", note:"small to medium size", price:"₹800 – ₹4,000"}
  ]}
];

const CULTURE = [
  {tag:"Festival · April", t:"Bihu, Assam", d:"Three Bihus mark the farming year — Bohag (spring, New Year), Kati (autumn) and Magh (harvest) — with dance, feasting and the dhol."},
  {tag:"Festival · December", t:"Hornbill Festival, Nagaland", d:"All 17 recognised Naga tribes gather at Kisama for ten days of dance, wrestling, food and music — the region's biggest cultural stage."},
  {tag:"Festival · Feb/Mar", t:"Losar, Sikkim & Arunachal", d:"Tibetan Buddhist New Year — monastery cham dances, butter lamps, and family reunions across the high valleys."},
  {tag:"Festival · March", t:"Chapchar Kut, Mizoram", d:"A spring festival celebrating the end of jungle-clearing season, marked by the bamboo Cheraw dance."},
  {tag:"Cuisine", t:"Bamboo, fish & fermentation", d:"Bamboo shoot, akhuni (fermented soybean), smoked pork and river fish define Northeast kitchens — light on oil, heavy on flavour."},
  {tag:"Craft", t:"Looms of the hills", d:"Every state weaves — Assam's muga silk, Manipur's moirang phee, Naga shawls coded by clan and rank, Mizo puan skirts."}
];

/* ============================================================
   RENDER: SEASON STRIP
   ============================================================ */
const monthStrip = document.getElementById('monthStrip');
MONTHS.forEach((mo, i)=>{
  const btn = document.createElement('button');
  btn.className = 'month-btn ' + mo.status;
  btn.textContent = mo.m;
  btn.addEventListener('click', ()=>selectMonth(i));
  monthStrip.appendChild(btn);
});
function selectMonth(i){
  [...monthStrip.children].forEach((b,idx)=>b.classList.toggle('selected', idx===i));
  const mo = MONTHS[i];
  const statusLabel = mo.status==='best' ? 'Best window' : mo.status==='good' ? 'Good & economical' : 'Flood / landslide risk';
  document.getElementById('statStatus').textContent = statusLabel;
  document.getElementById('statStatus').style.color = mo.status==='flood' ? 'var(--terracotta)' : 'var(--pine)';
  document.getElementById('statExpect').textContent = mo.expect;
  document.getElementById('statGood').textContent = mo.good;
}
// default to October
selectMonth(9);

/* ============================================================
   RENDER: ITINERARY BUILDER
   ============================================================ */
const daysRange = document.getElementById('daysRange');
const daysValue = document.getElementById('daysValue');
daysRange.addEventListener('input', ()=> daysValue.textContent = daysRange.value);

document.getElementById('generateBtn').addEventListener('click', buildItinerary);

function buildItinerary(){
  const days = parseInt(daysRange.value,10);
  const budgetKey = document.getElementById('budgetSelect').value;
  const circuitKey = document.getElementById('circuitSelect').value;
  const budget = BUDGET_META[budgetKey];
  const template = CIRCUITS[circuitKey];

  // build day list: slice or extend by repeating a leisure/onward-travel day
  let plan = [];
  for(let d=0; d<days; d++){
    if(d < template.length){
      plan.push(template[d]);
    } else {
      const last = template[template.length-1];
      plan.push({state:last.state, place:last.place, act:"Leisure day — explore at your own pace, optional local excursion or rest before departure."});
    }
  }

  const dailyCost = Math.round(budget.perDay);
  const totalCost = dailyCost * days;

  const out = document.getElementById('itineraryOutput');
  out.innerHTML = '';

  const summary = document.createElement('div');
  summary.className = 'itinerary-summary';
  summary.innerHTML = `
    <div class="box"><span class="stat-label">Duration</span><div class="stat-value">${days} days</div></div>
    <div class="box"><span class="stat-label">Style</span><div class="stat-value" style="font-size:18px;">${budget.label}</div></div>
    <div class="box"><span class="stat-label">Estimated daily spend</span><div class="stat-value">₹${dailyCost.toLocaleString('en-IN')}</div></div>
    <div class="box"><span class="stat-label">Estimated trip total</span><div class="stat-value">₹${totalCost.toLocaleString('en-IN')}</div></div>
  `;
  out.appendChild(summary);

  plan.forEach((day, idx)=>{
    const row = document.createElement('div');
    row.className = 'day-card';
    row.innerHTML = `
      <div class="day-num">DAY<br>${idx+1}</div>
      <div class="day-body">
        <span class="day-state">${day.state} · ${day.place}</span>
        <h4>${day.act.split('.')[0]}${day.act.includes('.') && day.act.split('.')[0].length < day.act.length ? '' : ''}</h4>
        <p>${day.act}</p>
      </div>
      <div class="day-cost">~ ₹${dailyCost.toLocaleString('en-IN')}<br><span style="font-size:11px; color:var(--ink-soft);">per person</span></div>
    `;
    out.appendChild(row);
  });

  const note = document.createElement('p');
  note.className = 'price-note';
  note.style.marginTop = '18px';
  note.textContent = `Estimate covers stay, food and local transport at the "${budget.label}" level (${budget.note}). Inter-state flights and permits are extra.`;
  out.appendChild(note);

  out.scrollIntoView({behavior:'smooth', block:'nearest'});
}
buildItinerary(); // render a default plan on load

/* ============================================================
   RENDER: STATE GRID
   ============================================================ */
const stateGrid = document.getElementById('stateGrid');
let openState = null;

function photoSearchUrl(place, state){
  return 'https://www.google.com/search?tbm=isch&q=' + encodeURIComponent(place + ', ' + state + ', India');
}

function renderStates(){
  stateGrid.innerHTML = '';
  STATES.forEach(s=>{
    const photo = STATE_PHOTOS[s.id];
    const card = document.createElement('div');
    card.className = 'state-card' + (openState===s.id ? ' open' : '');
    card.style.setProperty('--accent', s.accent);
    card.innerHTML = `
      <div class="state-card-photo" style="background-image:url('${photo.url}')">
        <div class="icon-chip">${ICONS[s.icon]}</div>
      </div>
      <span class="expand">+</span>
      <h3>${s.name}</h3>
      <span class="tag">${s.tag}</span>
    `;
    card.addEventListener('click', ()=>{
      openState = openState === s.id ? null : s.id;
      renderStates();
      if(openState === s.id){
        setTimeout(()=>{ document.getElementById('panel-'+s.id)?.scrollIntoView({behavior:'smooth', block:'nearest'}); }, 60);
      }
    });
    stateGrid.appendChild(card);

    if(openState === s.id){
      const panel = document.createElement('div');
      panel.className = 'state-panel open';
      panel.id = 'panel-'+s.id;
      panel.innerHTML = `
        <div class="state-panel-hero" style="background-image:url('${photo.url}')">
          <div class="caption">
            <span class="place-name">📍 ${photo.place}</span>
            <a href="${photo.src}" target="_blank" rel="noopener">Photo: Wikimedia Commons · ${photo.license} ↗</a>
          </div>
        </div>
        <div class="state-panel-meta">
          <div><b>Best time</b>${s.best}</div>
          <div><b>Known for</b>${s.knownFor}</div>
        </div>
        <div class="places">
          ${s.places.map(p=>`
            <div class="place">
              <div class="photo" style="background:${p.g}">${p.e}</div>
              <div class="body">
                <h5>${p.n}</h5>
                <p>${p.d}</p>
                <a class="photo-link" href="${photoSearchUrl(p.n, s.name)}" target="_blank" rel="noopener">📷 More real photos — Google Images ↗</a>
              </div>
            </div>
          `).join('')}
        </div>
      `;
      stateGrid.appendChild(panel);
    }
  });
}
renderStates();

/* ============================================================
   ASK NEVYRA — CHAT WIZARD
   ============================================================ */
const chatBody = document.getElementById('chatBody');
const chatChoices = document.getElementById('chatChoices');

const CIRCUIT_LABEL = {
  classic:"Waterfalls & root bridges — Assam + Meghalaya",
  sikkim:"Mountains & monasteries — Sikkim",
  tribal:"Tribal culture & festivals — Nagaland + Manipur",
  grand:"A bit of everything — the Grand Northeast"
};
const BUDGET_LABEL = { budget:"shoestring", mid:"comfy mid-range", luxury:"treat-yourself" };

const chatAnswers = {};
let chatStepIndex = 0;

const CHAT_STEPS = [
  { key:'who', bot:["hey! 👋 I'm Nevyra.", "instead of you scrolling through everything, let me just ask a few things and build your trip."],
    question:"first — who's this trip for?",
    choices:[
      {label:"Just me", value:"solo"},
      {label:"Me + partner", value:"duo"},
      {label:"The whole squad", value:"squad"},
      {label:"Family, kids in tow", value:"family"}
    ]},
  { key:'circuit', botFrom:(a)=> a.who==='solo' ? ["okay, solo era. respect."] : ["love that for you."],
    question:"what's calling you right now?",
    choices:[
      {label:"Mountains & monasteries 🏔️", value:"sikkim"},
      {label:"Waterfalls & root bridges 🌿", value:"classic"},
      {label:"Tribal culture & festivals 🥁", value:"tribal"},
      {label:"Honestly, all of it", value:"grand"}
    ]},
  { key:'days', bot:["good pick, that's a genuinely underrated corner of the map."],
    question:"how many days can you actually get away?",
    choices:[
      {label:"Long weekend (4d)", value:"4"},
      {label:"About a week (7d)", value:"7"},
      {label:"Two weeks+ (12d)", value:"12"}
    ]},
  { key:'budget', bot:["noted."],
    question:"and what's the budget energy?",
    choices:[
      {label:"Shoestring 🎒", value:"budget"},
      {label:"Comfy mid-range ✨", value:"mid"},
      {label:"Treat myself 💸", value:"luxury"}
    ]}
];

function addBubble(text, cls){
  const b = document.createElement('div');
  b.className = 'bubble ' + cls;
  b.textContent = text;
  chatBody.appendChild(b);
  chatBody.scrollTop = chatBody.scrollHeight;
  return b;
}
function addTyping(){
  const t = document.createElement('div');
  t.className = 'typing';
  t.id = 'typingNow';
  t.innerHTML = '<span></span><span></span><span></span>';
  chatBody.appendChild(t);
  chatBody.scrollTop = chatBody.scrollHeight;
}
function removeTyping(){
  document.getElementById('typingNow')?.remove();
}

function renderChatChoices(choices, onPick){
  chatChoices.innerHTML = '';
  choices.forEach(c=>{
    const btn = document.createElement('button');
    btn.textContent = c.label;
    btn.addEventListener('click', ()=>onPick(c));
    chatChoices.appendChild(btn);
  });
}

function startChat(){
  chatBody.innerHTML = '';
  chatChoices.innerHTML = '';
  chatStepIndex = 0;
  Object.keys(chatAnswers).forEach(k=>delete chatAnswers[k]);
  runChatStep();
}

function runChatStep(){
  const step = CHAT_STEPS[chatStepIndex];
  if(!step){ return finishChat(); }

  const lines = step.bot ? step.bot : (step.botFrom ? step.botFrom(chatAnswers) : []);
  let delay = 0;
  const showNext = (i)=>{
    if(i < lines.length){
      addTyping();
      setTimeout(()=>{
        removeTyping();
        addBubble(lines[i], 'bot');
        showNext(i+1);
      }, 550);
    } else {
      addTyping();
      setTimeout(()=>{
        removeTyping();
        addBubble(step.question, 'bot');
        renderChatChoices(step.choices, (choice)=>{
          addBubble(choice.label, 'user');
          chatAnswers[step.key] = choice.value;
          chatChoices.innerHTML = '';
          chatStepIndex++;
          setTimeout(runChatStep, 350);
        });
      }, 550);
    }
  };
  showNext(0);
}

function finishChat(){
  addTyping();
  setTimeout(()=>{
    removeTyping();
    addBubble("okay, i've got it 🧠", 'bot');
    addTyping();
    setTimeout(()=>{
      removeTyping();
      const result = document.createElement('div');
      result.className = 'bubble result';
      result.innerHTML = `
        <h4>Your trip, roughly</h4>
        <p><b>${chatAnswers.days} days</b> on the <b>${CIRCUIT_LABEL[chatAnswers.circuit]}</b> route, at a <b>${BUDGET_LABEL[chatAnswers.budget]}</b> pace.</p>
        <button class="go-btn" id="chatBuildBtn" type="button">Build my full itinerary ↓</button>
      `;
      chatBody.appendChild(result);
      chatBody.scrollTop = chatBody.scrollHeight;
      document.getElementById('chatBuildBtn').addEventListener('click', ()=>{
        document.getElementById('daysRange').value = chatAnswers.days;
        document.getElementById('daysValue').textContent = chatAnswers.days;
        document.getElementById('budgetSelect').value = chatAnswers.budget;
        document.getElementById('circuitSelect').value = chatAnswers.circuit;
        buildItinerary();
        document.getElementById('plan').scrollIntoView({behavior:'smooth', block:'start'});
      });
    }, 700);
  }, 500);
}

document.getElementById('chatRestart').addEventListener('click', startChat);
startChat();

/* ============================================================
   RENDER: LOCAL GUIDES
   ============================================================ */
const guideGrid = document.getElementById('guideGrid');
GUIDES.forEach(g=>{
  const card = document.createElement('div');
  card.className = 'guide-card';
  card.innerHTML = `
    <div class="head" style="--accent:${g.accent}; background:${g.accent};">
      <h4>${g.state}</h4>
      <span class="spec">${g.spec}</span>
    </div>
    <div class="body">
      <div class="guide-rate"><span class="who">Indian nationals</span><b>${g.indian}</b></div>
      <div class="guide-rate"><span class="who">Foreign nationals</span><b>${g.foreign}</b></div>
      <p style="font-size:12.5px; color:var(--ink-soft); margin:0;">${g.note}</p>
      <a class="guide-link" style="--accent:${g.accent};" href="${g.url}" target="_blank" rel="noopener">Official tourism site — ${g.label} ↗</a>
    </div>
  `;
  guideGrid.appendChild(card);
});

/* ============================================================
   RENDER: HOTELS
   ============================================================ */
const hotelStateSelect = document.getElementById('hotelState');
STATES.forEach(s=>{
  const opt = document.createElement('option');
  opt.value = s.id; opt.textContent = s.name;
  hotelStateSelect.appendChild(opt);
});
hotelStateSelect.value = 'assam';

let currentTier = 'budget';
const swatchColors = {budget:'linear-gradient(135deg,#DCEEDC,#B7DAB8)', mid:'linear-gradient(135deg,#F5EBD2,#E7CE93)', luxury:'linear-gradient(135deg,#EADFF5,#C9A9E8)'};

function renderHotels(){
  const stateId = hotelStateSelect.value;
  const grid = document.getElementById('hotelGrid');
  grid.innerHTML = '';
  const list = (HOTELS[stateId] && HOTELS[stateId][currentTier]) || [];
  if(list.length===0){
    grid.innerHTML = `<p style="color:var(--ink-soft);">No listings yet for this combination — try another tier.</p>`;
    return;
  }
  list.forEach(h=>{
    const card = document.createElement('div');
    card.className = 'hotel-card';
    card.innerHTML = `
      <div class="swatch" style="background:${swatchColors[currentTier]}"></div>
      <div class="body">
        <span class="tier-badge ${currentTier}">${currentTier==='budget'?'Affordable':currentTier==='mid'?'Mid-range':'Luxury'}</span>
        <h4 style="margin-top:10px;">${h.n}</h4>
        <span class="loc">${h.loc}</span>
        <p>${h.d}</p>
        <div class="price"><span class="amt">${h.range.split(' / ')[0]}</span><span class="per">/ night</span></div>
      </div>
    `;
    grid.appendChild(card);
  });
}
hotelStateSelect.addEventListener('change', renderHotels);
document.querySelectorAll('#tierToggle .btn-ghost').forEach(btn=>{
  btn.addEventListener('click', ()=>{
    document.querySelectorAll('#tierToggle .btn-ghost').forEach(b=>b.classList.remove('active'));
    btn.classList.add('active');
    currentTier = btn.dataset.tier;
    renderHotels();
  });
});
renderHotels();

/* ============================================================
   RENDER: PRICE TABLE
   ============================================================ */
const priceGroupsEl = document.getElementById('priceGroups');
PRICE_GROUPS.forEach(group=>{
  const div = document.createElement('div');
  div.className = 'price-group';
  div.innerHTML = `
    <h4>${group.title}</h4>
    ${group.rows.map(r=>`
      <div class="price-row">
        <div class="item">${r.item}<small>${r.note}</small></div>
        <div class="amount">${r.price}</div>
      </div>
    `).join('')}
  `;
  priceGroupsEl.appendChild(div);
});
const note = document.createElement('p');
note.className = 'price-note';
note.style.gridColumn = '1/-1';
note.textContent = 'All figures are typical ranges for independent travel, gathered as a general guide — they will vary with season, location and bargaining, so treat them as a starting point rather than a quote.';
priceGroupsEl.appendChild(note);

/* ============================================================
   RENDER: CULTURE
   ============================================================ */
const cultureGrid = document.getElementById('cultureGrid');
CULTURE.forEach(c=>{
  const div = document.createElement('div');
  div.className = 'culture-card';
  div.innerHTML = `<span class="eyebrow">${c.tag}</span><h4>${c.t}</h4><p>${c.d}</p>`;
  cultureGrid.appendChild(div);
});

/* ============================================================
   NAV TOGGLE + REVEAL ON SCROLL
   ============================================================ */
document.getElementById('navToggle').addEventListener('click', ()=>{
  document.getElementById('navLinks').classList.toggle('open');
});
document.querySelectorAll('.nav-links a').forEach(a=>{
  a.addEventListener('click', ()=> document.getElementById('navLinks').classList.remove('open'));
});

const io = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
},{threshold:0.12});
document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>
</body>
</html>
