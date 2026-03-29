<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Shree Ganesh Flour Mill – Baarik Punjabi Aatta</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --wheat: #C8883A;
    --wheat-light: #F5E9D6;
    --wheat-dark: #8B5E1E;
    --cream: #FAF6EF;
    --dark: #1E1A14;
    --mid: #5C4A2A;
    --muted: #9C8569;
    --white: #FFFFFF;
    --radius: 12px;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--dark);
    line-height: 1.7;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(250, 246, 239, 0.92);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(200, 136, 58, 0.2);
    padding: 0 2rem;
    display: flex; align-items: center; justify-content: space-between;
    height: 64px;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--wheat-dark);
    letter-spacing: 0.01em;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-size: 0.875rem;
    font-weight: 500;
    color: var(--mid);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--wheat); }
  .nav-cta {
    background: var(--wheat);
    color: var(--white) !important;
    padding: 0.5rem 1.25rem;
    border-radius: 100px;
    font-size: 0.875rem !important;
    font-weight: 500 !important;
    text-decoration: none;
    transition: background 0.2s;
  }
  .nav-cta:hover { background: var(--wheat-dark) !important; color: var(--white) !important; }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 100px 2rem 4rem;
    background:
      radial-gradient(ellipse at 80% 20%, rgba(200,136,58,0.13) 0%, transparent 60%),
      radial-gradient(ellipse at 10% 80%, rgba(200,136,58,0.08) 0%, transparent 50%),
      var(--cream);
    position: relative; overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: -100px; right: -100px;
    width: 500px; height: 500px;
    border-radius: 50%;
    border: 60px solid rgba(200,136,58,0.07);
    pointer-events: none;
  }
  .hero::after {
    content: '';
    position: absolute; bottom: -80px; left: -80px;
    width: 300px; height: 300px;
    border-radius: 50%;
    border: 40px solid rgba(200,136,58,0.05);
    pointer-events: none;
  }
  .hero-inner {
    max-width: 1100px; margin: 0 auto; width: 100%;
    display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center;
  }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--wheat-light);
    color: var(--wheat-dark);
    font-size: 0.78rem; font-weight: 500;
    letter-spacing: 0.08em; text-transform: uppercase;
    padding: 0.4rem 1rem; border-radius: 100px;
    margin-bottom: 1.5rem;
  }
  .hero-badge span { width: 6px; height: 6px; border-radius: 50%; background: var(--wheat); display: inline-block; }
  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.4rem, 5vw, 3.8rem);
    font-weight: 700;
    line-height: 1.15;
    color: var(--dark);
    margin-bottom: 1.25rem;
  }
  h1 em { color: var(--wheat); font-style: normal; }
  .hero-sub {
    font-size: 1.05rem;
    color: var(--muted);
    font-weight: 300;
    max-width: 420px;
    margin-bottom: 2.5rem;
    line-height: 1.8;
  }
  .hero-buttons { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn-primary {
    background: var(--wheat);
    color: var(--white);
    padding: 0.85rem 2rem;
    border-radius: 100px;
    font-weight: 500;
    font-size: 0.95rem;
    text-decoration: none;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }
  .btn-primary:hover { background: var(--wheat-dark); transform: translateY(-1px); }
  .btn-outline {
    background: transparent;
    color: var(--wheat-dark);
    padding: 0.85rem 2rem;
    border-radius: 100px;
    font-weight: 500;
    font-size: 0.95rem;
    text-decoration: none;
    border: 1.5px solid var(--wheat);
    transition: all 0.2s;
    display: inline-block;
  }
  .btn-outline:hover { background: var(--wheat-light); transform: translateY(-1px); }

  .hero-visual {
    display: flex;
    align-items: flex-end;
    justify-content: center;
    position: relative;
    min-height: 420px;
  }
  .grain-card {
    background: var(--white);
    border-radius: var(--radius);
    padding: 1.5rem 1.25rem;
    border: 1px solid rgba(200,136,58,0.15);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .grain-card:hover { transform: translateY(-3px); box-shadow: 0 12px 30px rgba(200,136,58,0.12); }
  .grain-card:nth-child(2) { margin-top: 1.5rem; }
  .grain-card:nth-child(4) { margin-top: -1.5rem; }
  .grain-icon {
    font-size: 2rem; margin-bottom: 0.75rem; display: block;
    width: 52px; height: 52px; border-radius: 12px;
    background: var(--wheat-light);
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 1rem;
  }
  .grain-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 0.95rem;
    font-weight: 600;
    color: var(--dark);
    margin-bottom: 0.25rem;
  }
  .grain-card p { font-size: 0.78rem; color: var(--muted); line-height: 1.5; }

  /* SECTION SHARED */
  section { padding: 5rem 2rem; }
  .section-inner { max-width: 1100px; margin: 0 auto; }
  .section-label {
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--wheat);
    margin-bottom: 0.75rem;
  }
  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.6rem);
    font-weight: 700;
    color: var(--dark);
    line-height: 1.25;
    margin-bottom: 1rem;
  }
  .section-desc {
    font-size: 1rem;
    color: var(--muted);
    max-width: 500px;
    line-height: 1.8;
    font-weight: 300;
  }

  /* STATS */
  .stats {
    background: var(--wheat-dark);
    padding: 3.5rem 2rem;
  }
  .stats-grid {
    max-width: 1100px; margin: 0 auto;
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem;
    text-align: center;
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.8rem; font-weight: 700;
    color: var(--white);
    line-height: 1;
    margin-bottom: 0.4rem;
  }
  .stat-label { font-size: 0.875rem; color: rgba(255,255,255,0.65); font-weight: 300; }

  /* PRODUCTS */
  .products { background: var(--white); }
  .products-header {
    display: flex; justify-content: space-between; align-items: flex-end;
    margin-bottom: 3rem; flex-wrap: wrap; gap: 1rem;
  }
  .products-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(230px, 1fr)); gap: 1.5rem;
  }
  .product-card {
    border: 1px solid rgba(200,136,58,0.15);
    border-radius: var(--radius);
    padding: 2rem 1.5rem;
    transition: all 0.2s;
    position: relative; overflow: hidden;
  }
  .product-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--wheat), var(--wheat-dark));
    opacity: 0;
    transition: opacity 0.2s;
  }
  .product-card:hover { transform: translateY(-4px); box-shadow: 0 16px 40px rgba(200,136,58,0.1); }
  .product-card:hover::before { opacity: 1; }
  .product-emoji {
    width: 56px; height: 56px;
    background: var(--wheat-light);
    border-radius: 14px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.6rem;
    margin-bottom: 1.25rem;
  }
  .product-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem; font-weight: 600;
    color: var(--dark);
    margin-bottom: 0.5rem;
  }
  .product-card p { font-size: 0.875rem; color: var(--muted); line-height: 1.65; }
  .product-tag {
    display: inline-block;
    margin-top: 1.25rem;
    font-size: 0.75rem; font-weight: 500;
    color: var(--wheat-dark);
    background: var(--wheat-light);
    padding: 0.3rem 0.75rem;
    border-radius: 100px;
  }

  /* WHO WE SERVE */
  .serve { background: var(--cream); }
  .serve-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
    margin-top: 2.5rem;
  }
  .serve-card {
    background: var(--white);
    border-radius: var(--radius);
    padding: 2rem 1.5rem;
    border: 1px solid rgba(200,136,58,0.12);
  }
  .serve-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.5rem; font-weight: 700;
    color: var(--wheat-light);
    line-height: 1;
    margin-bottom: 0.5rem;
  }
  .serve-card h3 { font-family: 'Playfair Display', serif; font-size: 1.1rem; font-weight: 600; color: var(--dark); margin-bottom: 0.5rem; }
  .serve-card p { font-size: 0.875rem; color: var(--muted); line-height: 1.65; }

  /* WHY US */
  .why { background: var(--white); }
  .why-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;
    margin-top: 2.5rem;
  }
  .why-item {
    display: flex; gap: 1rem;
    background: var(--cream);
    padding: 1.5rem;
    border-radius: var(--radius);
    align-items: flex-start;
  }
  .why-dot {
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--wheat);
    margin-top: 7px; flex-shrink: 0;
  }
  .why-item h4 { font-size: 0.95rem; font-weight: 500; color: var(--dark); margin-bottom: 0.25rem; }
  .why-item p { font-size: 0.85rem; color: var(--muted); line-height: 1.6; }

  /* CTA BAND */
  .cta-band {
    background:
      radial-gradient(ellipse at 20% 50%, rgba(255,255,255,0.06) 0%, transparent 60%),
      var(--wheat-dark);
    padding: 5rem 2rem;
    text-align: center;
  }
  .cta-band h2 { color: var(--white); margin-bottom: 1rem; }
  .cta-band p { color: rgba(255,255,255,0.7); max-width: 480px; margin: 0 auto 2.5rem; font-weight: 300; line-height: 1.8; }
  .cta-buttons { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
  .btn-white {
    background: var(--white);
    color: var(--wheat-dark);
    padding: 0.9rem 2rem;
    border-radius: 100px;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.2s;
    display: inline-flex; align-items: center; gap: 0.5rem;
  }
  .btn-white:hover { background: var(--wheat-light); transform: translateY(-1px); }
  .btn-ghost {
    background: transparent;
    color: var(--white);
    border: 1.5px solid rgba(255,255,255,0.4);
    padding: 0.9rem 2rem;
    border-radius: 100px;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.2s;
    display: inline-block;
  }
  .btn-ghost:hover { background: rgba(255,255,255,0.1); transform: translateY(-1px); }

  /* CONTACT */
  .contact { background: var(--cream); }
  .contact-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 4rem;
    align-items: start; margin-top: 2.5rem;
  }
  .contact-info h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; font-weight: 600;
    color: var(--dark); margin-bottom: 1.5rem;
  }
  .contact-item {
    display: flex; gap: 1rem; align-items: flex-start;
    margin-bottom: 1.25rem;
  }
  .contact-icon {
    width: 40px; height: 40px; border-radius: 10px;
    background: var(--wheat-light);
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem; flex-shrink: 0;
  }
  .contact-item strong { font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.05em; color: var(--muted); display: block; margin-bottom: 0.15rem; }
  .contact-item span { font-size: 0.95rem; color: var(--dark); }
  .contact-item a { color: var(--wheat-dark); text-decoration: none; }
  .contact-item a:hover { text-decoration: underline; }

  .contact-form {
    background: var(--white);
    border-radius: var(--radius);
    padding: 2rem;
    border: 1px solid rgba(200,136,58,0.15);
  }
  .contact-form h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; font-weight: 600;
    color: var(--dark); margin-bottom: 1.5rem;
  }
  .form-group { margin-bottom: 1.25rem; }
  .form-group label { font-size: 0.82rem; font-weight: 500; color: var(--mid); display: block; margin-bottom: 0.4rem; }
  .form-group input, .form-group textarea, .form-group select {
    width: 100%;
    border: 1.5px solid rgba(200,136,58,0.2);
    border-radius: 8px;
    padding: 0.7rem 1rem;
    font-size: 0.9rem;
    font-family: 'DM Sans', sans-serif;
    color: var(--dark);
    background: var(--cream);
    transition: border-color 0.2s;
    outline: none;
  }
  .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
    border-color: var(--wheat);
    background: var(--white);
  }
  .form-group textarea { resize: vertical; min-height: 100px; }
  .form-submit {
    width: 100%;
    background: var(--wheat);
    color: var(--white);
    border: none;
    padding: 0.9rem 2rem;
    border-radius: 100px;
    font-size: 0.95rem;
    font-weight: 500;
    font-family: 'DM Sans', sans-serif;
    cursor: pointer;
    transition: background 0.2s;
  }
  .form-submit:hover { background: var(--wheat-dark); }

  /* FOOTER */
  footer {
    background: var(--dark);
    padding: 2.5rem 2rem;
    text-align: center;
  }
  .footer-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; font-weight: 700;
    color: var(--wheat);
    margin-bottom: 0.5rem;
  }
  footer p { font-size: 0.8rem; color: rgba(255,255,255,0.35); }

  /* WHATSAPP FLOAT */
  .wa-float {
    position: fixed; bottom: 2rem; right: 2rem; z-index: 200;
    width: 56px; height: 56px;
    background: #25D366;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    text-decoration: none;
    box-shadow: 0 4px 20px rgba(37,211,102,0.4);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .wa-float:hover { transform: scale(1.1); box-shadow: 0 6px 28px rgba(37,211,102,0.5); }
  .wa-float svg { width: 28px; height: 28px; fill: white; }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    .hero-inner { grid-template-columns: 1fr; gap: 3rem; }
    .hero-visual { display: none; }
    .nav-links { display: none; }
    .stats-grid { grid-template-columns: 1fr; gap: 1.5rem; }
    .serve-grid { grid-template-columns: 1fr; }
    .why-grid { grid-template-columns: 1fr; }
    .contact-grid { grid-template-columns: 1fr; gap: 2rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Shree Ganesh Flour Mill</div>
  <ul class="nav-links">
    <li><a href="#products">Products</a></li>
    <li><a href="#why">Why Us</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="https://wa.me/919867074565" class="nav-cta">WhatsApp Us</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-inner">
    <div>
      <div style="margin-bottom: 1.25rem;">
        <span style="font-family: 'Playfair Display', serif; font-size: clamp(1.5rem, 3vw, 2rem); font-weight: 700; color: #3a1f00; letter-spacing: 0.06em; text-transform: uppercase; border-bottom: 3px solid var(--wheat); padding-bottom: 6px; display: inline-block;">Shree Ganesh Flour Mill</span>
      </div>
      <div class="hero-badge"><span></span> Pure · Fresh · Traditional</div>
      <h1>The Finest <em>Baarik Punjabi</em> Aatta</h1>
      <p class="hero-sub">Stone-ground flour crafted with generations of tradition. From your kitchen to your table — pure, fresh, and nourishing every time.</p>
      <div class="hero-buttons">
        <a href="#contact" class="btn-primary">Book a Consultation</a>
        <a href="#products" class="btn-outline">View Products</a>
      </div>
    </div>
    <div class="hero-visual" style="display:flex; align-items:flex-end; justify-content:center; position:relative;">
      <!-- White bg box to neutralise black image background -->
      <div style="position:absolute; inset:0; background:#FAF6EF; border-radius:16px;"></div>
      <!-- Decorative circle -->
      <div style="position:absolute; bottom:0; left:50%; transform:translateX(-50%); width:340px; height:340px; border-radius:50%; background:rgba(200,136,58,0.08); border:2px solid rgba(200,136,58,0.12);"></div>
      <img
        src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/4gHYSUNDX1BST0ZJTEUAAQEAAAHIAAAAAAQwAABtbnRyUkdCIFhZWiAH4AABAAEAAAAAAABhY3NwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAA9tYAAQAAAADTLQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAlkZXNjAAAA8AAAACRyWFlaAAABFAAAABRnWFlaAAABKAAAABRiWFlaAAABPAAAABR3dHB0AAABUAAAABRyVFJDAAABZAAAAChnVFJDAAABZAAAAChiVFJDAAABZAAAAChjcHJ0AAABjAAAADxtbHVjAAAAAAAAAAEAAAAMZW5VUwAAAAgAAAAcAHMAUgBHAEJYWVogAAAAAAAAb6IAADj1AAADkFhZWiAAAAAAAABimQAAt4UAABjaWFlaIAAAAAAAACSgAAAPhAAAts9YWVogAAAAAAAA9tYAAQAAAADTLXBhcmEAAAAAAAQAAAACZmYAAPKnAAANWQAAE9AAAApbAAAAAAAAAABtbHVjAAAAAAAAAAEAAAAMZW5VUwAAACAAAAAcAEcAbwBvAGcAbABlACAASQBuAGMALgAgADIAMAAxADb/2wBDAAUDBAQEAwUEBAQFBQUGBwwIBwcHBw8LCwkMEQ8SEhEPERETFhwXExQaFRERGCEYGh0dHx8fExciJCIeJBweHx7/2wBDAQUFBQcGBw4ICA4eFBEUHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh7/wAARCAJBAbEDASIAAhEBAxEB/8QAHQABAAEFAQEBAAAAAAAAAAAAAAUDBAYHCAIBCf/EAEsQAAEEAQIEAwUGAwYCCAQHAAEAAgMRBAUhBhIxQRNRYQcicYGRCBQyobHB0eHwFSMzQlLxJHIWNENTYnOCkiU1srM2N2N0oqPC/8QAGgEBAAIDAQAAAAAAAAAAAAAAAAECAwQFBv/EACoRAQEAAgICAQMDBAMBAAAAAAABAhEDIQQxEgVBURMiMiMzYXEUQoHw/9oADAMBAAIRAxEAPwDjJERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBF9a0uIDQSStqexz2Wy8TajFl6sTFprBzyCqJH9dlFulscLldRgPDnDWt8Q5Ig0nT5sk93Nb7o+JWeYPsgymOrVdSZC4fiZEyy0/E0ulMnU9C4f0JmgcM6RFjNjbyukLKd6nzv1WIyESOL3tBeVq8/P8esXS8bwfn3k1kz2RaN4NHNy3POwdYG9eXdROqeyKUWNNzw9wH/aigfpa3A+N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"
        alt="Founder of Shree Ganesh Flour Mill"
        style="
          width: 100%;
          max-width: 380px;
          display: block;
          position: relative;
          z-index: 1;
          mix-blend-mode: multiply;
          filter: brightness(1.08);
        "
      />
    </div>
  </div>
</section>

<!-- STATS -->
<div class="stats">
  <div class="stats-grid">
    <div>
      <div class="stat-num">25+</div>
      <div class="stat-label">Years of Experience</div>
    </div>
    <div>
      <div class="stat-num">5000+</div>
      <div class="stat-label">Happy Customers</div>
    </div>
    <div>
      <div class="stat-num">100%</div>
      <div class="stat-label">Pure & Natural Ingredients</div>
    </div>
  </div>
</div>

<!-- PRODUCTS -->
<section class="products" id="products">
  <div class="section-inner">
    <div class="products-header">
      <div>
        <div class="section-label">Our Products</div>
        <h2>Freshly Milled, Every Day</h2>
      </div>
      <p class="section-desc">Sourced from the finest grains, milled fresh to preserve nutrition and flavour.</p>
    </div>
    <div class="products-grid">
      <div class="product-card">
        <div class="product-emoji">🌾</div>
        <h3>Wheat Flour (Atta)</h3>
        <p>Our signature baarik Punjabi atta — finely ground, soft in texture, and ideal for soft rotis and parathas. The taste of tradition in every knead.</p>
        <span class="product-tag">Best Seller</span>
      </div>
      <div class="product-card">
        <div class="product-emoji">🍚</div>
        <h3>Rice Flour</h3>
        <p>Pure, finely milled rice flour with a smooth texture. Perfect for South Indian recipes, desserts, and gluten-free baking needs.</p>
        <span class="product-tag">Available in bulk</span>
      </div>
      <div class="product-card">
        <div class="product-emoji">🫘</div>
        <h3>Chickpea Flour (Besan)</h3>
        <p>Rich, golden besan made from premium chickpeas. Ideal for pakoras, kadhi, mithai, and a wide range of savoury dishes.</p>
        <span class="product-tag">Wholesale available</span>
      </div>
      <div class="product-card">
        <div class="product-emoji">🌿</div>
        <h3>Multigrain Flour</h3>
        <p>A nourishing blend of wheat, oats, and other wholesome grains. Perfect for health-focused families and restaurants.</p>
        <span class="product-tag">New</span>
      </div>
    </div>
  </div>
</section>

<!-- WHO WE SERVE -->
<section class="serve" id="serve">
  <div class="section-inner">
    <div class="section-label">Who We Serve</div>
    <h2>Flour for Every Need</h2>
    <div class="serve-grid">
      <div class="serve-card">
        <div class="serve-num">01</div>
        <h3>Home Cooks & Families</h3>
        <p>Fresh, pure flour delivered in convenient packs. Taste the difference that quality grain makes in your daily cooking.</p>
      </div>
      <div class="serve-card">
        <div class="serve-num">02</div>
        <h3>Restaurants & Hotels</h3>
        <p>Consistent quality, every single order. Our flour keeps your kitchen running and your customers coming back.</p>
      </div>
      <div class="serve-card">
        <div class="serve-num">03</div>
        <h3>Wholesale & Bulk Buyers</h3>
        <p>Competitive pricing for large orders. We supply bakeries, caterers, and distributors across the region.</p>
      </div>
    </div>
  </div>
</section>

<!-- WHY US -->
<section class="why" id="why">
  <div class="section-inner">
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center;">
      <div>
        <div class="section-label">Why Choose Us</div>
        <h2>Quality You Can Taste, Trust You Can Count On</h2>
        <p class="section-desc" style="margin-top: 1rem;">At Shree Ganesh Flour Mill, we take pride in every grain we mill. Our process is transparent, our ingredients are pure, and our commitment to quality is unwavering.</p>
      </div>
      <div class="why-grid">
        <div class="why-item">
          <div class="why-dot"></div>
          <div>
            <h4>Stone-ground freshness</h4>
            <p>Milled daily to retain maximum nutrition and natural flavour.</p>
          </div>
        </div>
        <div class="why-item">
          <div class="why-dot"></div>
          <div>
            <h4>No preservatives</h4>
            <p>100% pure flour with zero additives or artificial agents.</p>
          </div>
        </div>
        <div class="why-item">
          <div class="why-dot"></div>
          <div>
            <h4>Bulk & custom orders</h4>
            <p>Flexible quantities for homes, businesses and wholesalers.</p>
          </div>
        </div>
        <div class="why-item">
          <div class="why-dot"></div>
          <div>
            <h4>Generations of trust</h4>
            <p>A family business built on quality, consistency, and care.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- MEET THE OWNER -->
<section style="background: var(--cream); padding: 5rem 2rem; overflow: hidden;">
  <div style="max-width: 1100px; margin: 0 auto;">
    <div style="font-size: 0.75rem; font-weight: 500; letter-spacing: 0.1em; text-transform: uppercase; color: var(--wheat); margin-bottom: 0.75rem;">Meet the Founder</div>
    <h2 style="font-family: Playfair Display, serif; font-size: clamp(1.8rem, 3.5vw, 2.6rem); font-weight: 700; color: var(--dark); line-height: 1.25; margin-bottom: 1.25rem; max-width: 600px;">A Legacy Built on Quality Grain</h2>
    <p style="font-size: 1rem; color: var(--muted); font-weight: 300; line-height: 1.8; margin-bottom: 1.5rem; max-width: 620px;">With over 25 years of dedication to the craft of flour milling, our founder has built Shree Ganesh Flour Mill from the ground up — driven by a passion for purity and an unwavering commitment to every customer's satisfaction.</p>
    <p style="font-size: 1rem; color: var(--muted); font-weight: 300; line-height: 1.8; max-width: 620px;">Every bag of flour that leaves our mill carries with it generations of knowledge, tradition, and care. That is the promise of Shree Ganesh Flour Mill.</p>
    <div style="margin-top: 2rem; display: flex; align-items: center; gap: 1rem;">
      <div style="width: 48px; height: 2px; background: var(--wheat);"></div>
      <span style="font-family: Playfair Display, serif; font-size: 1rem; color: var(--muted); font-style: italic;">Shree Ganesh Flour Mill</span>
    </div>
  </div>
</section>

<!-- CTA BAND -->
<div class="cta-band">
  <h2>Ready to Order or Have Questions?</h2>
  <p>Reach out today for bulk pricing, a free consultation, or to place your first order. We're just a message away.</p>
  <div class="cta-buttons">
    <a href="https://wa.me/919867074565" class="btn-white">
      <svg viewBox="0 0 24 24" width="16" height="16" fill="#25D366"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12.05 2C6.495 2 2 6.495 2 12.05 2 13.9 2.52 15.63 3.41 17.11L2 22l5.05-1.38C8.52 21.49 10.24 22 12.05 22 17.6 22 22 17.5 22 11.95 22 6.495 17.6 2 12.05 2zm0 18.2c-1.65 0-3.18-.47-4.48-1.27l-.32-.19-3 .79.81-2.96-.21-.33A8.16 8.16 0 0 1 3.8 12.05 8.25 8.25 0 0 1 12.05 3.8a8.25 8.25 0 0 1 8.25 8.25 8.25 8.25 0 0 1-8.25 8.15z"/></svg>
      WhatsApp Us
    </a>
    <a href="#contact" class="btn-ghost">Book a Consultation</a>
  </div>
</div>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="section-inner">
    <div class="section-label">Get in Touch</div>
    <h2>Let's Talk Flour</h2>
    <div class="contact-grid">
      <div class="contact-info">
        <h3>We'd love to hear from you</h3>
        <div class="contact-item">
          <div class="contact-icon">📱</div>
          <div>
            <strong>WhatsApp / Call</strong>
            <span><a href="https://wa.me/919867074565">+91 98670 74565</a></span>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">🕐</div>
          <div>
            <strong>Business Hours</strong>
            <span>Monday – Saturday, 9:00 AM – 7:00 PM</span>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📦</div>
          <div>
            <strong>Order Types</strong>
            <span>Retail · Bulk · Wholesale · Custom</span>
          </div>
        </div>
        <br/>
        <a href="https://wa.me/919867074565?text=Hi%2C%20I%20would%20like%20to%20enquire%20about%20your%20flour%20products." class="btn-primary" style="display:inline-flex;align-items:center;gap:8px;">
          <svg viewBox="0 0 24 24" width="16" height="16" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12.05 2C6.495 2 2 6.495 2 12.05 2 13.9 2.52 15.63 3.41 17.11L2 22l5.05-1.38C8.52 21.49 10.24 22 12.05 22 17.6 22 22 17.5 22 11.95 22 6.495 17.6 2 12.05 2zm0 18.2c-1.65 0-3.18-.47-4.48-1.27l-.32-.19-3 .79.81-2.96-.21-.33A8.16 8.16 0 0 1 3.8 12.05 8.25 8.25 0 0 1 12.05 3.8a8.25 8.25 0 0 1 8.25 8.25 8.25 8.25 0 0 1-8.25 8.15z"/></svg>
          Message on WhatsApp
        </a>
      </div>
      <div class="contact-form">
        <h3>Book a Consultation</h3>
        <div class="form-group">
          <label>Your Name</label>
          <input type="text" placeholder="e.g. Ramesh Kumar" />
        </div>
        <div class="form-group">
          <label>Phone Number</label>
          <input type="tel" placeholder="+91 00000 00000" />
        </div>
        <div class="form-group">
          <label>I'm interested in</label>
          <select>
            <option>Wheat Flour (Atta)</option>
            <option>Rice Flour</option>
            <option>Chickpea Flour (Besan)</option>
            <option>Multigrain Flour</option>
            <option>Multiple Products / Bulk Order</option>
          </select>
        </div>
        <div class="form-group">
          <label>Message (optional)</label>
          <textarea placeholder="Tell us about your requirements — quantity, frequency, or any questions..."></textarea>
        </div>
        <button class="form-submit" onclick="handleSubmit()">Send Enquiry →</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Shree Ganesh Flour Mill</div>
  <p style="margin-top: 0.25rem; margin-bottom: 0.5rem; color: rgba(255,255,255,0.5); font-size: 0.85rem;">Baarik Punjabi Aatta — Pure, Fresh & Traditional</p>
  <p>© 2025 Shree Ganesh Flour Mill. All rights reserved.</p>
</footer>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/919867074565?text=Hi%2C%20I%20would%20like%20to%20enquire%20about%20your%20flour%20products." class="wa-float" target="_blank" title="Chat on WhatsApp">
  <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12.05 2C6.495 2 2 6.495 2 12.05 2 13.9 2.52 15.63 3.41 17.11L2 22l5.05-1.38C8.52 21.49 10.24 22 12.05 22 17.6 22 22 17.5 22 11.95 22 6.495 17.6 2 12.05 2zm0 18.2c-1.65 0-3.18-.47-4.48-1.27l-.32-.19-3 .79.81-2.96-.21-.33A8.16 8.16 0 0 1 3.8 12.05 8.25 8.25 0 0 1 12.05 3.8a8.25 8.25 0 0 1 8.25 8.25 8.25 8.25 0 0 1-8.25 8.15z"/></svg>
</a>

<script>
function handleSubmit() {
  const btn = document.querySelector('.form-submit');
  btn.textContent = 'Enquiry Sent! ✓';
  btn.style.background = '#4CAF50';
  setTimeout(() => {
    btn.textContent = 'Send Enquiry →';
    btn.style.background = '';
  }, 3000);
}
</script>
</body>
</html>
