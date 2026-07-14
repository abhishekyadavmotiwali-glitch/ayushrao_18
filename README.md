<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<meta name="author" content="Abhishek Yadav"/>
<meta name="description" content="Abhishek Yadav — Full Stack MERN Developer building high-performance web apps, AI integrations, and scalable platforms."/>
<meta property="og:title" content="Abhishek Yadav | Full Stack MERN Developer"/>
<meta name="theme-color" content="#09090b"/>
<title>Abhishek Yadav | Full Stack MERN Developer</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#09090b;--bg2:#0f0f14;--bg3:#13131a;--bg4:#18181f;
  --border:#1e1e2a;--border2:#28283a;
  --text:#f0f0f8;--text2:#8888a8;--text3:#5555778;
  --purple:#8b5cf6;--purple2:#7c3aed;--purple3:#6d28d9;
  --cyan:#06b6d4;--cyan2:#0891b2;
  --green:#22c55e;--orange:#f97316;--pink:#ec4899;
  --r:16px;--r2:12px;--r3:8px;
}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text);font-family:'Inter',sans-serif;line-height:1.6;overflow-x:hidden}
::selection{background:rgba(139,92,246,.25);color:var(--text)}
::-webkit-scrollbar{width:5px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--border2);border-radius:10px}

/* BLOBS */
.blob{position:fixed;border-radius:50%;filter:blur(100px);pointer-events:none;z-index:0;animation:blobmove 12s ease-in-out infinite}
.blob1{width:700px;height:700px;background:radial-gradient(circle,rgba(139,92,246,.1),transparent 70%);top:-200px;right:-200px;animation-delay:0s}
.blob2{width:600px;height:600px;background:radial-gradient(circle,rgba(6,182,212,.07),transparent 70%);bottom:-200px;left:-200px;animation-delay:4s}
.blob3{width:400px;height:400px;background:radial-gradient(circle,rgba(139,92,246,.05),transparent 70%);top:40%;left:40%;animation-delay:8s}
@keyframes blobmove{0%,100%{transform:translate(0,0)}50%{transform:translate(30px,20px)}}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:1000;height:68px;
  display:flex;align-items:center;justify-content:space-between;
  padding:0 clamp(20px,5vw,80px);
  background:rgba(9,9,11,.88);backdrop-filter:blur(24px);
  border-bottom:1px solid rgba(255,255,255,.06)}
