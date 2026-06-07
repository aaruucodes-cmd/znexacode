<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Znexaa Codes — Premium Website Development</title>
<meta name="description" content="Custom websites, landing pages, portfolios, e-commerce stores, and business solutions built with modern technology. Premium quality. Affordable pricing.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #030308;
  --bg2: #07070f;
  --surface: rgba(255,255,255,0.03);
  --surface2: rgba(255,255,255,0.06);
  --border: rgba(255,255,255,0.08);
  --border2: rgba(255,255,255,0.15);
  --text: #f0eeff;
  --text2: #9b98b8;
  --text3: #6b6890;
  --accent: #7c3aed;
  --accent2: #a855f7;
  --accent3: #6366f1;
  --blue: #3b82f6;
  --cyan: #06b6d4;
  --glow: rgba(124, 58, 237, 0.4);
  --glow2: rgba(99, 102, 241, 0.3);
  --font-display: 'Syne', sans-serif;
  --font-body: 'DM Sans', sans-serif;
  --radius: 16px;
  --radius2: 24px;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; font-size: 16px; }
body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-body);
  overflow-x: hidden;
  cursor: none;
}
a { color: inherit; text-decoration: none; }

/* ── CUSTOM CURSOR ── */
#cursor { position:fixed;width:12px;height:12px;background:var(--accent2);border-radius:50%;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);transition:transform .1s,background .2s;mix-blend-mode:screen; }
#cursor-trail { position:fixed;width:36px;height:36px;border:1px solid rgba(168,85,247,.4);border-radius:50%;pointer-events:none;z-index:9998;transform:translate(-50%,-50%);transition:all .25s ease; }

/* ── SCROLL PROGRESS ── */
#progress { position:fixed;top:0;left:0;height:2px;background:linear-gradient(90deg,var(--accent),var(--cyan));z-index:10000;width:0%;transition:width .1s linear; }

/* ── LOADER ── */
#loader {
  position:fixed;inset:0;background:var(--bg);z-index:99999;
  display:flex;flex-direction:column;align-items:center;justify-content:center;gap:24px;
  transition:opacity .5s,visibility .5s;
}
#loader .logo-text { font-family:var(--font-display);font-size:2rem;font-weight:800;letter-spacing:-.02em;background:linear-gradient(135deg,var(--accent2),var(--cyan));-webkit-background-clip:text;-webkit-text-fill-color:transparent; }
#loader .bar-wrap { width:200px;height:2px;background:var(--border);border-radius:99px;overflow:hidden; }
#loader .bar-fill { height:100%;background:linear-gradient(90deg,var(--accent),var(--cyan));border-radius:99px;width:0%;transition:width .05s; }
#loader.hide { opacity:0;visibility:hidden; }

/* ── NAV ── */
nav {
  position:fixed;top:0;left:0;right:0;z-index:1000;
  display:flex;align-items:center;justify-content:space-between;
  padding:20px 5%;
  backdrop-filter:blur(20px);background:rgba(3,3,8,.7);
  border-bottom:1px solid transparent;
  transition:border-color .3s,padding .3s;
}
nav.scrolled { border-color:var(--border);padding:14px 5%; }
.nav-logo { font-family:var(--font-display);font-size:1.35rem;font-weight:800;letter-spacing:-.02em; }
.nav-logo span { background:linear-gradient(135deg,var(--accent2),var(--cyan));-webkit-background-clip:text;-webkit-text-fill-color:transparent; }
.nav-links { display:flex;gap:36px;list-style:none; }
.nav-links a { font-size:.9rem;font-weight:500;color:var(--text2);transition:color .2s; }
.nav-links a:hover { color:var(--text); }
.nav-cta { background:linear-gradient(135deg,var(--accent),var(--accent3));padding:10px 22px;border-radius:8px;font-size:.875rem;font-weight:600;transition:transform .2s,box-shadow .2s; }
.nav-cta:hover { transform:translateY(-1px);box-shadow:0 8px 24px var(--glow); }
.hamburger { display:none;flex-direction:column;gap:5px;cursor:none;background:none;border:none;padding:4px; }
.hamburger span { display:block;width:22px;height:1.5px;background:var(--text);transition:.3s; }

/* ── HERO ── */
#hero {
  min-height:100vh;display:flex;align-items:center;justify-content:center;
  padding:140px 5% 100px;position:relative;overflow:hidden;text-align:center;
}
.hero-bg {
  position:absolute;inset:0;z-index:0;
  background:radial-gradient(ellipse 80% 60% at 50% 0%,rgba(124,58,237,.18) 0%,transparent 70%),
             radial-gradient(ellipse 40% 40% at 20% 60%,rgba(99,102,241,.12) 0%,transparent 60%),
             radial-gradient(ellipse 40% 40% at 80% 80%,rgba(6,182,212,.08) 0%,transparent 60%);
}
#particles-canvas { position:absolute;inset:0;z-index:1; }
.hero-content { position:relative;z-index:2;max-width:900px;margin:0 auto; }
.hero-badge {
  display:inline-flex;align-items:center;gap:8px;padding:8px 18px;
  border:1px solid rgba(168,85,247,.3);border-radius:99px;
  background:rgba(124,58,237,.1);backdrop-filter:blur(12px);
  font-size:.8rem;font-weight:500;color:var(--accent2);margin-bottom:32px;
  animation:fadeInUp .8s ease both;
}
.hero-badge .dot { width:6px;height:6px;border-radius:50%;background:var(--accent2);animation:pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.5;transform:scale(1.3)} }
.hero-h1 {
  font-family:var(--font-display);font-size:clamp(2.8rem,7vw,5.2rem);font-weight:800;
  line-height:1.05;letter-spacing:-.04em;margin-bottom:24px;
  animation:fadeInUp .8s .15s ease both;
}
.hero-h1 .grad { background:linear-gradient(135deg,#fff 0%,var(--accent2) 50%,var(--cyan) 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent; }
.hero-sub {
  font-size:clamp(1rem,2vw,1.2rem);color:var(--text2);max-width:600px;margin:0 auto 44px;
  font-weight:300;line-height:1.7;animation:fadeInUp .8s .3s ease both;
}
.hero-btns { display:flex;gap:16px;justify-content:center;flex-wrap:wrap;animation:fadeInUp .8s .45s ease both; }
.btn-primary {
  display:inline-flex;align-items:center;gap:10px;
  background:linear-gradient(135deg,var(--accent),var(--accent3));
  padding:15px 32px;border-radius:12px;font-weight:600;font-size:1rem;
  box-shadow:0 0 40px rgba(124,58,237,.4);transition:transform .2s,box-shadow .2s;
}
.btn-primary:hover { transform:translateY(-2px);box-shadow:0 0 60px rgba(124,58,237,.6); }
.btn-secondary {
  display:inline-flex;align-items:center;gap:10px;
  border:1px solid var(--border2);background:var(--surface2);
  padding:15px 32px;border-radius:12px;font-weight:500;font-size:1rem;
  backdrop-filter:blur(12px);transition:border-color .2s,background .2s,transform .2s;
}
.btn-secondary:hover { border-color:var(--accent2);background:rgba(124,58,237,.1);transform:translateY(-2px); }
.hero-float {
  position:absolute;z-index:1;border-radius:16px;backdrop-filter:blur(16px);
  background:rgba(255,255,255,.05);border:1px solid var(--border);padding:16px 20px;
  animation:float 6s ease-in-out infinite;
}
.hero-float1 { left:5%;top:35%;animation-delay:0s; }
.hero-float2 { right:5%;top:30%;animation-delay:-2s; }
.hero-float3 { left:8%;bottom:20%;animation-delay:-4s; }
@keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-16px)} }
.float-label { font-size:.7rem;color:var(--text3);margin-bottom:4px; }
.float-val { font-family:var(--font-display);font-size:1.1rem;font-weight:700;color:var(--accent2); }
@keyframes fadeInUp { from{opacity:0;transform:translateY(30px)} to{opacity:1;transform:translateY(0)} }
.reveal { opacity:0;transform:translateY(40px);transition:opacity .7s ease,transform .7s ease; }
.reveal.visible { opacity:1;transform:none; }

