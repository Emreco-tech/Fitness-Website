<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>APEX FIT Bad Oeynhausen – Dein Premium Fitnessstudio</title>
<meta name="description" content="APEX FIT Bad Oeynhausen – Modernste Geräte, KI-basiertes Training, Wellness & Sauna. Jetzt ab 19,90€/Monat. Probetraining kostenlos buchen." />
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
<style>
  /* ===== RESET & BASE ===== */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --red: #E8001D;
    --red-dark: #B00015;
    --red-glow: rgba(232,0,29,0.25);
    --black: #080808;
    --black2: #0f0f0f;
    --black3: #161616;
    --gray1: #1e1e1e;
    --gray2: #2a2a2a;
    --gray3: #3d3d3d;
    --text: #f0f0f0;
    --text-muted: #888;
    --white: #ffffff;
    --font-display: 'Bebas Neue', sans-serif;
    --font-ui: 'Syne', sans-serif;
    --font-body: 'DM Sans', sans-serif;
  }
  html { scroll-behavior: smooth; }
  body {
    background: var(--black);
    color: var(--text);
    font-family: var(--font-body);
    font-weight: 300;
    overflow-x: hidden;
    line-height: 1.65;
  }
  img { max-width: 100%; display: block; }
  a { text-decoration: none; color: inherit; }

  /* ===== SCROLLBAR ===== */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--black); }
  ::-webkit-scrollbar-thumb { background: var(--red); border-radius: 2px; }

  /* ===== UTILITIES ===== */
  .container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
  .section-label {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--red);
    margin-bottom: 16px;
  }
  .section-title {
    font-family: var(--font-display);
    font-size: clamp(42px, 6vw, 80px);
    line-height: 0.95;
    letter-spacing: 0.02em;
    color: var(--white);
  }
  .section-title span { color: var(--red); }
  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: var(--red);
    color: var(--white);
    font-family: var(--font-ui);
    font-weight: 700;
    font-size: 13px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 16px 32px;
    border: none;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    transition: all 0.3s ease;
    clip-path: polygon(0 0, calc(100% - 12px) 0, 100% 12px, 100% 100%, 12px 100%, 0 calc(100% - 12px));
  }
  .btn-primary::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--red-dark);
    transform: translateX(-100%);
    transition: transform 0.3s ease;
  }
  .btn-primary:hover::before { transform: translateX(0); }
  .btn-primary span { position: relative; z-index: 1; }
  .btn-outline {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: transparent;
    color: var(--white);
    font-family: var(--font-ui);
    font-weight: 600;
    font-size: 13px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 15px 31px;
    border: 1px solid rgba(255,255,255,0.25);
    cursor: pointer;
    transition: all 0.3s ease;
    clip-path: polygon(0 0, calc(100% - 12px) 0, 100% 12px, 100% 100%, 12px 100%, 0 calc(100% - 12px));
  }
  .btn-outline:hover { border-color: var(--red); color: var(--red); }

  /* ===== NOISE OVERLAY ===== */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.03'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.4;
  }

  /* ===== NAVBAR ===== */
  nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    padding: 0 24px;
    background: rgba(8,8,8,0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid rgba(255,255,255,0.05);
    transition: all 0.3s ease;
  }
  .nav-inner {
    max-width: 1200px;
    margin: 0 auto;
    height: 72px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .nav-logo {
    font-family: var(--font-display);
    font-size: 28px;
    letter-spacing: 0.08em;
    color: var(--white);
    display: flex;
    align-items: center;
    gap: 4px;
  }
  .nav-logo .logo-accent { color: var(--red); }
  .nav-links {
    display: flex;
    align-items: center;
    gap: 32px;
    list-style: none;
  }
  .nav-links a {
    font-family: var(--font-ui);
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--text-muted);
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--white); }
  .nav-cta { display: flex; align-items: center; gap: 12px; }
  .hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
    padding: 4px;
  }
  .hamburger span {
    display: block;
    width: 24px;
    height: 2px;
    background: var(--white);
    transition: all 0.3s;
  }

  /* ===== HERO ===== */
  .hero {
    min-height: 100vh;
    position: relative;
    display: flex;
    align-items: flex-end;
    padding-bottom: 80px;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute;
    inset: 0;
    background: 
      linear-gradient(135deg, rgba(232,0,29,0.15) 0%, transparent 50%),
      linear-gradient(to bottom, transparent 40%, var(--black) 100%),
      linear-gradient(to right, var(--black) 0%, transparent 30%);
    z-index: 2;
  }
  .hero-grid {
    position: absolute;
    inset: 0;
    background-image: 
      linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    z-index: 1;
  }
  .hero-image-bg {
    position: absolute;
    inset: 0;
    background: 
      radial-gradient(ellipse at 70% 50%, rgba(232,0,29,0.08) 0%, transparent 60%),
      linear-gradient(to bottom right, #1a0005 0%, #080808 100%);
    z-index: 0;
  }
  /* Decorative athletic silhouette */
  .hero-visual {
    position: absolute;
    right: -40px;
    top: 50%;
    transform: translateY(-50%);
    width: 55%;
    height: 90%;
    z-index: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }
  .hero-visual svg {
    width: 100%;
    height: 100%;
    opacity: 0.12;
  }
  .hero-glow {
    position: absolute;
    right: 10%;
    top: 50%;
    transform: translateY(-50%);
    width: 400px;
    height: 400px;
    background: radial-gradient(circle, rgba(232,0,29,0.3) 0%, transparent 70%);
    z-index: 1;
    animation: pulseGlow 4s ease-in-out infinite;
  }
  @keyframes pulseGlow {
    0%, 100% { transform: translateY(-50%) scale(1); opacity: 0.6; }
    50% { transform: translateY(-50%) scale(1.15); opacity: 1; }
  }
  .hero-content {
    position: relative;
    z-index: 10;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
    width: 100%;
  }
  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(232,0,29,0.1);
    border: 1px solid rgba(232,0,29,0.3);
    padding: 8px 16px;
    margin-bottom: 32px;
    animation: fadeInUp 0.6s ease both;
  }
  .hero-badge-dot {
    width: 6px;
    height: 6px;
    background: var(--red);
    border-radius: 50%;
    animation: blink 1.5s ease infinite;
  }
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }
  .hero-badge span {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--red);
  }
  .hero-title {
    font-family: var(--font-display);
    font-size: clamp(72px, 11vw, 160px);
    line-height: 0.88;
    letter-spacing: 0.02em;
    margin-bottom: 8px;
    animation: fadeInUp 0.6s ease 0.1s both;
  }
  .hero-title-sub {
    font-family: var(--font-display);
    font-size: clamp(36px, 5.5vw, 76px);
    line-height: 0.88;
    letter-spacing: 0.02em;
    color: var(--red);
    margin-bottom: 32px;
    animation: fadeInUp 0.6s ease 0.2s both;
  }
  .hero-desc {
    font-size: 17px;
    color: rgba(240,240,240,0.65);
    max-width: 520px;
    margin-bottom: 40px;
    line-height: 1.7;
    animation: fadeInUp 0.6s ease 0.3s both;
  }
  .hero-cta {
    display: flex;
    align-items: center;
    gap: 16px;
    flex-wrap: wrap;
    animation: fadeInUp 0.6s ease 0.4s both;
  }
  .hero-stats {
    display: flex;
    gap: 40px;
    margin-top: 64px;
    padding-top: 40px;
    border-top: 1px solid rgba(255,255,255,0.06);
    animation: fadeInUp 0.6s ease 0.5s both;
  }
  .hero-stat-num {
    font-family: var(--font-display);
    font-size: 42px;
    line-height: 1;
    color: var(--white);
  }
  .hero-stat-num span { color: var(--red); }
  .hero-stat-label {
    font-family: var(--font-body);
    font-size: 12px;
    color: var(--text-muted);
    letter-spacing: 0.05em;
    margin-top: 4px;
  }
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-scroll {
    position: absolute;
    bottom: 32px;
    right: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    z-index: 10;
  }
  .hero-scroll-text {
    font-family: var(--font-ui);
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--text-muted);
    writing-mode: vertical-rl;
  }
  .hero-scroll-line {
    width: 1px;
    height: 60px;
    background: linear-gradient(to bottom, var(--red), transparent);
    animation: scrollLine 2s ease infinite;
  }
  @keyframes scrollLine {
    0% { transform: scaleY(0); transform-origin: top; }
    50% { transform: scaleY(1); transform-origin: top; }
    51% { transform: scaleY(1); transform-origin: bottom; }
    100% { transform: scaleY(0); transform-origin: bottom; }
  }

  /* ===== PROMO BANNER ===== */
  .promo-banner {
    background: var(--red);
    padding: 18px 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .promo-banner::before {
    content: '';
    position: absolute;
    inset: 0;
    background: repeating-linear-gradient(
      45deg,
      transparent,
      transparent 20px,
      rgba(255,255,255,0.05) 20px,
      rgba(255,255,255,0.05) 40px
    );
  }
  .promo-banner-inner {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
  }
  .promo-banner-text {
    font-family: var(--font-ui);
    font-weight: 800;
    font-size: 15px;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--white);
  }
  .promo-banner-fire { font-size: 18px; }
  .promo-banner-link {
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    color: white;
    font-family: var(--font-ui);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 8px 20px;
    cursor: pointer;
    transition: background 0.2s;
  }
  .promo-banner-link:hover { background: rgba(255,255,255,0.25); }

  /* ===== FEATURES STRIP ===== */
  .features-strip {
    background: var(--black2);
    border-top: 1px solid rgba(255,255,255,0.05);
    border-bottom: 1px solid rgba(255,255,255,0.05);
    padding: 20px 0;
    overflow: hidden;
  }
  .features-strip-inner {
    display: flex;
    gap: 0;
  }
  .features-strip-track {
    display: flex;
    gap: 0;
    animation: marquee 25s linear infinite;
    white-space: nowrap;
  }
  .features-strip-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 0 40px;
    border-right: 1px solid rgba(255,255,255,0.08);
  }
  .features-strip-icon {
    color: var(--red);
    font-size: 18px;
  }
  .features-strip-label {
    font-family: var(--font-ui);
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--text-muted);
  }
  @keyframes marquee {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }

  /* ===== ABOUT ===== */
  .about { padding: 120px 0; background: var(--black2); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }
  .about-image-wrap {
    position: relative;
  }
  .about-image-main {
    width: 100%;
    aspect-ratio: 4/5;
    background: var(--gray1);
    position: relative;
    overflow: hidden;
    clip-path: polygon(0 0, calc(100% - 30px) 0, 100% 30px, 100% 100%, 30px 100%, 0 calc(100% - 30px));
  }
  .about-image-main-inner {
    width: 100%;
    height: 100%;
    background: 
      linear-gradient(135deg, #1a1a1a 0%, #2d0008 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }
  /* Stylized gym illustration */
  .about-image-main-inner svg {
    width: 80%;
    opacity: 0.3;
  }
  .about-image-tag {
    position: absolute;
    bottom: -20px;
    right: -20px;
    background: var(--red);
    padding: 24px 28px;
    clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px));
  }
  .about-image-tag-num {
    font-family: var(--font-display);
    font-size: 36px;
    line-height: 1;
    color: var(--white);
  }
  .about-image-tag-label {
    font-family: var(--font-ui);
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.7);
    margin-top: 4px;
  }
  .about-image-accent {
    position: absolute;
    top: 24px;
    left: -24px;
    width: 80px;
    height: 80px;
    border: 2px solid var(--red);
    opacity: 0.4;
  }
  .about-text { }
  .about-body {
    font-size: 16px;
    color: rgba(240,240,240,0.65);
    line-height: 1.8;
    margin: 24px 0 40px;
  }
  .about-perks {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 40px;
  }
  .about-perk {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 16px;
    background: rgba(255,255,255,0.02);
    border: 1px solid rgba(255,255,255,0.06);
    transition: border-color 0.3s;
  }
  .about-perk:hover { border-color: rgba(232,0,29,0.3); }
  .about-perk-icon {
    width: 36px;
    height: 36px;
    background: rgba(232,0,29,0.1);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    font-size: 16px;
  }
  .about-perk-text {
    font-family: var(--font-ui);
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
    line-height: 1.4;
  }

  /* ===== SERVICES ===== */
  .services { padding: 120px 0; background: var(--black); }
  .services-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    margin-bottom: 64px;
    flex-wrap: wrap;
    gap: 24px;
  }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
  }
  .service-card {
    background: var(--black2);
    padding: 40px 32px;
    position: relative;
    overflow: hidden;
    cursor: pointer;
    transition: all 0.3s ease;
    border: 1px solid rgba(255,255,255,0.04);
  }
  .service-card::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: var(--red);
    transform: scaleX(0);
    transition: transform 0.3s ease;
  }
  .service-card:hover { background: var(--black3); transform: translateY(-4px); }
  .service-card:hover::before { transform: scaleX(1); }
  .service-card.featured {
    background: var(--red);
    grid-column: span 1;
  }
  .service-card.featured::before { display: none; }
  .service-num {
    font-family: var(--font-display);
    font-size: 64px;
    line-height: 1;
    color: rgba(255,255,255,0.05);
    position: absolute;
    top: 20px;
    right: 24px;
  }
  .service-icon {
    font-size: 32px;
    margin-bottom: 20px;
  }
  .service-title {
    font-family: var(--font-ui);
    font-size: 18px;
    font-weight: 800;
    color: var(--white);
    margin-bottom: 12px;
    letter-spacing: 0.02em;
  }
  .service-desc {
    font-size: 14px;
    color: rgba(240,240,240,0.55);
    line-height: 1.7;
  }
  .service-card.featured .service-desc { color: rgba(255,255,255,0.75); }
  .service-arrow {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: var(--font-ui);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--red);
    margin-top: 20px;
  }
  .service-card.featured .service-arrow { color: var(--white); }

  /* ===== DIGITAL FITNESS ===== */
  .digital { padding: 120px 0; background: var(--black3); position: relative; overflow: hidden; }
  .digital::before {
    content: '';
    position: absolute;
    left: -200px;
    top: -200px;
    width: 600px;
    height: 600px;
    background: radial-gradient(circle, rgba(232,0,29,0.1) 0%, transparent 70%);
    pointer-events: none;
  }
  .digital-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }
  .digital-features {
    display: flex;
    flex-direction: column;
    gap: 0;
    margin-top: 40px;
  }
  .digital-feature {
    display: flex;
    gap: 20px;
    padding: 24px 0;
    border-bottom: 1px solid rgba(255,255,255,0.06);
    transition: all 0.3s;
    cursor: default;
  }
  .digital-feature:first-child { border-top: 1px solid rgba(255,255,255,0.06); }
  .digital-feature:hover .digital-feature-icon { background: var(--red); }
  .digital-feature-icon {
    width: 48px;
    height: 48px;
    background: rgba(232,0,29,0.1);
    border: 1px solid rgba(232,0,29,0.2);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    font-size: 20px;
    transition: background 0.3s;
  }
  .digital-feature-content {}
  .digital-feature-title {
    font-family: var(--font-ui);
    font-size: 15px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 6px;
  }
  .digital-feature-desc {
    font-size: 14px;
    color: rgba(240,240,240,0.55);
    line-height: 1.6;
  }
  .digital-visual {
    position: relative;
  }
  .digital-device {
    background: var(--gray1);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 4px;
    padding: 32px;
    position: relative;
    overflow: hidden;
  }
  .digital-device::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(to right, var(--red), transparent);
  }
  .device-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 32px;
  }
  .device-label {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text-muted);
  }
  .device-status {
    display: flex;
    align-items: center;
    gap: 6px;
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 600;
    color: #22c55e;
  }
  .device-status-dot {
    width: 6px;
    height: 6px;
    background: #22c55e;
    border-radius: 50%;
    animation: blink 2s infinite;
  }
  .bio-age-widget {
    text-align: center;
    padding: 40px 20px;
    background: rgba(232,0,29,0.05);
    border: 1px solid rgba(232,0,29,0.15);
    margin-bottom: 24px;
  }
  .bio-age-label {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 12px;
  }
  .bio-age-num {
    font-family: var(--font-display);
    font-size: 80px;
    line-height: 1;
    color: var(--red);
  }
  .bio-age-sub {
    font-family: var(--font-ui);
    font-size: 12px;
    color: rgba(255,255,255,0.5);
    margin-top: 8px;
  }
  .progress-bars {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .progress-item {}
  .progress-top {
    display: flex;
    justify-content: space-between;
    margin-bottom: 6px;
    font-family: var(--font-ui);
    font-size: 12px;
    font-weight: 600;
  }
  .progress-name { color: var(--text-muted); }
  .progress-val { color: var(--white); }
  .progress-bar {
    height: 4px;
    background: rgba(255,255,255,0.08);
    border-radius: 2px;
    overflow: hidden;
  }
  .progress-fill {
    height: 100%;
    background: linear-gradient(to right, var(--red), #ff4458);
    border-radius: 2px;
    animation: fillBar 1.5s ease-out both;
  }
  @keyframes fillBar {
    from { width: 0 !important; }
  }

  /* ===== PRICING ===== */
  .pricing { padding: 120px 0; background: var(--black2); }
  .pricing-header { text-align: center; margin-bottom: 64px; }
  .pricing-header .section-title { margin-bottom: 16px; }
  .pricing-header p {
    font-size: 16px;
    color: var(--text-muted);
    max-width: 480px;
    margin: 0 auto;
  }
  .pricing-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    position: relative;
  }
  .pricing-card {
    background: var(--black3);
    padding: 40px 32px;
    position: relative;
    overflow: hidden;
    border: 1px solid rgba(255,255,255,0.05);
    transition: all 0.3s;
  }
  .pricing-card:hover { border-color: rgba(232,0,29,0.2); }
  .pricing-card.popular {
    background: var(--black);
    border-color: var(--red);
    transform: scale(1.03);
    z-index: 2;
  }
  .popular-badge {
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    background: var(--red);
    font-family: var(--font-ui);
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--white);
    padding: 6px 20px;
  }
  .pricing-plan-name {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 24px;
    margin-top: 12px;
  }
  .pricing-card.popular .pricing-plan-name { margin-top: 24px; }
  .pricing-price {
    display: flex;
    align-items: flex-start;
    gap: 4px;
    margin-bottom: 8px;
  }
  .pricing-currency {
    font-family: var(--font-display);
    font-size: 28px;
    color: var(--text-muted);
    margin-top: 8px;
  }
  .pricing-amount {
    font-family: var(--font-display);
    font-size: 72px;
    line-height: 0.9;
    color: var(--white);
  }
  .pricing-card.popular .pricing-amount { color: var(--red); }
  .pricing-period {
    font-family: var(--font-ui);
    font-size: 12px;
    color: var(--text-muted);
    align-self: flex-end;
    margin-bottom: 4px;
  }
  .pricing-tagline {
    font-size: 13px;
    color: var(--text-muted);
    margin-bottom: 32px;
    line-height: 1.5;
  }
  .pricing-divider {
    height: 1px;
    background: rgba(255,255,255,0.06);
    margin-bottom: 28px;
  }
  .pricing-features {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 36px;
  }
  .pricing-features li {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 14px;
    color: rgba(240,240,240,0.7);
  }
  .pricing-features li .check {
    width: 18px;
    height: 18px;
    background: rgba(232,0,29,0.1);
    border: 1px solid rgba(232,0,29,0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 10px;
    color: var(--red);
    flex-shrink: 0;
  }
  .pricing-features li .cross {
    width: 18px;
    height: 18px;
    background: rgba(255,255,255,0.03);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 10px;
    color: var(--text-muted);
    flex-shrink: 0;
  }
  .pricing-features li.muted { color: var(--text-muted); }
  .pricing-note {
    text-align: center;
    margin-top: 40px;
    font-size: 13px;
    color: var(--text-muted);
  }

  /* ===== TESTIMONIALS ===== */
  .testimonials { padding: 120px 0; background: var(--black); overflow: hidden; }
  .testimonials-header { margin-bottom: 64px; }
  .testimonials-track {
    display: flex;
    gap: 24px;
    overflow-x: auto;
    scrollbar-width: none;
    padding-bottom: 16px;
  }
  .testimonials-track::-webkit-scrollbar { display: none; }
  .testimonial-card {
    background: var(--black2);
    border: 1px solid rgba(255,255,255,0.06);
    padding: 36px 32px;
    min-width: 360px;
    max-width: 360px;
    position: relative;
    flex-shrink: 0;
    transition: border-color 0.3s;
  }
  .testimonial-card:hover { border-color: rgba(232,0,29,0.25); }
  .testimonial-stars {
    display: flex;
    gap: 3px;
    margin-bottom: 20px;
  }
  .star { color: var(--red); font-size: 14px; }
  .testimonial-text {
    font-size: 15px;
    color: rgba(240,240,240,0.75);
    line-height: 1.75;
    margin-bottom: 28px;
    font-style: italic;
  }
  .testimonial-author {
    display: flex;
    align-items: center;
    gap: 14px;
  }
  .testimonial-avatar {
    width: 44px;
    height: 44px;
    background: var(--gray2);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--font-display);
    font-size: 18px;
    color: var(--red);
    flex-shrink: 0;
  }
  .testimonial-name {
    font-family: var(--font-ui);
    font-size: 14px;
    font-weight: 700;
    color: var(--white);
  }
  .testimonial-meta {
    font-size: 12px;
    color: var(--text-muted);
    margin-top: 2px;
  }
  .testimonial-quote {
    position: absolute;
    top: 24px;
    right: 24px;
    font-family: var(--font-display);
    font-size: 80px;
    line-height: 1;
    color: rgba(232,0,29,0.08);
  }

  /* ===== TEAM ===== */
  .team { padding: 120px 0; background: var(--black3); }
  .team-header { margin-bottom: 64px; }
  .team-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2px;
  }
  .team-card {
    position: relative;
    overflow: hidden;
    cursor: pointer;
  }
  .team-img {
    width: 100%;
    aspect-ratio: 3/4;
    background: var(--gray1);
    position: relative;
    overflow: hidden;
  }
  .team-img-inner {
    width: 100%;
    height: 100%;
    background: linear-gradient(160deg, #1f1f1f, #0d0d0d);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 80px;
    opacity: 0.3;
    transition: transform 0.5s ease;
  }
  .team-card:hover .team-img-inner { transform: scale(1.08); }
  .team-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(to top, rgba(8,8,8,0.9) 30%, transparent 100%);
  }
  .team-info {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 24px;
  }
  .team-name {
    font-family: var(--font-ui);
    font-size: 16px;
    font-weight: 800;
    color: var(--white);
  }
  .team-role {
    font-family: var(--font-body);
    font-size: 12px;
    color: var(--red);
    margin-top: 4px;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  /* ===== FAQ ===== */
  .faq { padding: 120px 0; background: var(--black2); }
  .faq-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }
  .faq-left {}
  .faq-list {
    display: flex;
    flex-direction: column;
    gap: 0;
  }
  .faq-item {
    border-bottom: 1px solid rgba(255,255,255,0.06);
    overflow: hidden;
  }
  .faq-question {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 22px 0;
    cursor: pointer;
    gap: 20px;
  }
  .faq-q-text {
    font-family: var(--font-ui);
    font-size: 15px;
    font-weight: 600;
    color: var(--white);
    line-height: 1.4;
  }
  .faq-icon {
    width: 28px;
    height: 28px;
    background: rgba(232,0,29,0.1);
    border: 1px solid rgba(232,0,29,0.2);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    font-size: 16px;
    color: var(--red);
    transition: all 0.3s;
  }
  .faq-item.open .faq-icon {
    background: var(--red);
    color: var(--white);
    transform: rotate(45deg);
  }
  .faq-answer {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.4s ease;
  }
  .faq-item.open .faq-answer { max-height: 200px; }
  .faq-answer-inner {
    padding: 0 0 20px;
    font-size: 14px;
    color: rgba(240,240,240,0.6);
    line-height: 1.75;
  }
  .faq-cta-box {
    background: var(--black3);
    border: 1px solid rgba(255,255,255,0.06);
    padding: 48px 40px;
    position: sticky;
    top: 100px;
  }
  .faq-cta-box .section-title { font-size: 48px; margin-bottom: 16px; }
  .faq-cta-box p {
    font-size: 15px;
    color: var(--text-muted);
    line-height: 1.7;
    margin-bottom: 32px;
  }
  .faq-cta-info {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-top: 32px;
    padding-top: 32px;
    border-top: 1px solid rgba(255,255,255,0.06);
  }
  .faq-info-item {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 14px;
    color: rgba(240,240,240,0.65);
  }
  .faq-info-icon { color: var(--red); font-size: 16px; width: 20px; text-align: center; }

  /* ===== CONTACT ===== */
  .contact { padding: 120px 0; background: var(--black); }
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }
  .contact-info {}
  .contact-body {
    font-size: 16px;
    color: rgba(240,240,240,0.6);
    line-height: 1.75;
    margin: 24px 0 48px;
  }
  .contact-details {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  .contact-detail {
    display: flex;
    gap: 16px;
    align-items: flex-start;
  }
  .contact-detail-icon {
    width: 44px;
    height: 44px;
    background: rgba(232,0,29,0.1);
    border: 1px solid rgba(232,0,29,0.2);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    flex-shrink: 0;
  }
  .contact-detail-label {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 4px;
  }
  .contact-detail-value {
    font-size: 15px;
    color: var(--white);
  }
  .contact-form {}
  .form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 16px;
  }
  .form-group { display: flex; flex-direction: column; gap: 8px; margin-bottom: 16px; }
  .form-label {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text-muted);
  }
  .form-input {
    background: var(--black2);
    border: 1px solid rgba(255,255,255,0.08);
    color: var(--white);
    font-family: var(--font-body);
    font-size: 15px;
    padding: 14px 16px;
    outline: none;
    transition: border-color 0.2s;
    width: 100%;
    appearance: none;
    -webkit-appearance: none;
  }
  .form-input:focus { border-color: var(--red); }
  .form-input::placeholder { color: rgba(240,240,240,0.2); }
  textarea.form-input { resize: vertical; min-height: 120px; }
  .form-select {
    background: var(--black2);
    border: 1px solid rgba(255,255,255,0.08);
    color: var(--white);
    font-family: var(--font-body);
    font-size: 15px;
    padding: 14px 16px;
    outline: none;
    transition: border-color 0.2s;
    width: 100%;
    cursor: pointer;
    appearance: none;
    -webkit-appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%23888' stroke-width='1.5' fill='none'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 16px center;
  }
  .form-select:focus { border-color: var(--red); }
  .form-select option { background: var(--black2); }
  .form-check {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    margin-bottom: 24px;
    cursor: pointer;
  }
  .form-check input[type="checkbox"] {
    width: 18px;
    height: 18px;
    flex-shrink: 0;
    accent-color: var(--red);
    cursor: pointer;
    margin-top: 2px;
  }
  .form-check-label {
    font-size: 13px;
    color: var(--text-muted);
    line-height: 1.5;
  }
  .form-check-label a { color: var(--red); }

  /* ===== OPENING HOURS ===== */
  .hours-strip {
    background: var(--black3);
    padding: 60px 0;
    border-top: 1px solid rgba(255,255,255,0.05);
    border-bottom: 1px solid rgba(255,255,255,0.05);
  }
  .hours-grid {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 80px;
    align-items: center;
  }
  .hours-label-wrap {}
  .hours-title {
    font-family: var(--font-display);
    font-size: 48px;
    color: var(--white);
    line-height: 0.95;
    margin-top: 12px;
  }
  .hours-table {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    gap: 2px;
  }
  .hours-day {
    background: var(--gray1);
    padding: 16px 12px;
    text-align: center;
    border-top: 2px solid transparent;
    transition: all 0.2s;
  }
  .hours-day.today { border-top-color: var(--red); background: rgba(232,0,29,0.08); }
  .hours-day-name {
    font-family: var(--font-ui);
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 8px;
  }
  .hours-day.today .hours-day-name { color: var(--red); }
  .hours-time {
    font-family: var(--font-ui);
    font-size: 12px;
    font-weight: 600;
    color: var(--white);
    line-height: 1.4;
  }

  /* ===== MAP ===== */
  .map-section { height: 400px; background: var(--gray1); position: relative; overflow: hidden; }
  .map-placeholder {
    width: 100%;
    height: 100%;
    background: 
      linear-gradient(rgba(22,22,22,0.8), rgba(22,22,22,0.8)),
      repeating-linear-gradient(0deg, transparent, transparent 40px, rgba(255,255,255,0.02) 40px, rgba(255,255,255,0.02) 41px),
      repeating-linear-gradient(90deg, transparent, transparent 40px, rgba(255,255,255,0.02) 40px, rgba(255,255,255,0.02) 41px);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 16px;
  }
  .map-pin {
    font-size: 48px;
    animation: bounce 2s ease infinite;
  }
  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
  }
  .map-address {
    font-family: var(--font-ui);
    font-size: 16px;
    font-weight: 600;
    color: var(--white);
    text-align: center;
  }
  .map-address-sub {
    font-size: 13px;
    color: var(--text-muted);
    text-align: center;
    margin-top: 4px;
  }
  .map-cta-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--red);
    color: white;
    font-family: var(--font-ui);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 12px 24px;
    margin-top: 8px;
    cursor: pointer;
    transition: background 0.2s;
  }
  .map-cta-btn:hover { background: var(--red-dark); }

  /* ===== FOOTER ===== */
  footer {
    background: var(--black2);
    padding: 80px 0 0;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 48px;
    margin-bottom: 64px;
  }
  .footer-brand {}
  .footer-logo {
    font-family: var(--font-display);
    font-size: 32px;
    letter-spacing: 0.08em;
    color: var(--white);
    margin-bottom: 16px;
  }
  .footer-logo span { color: var(--red); }
  .footer-desc {
    font-size: 14px;
    color: var(--text-muted);
    line-height: 1.75;
    max-width: 280px;
  }
  .footer-social {
    display: flex;
    gap: 8px;
    margin-top: 24px;
  }
  .footer-social-btn {
    width: 36px;
    height: 36px;
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 15px;
    cursor: pointer;
    transition: all 0.2s;
  }
  .footer-social-btn:hover { background: var(--red); border-color: var(--red); }
  .footer-col-title {
    font-family: var(--font-ui);
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--white);
    margin-bottom: 20px;
  }
  .footer-links {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .footer-links a {
    font-size: 14px;
    color: var(--text-muted);
    transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--white); }
  .footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.05);
    padding: 24px 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 16px;
    flex-wrap: wrap;
  }
  .footer-bottom-text {
    font-size: 13px;
    color: var(--text-muted);
  }
  .footer-bottom-links {
    display: flex;
    gap: 24px;
  }
  .footer-bottom-links a {
    font-size: 13px;
    color: var(--text-muted);
    transition: color 0.2s;
  }
  .footer-bottom-links a:hover { color: var(--white); }

  /* ===== MOBILE NAV OVERLAY ===== */
  .mobile-menu {
    display: none;
    position: fixed;
    inset: 0;
    background: var(--black);
    z-index: 999;
    padding: 100px 24px 40px;
    flex-direction: column;
    gap: 8px;
  }
  .mobile-menu.open { display: flex; }
  .mobile-menu a {
    font-family: var(--font-display);
    font-size: 42px;
    letter-spacing: 0.04em;
    color: rgba(255,255,255,0.4);
    padding: 8px 0;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    transition: color 0.2s;
  }
  .mobile-menu a:hover { color: var(--white); }
  .mobile-close {
    position: absolute;
    top: 20px;
    right: 24px;
    font-size: 32px;
    cursor: pointer;
    color: var(--text-muted);
    background: none;
    border: none;
    line-height: 1;
  }

  /* ===== SCROLL ANIMATIONS ===== */
  .reveal {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 1024px) {
    .about-grid,
    .digital-grid,
    .contact-grid,
    .faq-grid { grid-template-columns: 1fr; gap: 48px; }
    .services-grid { grid-template-columns: 1fr 1fr; }
    .pricing-grid { grid-template-columns: 1fr; }
    .pricing-card.popular { transform: none; }
    .team-grid { grid-template-columns: 1fr 1fr; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .hours-grid { grid-template-columns: 1fr; gap: 32px; }
    .hours-table { grid-template-columns: repeat(4, 1fr); }
  }
  @media (max-width: 768px) {
    .nav-links, .nav-cta { display: none; }
    .hamburger { display: flex; }
    .hero-title { font-size: 60px; }
    .hero-title-sub { font-size: 32px; }
    .hero-stats { gap: 24px; }
    .services-grid { grid-template-columns: 1fr; }
    .about-perks { grid-template-columns: 1fr; }
    .team-grid { grid-template-columns: 1fr 1fr; }
    .footer-grid { grid-template-columns: 1fr; }
    .hours-table { grid-template-columns: repeat(3, 1fr); }
    .form-row { grid-template-columns: 1fr; }
    .hero-scroll { display: none; }
    .testimonial-card { min-width: 300px; }
  }
</style>
</head>
<body>

<!-- ===== NAVBAR ===== -->
<nav id="navbar">
  <div class="nav-inner">
    <a href="#" class="nav-logo">APEX<span class="logo-accent">FIT</span></a>
    <ul class="nav-links">
      <li><a href="#about">Studio</a></li>
      <li><a href="#services">Leistungen</a></li>
      <li><a href="#pricing">Mitgliedschaft</a></li>
      <li><a href="#team">Team</a></li>
      <li><a href="#faq">FAQ</a></li>
      <li><a href="#contact">Kontakt</a></li>
    </ul>
    <div class="nav-cta">
      <a href="#contact" class="btn-outline" style="padding:11px 22px;font-size:12px;clip-path:polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 8px 100%, 0 calc(100% - 8px))"><span>Probetraining</span></a>
      <a href="#pricing" class="btn-primary" style="padding:11px 22px;font-size:12px;clip-path:polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 8px 100%, 0 calc(100% - 8px))"><span>Mitglied werden</span></a>
    </div>
    <div class="hamburger" onclick="toggleMenu()">
      <span></span><span></span><span></span>
    </div>
  </div>
</nav>

<!-- ===== MOBILE MENU ===== -->
<div class="mobile-menu" id="mobileMenu">
  <button class="mobile-close" onclick="toggleMenu()">✕</button>
  <a href="#about" onclick="toggleMenu()">Studio</a>
  <a href="#services" onclick="toggleMenu()">Leistungen</a>
  <a href="#pricing" onclick="toggleMenu()">Mitgliedschaft</a>
  <a href="#team" onclick="toggleMenu()">Team</a>
  <a href="#faq" onclick="toggleMenu()">FAQ</a>
  <a href="#contact" onclick="toggleMenu()">Kontakt</a>
</div>

<!-- ===== PROMO BANNER ===== -->
<div class="promo-banner" style="margin-top:72px;">
  <div class="promo-banner-inner">
    <span class="promo-banner-fire">🔥</span>
    <span class="promo-banner-text">SOMMERAKTION — Jetzt Mitglied werden & ersten Monat kostenlos trainieren!</span>
    <a href="#pricing" class="promo-banner-link">Jetzt sichern →</a>
  </div>
</div>

<!-- ===== HERO ===== -->
<section class="hero" style="margin-top:0;padding-top:80px;">
  <div class="hero-image-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-visual">
    <svg viewBox="0 0 400 600" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- Abstract athletic figure / dumbbell art -->
      <circle cx="200" cy="80" r="50" stroke="white" stroke-width="2"/>
      <line x1="200" y1="130" x2="200" y2="320" stroke="white" stroke-width="3"/>
      <line x1="200" y1="200" x2="100" y2="260" stroke="white" stroke-width="3"/>
      <line x1="200" y1="200" x2="300" y2="260" stroke="white" stroke-width="3"/>
      <line x1="200" y1="320" x2="140" y2="480" stroke="white" stroke-width="3"/>
      <line x1="200" y1="320" x2="260" y2="480" stroke="white" stroke-width="3"/>
      <!-- Dumbbell left -->
      <rect x="40" y="245" width="60" height="30" rx="4" stroke="white" stroke-width="2" fill="none"/>
      <rect x="20" y="238" width="20" height="44" rx="3" stroke="white" stroke-width="2" fill="none"/>
      <rect x="100" y="238" width="20" height="44" rx="3" stroke="white" stroke-width="2" fill="none"/>
      <!-- Dumbbell right -->
      <rect x="300" y="245" width="60" height="30" rx="4" stroke="white" stroke-width="2" fill="none"/>
      <rect x="280" y="238" width="20" height="44" rx="3" stroke="white" stroke-width="2" fill="none"/>
      <rect x="360" y="238" width="20" height="44" rx="3" stroke="white" stroke-width="2" fill="none"/>
      <!-- Ground -->
      <line x1="80" y1="520" x2="320" y2="520" stroke="white" stroke-width="2" opacity="0.3"/>
    </svg>
  </div>
  <div class="hero-glow"></div>
  <div class="hero-bg"></div>

  <div class="hero-content">
    <div class="hero-badge">
      <div class="hero-badge-dot"></div>
      <span>Bad Oeynhausen · Jetzt geöffnet</span>
    </div>
    <h1 class="hero-title">KEIN<br>LIMIT.</h1>
    <div class="hero-title-sub">NUR ERGEBNISSE.</div>
    <p class="hero-desc">
      Dein Premium-Fitnessstudio in Bad Oeynhausen. KI-basiertes Training, modernste Geräte, Wellness &amp; Sauna – alles an einem Ort. Für alle, die es ernst meinen.
    </p>
    <div class="hero-cta">
      <a href="#pricing" class="btn-primary"><span>Jetzt Mitglied werden</span><span>→</span></a>
      <a href="#contact" class="btn-outline"><span>Kostenlos Probetraining</span></a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="hero-stat-num">2<span>,4K</span></div>
        <div class="hero-stat-label">Aktive Mitglieder</div>
      </div>
      <div>
        <div class="hero-stat-num">150<span>+</span></div>
        <div class="hero-stat-label">Moderne Geräte</div>
      </div>
      <div>
        <div class="hero-stat-num">24<span>/7</span></div>
        <div class="hero-stat-label">Geöffnet</div>
      </div>
      <div>
        <div class="hero-stat-num">4<span>,8★</span></div>
        <div class="hero-stat-label">Google Bewertung</div>
      </div>
    </div>
  </div>

  <div class="hero-scroll">
    <span class="hero-scroll-text">Scroll</span>
    <div class="hero-scroll-line"></div>
  </div>
</section>

<!-- ===== FEATURES STRIP ===== -->
<div class="features-strip">
  <div class="features-strip-inner">
    <div class="features-strip-track" id="stripTrack">
      <div class="features-strip-item"><span class="features-strip-icon">⚡</span><span class="features-strip-label">KI-Training</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🏋️</span><span class="features-strip-label">150+ Geräte</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🧖</span><span class="features-strip-label">Sauna & Wellness</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">📊</span><span class="features-strip-label">BIO Age Tracking</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🕐</span><span class="features-strip-label">24/7 Geöffnet</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🏆</span><span class="features-strip-label">Zertifizierte Trainer</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">📱</span><span class="features-strip-label">App-Anbindung</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🚿</span><span class="features-strip-label">Umkleiden & Duschen</span></div>
      <!-- Duplicate for seamless loop -->
      <div class="features-strip-item"><span class="features-strip-icon">⚡</span><span class="features-strip-label">KI-Training</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🏋️</span><span class="features-strip-label">150+ Geräte</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🧖</span><span class="features-strip-label">Sauna & Wellness</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">📊</span><span class="features-strip-label">BIO Age Tracking</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🕐</span><span class="features-strip-label">24/7 Geöffnet</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🏆</span><span class="features-strip-label">Zertifizierte Trainer</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">📱</span><span class="features-strip-label">App-Anbindung</span></div>
      <div class="features-strip-item"><span class="features-strip-icon">🚿</span><span class="features-strip-label">Umkleiden & Duschen</span></div>
    </div>
  </div>
</div>

<!-- ===== ABOUT ===== -->
<section class="about" id="about">
  <div class="container">
    <div class="about-grid">
      <div class="about-image-wrap reveal">
        <div class="about-image-accent"></div>
        <div class="about-image-main">
          <div class="about-image-main-inner">
            <svg viewBox="0 0 300 400" fill="none" xmlns="http://www.w3.org/2000/svg">
              <!-- Stylized weight rack -->
              <rect x="20" y="80" width="260" height="8" rx="2" fill="white"/>
              <rect x="20" y="180" width="260" height="8" rx="2" fill="white"/>
              <rect x="20" y="280" width="260" height="8" rx="2" fill="white"/>
              <rect x="25" y="80" width="8" height="208" fill="white"/>
              <rect x="267" y="80" width="8" height="208" fill="white"/>
              <!-- Dumbbells on rack -->
              <circle cx="80" cy="76" r="16" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="130" cy="76" r="20" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="185" cy="76" r="14" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="230" cy="76" r="18" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="80" cy="176" r="20" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="140" cy="176" r="24" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="210" cy="176" r="16" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="90" cy="276" r="24" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="155" cy="276" r="28" stroke="white" stroke-width="2" fill="none"/>
              <circle cx="230" cy="276" r="20" stroke="white" stroke-width="2" fill="none"/>
              <!-- Floor line -->
              <line x1="0" y1="380" x2="300" y2="380" stroke="white" stroke-width="2" opacity="0.3"/>
            </svg>
          </div>
        </div>
        <div class="about-image-tag">
          <div class="about-image-tag-num">10+</div>
          <div class="about-image-tag-label">Jahre Erfahrung</div>
        </div>
      </div>
      <div class="about-text reveal reveal-delay-2">
        <div class="section-label">Über uns</div>
        <h2 class="section-title">DEIN STUDIO.<br><span>DEINE ZONE.</span></h2>
        <p class="about-body">
          Im APEX FIT Bad Oeynhausen triffst du auf eine Atmosphäre, die dich pusht. Mit über 150 modernen Trainingsgeräten, KI-gestützten EGYM-Systemen und zertifizierten Trainern begleiten wir dich auf deinem Weg – egal ob Einsteiger oder Profi.
        </p>
        <div class="about-perks">
          <div class="about-perk">
            <div class="about-perk-icon">💪</div>
            <div class="about-perk-text">150+ Geräte auf 2.000 m²</div>
          </div>
          <div class="about-perk">
            <div class="about-perk-icon">🤖</div>
            <div class="about-perk-text">KI-basiertes EGYM Training</div>
          </div>
          <div class="about-perk">
            <div class="about-perk-icon">🧖</div>
            <div class="about-perk-text">Sauna & Wellness Area</div>
          </div>
          <div class="about-perk">
            <div class="about-perk-icon">📋</div>
            <div class="about-perk-text">Persönlicher Trainingsplan</div>
          </div>
          <div class="about-perk">
            <div class="about-perk-icon">🔬</div>
            <div class="about-perk-text">Medizinische Körperanalyse</div>
          </div>
          <div class="about-perk">
            <div class="about-perk-icon">🅿️</div>
            <div class="about-perk-text">Kostenfreies Parken</div>
          </div>
        </div>
        <a href="#contact" class="btn-primary"><span>Jetzt Probetraining buchen</span><span>→</span></a>
      </div>
    </div>
  </div>
</section>

<!-- ===== SERVICES ===== -->
<section class="services" id="services">
  <div class="container">
    <div class="services-header">
      <div class="reveal">
        <div class="section-label">Leistungen</div>
        <h2 class="section-title">WAS WIR<br><span>BIETEN.</span></h2>
      </div>
      <a href="#pricing" class="btn-outline reveal">Alle Leistungen →</a>
    </div>
    <div class="services-grid">
      <div class="service-card reveal">
        <div class="service-num">01</div>
        <div class="service-icon">🏋️</div>
        <div class="service-title">Kraft & Ausdauer</div>
        <p class="service-desc">Modernste Geräte von Matrix, Life Fitness und EGYM für optimales Kraft- und Ausdauertraining. Für Anfänger und Fortgeschrittene.</p>
        <div class="service-arrow">Mehr erfahren →</div>
      </div>
      <div class="service-card featured reveal reveal-delay-1">
        <div class="service-num">02</div>
        <div class="service-icon">🤖</div>
        <div class="service-title">Digital Fitness Floor</div>
        <p class="service-desc">KI-gestützte EGYM-Geräte passen sich automatisch an dein Level an. 30 Minuten für maximale Ergebnisse – messbar durch deinen BIO Age.</p>
        <div class="service-arrow">Jetzt starten →</div>
      </div>
      <div class="service-card reveal reveal-delay-2">
        <div class="service-num">03</div>
        <div class="service-icon">🧘</div>
        <div class="service-title">Kurse & Gruppentraining</div>
        <p class="service-desc">Über 50 Kurse pro Woche: Yoga, Spinning, HIIT, Zumba und mehr. Gemeinsam stärker – in der Gruppe läuft es sich leichter.</p>
        <div class="service-arrow">Kursplan ansehen →</div>
      </div>
      <div class="service-card reveal">
        <div class="service-num">04</div>
        <div class="service-icon">🧖</div>
        <div class="service-title">Wellness & Sauna</div>
        <p class="service-desc">Regeneriere nach dem Training in unserer Wellness Area mit finnischer Sauna, Dampfbad und Ruhebereich. Inklusive in der Premium-Mitgliedschaft.</p>
        <div class="service-arrow">Mehr erfahren →</div>
      </div>
      <div class="service-card reveal reveal-delay-1">
        <div class="service-num">05</div>
        <div class="service-icon">📊</div>
        <div class="service-title">Körperanalyse & Coaching</div>
        <p class="service-desc">Professionelle InBody-Körperanalyse und persönliche Trainingsplanerstellung durch unsere zertifizierten Trainer – fundiert und individuell.</p>
        <div class="service-arrow">Beratung buchen →</div>
      </div>
      <div class="service-card reveal reveal-delay-2">
        <div class="service-num">06</div>
        <div class="service-icon">🥤</div>
        <div class="service-title">Supplement & Juice Bar</div>
        <p class="service-desc">Frische Protein-Shakes, Smoothies und hochwertige Supplements direkt im Studio. Die optimale Ergänzung zu deinem Training.</p>
        <div class="service-arrow">Mehr erfahren →</div>
      </div>
    </div>
  </div>
</section>

<!-- ===== DIGITAL FITNESS ===== -->
<section class="digital" id="digital">
  <div class="container">
    <div class="digital-grid">
      <div>
        <div class="section-label reveal">Digital Fitness Floor</div>
        <h2 class="section-title reveal">SMARTER<br><span>TRAINIEREN.</span></h2>
        <div class="digital-features">
          <div class="digital-feature reveal">
            <div class="digital-feature-icon">⏱️</div>
            <div class="digital-feature-content">
              <div class="digital-feature-title">30 Minuten – Maximum Wirkung</div>
              <p class="digital-feature-desc">Effektives Ganzkörper-Training in nur einer halben Stunde. Ideal für Menschen mit vollem Alltag, die keine Kompromisse bei den Ergebnissen machen.</p>
            </div>
          </div>
          <div class="digital-feature reveal reveal-delay-1">
            <div class="digital-feature-icon">📈</div>
            <div class="digital-feature-content">
              <div class="digital-feature-title">BIO Age Tracking</div>
              <p class="digital-feature-desc">Dein biologisches Alter zeigt dir messbar, wie sich dein Training auf deine Gesundheit auswirkt. Motivierendes, klares Feedback in Echtzeit.</p>
            </div>
          </div>
          <div class="digital-feature reveal reveal-delay-2">
            <div class="digital-feature-icon">🤖</div>
            <div class="digital-feature-content">
              <div class="digital-feature-title">Automatische Anpassung</div>
              <p class="digital-feature-desc">Die EGYM-Geräte stellen sich per RFID-Chip automatisch auf dein Profil ein – kein manuelles Einstellen, einfach einsteigen und loslegen.</p>
            </div>
          </div>
          <div class="digital-feature reveal reveal-delay-3">
            <div class="digital-feature-icon">🎯</div>
            <div class="digital-feature-content">
              <div class="digital-feature-title">Für jeden geeignet</div>
              <p class="digital-feature-desc">Ob Einsteiger oder Profi – das System erkennt dein Level und passt Gewicht, Tempo und Übungsauswahl automatisch an. Null Lernkurve.</p>
            </div>
          </div>
        </div>
      </div>
      <div class="digital-visual reveal">
        <div class="digital-device">
          <div class="device-header">
            <span class="device-label">EGYM Dashboard</span>
            <div class="device-status"><div class="device-status-dot"></div>Live</div>
          </div>
          <div class="bio-age-widget">
            <div class="bio-age-label">Dein BIO Age</div>
            <div class="bio-age-num">28</div>
            <div class="bio-age-sub">Chronologisches Alter: 35 · ↓ 7 Jahre verbessert</div>
          </div>
          <div class="progress-bars">
            <div class="progress-item">
              <div class="progress-top"><span class="progress-name">Kraft</span><span class="progress-val">87%</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:87%"></div></div>
            </div>
            <div class="progress-item">
              <div class="progress-top"><span class="progress-name">Ausdauer</span><span class="progress-val">74%</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:74%"></div></div>
            </div>
            <div class="progress-item">
              <div class="progress-top"><span class="progress-name">Beweglichkeit</span><span class="progress-val">65%</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:65%"></div></div>
            </div>
            <div class="progress-item">
              <div class="progress-top"><span class="progress-name">Regeneration</span><span class="progress-val">91%</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:91%"></div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== PRICING ===== -->
<section class="pricing" id="pricing">
  <div class="container">
    <div class="pricing-header reveal">
      <div class="section-label">Mitgliedschaft</div>
      <h2 class="section-title">DEIN <span>PLAN.</span></h2>
      <p>Keine versteckten Kosten. Transparent, fair und flexibel – für jeden das passende Paket.</p>
    </div>
    <div class="pricing-grid">
      <!-- BASIC -->
      <div class="pricing-card reveal">
        <div class="pricing-plan-name">Basic</div>
        <div class="pricing-price">
          <span class="pricing-currency">€</span>
          <span class="pricing-amount">19</span>
          <span class="pricing-period">,90 / Monat</span>
        </div>
        <p class="pricing-tagline">Perfekt für den Einstieg. Alle wichtigen Bereiche, kein Schnickschnack.</p>
        <div class="pricing-divider"></div>
        <ul class="pricing-features">
          <li><span class="check">✓</span> Gerätebereich unbegrenzt</li>
          <li><span class="check">✓</span> Umkleiden & Duschen</li>
          <li><span class="check">✓</span> Basis-Trainingsplan</li>
          <li><span class="check">✓</span> App-Zugang</li>
          <li class="muted"><span class="cross">–</span> Sauna & Wellness</li>
          <li class="muted"><span class="cross">–</span> Kurse & Gruppentraining</li>
          <li class="muted"><span class="cross">–</span> Digital Fitness Floor</li>
          <li class="muted"><span class="cross">–</span> Körperanalyse</li>
        </ul>
        <a href="#contact" class="btn-outline" style="width:100%;justify-content:center;"><span>Auswählen</span></a>
      </div>
      <!-- PREMIUM (POPULAR) -->
      <div class="pricing-card popular reveal reveal-delay-1">
        <div class="popular-badge">Beliebteste Wahl</div>
        <div class="pricing-plan-name">Black Label</div>
        <div class="pricing-price">
          <span class="pricing-currency">€</span>
          <span class="pricing-amount">29</span>
          <span class="pricing-period">,90 / Monat</span>
        </div>
        <p class="pricing-tagline">Das komplette Paket. Für Menschen, die Ergebnisse wollen.</p>
        <div class="pricing-divider"></div>
        <ul class="pricing-features">
          <li><span class="check">✓</span> Alle Basic-Leistungen</li>
          <li><span class="check">✓</span> Sauna & Wellness Area</li>
          <li><span class="check">✓</span> 50+ Kurse pro Woche</li>
          <li><span class="check">✓</span> Digital Fitness Floor</li>
          <li><span class="check">✓</span> BIO Age Tracking</li>
          <li><span class="check">✓</span> Körperanalyse (1x / Quartal)</li>
          <li><span class="check">✓</span> Persönlicher Trainingsplan</li>
          <li><span class="check">✓</span> Bundesweite Studionutzung</li>
        </ul>
        <a href="#contact" class="btn-primary" style="width:100%;justify-content:center;"><span>Jetzt starten</span></a>
      </div>
      <!-- ELITE -->
      <div class="pricing-card reveal reveal-delay-2">
        <div class="pricing-plan-name">Elite Coaching</div>
        <div class="pricing-price">
          <span class="pricing-currency">€</span>
          <span class="pricing-amount">59</span>
          <span class="pricing-period">,90 / Monat</span>
        </div>
        <p class="pricing-tagline">1-on-1 Coaching, maximale Betreuung und schnellste Ergebnisse.</p>
        <div class="pricing-divider"></div>
        <ul class="pricing-features">
          <li><span class="check">✓</span> Alle Black Label-Leistungen</li>
          <li><span class="check">✓</span> 4x / Monat Personal Training</li>
          <li><span class="check">✓</span> Monatliche Körperanalyse</li>
          <li><span class="check">✓</span> Ernährungsberatung</li>
          <li><span class="check">✓</span> Priorisierte Trainer-Betreuung</li>
          <li><span class="check">✓</span> Supplement-Paket inklusive</li>
          <li><span class="check">✓</span> Exklusiver Workout-Plan</li>
          <li><span class="check">✓</span> Whatsapp-Support</li>
        </ul>
        <a href="#contact" class="btn-outline" style="width:100%;justify-content:center;"><span>Beratung anfordern</span></a>
      </div>
    </div>
    <p class="pricing-note">Alle Preise inkl. MwSt. · Mindestlaufzeit 12 Monate · Kündigung jederzeit zum Ende der Laufzeit möglich<br>Einmalige Verwaltungspauschale 29,90 € · Kein versteckter Vertrag</p>
  </div>
</section>

<!-- ===== TESTIMONIALS ===== -->
<section class="testimonials">
  <div class="container">
    <div class="testimonials-header reveal">
      <div class="section-label">Bewertungen</div>
      <h2 class="section-title">WAS UNSERE<br><span>MITGLIEDER SAGEN.</span></h2>
    </div>
    <div class="testimonials-track">
      <div class="testimonial-card">
        <div class="testimonial-quote">"</div>
        <div class="testimonial-stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="testimonial-text">Das APEX FIT hat mein Leben verändert. Der Digital Fitness Floor ist unglaublich – in 30 Minuten mehr Ergebnisse als früher in 90 Minuten. Mein BIO Age hat sich in 6 Monaten um 4 Jahre verbessert!</p>
        <div class="testimonial-author">
          <div class="testimonial-avatar">M</div>
          <div>
            <div class="testimonial-name">Marco S.</div>
            <div class="testimonial-meta">Mitglied seit 2022 · Black Label</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="testimonial-quote">"</div>
        <div class="testimonial-stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="testimonial-text">Als Mutter von zwei Kindern habe ich wenig Zeit. Hier bekomme ich in 30 Minuten ein komplettes Training hin, das sich lohnt. Das Team ist super freundlich und die Sauna danach ist das Beste!</p>
        <div class="testimonial-author">
          <div class="testimonial-avatar">S</div>
          <div>
            <div class="testimonial-name">Sandra K.</div>
            <div class="testimonial-meta">Mitglied seit 2023 · Black Label</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="testimonial-quote">"</div>
        <div class="testimonial-stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="testimonial-text">Ich war sehr skeptisch wegen dem KI-Training, aber nach 3 Monaten bin ich absolut überzeugt. Die Geräte führen einen wirklich durch alles durch. Kein anderes Studio in Bad Oeynhausen kommt ran.</p>
        <div class="testimonial-author">
          <div class="testimonial-avatar">T</div>
          <div>
            <div class="testimonial-name">Thomas W.</div>
            <div class="testimonial-meta">Mitglied seit 2021 · Elite Coaching</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="testimonial-quote">"</div>
        <div class="testimonial-stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="testimonial-text">Sauberkeit, Ausstattung und Service sind top. Ich trainiere hier seit über 2 Jahren und habe noch nie eine negative Erfahrung gemacht. Parking ist immer verfügbar, die Trainer sind immer ansprechbar.</p>
        <div class="testimonial-author">
          <div class="testimonial-avatar">L</div>
          <div>
            <div class="testimonial-name">Laura B.</div>
            <div class="testimonial-meta">Mitglied seit 2020 · Black Label</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="testimonial-quote">"</div>
        <div class="testimonial-stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="testimonial-text">Mein Personal Trainer hat mir nicht nur gezeigt wie man richtig trainiert, sondern auch wie man isst. -12 kg in 4 Monaten – ich bin fassungslos und überglücklich. Das Elite-Paket ist jeden Cent wert.</p>
        <div class="testimonial-author">
          <div class="testimonial-avatar">F</div>
          <div>
            <div class="testimonial-name">Felix D.</div>
            <div class="testimonial-meta">Mitglied seit 2023 · Elite Coaching</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== TEAM ===== -->
<section class="team" id="team">
  <div class="container">
    <div class="team-header">
      <div class="reveal">
        <div class="section-label">Das Team</div>
        <h2 class="section-title">DEINE <span>TRAINER.</span></h2>
      </div>
    </div>
    <div class="team-grid">
      <div class="team-card reveal">
        <div class="team-img">
          <div class="team-img-inner">💪</div>
          <div class="team-overlay"></div>
        </div>
        <div class="team-info">
          <div class="team-name">Max Berger</div>
          <div class="team-role">Head Coach · Kraft & Kondition</div>
        </div>
      </div>
      <div class="team-card reveal reveal-delay-1">
        <div class="team-img">
          <div class="team-img-inner">🧘</div>
          <div class="team-overlay"></div>
        </div>
        <div class="team-info">
          <div class="team-name">Lena Hoffmann</div>
          <div class="team-role">Yoga & Wellness Coach</div>
        </div>
      </div>
      <div class="team-card reveal reveal-delay-2">
        <div class="team-img">
          <div class="team-img-inner">🏃</div>
          <div class="team-overlay"></div>
        </div>
        <div class="team-info">
          <div class="team-name">Jonas Müller</div>
          <div class="team-role">Ausdauer & HIIT Trainer</div>
        </div>
      </div>
      <div class="team-card reveal reveal-delay-3">
        <div class="team-img">
          <div class="team-img-inner">🥗</div>
          <div class="team-overlay"></div>
        </div>
        <div class="team-info">
          <div class="team-name">Julia Schneider</div>
          <div class="team-role">Ernährungsberatung & Coaching</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== OPENING HOURS ===== -->
<section class="hours-strip">
  <div class="container">
    <div class="hours-grid">
      <div>
        <div class="section-label">Öffnungszeiten</div>
        <div class="hours-title">IMMER<br>FÜR<br>DICH DA.</div>
      </div>
      <div class="hours-table">
        <div class="hours-day">
          <div class="hours-day-name">Mo</div>
          <div class="hours-time">06:00<br>–<br>23:00</div>
        </div>
        <div class="hours-day">
          <div class="hours-day-name">Di</div>
          <div class="hours-time">06:00<br>–<br>23:00</div>
        </div>
        <div class="hours-day">
          <div class="hours-day-name">Mi</div>
          <div class="hours-time">06:00<br>–<br>23:00</div>
        </div>
        <div class="hours-day">
          <div class="hours-day-name">Do</div>
          <div class="hours-time">06:00<br>–<br>23:00</div>
        </div>
        <div class="hours-day today">
          <div class="hours-day-name">Fr ◀</div>
          <div class="hours-time">06:00<br>–<br>22:00</div>
        </div>
        <div class="hours-day">
          <div class="hours-day-name">Sa</div>
          <div class="hours-time">08:00<br>–<br>20:00</div>
        </div>
        <div class="hours-day">
          <div class="hours-day-name">So</div>
          <div class="hours-time">08:00<br>–<br>18:00</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== FAQ ===== -->
<section class="faq" id="faq">
  <div class="container">
    <div class="faq-grid">
      <div class="faq-left reveal">
        <div class="section-label">FAQ</div>
        <h2 class="section-title" style="margin-bottom:40px;">HÄUFIGE<br><span>FRAGEN.</span></h2>
        <div class="faq-list">
          <div class="faq-item open">
            <div class="faq-question" onclick="toggleFaq(this)">
              <span class="faq-q-text">Kann ich das Studio vorher kostenlos testen?</span>
              <div class="faq-icon">+</div>
            </div>
            <div class="faq-answer">
              <div class="faq-answer-inner">Ja! Wir bieten jedem Interessenten ein kostenloses Probetraining an. Einfach online buchen oder direkt an der Rezeption vorbeikommen. Kein Druck, keine Verpflichtung.</div>
            </div>
          </div>
          <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">
              <span class="faq-q-text">Wie lange läuft der Vertrag?</span>
              <div class="faq-icon">+</div>
            </div>
            <div class="faq-answer">
              <div class="faq-answer-inner">Die Mindestlaufzeit beträgt 12 Monate, danach monatlich kündbar. Bei Aktionsangeboten gelten ggf. abweichende Konditionen – diese sind immer transparent ausgewiesen.</div>
            </div>
          </div>
          <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">
              <span class="faq-q-text">Was ist der Digital Fitness Floor?</span>
              <div class="faq-icon">+</div>
            </div>
            <div class="faq-answer">
              <div class="faq-answer-inner">Der Digital Fitness Floor ist ein Zirkel aus KI-gestützten EGYM-Geräten, die sich per RFID automatisch auf dein Profil einstellen. Du sparst Zeit, trainierst effizienter und bekommst messbare Ergebnisse über dein BIO Age.</div>
            </div>
          </div>
          <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">
              <span class="faq-q-text">Gibt es Parkplätze?</span>
              <div class="faq-icon">+</div>
            </div>
            <div class="faq-answer">
              <div class="faq-answer-inner">Ja, direkt am Studio stehen ausreichend kostenfreie Parkplätze für unsere Mitglieder zur Verfügung. Kein Stress beim Ankommen.</div>
            </div>
          </div>
          <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">
              <span class="faq-q-text">Kann ich meine Mitgliedschaft pausieren?</span>
              <div class="faq-icon">+</div>
            </div>
            <div class="faq-answer">
              <div class="faq-answer-inner">Ja, bei nachgewiesenen Gründen (z.B. Krankheit, Schwangerschaft, beruflicher Auslandsaufenthalt) ist eine Pausierung der Mitgliedschaft möglich. Sprich uns einfach an.</div>
            </div>
          </div>
          <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">
              <span class="faq-q-text">Darf ich auch andere Studios nutzen?</span>
              <div class="faq-icon">+</div>
            </div>
            <div class="faq-answer">
              <div class="faq-answer-inner">Mit der Black Label und Elite Mitgliedschaft hast du bundesweiten Zugang zu allen APEX FIT Partnerstudios. So bist du auch auf Reisen nie ohne Training.</div>
            </div>
          </div>
        </div>
      </div>
      <div class="reveal reveal-delay-2">
        <div class="faq-cta-box">
          <div class="section-label">Jetzt starten</div>
          <h3 class="section-title">STARTE<br><span>HEUTE.</span></h3>
          <p>Warte nicht auf den perfekten Moment. Der perfekte Moment ist jetzt. Sichere dir deinen kostenlosen Probetraining-Termin.</p>
          <a href="#contact" class="btn-primary" style="width:100%;justify-content:center;"><span>Probetraining buchen</span><span>→</span></a>
          <div class="faq-cta-info">
            <div class="faq-info-item"><span class="faq-info-icon">📍</span> Musterstraße 12, 32545 Bad Oeynhausen</div>
            <div class="faq-info-item"><span class="faq-info-icon">📞</span> 05731 / 123 456 0</div>
            <div class="faq-info-item"><span class="faq-info-icon">📧</span> info@apexfit-badoeynhausen.de</div>
            <div class="faq-info-item"><span class="faq-info-icon">⏰</span> Mo–Fr 06:00–23:00 Uhr</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== CONTACT ===== -->
<section class="contact" id="contact">
  <div class="container">
    <div class="contact-grid">
      <div class="reveal">
        <div class="section-label">Kontakt</div>
        <h2 class="section-title">LASS UNS<br><span>REDEN.</span></h2>
        <p class="contact-body">
          Du hast Fragen, willst ein Probetraining buchen oder einfach reinschnuppern? Schreib uns oder komm direkt vorbei. Wir freuen uns auf dich.
        </p>
        <div class="contact-details">
          <div class="contact-detail">
            <div class="contact-detail-icon">📍</div>
            <div>
              <div class="contact-detail-label">Adresse</div>
              <div class="contact-detail-value">Musterstraße 12<br>32545 Bad Oeynhausen</div>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">📞</div>
            <div>
              <div class="contact-detail-label">Telefon</div>
              <div class="contact-detail-value">05731 / 123 456 0</div>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">📧</div>
            <div>
              <div class="contact-detail-label">E-Mail</div>
              <div class="contact-detail-value">info@apexfit-badoeynhausen.de</div>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">📱</div>
            <div>
              <div class="contact-detail-label">Social Media</div>
              <div class="contact-detail-value">@apexfit.badoeynhausen</div>
            </div>
          </div>
        </div>
      </div>
      <div class="contact-form reveal reveal-delay-2">
        <div class="form-row">
          <div class="form-group">
            <label class="form-label">Vorname</label>
            <input type="text" class="form-input" placeholder="Max" />
          </div>
          <div class="form-group">
            <label class="form-label">Nachname</label>
            <input type="text" class="form-input" placeholder="Mustermann" />
          </div>
        </div>
        <div class="form-group">
          <label class="form-label">E-Mail</label>
          <input type="email" class="form-input" placeholder="max@example.de" />
        </div>
        <div class="form-group">
          <label class="form-label">Telefon (optional)</label>
          <input type="tel" class="form-input" placeholder="0175 123 456 78" />
        </div>
        <div class="form-group">
          <label class="form-label">Ich interessiere mich für</label>
          <select class="form-select">
            <option value="">Bitte wählen...</option>
            <option>Kostenloses Probetraining</option>
            <option>Mitgliedschaft Basic</option>
            <option>Mitgliedschaft Black Label</option>
            <option>Elite Coaching</option>
            <option>Körperanalyse</option>
            <option>Allgemeine Anfrage</option>
          </select>
        </div>
        <div class="form-group">
          <label class="form-label">Nachricht</label>
          <textarea class="form-input" placeholder="Deine Nachricht an uns..."></textarea>
        </div>
        <label class="form-check">
          <input type="checkbox" />
          <span class="form-check-label">Ich stimme der <a href="#">Datenschutzerklärung</a> zu und bin damit einverstanden, kontaktiert zu werden.</span>
        </label>
        <button class="btn-primary" style="width:100%;justify-content:center;" onclick="submitForm()">
          <span>Jetzt Anfrage senden</span><span>→</span>
        </button>
      </div>
    </div>
  </div>
</section>

<!-- ===== MAP ===== -->
<div class="map-section">
  <div class="map-placeholder">
    <div class="map-pin">📍</div>
    <div class="map-address">APEX FIT Bad Oeynhausen</div>
    <div class="map-address-sub">Musterstraße 12 · 32545 Bad Oeynhausen</div>
    <a href="https://maps.google.com/?q=Bad+Oeynhausen" target="_blank" class="map-cta-btn">In Google Maps öffnen →</a>
  </div>
</div>

<!-- ===== FOOTER ===== -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="footer-logo">APEX<span>FIT</span></div>
        <p class="footer-desc">Dein Premium-Fitnessstudio in Bad Oeynhausen. Modern. Smart. Für Ergebnisse, die man sieht und fühlt.</p>
        <div class="footer-social">
          <div class="footer-social-btn">f</div>
          <div class="footer-social-btn">in</div>
          <div class="footer-social-btn">yt</div>
          <div class="footer-social-btn">ig</div>
        </div>
      </div>
      <div>
        <div class="footer-col-title">Studio</div>
        <ul class="footer-links">
          <li><a href="#about">Über uns</a></li>
          <li><a href="#services">Leistungen</a></li>
          <li><a href="#digital">Digital Fitness</a></li>
          <li><a href="#team">Unser Team</a></li>
          <li><a href="#">Kursplan</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-col-title">Mitgliedschaft</div>
        <ul class="footer-links">
          <li><a href="#pricing">Basic</a></li>
          <li><a href="#pricing">Black Label</a></li>
          <li><a href="#pricing">Elite Coaching</a></li>
          <li><a href="#contact">Probetraining</a></li>
          <li><a href="#">Member Login</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-col-title">Info</div>
        <ul class="footer-links">
          <li><a href="#faq">FAQ</a></li>
          <li><a href="#contact">Kontakt</a></li>
          <li><a href="#">Jobs & Karriere</a></li>
          <li><a href="#">Impressum</a></li>
          <li><a href="#">Datenschutz</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span class="footer-bottom-text">© 2025 APEX FIT Bad Oeynhausen. Alle Rechte vorbehalten.</span>
      <div class="footer-bottom-links">
        <a href="#">Impressum</a>
        <a href="#">Datenschutz</a>
        <a href="#">AGB</a>
        <a href="#">Cookies</a>
      </div>
    </div>
  </div>
</footer>

<script>
  // ===== NAVBAR SCROLL =====
  const navbar = document.getElementById('navbar');
  window.addEventListener('scroll', () => {
    if (window.scrollY > 80) {
      navbar.style.background = 'rgba(8,8,8,0.97)';
      navbar.style.borderBottomColor = 'rgba(255,255,255,0.08)';
    } else {
      navbar.style.background = 'rgba(8,8,8,0.85)';
      navbar.style.borderBottomColor = 'rgba(255,255,255,0.05)';
    }
  });

  // ===== MOBILE MENU =====
  function toggleMenu() {
    const menu = document.getElementById('mobileMenu');
    menu.classList.toggle('open');
    document.body.style.overflow = menu.classList.contains('open') ? 'hidden' : '';
  }

  // ===== FAQ ACCORDION =====
  function toggleFaq(el) {
    const item = el.closest('.faq-item');
    const allItems = document.querySelectorAll('.faq-item');
    allItems.forEach(i => { if (i !== item) i.classList.remove('open'); });
    item.classList.toggle('open');
  }

  // ===== SCROLL REVEAL =====
  const revealEls = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  revealEls.forEach(el => observer.observe(el));

  // ===== FORM SUBMIT =====
  function submitForm() {
    const btn = event.currentTarget;
    const orig = btn.innerHTML;
    btn.innerHTML = '<span>Wird gesendet...</span>';
    btn.style.opacity = '0.7';
    setTimeout(() => {
      btn.innerHTML = '<span>✓ Nachricht gesendet!</span>';
      btn.style.background = '#16a34a';
      setTimeout(() => {
        btn.innerHTML = orig;
        btn.style.background = '';
        btn.style.opacity = '';
      }, 3000);
    }, 1200);
  }

  // ===== SMOOTH ACTIVE NAV =====
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(section => {
      const sectionTop = section.offsetTop - 120;
      if (window.scrollY >= sectionTop) current = section.getAttribute('id');
    });
    navLinks.forEach(link => {
      link.style.color = link.getAttribute('href') === `#${current}` ? 'white' : '';
    });
  });
</script>
</body>
</html>