.nav-logo{font-family:'JetBrains Mono',monospace;font-size:1.05rem;font-weight:700;text-decoration:none;display:flex;align-items:center;gap:2px}
.nl-b{color:var(--purple);font-size:1.2rem}
.nl-n{background:linear-gradient(135deg,#fff,rgba(255,255,255,.75));-webkit-background-clip:text;-webkit-text-fill-color:transparent}
.nav-links{display:flex;align-items:center;gap:2px;list-style:none}
.nav-links a{color:var(--text2);text-decoration:none;font-size:.83rem;font-weight:500;padding:7px 13px;border-radius:var(--r3);transition:color .2s,background .2s}
.nav-links a:hover,.nav-links a.active{color:var(--text);background:rgba(255,255,255,.07)}
.nav-btn{display:flex;align-items:center;gap:7px;padding:8px 20px;border-radius:var(--r3);background:var(--purple2);color:#fff;font-size:.83rem;font-weight:600;text-decoration:none;transition:background .2s,transform .15s;box-shadow:0 0 20px rgba(139,92,246,.28)}
.nav-btn:hover{background:var(--purple3);transform:translateY(-1px)}
.hbg{display:none;background:none;border:none;color:var(--text);font-size:1.25rem;cursor:pointer;padding:8px}
.mobnav{display:none;position:fixed;top:68px;left:0;right:0;background:rgba(9,9,11,.97);backdrop-filter:blur(24px);border-bottom:1px solid var(--border);z-index:999;flex-direction:column;padding:12px}
.mobnav.open{display:flex}
.mobnav a{color:var(--text2);text-decoration:none;padding:13px 16px;border-radius:var(--r3);font-size:.93rem;transition:color .2s,background .2s}
.mobnav a:hover{color:var(--text);background:rgba(255,255,255,.06)}

/* LAYOUT */
.wrap{max-width:1160px;margin:0 auto;padding:0 clamp(20px,5vw,60px);position:relative;z-index:1}
section{padding:96px 0}

/* SEC HEADER */
.stag{display:inline-flex;align-items:center;gap:6px;background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.22);border-radius:100px;padding:4px 14px;font-size:.72rem;font-weight:600;color:var(--purple);letter-spacing:.07em;text-transform:uppercase;margin-bottom:14px}
.sh{font-size:clamp(1.8rem,3.5vw,2.5rem);font-weight:800;line-height:1.2;margin-bottom:12px}
.sh .g{background:linear-gradient(135deg,var(--purple),var(--cyan));-webkit-background-clip:text;-webkit-text-fill-color:transparent}
.ssub{color:var(--text2);font-size:.97rem;line-height:1.7;max-width:540px}
.sec-hd{margin-bottom:52px}

/* ===== HERO ===== */
#hero{min-height:100vh;display:flex;align-items:center;padding-top:68px;position:relative;overflow:hidden}
.hero-grid{display:grid;grid-template-columns:1fr 400px;align-items:center;gap:72px;width:100%}

.htag{display:inline-flex;align-items:center;gap:10px;background:rgba(34,197,94,.08);border:1px solid rgba(34,197,94,.2);border-radius:100px;padding:6px 18px;font-size:.76rem;font-weight:600;color:var(--green);margin-bottom:28px}
.ping-dot{width:8px;height:8px;border-radius:50%;background:var(--green);position:relative;flex-shrink:0}
.ping-dot::before{content:'';position:absolute;inset:-4px;border-radius:50%;background:rgba(34,197,94,.35);animation:ping 1.6s ease-out infinite}
@keyframes ping{0%{transform:scale(1);opacity:.8}100%{transform:scale(2.8);opacity:0}}

.hint{font-family:'JetBrains Mono',monospace;font-size:.95rem;color:var(--text2);margin-bottom:8px}
.hint span{color:var(--purple)}
.hh{font-size:clamp(2.8rem,6vw,4.5rem);font-weight:800;line-height:1.08;margin-bottom:18px}
.hh .gn{background:linear-gradient(135deg,var(--purple) 20%,var(--cyan) 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;display:block}
.hrole{font-family:'JetBrains Mono',monospace;color:var(--cyan);font-size:1rem;font-weight:500;margin-bottom:22px}
.hrole .cm{color:var(--text2)}
.hp{color:var(--text2);font-size:.98rem;line-height:1.82;max-width:510px;margin-bottom:38px}
.hbtns{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:44px}
.btn-g{display:inline-flex;align-items:center;gap:8px;padding:12px 26px;border-radius:var(--r3);background:linear-gradient(135deg,var(--purple2),var(--cyan2));color:#fff;font-size:.88rem;font-weight:600;text-decoration:none;box-shadow:0 4px 22px rgba(139,92,246,.32);transition:transform .2s,box-shadow .2s}
.btn-g:hover{transform:translateY(-2px);box-shadow:0 8px 32px rgba(139,92,246,.48)}
.btn-gh{display:inline-flex;align-items:center;gap:8px;padding:12px 26px;border-radius:var(--r3);background:rgba(255,255,255,.05);border:1px solid var(--border2);color:var(--text);font-size:.88rem;font-weight:600;text-decoration:none;transition:background .2s,border-color .2s,transform .2s}
.btn-gh:hover{background:rgba(255,255,255,.09);border-color:var(--purple);transform:translateY(-2px)}
.hstats{display:flex;gap:36px;padding-top:28px;border-top:1px solid var(--border)}
.hs-n{font-size:1.9rem;font-weight:800;line-height:1}
.hs-n span{color:var(--purple)}
.hs-l{font-size:.76rem;color:var(--text2);margin-top:4px}

/* PROFILE CARD */
.pcard{position:relative;background:var(--bg3);border:1px solid var(--border2);border-radius:24px;overflow:hidden;padding:28px}
.pcard::before{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(139,92,246,.07),transparent 60%);pointer-events:none}
.pimg-wrap{position:relative;width:148px;height:148px;margin:0 auto 20px}
.pimg-ring{width:100%;height:100%;border-radius:50%;background:conic-gradient(from 0deg,var(--purple),var(--cyan),#ec4899,var(--purple));padding:3px;animation:spin360 7s linear infinite}
@keyframes spin360{to{transform:rotate(360deg)}}
.pimg-in{width:100%;height:100%;border-radius:50%;background:var(--bg3);overflow:hidden}
.pimg-in img{width:100%;height:100%;object-fit:cover;object-position:top center;border-radius:50%}
.pstatus{position:absolute;bottom:4px;right:4px;width:20px;height:20px;border-radius:50%;background:var(--green);border:3px solid var(--bg3)}
.pname{text-align:center;font-size:1.15rem;font-weight:700;margin-bottom:3px}
.ptitle{text-align:center;font-size:.8rem;color:var(--text2);margin-bottom:18px}
.pchips{display:flex;flex-wrap:wrap;gap:7px;justify-content:center;margin-bottom:20px}
.pchip{background:rgba(139,92,246,.12);border:1px solid rgba(139,92,246,.2);border-radius:100px;padding:3px 11px;font-size:.7rem;font-weight:600;color:var(--purple)}
.pchip.c{background:rgba(6,182,212,.1);border-color:rgba(6,182,212,.2);color:var(--cyan)}
.pchip.g{background:rgba(34,197,94,.1);border-color:rgba(34,197,94,.2);color:var(--green)}
.pdiv{height:1px;background:var(--border);margin-bottom:18px}
.pinfo{display:flex;flex-direction:column;gap:11px}
.pi{display:flex;align-items:center;gap:9px;font-size:.8rem}
.pi i{width:16px;color:var(--purple);font-size:.8rem;flex-shrink:0}
.pi span{color:var(--text2)}
.pi strong{color:var(--text);margin-left:4px}

/* ===== ABOUT ===== */
#about{background:linear-gradient(180deg,var(--bg),rgba(139,92,246,.02) 50%,var(--bg))}
.agrid{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center}
.at p{color:var(--text2);line-height:1.85;margin-bottom:16px;font-size:.95rem}
.aminis{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:24px}
.amini{background:var(--bg3);border:1px solid var(--border);border-radius:var(--r2);padding:16px;display:flex;align-items:flex-start;gap:10px}
.ami{width:34px;height:34px;border-radius:var(--r3);background:rgba(139,92,246,.12);display:flex;align-items:center;justify-content:center;font-size:.85rem;flex-shrink:0}
.amini h4{font-size:.83rem;font-weight:600;margin-bottom:2px}
.amini p{font-size:.73rem;color:var(--text2);margin:0}
.svbox{background:var(--bg3);border:1px solid var(--border);border-radius:var(--r);padding:28px}
.svbox-t{font-size:.88rem;font-weight:700;margin-bottom:22px;display:flex;align-items:center;gap:8px}
.svbox-t i{color:var(--purple)}
.sbar{margin-bottom:16px}
.sbar-top{display:flex;justify-content:space-between;font-size:.8rem;margin-bottom:6px}
.sbar-top span:last-child{color:var(--text2)}
.sbar-tr{height:5px;background:var(--border);border-radius:3px;overflow:hidden}
.sbar-f{height:100%;border-radius:3px;background:linear-gradient(90deg,var(--purple2),var(--cyan))}

/* ===== SERVICES ===== */
#services{}
.svcgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.svcc{background:var(--bg3);border:1px solid var(--border);border-radius:var(--r);padding:28px;position:relative;overflow:hidden;transition:border-color .3s,transform .3s}
.svcc::after{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(139,92,246,.06),transparent 60%);opacity:0;transition:opacity .3s}
.svcc:hover{border-color:rgba(139,92,246,.38);transform:translateY(-4px)}
.svcc:hover::after{opacity:1}
.svci{width:52px;height:52px;border-radius:14px;margin-bottom:18px;background:rgba(139,92,246,.12);border:1px solid rgba(139,92,246,.2);display:flex;align-items:center;justify-content:center;font-size:1.3rem}
.svcc h3{font-size:1rem;font-weight:700;margin-bottom:9px}
.svcc p{color:var(--text2);font-size:.84rem;line-height:1.7}
.svctags{display:flex;flex-wrap:wrap;gap:6px;margin-top:14px}
.svctag{background:rgba(255,255,255,.05);border:1px solid var(--border2);border-radius:5px;padding:3px 9px;font-size:.7rem;color:var(--text2)}

/* ===== SKILLS ===== */
#skills{background:linear-gradient(180deg,var(--bg),rgba(6,182,212,.02) 50%,var(--bg))}
.skcats{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
.skcat{background:var(--bg3);border:1px solid var(--border);border-radius:var(--r);padding:26px;transition:border-color .3s,transform .3s}
.skcat:hover{border-color:rgba(139,92,246,.28);transform:translateY(-3px)}
.skcathd{display:flex;align-items:center;gap:11px;margin-bottom:18px}
.skcati{width:42px;height:42px;border-radius:10px;background:rgba(139,92,246,.12);display:flex;align-items:center;justify-content:center;font-size:1.05rem;color:var(--purple)}
.skcat h3{font-size:.92rem;font-weight:700}
.sktags{display:flex;flex-wrap:wrap;gap:7px}
.sktag{background:rgba(255,255,255,.04);border:1px solid var(--border2);border-radius:6px;padding:5px 12px;font-size:.76rem;color:var(--text2);transition:color .2s,border-color .2s,background .2s;cursor:default}
.sktag:hover{color:var(--purple);border-color:rgba(139,92,246,.3);background:rgba(139,92,246,.07)}

/* ===== PROJECTS ===== */
#projects{}
.pgrid{display:grid;grid-template-columns:repeat(2,1fr);gap:22px}
.pcard{background:var(--bg3);border:1px solid var(--border);border-radius:var(--r);overflow:hidden;transition:border-color .3s,transform .3s;display:flex;flex-direction:column}
.pcard:hover{border-color:rgba(139,92,246,.32);transform:translateY(-4px)}
.pbanner{height:170px;display:flex;align-items:center;justify-content:center;font-size:3.2rem;position:relative}
.pb1{background:linear-gradient(135deg,rgba(139,92,246,.25),rgba(6,182,212,.18))}
.pb2{background:linear-gradient(135deg,rgba(249,115,22,.25),rgba(239,68,68,.18))}
.pb3{background:linear-gradient(135deg,rgba(34,197,94,.25),rgba(6,182,212,.18))}
.pb4{background:linear-gradient(135deg,rgba(236,72,153,.25),rgba(139,92,246,.18))}
.pb5{background:linear-gradient(135deg,rgba(6,182,212,.25),rgba(59,130,246,.18))}
.pb6{background:linear-gradient(135deg,rgba(139,92,246,.25),rgba(236,72,153,.18))}
.pbody{padding:22px;flex:1;display:flex;flex-direction:column}
.ptop{display:flex;justify-content:space-between;align-items:center;margin-bottom:10px}
.plinks{display:flex;gap:7px}
.plbtn{width:31px;height:31px;border-radius:var(--r3);background:rgba(255,255,255,.06);border:1px solid var(--border2);display:flex;align-items:center;justify-content:center;color:var(--text2);text-decoration:none;font-size:.83rem;transition:color .2s,border-color .2s}
.plbtn:hover{color:var(--purple);border-color:rgba(139,92,246,.38)}
.pcat{font-size:.7rem;font-weight:600;color:var(--purple);text-transform:uppercase;letter-spacing:.07em}
.pbody h3{font-size:1rem;font-weight:700;margin-bottom:7px}
.pbody p{color:var(--text2);font-size:.83rem;line-height:1.65;flex:1}
.pstack{display:flex;flex-wrap:wrap;gap:5px;margin-top:14px}
.pstag{background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.2);border-radius:5px;padding:3px 9px;font-size:.7rem;color:var(--purple)}

/* ===== EDUCATION ===== */
#education{background:linear-gradient(180deg,var(--bg),rgba(139,92,246,.025) 50%,var(--bg))}
.educards{display:grid;grid-template-columns:repeat(3,1fr);gap:22px}
.educard{background:var(--bg3);border:1px solid var(--border);border-radius:var(--r);padding:26px;position:relative;overflow:hidden;transition:border-color .3s,transform .3s}
.educard::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--purple2),var(--cyan))}
.educard:hover{border-color:rgba(139,92,246,.32);transform:translateY(-3px)}
.eduicon{font-size:2rem;margin-bottom:14px}
.eduyear{display:inline-block;background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.2);border-radius:100px;padding:3px 11px;font-size:.7rem;font-weight:600;color:var(--purple);margin-bottom:11px}
.educard h3{font-size:.97rem;font-weight:700;margin-bottom:5px}
.eduinst{font-size:.8rem;color:var(--cyan);font-weight:500;margin-bottom:12px}
.edupct{font-size:2.4rem;font-weight:800;background:linear-gradient(135deg,var(--purple),var(--cyan));-webkit-background-clip:text;-webkit-text-fill-color:transparent;line-height:1;margin-bottom:3px}
.edupl{font-size:.72rem;color:var(--text2)}
.edulist{list-style:none;margin-top:13px}
.edulist li{font-size:.8rem;color:var(--text2);padding:3px 0 3px 13px;position:relative}
.edulist li::before{content:'▸';position:absolute;left:0;color:var(--purple)}