/* ── STATS ── */
#stats { padding:80px 5%;position:relative; }
.stats-grid { display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:2px;max-width:1100px;margin:0 auto;border:1px solid var(--border);border-radius:var(--radius2);overflow:hidden; }
.stat-item {
  padding:40px 24px;text-align:center;background:var(--surface);
  position:relative;overflow:hidden;transition:background .3s;
}
.stat-item:hover { background:var(--surface2); }
.stat-item::before { content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(124,58,237,.08),transparent);opacity:0;transition:.3s; }
.stat-item:hover::before { opacity:1; }
.stat-num { font-family:var(--font-display);font-size:3rem;font-weight:800;line-height:1;background:linear-gradient(135deg,var(--text),var(--accent2));-webkit-background-clip:text;-webkit-text-fill-color:transparent; }
.stat-label { font-size:.85rem;color:var(--text3);margin-top:8px;font-weight:500;letter-spacing:.05em;text-transform:uppercase; }

/* ── SECTION COMMON ── */
section { padding:100px 5%; }
.section-tag { display:inline-block;font-size:.75rem;font-weight:600;letter-spacing:.15em;text-transform:uppercase;color:var(--accent2);margin-bottom:16px; }
.section-title { font-family:var(--font-display);font-size:clamp(2rem,4vw,3rem);font-weight:800;line-height:1.1;letter-spacing:-.03em;margin-bottom:16px; }
.section-sub { color:var(--text2);font-size:1.05rem;line-height:1.7;max-width:560px; }
.section-head { margin-bottom:60px; }
.centered { text-align:center; }
.centered .section-sub { margin:0 auto; }

/* ── ABOUT ── */
#about { background:linear-gradient(180deg,var(--bg) 0%,var(--bg2) 100%); }
.about-grid { display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;max-width:1200px;margin:0 auto; }
.about-visual {
  position:relative;border-radius:var(--radius2);overflow:hidden;
  background:linear-gradient(135deg,rgba(124,58,237,.15),rgba(6,182,212,.1));
  border:1px solid var(--border);padding:48px;min-height:380px;
  display:flex;align-items:center;justify-content:center;
}
.about-svg-wrap { width:100%;max-width:280px; }
.about-visual::before {
  content:'';position:absolute;inset:0;
  background:radial-gradient(ellipse at 30% 30%,rgba(124,58,237,.2),transparent 60%);
}
.about-text .section-sub { margin-bottom:32px; }
.about-tags { display:flex;flex-wrap:wrap;gap:10px; }
.about-tag { padding:8px 16px;border:1px solid var(--border);border-radius:8px;font-size:.8rem;color:var(--text2);background:var(--surface); }

/* ── SERVICES ── */
#services { background:var(--bg); }
.services-grid { display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px;max-width:1200px;margin:0 auto; }
.service-card {
  padding:36px 28px;border-radius:var(--radius2);
  background:var(--surface);border:1px solid var(--border);
  position:relative;overflow:hidden;transition:border-color .3s,transform .3s,box-shadow .3s;
  cursor:none;
}
.service-card:hover { border-color:rgba(168,85,247,.4);transform:translateY(-4px);box-shadow:0 20px 60px rgba(124,58,237,.15); }
.service-card::before { content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(124,58,237,.06),transparent);opacity:0;transition:.3s; }
.service-card:hover::before { opacity:1; }
.service-icon {
  width:52px;height:52px;border-radius:14px;
  background:linear-gradient(135deg,rgba(124,58,237,.25),rgba(99,102,241,.15));
  border:1px solid rgba(168,85,247,.2);
  display:flex;align-items:center;justify-content:center;
  margin-bottom:20px;font-size:1.4rem;
}
.service-title { font-family:var(--font-display);font-size:1.15rem;font-weight:700;margin-bottom:10px; }
.service-desc { font-size:.9rem;color:var(--text2);line-height:1.6; }

/* ── PORTFOLIO ── */
#portfolio { background:var(--bg2); }
.portfolio-grid { display:grid;grid-template-columns:repeat(auto-fill,minmax(340px,1fr));gap:24px;max-width:1200px;margin:0 auto; }
.port-card {
  border-radius:var(--radius2);overflow:hidden;
  background:var(--surface);border:1px solid var(--border);
  transition:transform .3s,box-shadow .3s,border-color .3s;position:relative;
}
.port-card:hover { transform:translateY(-6px);box-shadow:0 30px 80px rgba(0,0,0,.4);border-color:var(--border2); }
.port-img {
  width:100%;height:220px;object-fit:cover;display:block;
  background:linear-gradient(135deg,rgba(124,58,237,.2),rgba(6,182,212,.15));
  position:relative;overflow:hidden;
}
.port-img-inner { width:100%;height:100%;display:flex;align-items:center;justify-content:center;font-size:3rem;position:relative;z-index:1; }
.port-img::before { content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(124,58,237,.3),rgba(6,182,212,.2)); }
.port-overlay {
  position:absolute;inset:0;height:220px;
  background:rgba(0,0,0,.8);backdrop-filter:blur(4px);
  display:flex;align-items:center;justify-content:center;gap:12px;
  opacity:0;transition:opacity .3s;
}
.port-card:hover .port-overlay { opacity:1; }
.port-btn { padding:10px 20px;border-radius:8px;font-size:.85rem;font-weight:600;background:linear-gradient(135deg,var(--accent),var(--accent3));transition:transform .2s; }
.port-btn:hover { transform:scale(1.05); }
.port-body { padding:24px; }
.port-cats { display:flex;gap:8px;margin-bottom:10px; }
.port-cat { font-size:.7rem;padding:4px 10px;border-radius:99px;background:rgba(124,58,237,.15);color:var(--accent2);border:1px solid rgba(168,85,247,.2); }
.port-title { font-family:var(--font-display);font-size:1.1rem;font-weight:700;margin-bottom:8px; }
.port-tech { display:flex;flex-wrap:wrap;gap:6px; }
.port-tech span { font-size:.7rem;color:var(--text3);padding:3px 8px;border-radius:6px;background:var(--surface2); }

/* ── WHY SECTION ── */
#why { background:var(--bg); }
.why-grid { display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;max-width:1200px;margin:0 auto; }
.why-list { display:grid;grid-template-columns:1fr 1fr;gap:16px; }
.why-item {
  display:flex;align-items:center;gap:12px;
  padding:18px;border-radius:var(--radius);
  background:var(--surface);border:1px solid var(--border);
  transition:border-color .3s,background .3s;
}
.why-item:hover { border-color:rgba(168,85,247,.3);background:var(--surface2); }
.why-check { width:28px;height:28px;border-radius:8px;background:linear-gradient(135deg,var(--accent),var(--accent3));display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:.85rem; }
.why-label { font-size:.9rem;font-weight:500; }

/* ── PRICING ── */
#pricing { background:var(--bg2); }
.pricing-grid { display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:24px;max-width:1050px;margin:0 auto; }
.price-card {
  padding:40px 32px;border-radius:var(--radius2);
  background:var(--surface);border:1px solid var(--border);
  position:relative;overflow:hidden;transition:transform .3s,box-shadow .3s;
}
.price-card:hover { transform:translateY(-6px);box-shadow:0 30px 80px rgba(0,0,0,.3); }
.price-card.featured {
  background:linear-gradient(135deg,rgba(124,58,237,.12),rgba(99,102,241,.08));
  border-color:rgba(168,85,247,.4);
  box-shadow:0 0 60px rgba(124,58,237,.15);
}
.price-badge {
  position:absolute;top:20px;right:20px;
  background:linear-gradient(135deg,var(--accent),var(--accent3));
  padding:4px 12px;border-radius:99px;font-size:.7rem;font-weight:700;
}
.price-tier { font-size:.8rem;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--text3);margin-bottom:12px; }
.price-val { font-family:var(--font-display);font-size:3.2rem;font-weight:800;line-height:1;margin-bottom:4px; }
.price-val small { font-size:1.2rem;vertical-align:top;margin-top:10px;display:inline-block;font-weight:400;color:var(--text2); }
.price-desc { font-size:.85rem;color:var(--text3);margin-bottom:28px; }
.price-divider { height:1px;background:var(--border);margin-bottom:24px; }
.price-features { list-style:none;display:flex;flex-direction:column;gap:12px;margin-bottom:32px; }
.price-features li { display:flex;align-items:center;gap:10px;font-size:.9rem;color:var(--text2); }
.price-features li::before { content:'✓';color:var(--accent2);font-weight:700;flex-shrink:0; }
.price-cta {
  display:block;text-align:center;padding:14px;border-radius:12px;font-weight:600;
  border:1px solid var(--border2);background:var(--surface2);transition:all .2s;
}
.price-cta:hover { border-color:var(--accent2);background:rgba(124,58,237,.15); }
.price-card.featured .price-cta {
  background:linear-gradient(135deg,var(--accent),var(--accent3));
  border:none;box-shadow:0 8px 30px var(--glow);
}
.price-card.featured .price-cta:hover { box-shadow:0 12px 40px var(--glow);transform:translateY(-1px); }

/* ── TESTIMONIALS ── */
#testimonials { background:var(--bg); }
.testimonials-track-wrap { overflow:hidden;position:relative;max-width:1200px;margin:0 auto; }
.testimonials-track { display:flex;gap:24px;transition:transform .5s cubic-bezier(.4,0,.2,1); }
.testi-card {
  min-width:380px;padding:32px;border-radius:var(--radius2);
  background:var(--surface);border:1px solid var(--border);flex-shrink:0;
  transition:border-color .3s;
}
.testi-card:hover { border-color:var(--border2); }
.testi-stars { color:#fbbf24;font-size:1rem;margin-bottom:16px;letter-spacing:2px; }
.testi-text { font-size:.95rem;color:var(--text2);line-height:1.7;margin-bottom:24px;font-style:italic; }
.testi-person { display:flex;align-items:center;gap:12px; }
.testi-avatar {
  width:44px;height:44px;border-radius:50%;
  background:linear-gradient(135deg,var(--accent),var(--cyan));
  display:flex;align-items:center;justify-content:center;font-weight:700;font-size:1rem;
  flex-shrink:0;
}
.testi-name { font-weight:600;font-size:.95rem; }
.testi-role { font-size:.8rem;color:var(--text3); }
.testi-nav { display:flex;justify-content:center;gap:12px;margin-top:32px; }
.testi-dot { width:8px;height:8px;border-radius:99px;background:var(--border2);cursor:none;transition:all .3s;border:none; }
.testi-dot.active { background:var(--accent2);width:28px; }

/* ── FAQ ── */
#faq { background:var(--bg2); }
.faq-list { max-width:800px;margin:0 auto;display:flex;flex-direction:column;gap:12px; }
.faq-item { border:1px solid var(--border);border-radius:var(--radius);overflow:hidden;transition:border-color .3s; }
.faq-item.open { border-color:rgba(168,85,247,.4); }
.faq-q {
  width:100%;background:var(--surface);border:none;padding:22px 24px;
  display:flex;align-items:center;justify-content:space-between;gap:16px;
  font-family:var(--font-body);font-size:1rem;font-weight:600;color:var(--text);
  cursor:none;text-align:left;transition:background .2s;
}
.faq-q:hover { background:var(--surface2); }
.faq-icon { flex-shrink:0;width:24px;height:24px;border-radius:6px;background:rgba(124,58,237,.15);display:flex;align-items:center;justify-content:center;font-size:.9rem;transition:transform .3s,background .3s; }
.faq-item.open .faq-icon { transform:rotate(45deg);background:rgba(124,58,237,.3); }
.faq-a { max-height:0;overflow:hidden;transition:max-height .4s ease,padding .3s; background:var(--surface); }
.faq-a p { padding:0 24px 22px;color:var(--text2);line-height:1.7;font-size:.95rem; }
.faq-item.open .faq-a { max-height:200px; }

/* ── CONTACT / CTA ── */
#contact {
  background:var(--bg);position:relative;overflow:hidden;text-align:center;
}
#contact::before {
  content:'';position:absolute;inset:0;
  background:radial-gradient(ellipse 80% 60% at 50% 50%,rgba(124,58,237,.12) 0%,transparent 70%);
}
.contact-inner { position:relative;z-index:1;max-width:700px;margin:0 auto; }
.contact-title { font-family:var(--font-display);font-size:clamp(2.2rem,5vw,3.8rem);font-weight:800;line-height:1.1;letter-spacing:-.03em;margin-bottom:20px; }
.contact-sub { color:var(--text2);font-size:1.1rem;margin-bottom:48px;line-height:1.7; }
.ig-btn {
  display:inline-flex;align-items:center;gap:14px;
  padding:18px 40px;border-radius:14px;font-size:1.1rem;font-weight:700;
  background:linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045);
  box-shadow:0 0 40px rgba(131,58,180,.5);
  animation:igGlow 3s ease-in-out infinite;
  transition:transform .2s;
}
.ig-btn:hover { transform:scale(1.05); }
@keyframes igGlow {
  0%,100% { box-shadow:0 0 40px rgba(131,58,180,.5); }
  50% { box-shadow:0 0 70px rgba(253,29,29,.6),0 0 100px rgba(131,58,180,.4); }
}
.ig-icon { font-size:1.4rem; }
.ig-handle { font-size:.85rem;font-weight:400;opacity:.8;display:block;margin-top:12px;color:var(--text3); }

/* ── FOOTER ── */
footer {
  background:var(--bg2);border-top:1px solid var(--border);
  padding:64px 5% 32px;
}
.footer-top { display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:48px;margin-bottom:48px; }
.footer-brand p { font-size:.9rem;color:var(--text3);line-height:1.7;margin-top:12px;max-width:300px; }
.footer-col h4 { font-family:var(--font-display);font-size:.85rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:var(--text3);margin-bottom:16px; }
.footer-col ul { list-style:none;display:flex;flex-direction:column;gap:10px; }
.footer-col ul a { font-size:.9rem;color:var(--text3);transition:color .2s; }
.footer-col ul a:hover { color:var(--accent2); }
.footer-social { display:flex;gap:10px;margin-top:20px; }
.social-btn {
  width:38px;height:38px;border-radius:10px;border:1px solid var(--border);background:var(--surface);
  display:flex;align-items:center;justify-content:center;font-size:1rem;
  transition:border-color .2s,background .2s,transform .2s;
}
.social-btn:hover { border-color:var(--accent2);background:rgba(124,58,237,.15);transform:translateY(-2px); }
.footer-bottom { border-top:1px solid var(--border);padding-top:24px;display:flex;align-items:center;justify-content:space-between; }
.footer-bottom p { font-size:.85rem;color:var(--text3); }
.footer-bottom .love { color:var(--accent2); }

/* ── FLOAT SOCIAL ── */
#float-social {
  position:fixed;bottom:32px;right:32px;z-index:500;
  width:52px;height:52px;border-radius:50%;
  background:linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045);
  display:flex;align-items:center;justify-content:center;
  font-size:1.4rem;box-shadow:0 8px 30px rgba(131,58,180,.5);
  animation:igGlow 3s infinite;transition:transform .2s;
}
#float-social:hover { transform:scale(1.1); }

/* ── RESPONSIVE ── */
@media(max-width:900px) {
  .about-grid,.why-grid { grid-template-columns:1fr; }
  .footer-top { grid-template-columns:1fr 1fr; }
  .hero-float1,.hero-float2,.hero-float3 { display:none; }
}
@media(max-width:680px) {
  .nav-links { display:none; }
  .nav-cta { display:none; }
  .hamburger { display:flex; }
  .why-list { grid-template-columns:1fr; }
  .footer-top { grid-template-columns:1fr; }
  .testi-card { min-width:300px; }
}

/* ── MOBILE MENU ── */
#mobile-menu {
  position:fixed;inset:0;z-index:999;
  background:rgba(3,3,8,.97);backdrop-filter:blur(20px);
  display:flex;flex-direction:column;align-items:center;justify-content:center;gap:32px;
  transform:translateX(100%);transition:transform .4s cubic-bezier(.4,0,.2,1);
}
#mobile-menu.open { transform:none; }
#mobile-menu a { font-family:var(--font-display);font-size:2rem;font-weight:700; }
#close-menu { position:absolute;top:24px;right:24px;background:none;border:none;color:var(--text);font-size:1.5rem;cursor:none; }
</style>
</head>
<body>

<!-- LOADER -->
<div id="loader">
  <div class="logo-text">Znexaa Codes</div>
  <div class="bar-wrap"><div class="bar-fill" id="loader-bar"></div></div>
</div>

<!-- SCROLL PROGRESS -->
<div id="progress"></div>

<!-- CUSTOM CURSOR -->
<div id="cursor"></div>
<div id="cursor-trail"></div>

<!-- NAV -->
<nav id="navbar">
  <a href="#" class="nav-logo"><span>Znexaa</span> Codes</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="nav-cta">Order Now →</a>
  <button class="hamburger" id="hamburger" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
</nav>

<!-- MOBILE MENU -->
<div id="mobile-menu">
  <button id="close-menu">✕</button>
  <a href="#about" class="mob-link">About</a>
  <a href="#services" class="mob-link">Services</a>
  <a href="#portfolio" class="mob-link">Portfolio</a>
  <a href="#pricing" class="mob-link">Pricing</a>
  <a href="#contact" class="mob-link">Contact</a>
</div>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <canvas id="particles-canvas"></canvas>
  <div class="hero-float hero-float1">
    <div class="float-label">Projects Done</div>
    <div class="float-val">50+</div>
  </div>
  <div class="hero-float hero-float2">
    <div class="float-label">Client Satisfaction</div>
    <div class="float-val">100%</div>
  </div>
  <div class="hero-float hero-float3">
    <div class="float-label">Avg. Delivery</div>
    <div class="float-val">3 Days</div>
  </div>
  <div class="hero-content">
    <div class="hero-badge"><span class="dot"></span>Available for new projects</div>
    <h1 class="hero-h1"><span class="grad">Premium Websites<br>That Grow Your Business</span></h1>
    <p class="hero-sub">Custom websites, landing pages, portfolios, e-commerce stores, and business solutions built with modern technology.</p>
    <div class="hero-btns">
      <a href="#portfolio" class="btn-primary">View Portfolio ↗</a>
      <a href="#contact" class="btn-secondary">Order Website →</a>
    </div>
  </div>
</section>

<!-- STATS -->
<div id="stats">
  <div class="stats-grid reveal">
    <div class="stat-item">
      <div class="stat-num" data-target="50">0</div>
      <div class="stat-label">Projects Completed</div>
    </div>
    <div class="stat-item">
      <div class="stat-num" data-target="100">0</div>
      <div class="stat-label">Client Satisfaction %</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">3</div>
      <div class="stat-label">Days Avg Delivery</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">★</div>
      <div class="stat-label">Premium Quality</div>
    </div>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-visual reveal">
      <div class="about-svg-wrap">
        <svg viewBox="0 0 280 280" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="20" y="50" width="240" height="160" rx="12" fill="rgba(124,58,237,0.1)" stroke="rgba(168,85,247,0.3)" stroke-width="1.5"/>
          <rect x="20" y="50" width="240" height="28" rx="12" fill="rgba(124,58,237,0.2)" stroke="rgba(168,85,247,0.3)" stroke-width="1.5"/>
          <circle cx="36" cy="64" r="5" fill="#ef4444"/>
          <circle cx="52" cy="64" r="5" fill="#fbbf24"/>
          <circle cx="68" cy="64" r="5" fill="#22c55e"/>
          <text x="36" y="105" font-family="monospace" font-size="11" fill="rgba(168,85,247,0.8)">&lt;hero&gt;</text>
          <text x="48" y="122" font-family="monospace" font-size="11" fill="rgba(99,102,241,0.7)">&lt;h1&gt;Your Brand&lt;/h1&gt;</text>
          <text x="48" y="139" font-family="monospace" font-size="11" fill="rgba(6,182,212,0.7)">&lt;button&gt;Get Started&lt;/button&gt;</text>
          <text x="36" y="156" font-family="monospace" font-size="11" fill="rgba(168,85,247,0.8)">&lt;/hero&gt;</text>
          <rect x="36" y="165" width="100" height="6" rx="3" fill="rgba(124,58,237,0.3)"/>
          <rect x="36" y="177" width="160" height="6" rx="3" fill="rgba(99,102,241,0.2)"/>
          <rect x="36" y="189" width="130" height="6" rx="3" fill="rgba(99,102,241,0.2)"/>
          <circle cx="230" cy="240" r="24" fill="rgba(124,58,237,0.2)" stroke="rgba(168,85,247,0.4)" stroke-width="1.5"/>
          <text x="222" y="246" font-family="monospace" font-size="14" fill="rgba(168,85,247,0.9)">{ }</text>
          <circle cx="50" cy="240" r="18" fill="rgba(6,182,212,0.15)" stroke="rgba(6,182,212,0.3)" stroke-width="1.5"/>
          <text x="43" y="245" font-family="monospace" font-size="11" fill="rgba(6,182,212,0.8)">&lt;/&gt;</text>
        </svg>
      </div>
    </div>
    <div class="about-text reveal">
      <div class="section-tag">About Us</div>
      <h2 class="section-title">Where Code Meets Creativity</h2>
      <p class="section-sub" style="margin-bottom:20px;">Znexaa Codes specializes in designing and developing modern, high-performance websites for businesses, creators, startups, and personal brands.</p>
      <p class="section-sub" style="margin-bottom:32px;">Every project is crafted with meticulous attention to detail, performance, and user experience — built to convert visitors into customers.</p>
      <div class="about-tags">
        <span class="about-tag">HTML5 / CSS3</span>
        <span class="about-tag">JavaScript</span>
        <span class="about-tag">React</span>
        <span class="about-tag">SEO Optimized</span>
        <span class="about-tag">Mobile First</span>
        <span class="about-tag">E-Commerce</span>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="section-head centered reveal">
    <div class="section-tag">What We Build</div>
    <h2 class="section-title">Services We Offer</h2>
    <p class="section-sub">From simple landing pages to complex web applications — we build it all with premium quality.</p>
  </div>
  <div class="services-grid">
    <div class="service-card reveal">
      <div class="service-icon">🏢</div>
      <div class="service-title">Business Websites</div>
      <p class="service-desc">Professional, trust-building websites for companies and local businesses that convert visitors into clients.</p>
    </div>
    <div class="service-card reveal">
      <div class="service-icon">🎨</div>
      <div class="service-title">Portfolio Websites</div>
      <p class="service-desc">Personal branding sites that showcase your work and skills with stunning visual design.</p>
    </div>
    <div class="service-card reveal">
      <div class="service-icon">🚀</div>
      <div class="service-title">Landing Pages</div>
      <p class="service-desc">High-converting marketing pages engineered to capture leads and drive sales.</p>
    </div>
    <div class="service-card reveal">
      <div class="service-icon">🛒</div>
      <div class="service-title">E-Commerce Stores</div>
      <p class="service-desc">Full-featured online stores with payment integration, product management, and smooth checkout.</p>
    </div>
    <div class="service-card reveal">
      <div class="service-icon">⚙️</div>
      <div class="service-title">Custom Web Applications</div>
      <p class="service-desc">Advanced web solutions for unique business needs — dashboards, portals, booking systems, and more.</p>
    </div>
    <div class="service-card reveal">
      <div class="service-icon">🔍</div>
      <div class="service-title">SEO & Performance</div>
      <p class="service-desc">Speed optimization and SEO setup to rank higher on Google and load blazing fast.</p>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="section-head centered reveal">
    <div class="section-tag">Our Work</div>
    <h2 class="section-title">Portfolio Showcase</h2>
    <p class="section-sub">A curated selection of projects that demonstrate our range, quality, and attention to detail.</p>
  </div>
  <div class="portfolio-grid">
    <div class="port-card reveal">
      <div class="port-img">
        <div class="port-img-inner" style="background:linear-gradient(135deg,#1e1b4b,#312e81);">🏪</div>
        <div class="port-overlay">
          <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="port-btn">Live Preview ↗</a>
        </div>
      </div>
      <div class="port-body">
        <div class="port-cats"><span class="port-cat">E-Commerce</span></div>
        <div class="port-title">FashionHub Store</div>
        <div class="port-tech"><span>HTML</span><span>CSS</span><span>JavaScript</span><span>Stripe</span></div>
      </div>
    </div>
    <div class="port-card reveal">
      <div class="port-img">
        <div class="port-img-inner" style="background:linear-gradient(135deg,#0f172a,#1e3a5f);">💼</div>
        <div class="port-overlay">
          <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="port-btn">Live Preview ↗</a>
        </div>
      </div>
      <div class="port-body">
        <div class="port-cats"><span class="port-cat">Business</span></div>
        <div class="port-title">TechCorp Solutions</div>
        <div class="port-tech"><span>React</span><span>Tailwind</span><span>Framer</span></div>
      </div>
    </div>
    <div class="port-card reveal">
      <div class="port-img">
        <div class="port-img-inner" style="background:linear-gradient(135deg,#1a0533,#4c1d95);">🎯</div>
        <div class="port-overlay">
          <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="port-btn">Live Preview ↗</a>
        </div>
      </div>
      <div class="port-body">
        <div class="port-cats"><span class="port-cat">Portfolio</span></div>
        <div class="port-title">Designer Portfolio</div>
        <div class="port-tech"><span>HTML5</span><span>GSAP</span><span>CSS3</span></div>
      </div>
    </div>
    <div class="port-card reveal">
      <div class="port-img">
        <div class="port-img-inner" style="background:linear-gradient(135deg,#042f2e,#065f46);">🍽️</div>
        <div class="port-overlay">
          <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="port-btn">Live Preview ↗</a>
        </div>
      </div>
      <div class="port-body">
        <div class="port-cats"><span class="port-cat">Landing Page</span></div>
        <div class="port-title">Restaurant Landing</div>
        <div class="port-tech"><span>HTML</span><span>CSS</span><span>JS</span></div>
      </div>
    </div>
    <div class="port-card reveal">
      <div class="port-img">
        <div class="port-img-inner" style="background:linear-gradient(135deg,#1c1917,#44403c);">📱</div>
        <div class="port-overlay">
          <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="port-btn">Live Preview ↗</a>
        </div>
      </div>
      <div class="port-body">
        <div class="port-cats"><span class="port-cat">SaaS</span></div>
        <div class="port-title">AppLaunch SaaS</div>
        <div class="port-tech"><span>React</span><span>Next.js</span><span>CSS</span></div>
      </div>
    </div>
    <div class="port-card reveal">
      <div class="port-img">
        <div class="port-img-inner" style="background:linear-gradient(135deg,#0c0a09,#1c0a2e);">🎵</div>
        <div class="port-overlay">
          <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="port-btn">Live Preview ↗</a>
        </div>
      </div>
      <div class="port-body">
        <div class="port-cats"><span class="port-cat">Creative</span></div>
        <div class="port-title">Artist Showcase</div>
        <div class="port-tech"><span>HTML5</span><span>WebGL</span><span>JS</span></div>
      </div>
    </div>
  </div>
</section>

<!-- WHY US -->
<section id="why">
  <div class="why-grid">
    <div class="reveal">
      <div class="section-tag">Why Znexaa</div>
      <h2 class="section-title">Built Different,<br>By Design</h2>
      <p class="section-sub">We don't use templates. Every website is custom-built to match your brand identity and business goals — with performance baked in from day one.</p>
    </div>
    <div class="why-list reveal">
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Premium Design</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Mobile Responsive</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">SEO Optimized</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Fast Performance</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Modern Tech Stack</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Secure & Reliable</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Affordable Pricing</span></div>
      <div class="why-item"><div class="why-check">✓</div><span class="why-label">Ongoing Support</span></div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing">
  <div class="section-head centered reveal">
    <div class="section-tag">Transparent Pricing</div>
    <h2 class="section-title">Simple, Honest Plans</h2>
    <p class="section-sub">No hidden fees. No surprises. Choose the plan that fits your needs and budget.</p>
  </div>
  <div class="pricing-grid">
    <div class="price-card reveal">
      <div class="price-tier">Starter</div>
      <div class="price-val"><small>₹</small>999</div>
      <p class="price-desc">Perfect for individuals & small businesses</p>
      <div class="price-divider"></div>
      <ul class="price-features">
        <li>Single Page Website</li>
        <li>Mobile Responsive</li>
        <li>Fast Delivery (2–3 Days)</li>
        <li>Basic SEO Setup</li>
        <li>Contact Form</li>
      </ul>
      <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="price-cta">Get Started →</a>
    </div>
    <div class="price-card featured reveal">
      <div class="price-badge">Most Popular</div>
      <div class="price-tier">Professional</div>
      <div class="price-val"><small>₹</small>2,999</div>
      <p class="price-desc">Best for growing businesses & brands</p>
      <div class="price-divider"></div>
      <ul class="price-features">
        <li>Multi-Page Website</li>
        <li>Premium Custom Design</li>
        <li>SEO Optimization</li>
        <li>Mobile Responsive</li>
        <li>Animations & Interactions</li>
        <li>1 Month Free Support</li>
      </ul>
      <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="price-cta">Order Now →</a>
    </div>
    <div class="price-card reveal">
      <div class="price-tier">Business Pro</div>
      <div class="price-val"><small>₹</small>5,999</div>
      <p class="price-desc">For enterprises & advanced needs</p>
      <div class="price-divider"></div>
      <ul class="price-features">
        <li>Advanced Features</li>
        <li>E-Commerce Integration</li>
        <li>Custom Functionality</li>
        <li>Priority Support</li>
        <li>Performance Audit</li>
        <li>3 Months Free Support</li>
      </ul>
      <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="price-cta">Get Started →</a>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="section-head centered reveal">
    <div class="section-tag">Client Reviews</div>
    <h2 class="section-title">What Clients Say</h2>
  </div>
  <div class="testimonials-track-wrap reveal">
    <div class="testimonials-track" id="testi-track">
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-text">"Znexaa Codes absolutely nailed our e-commerce website. The design was stunning and the delivery was faster than expected. Our sales increased by 40% in the first month!"</p>
        <div class="testi-person">
          <div class="testi-avatar">R</div>
          <div><div class="testi-name">Rahul Sharma</div><div class="testi-role">Founder, FashionHub</div></div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-text">"I needed a portfolio website urgently and Znexaa delivered in just 2 days. The quality was beyond my expectations — I've received so many compliments already."</p>
        <div class="testi-person">
          <div class="testi-avatar" style="background:linear-gradient(135deg,var(--blue),var(--cyan));">P</div>
          <div><div class="testi-name">Priya Mehta</div><div class="testi-role">Freelance Designer</div></div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-text">"Professional service from start to finish. The website they built for my restaurant looks premium and actually helps customers find us online. Very happy!"</p>
        <div class="testi-person">
          <div class="testi-avatar" style="background:linear-gradient(135deg,#f59e0b,#ef4444);">A</div>
          <div><div class="testi-name">Arjun Patel</div><div class="testi-role">Restaurant Owner</div></div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-text">"Best investment for my startup! The landing page converts visitors at an incredible rate. Znexaa really understands what businesses need online."</p>
        <div class="testi-person">
          <div class="testi-avatar" style="background:linear-gradient(135deg,#22c55e,#06b6d4);">N</div>
          <div><div class="testi-name">Neha Singh</div><div class="testi-role">Startup Founder</div></div>
        </div>
      </div>
    </div>
  </div>
  <div class="testi-nav" id="testi-nav">
    <button class="testi-dot active" data-i="0"></button>
    <button class="testi-dot" data-i="1"></button>
    <button class="testi-dot" data-i="2"></button>
    <button class="testi-dot" data-i="3"></button>
  </div>
</section>

<!-- FAQ -->
<section id="faq">
  <div class="section-head centered reveal">
    <div class="section-tag">FAQ</div>
    <h2 class="section-title">Frequently Asked Questions</h2>
  </div>
  <div class="faq-list">
    <div class="faq-item reveal">
      <button class="faq-q">How long does it take to build a website?<span class="faq-icon">+</span></button>
      <div class="faq-a"><p>Depending on the project complexity, delivery ranges from 2–3 days for a single page site to 7–14 days for multi-page or e-commerce projects. We always communicate timelines upfront.</p></div>
    </div>
    <div class="faq-item reveal">
      <button class="faq-q">How do I place an order?<span class="faq-icon">+</span></button>
      <div class="faq-a"><p>Simply message us on Instagram @znexaa.codes. We'll discuss your requirements, share a quote, and get started once confirmed. The process is simple and fully online.</p></div>
    </div>
    <div class="faq-item reveal">
      <button class="faq-q">Will my website be mobile-friendly?<span class="faq-icon">+</span></button>
      <div class="faq-a"><p>Absolutely! Every website we build is fully mobile-responsive and tested across all major devices and screen sizes. Mobile performance is never an afterthought.</p></div>
    </div>
    <div class="faq-item reveal">
      <button class="faq-q">Do you offer revisions?<span class="faq-icon">+</span></button>
      <div class="faq-a"><p>Yes! We include revision rounds in every project to ensure you're completely satisfied. We work with you until the final result matches your vision perfectly.</p></div>
    </div>
    <div class="faq-item reveal">
      <button class="faq-q">What do you need from me to get started?<span class="faq-icon">+</span></button>
      <div class="faq-a"><p>Just your brand name, logo (if any), color preferences, content (text/images), and a brief description of what you need. We handle the rest — from design to deployment.</p></div>
    </div>
    <div class="faq-item reveal">
      <button class="faq-q">Can you help with domain and hosting?<span class="faq-icon">+</span></button>
      <div class="faq-a"><p>Yes! We can guide you on domain registration and hosting setup. For certain plans, we also offer free deployment on platforms like Vercel or Netlify.</p></div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner">
    <div class="section-tag reveal">Get In Touch</div>
    <h2 class="contact-title reveal">Ready To Build Your<br>Dream Website?</h2>
    <p class="contact-sub reveal">Drop us a message on Instagram and let's bring your vision to life. Fast turnaround, premium quality, affordable pricing.</p>
    <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="ig-btn reveal">
      <span class="ig-icon">📸</span>
      Order on Instagram
    </a>
    <span class="ig-handle">@znexaa.codes</span>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div class="footer-brand">
      <div class="nav-logo" style="font-size:1.5rem;"><span>Znexaa</span> Codes</div>
      <p>Premium website development for businesses, creators, and startups. Built with modern technology and a passion for great design.</p>
      <div class="footer-social">
        <a href="https://www.instagram.com/znexaa.codes/" target="_blank" class="social-btn">📸</a>
      </div>
    </div>
    <div class="footer-col">
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#pricing">Pricing</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Services</h4>
      <ul>
        <li><a href="#services">Business Websites</a></li>
        <li><a href="#services">Portfolio Sites</a></li>
        <li><a href="#services">Landing Pages</a></li>
        <li><a href="#services">E-Commerce</a></li>
        <li><a href="#services">Web Applications</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Contact</h4>
      <ul>
        <li><a href="https://www.instagram.com/znexaa.codes/" target="_blank">Instagram</a></li>
        <li><a href="#pricing">Pricing Plans</a></li>
        <li><a href="#faq">FAQ</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 Znexaa Codes. All rights reserved.</p>
    <p>Made with <span class="love">♥</span> by Znexaa Codes</p>
  </div>
</footer>

<!-- FLOAT SOCIAL -->
<a href="https://www.instagram.com/znexaa.codes/" target="_blank" id="float-social" title="Order on Instagram">📸</a>

<script>
// ── LOADER ──
const loaderBar = document.getElementById('loader-bar');
const loader = document.getElementById('loader');
let w = 0;
const iv = setInterval(() => {
  w += Math.random() * 15;
  if (w >= 100) { w = 100; clearInterval(iv); setTimeout(() => loader.classList.add('hide'), 300); }
  loaderBar.style.width = w + '%';
}, 80);

// ── CURSOR ──
const cur = document.getElementById('cursor');
const curT = document.getElementById('cursor-trail');
let mx = 0, my = 0, tx = 0, ty = 0;
document.addEventListener('mousemove', e => { mx = e.clientX; my = e.clientY; cur.style.left = mx + 'px'; cur.style.top = my + 'px'; });
(function animCursor() {
  tx += (mx - tx) * .15; ty += (my - ty) * .15;
  curT.style.left = tx + 'px'; curT.style.top = ty + 'px';
  requestAnimationFrame(animCursor);
})();
document.querySelectorAll('a,button,.service-card,.port-card,.price-card,.faq-q,.testi-dot').forEach(el => {
  el.addEventListener('mouseenter', () => { cur.style.transform = 'translate(-50%,-50%) scale(2.5)'; curT.style.transform = 'translate(-50%,-50%) scale(1.5)'; });
  el.addEventListener('mouseleave', () => { cur.style.transform = 'translate(-50%,-50%) scale(1)'; curT.style.transform = 'translate(-50%,-50%) scale(1)'; });
});

// ── SCROLL PROGRESS ──
const prog = document.getElementById('progress');
document.addEventListener('scroll', () => {
  const s = document.documentElement.scrollTop, h = document.documentElement.scrollHeight - window.innerHeight;
  prog.style.width = (s / h * 100) + '%';
});

// ── NAVBAR ──
const nav = document.getElementById('navbar');
document.addEventListener('scroll', () => { nav.classList.toggle('scrolled', window.scrollY > 60); });

// ── MOBILE MENU ──
const menu = document.getElementById('mobile-menu');
document.getElementById('hamburger').addEventListener('click', () => menu.classList.add('open'));
document.getElementById('close-menu').addEventListener('click', () => menu.classList.remove('open'));
document.querySelectorAll('.mob-link').forEach(l => l.addEventListener('click', () => menu.classList.remove('open')));

// ── PARTICLES ──
const canvas = document.getElementById('particles-canvas');
const ctx = canvas.getContext('2d');
let W, H, pts = [];
function resize() { W = canvas.width = canvas.offsetWidth; H = canvas.height = canvas.offsetHeight; }
resize();
window.addEventListener('resize', resize);
for (let i = 0; i < 80; i++) {
  pts.push({ x: Math.random() * 2000, y: Math.random() * 800, vx: (Math.random() - .5) * .4, vy: (Math.random() - .5) * .4, r: Math.random() * 1.5 + .5, a: Math.random() });
}
function drawParts() {
  ctx.clearRect(0, 0, W, H);
  pts.forEach(p => {
    p.x += p.vx; p.y += p.vy;
    if (p.x < 0) p.x = W; if (p.x > W) p.x = 0;
    if (p.y < 0) p.y = H; if (p.y > H) p.y = 0;
    ctx.beginPath(); ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
    ctx.fillStyle = `rgba(168,85,247,${p.a * .4})`; ctx.fill();
  });
  pts.forEach((p, i) => pts.slice(i + 1).forEach(q => {
    const d = Math.hypot(p.x - q.x, p.y - q.y);
    if (d < 120) { ctx.beginPath(); ctx.moveTo(p.x, p.y); ctx.lineTo(q.x, q.y); ctx.strokeStyle = `rgba(124,58,237,${.15 * (1 - d / 120)})`; ctx.lineWidth = .5; ctx.stroke(); }
  }));
  requestAnimationFrame(drawParts);
}
drawParts();

// ── REVEAL ──
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); } });
}, { threshold: .12 });
document.querySelectorAll('.reveal').forEach(el => obs.observe(el));

// ── COUNTER ──
const countObs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (!e.isIntersecting) return;
    const el = e.target, target = +el.dataset.target;
    if (!target) return;
    let cur = 0; const step = target / 60;
    const iv = setInterval(() => { cur = Math.min(cur + step, target); el.textContent = Math.round(cur) + '+'; if (cur >= target) clearInterval(iv); }, 16);
    countObs.unobserve(el);
  });
}, { threshold: .5 });
document.querySelectorAll('[data-target]').forEach(el => countObs.observe(el));

// ── FAQ ──
document.querySelectorAll('.faq-q').forEach(btn => {
  btn.addEventListener('click', () => {
    const item = btn.parentElement;
    const isOpen = item.classList.contains('open');
    document.querySelectorAll('.faq-item.open').forEach(i => i.classList.remove('open'));
    if (!isOpen) item.classList.add('open');
  });
});

// ── TESTIMONIALS CAROUSEL ──
const track = document.getElementById('testi-track');
const dots = document.querySelectorAll('.testi-dot');
let cur2 = 0;
function goTo(i) {
  cur2 = i;
  const cardW = track.children[0].offsetWidth + 24;
  track.style.transform = `translateX(-${i * cardW}px)`;
  dots.forEach((d, j) => d.classList.toggle('active', j === i));
}
dots.forEach(d => d.addEventListener('click', () => goTo(+d.dataset.i)));
setInterval(() => goTo((cur2 + 1) % 4), 5000);
</script>
</body>
</html>