/* ===== EXPERIENCE ===== */
#experience{}
.exptl{position:relative;padding-left:30px}
.exptl::before{content:'';position:absolute;left:0;top:8px;bottom:8px;width:2px;background:linear-gradient(180deg,var(--purple),var(--cyan),transparent)}
.expcard{position:relative;margin-bottom:24px;background:var(--bg3);border:1px solid var(--border);border-radius:var(--r);padding:26px;transition:border-color .3s}
.expcard:hover{border-color:rgba(139,92,246,.32)}
.expdot{position:absolute;left:-38px;top:26px;width:15px;height:15px;border-radius:50%;background:linear-gradient(135deg,var(--purple),var(--cyan));border:2px solid var(--bg);box-shadow:0 0 10px rgba(139,92,246,.45)}
.exphd{display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:10px;margin-bottom:14px}
.expco{font-size:.78rem;color:var(--cyan);font-weight:600;margin-bottom:3px}
.exptitle{font-size:1.02rem;font-weight:700}
.expperiod{background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.2);border-radius:100px;padding:4px 13px;font-size:.72rem;color:var(--purple);font-weight:500;white-space:nowrap}
.explist{list-style:none}
.explist li{font-size:.855rem;color:var(--text2);padding:4px 0 4px 16px;position:relative;line-height:1.6}
.explist li::before{content:'▹';position:absolute;left:0;color:var(--purple)}

/* ===== CONTACT ===== */
#contact{background:linear-gradient(180deg,var(--bg),rgba(6,182,212,.02) 50%,var(--bg))}
.cwrap{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:start}
.cleft p{color:var(--text2);font-size:.95rem;line-height:1.82;margin-bottom:28px}
.ciitem{display:flex;align-items:center;gap:13px;margin-bottom:16px}
.ciicon{width:42px;height:42px;border-radius:var(--r3);background:rgba(139,92,246,.1);border:1px solid rgba(139,92,246,.2);display:flex;align-items:center;justify-content:center;color:var(--purple);flex-shrink:0}
.cilabel{font-size:.73rem;color:var(--text2)}
.cival{font-size:.88rem;color:var(--text)}
.cival a{color:var(--text);text-decoration:none;transition:color .2s}
.cival a:hover{color:var(--purple)}
.socials{display:flex;gap:9px;margin-top:24px}
.sbtn{width:42px;height:42px;border-radius:var(--r3);background:var(--bg3);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;color:var(--text2);text-decoration:none;font-size:.95rem;transition:color .2s,border-color .2s,transform .2s}
.sbtn:hover{color:var(--purple);border-color:rgba(139,92,246,.38);transform:translateY(-2px)}
.cform{display:flex;flex-direction:column;gap:14px}
.cfl{font-size:.78rem;color:var(--text2);margin-bottom:5px;display:block}
.cfi,.cfta{width:100%;background:var(--bg3);border:1px solid var(--border2);border-radius:var(--r3);padding:11px 15px;color:var(--text);font-family:inherit;font-size:.88rem;outline:none;transition:border-color .2s}
.cfi:focus,.cfta:focus{border-color:var(--purple)}
.cfta{resize:vertical;min-height:130px}
.cfrow{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.cfsub{width:100%;padding:13px;border-radius:var(--r3);font-size:.88rem;font-weight:700;background:linear-gradient(135deg,var(--purple2),var(--cyan2));color:#fff;border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;box-shadow:0 4px 20px rgba(139,92,246,.28);transition:transform .2s,box-shadow .2s}
.cfsub:hover{transform:translateY(-2px);box-shadow:0 8px 28px rgba(139,92,246,.45)}

/* FOOTER */
footer{border-top:1px solid var(--border);padding:32px 0;position:relative;z-index:1}
.fi{display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:14px}
.flogo{font-family:'JetBrains Mono',monospace;font-size:.88rem;color:var(--text2)}
.flogo span{color:var(--purple)}
footer p{color:var(--text2);font-size:.78rem}
.flinks{display:flex;gap:18px}
.flinks a{color:var(--text2);text-decoration:none;font-size:.78rem;transition:color .2s}
.flinks a:hover{color:var(--text)}

/* RESPONSIVE */
@media(max-width:1020px){
  .svcgrid{grid-template-columns:repeat(2,1fr)}
  .educards{grid-template-columns:1fr 1fr}
}
@media(max-width: