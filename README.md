<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shree Sonal Auto - Used Two Wheelers, Mandvi</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;900&family=Open+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --black: #0a0a0a;
      --dark: #141414;
      --card: #1e1e1e;
      --gold: #f5c518;
      --gold-dark: #c9a014;
      --white: #ffffff;
      --gray: #9ca3af;
      --light-gray: #f3f4f6;
      --blue: #1a3a6e;
    }
    html { scroll-behavior: smooth; }
    body { font-family: 'Open Sans', sans-serif; background: var(--black); color: var(--white); overflow-x: hidden; }

    /* NAV */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      background: rgba(10,10,10,0.95); backdrop-filter: blur(12px);
      padding: 14px 40px; display: flex; align-items: center; justify-content: space-between;
      border-bottom: 1px solid rgba(245,197,24,0.2);
    }
    .nav-logo { display: flex; align-items: center; gap: 12px; }
    .nav-logo img { width: 48px; height: 48px; border-radius: 50%; object-fit: cover; border: 2px solid var(--gold); }
    .nav-logo-text { font-family: 'Montserrat', sans-serif; font-size: 1.1rem; font-weight: 800; color: var(--white); line-height: 1.2; }
    .nav-logo-text span { color: var(--gold); }
    .nav-links { display: flex; gap: 28px; list-style: none; }
    .nav-links a { text-decoration: none; font-size: 0.85rem; font-weight: 600; color: rgba(255,255,255,0.75); letter-spacing: 0.5px; transition: color 0.2s; text-transform: uppercase; }
    .nav-links a:hover { color: var(--gold); }
    .nav-cta { background: var(--gold); color: var(--black); padding: 10px 22px; border-radius: 6px; font-size: 0.85rem; font-weight: 700; text-decoration: none; transition: all 0.2s; text-transform: uppercase; letter-spacing: 0.5px; }
    .nav-cta:hover { background: var(--gold-dark); transform: translateY(-1px); }

    /* HERO */
    .hero {
      min-height: 100vh;
      background: linear-gradient(135deg, #0a0a0a 0%, #141414 50%, #0d1f3c 100%);
      display: flex; align-items: center; justify-content: center;
      text-align: center; padding: 120px 24px 80px; position: relative; overflow: hidden;
    }
    .hero-bg-text {
      position: absolute; font-family: 'Montserrat', sans-serif; font-size: 20vw;
      font-weight: 900; color: rgba(245,197,24,0.04); letter-spacing: -5px;
      top: 50%; left: 50%; transform: translate(-50%, -50%); white-space: nowrap; user-select: none;
    }
    .hero-badge {
      display: inline-block; background: rgba(245,197,24,0.1); border: 1px solid rgba(245,197,24,0.3);
      color: var(--gold); font-size: 0.75rem; font-weight: 700; letter-spacing: 3px;
      text-transform: uppercase; padding: 7px 20px; border-radius: 4px; margin-bottom: 24px;
      animation: fadeUp 0.8s ease both;
    }
    .hero-logo { width: 120px; height: 120px; border-radius: 50%; object-fit: cover; border: 3px solid var(--gold); margin-bottom: 24px; box-shadow: 0 0 40px rgba(245,197,24,0.3); animation: fadeUp 0.8s 0.1s ease both; }
    .hero h1 { font-family: 'Montserrat', sans-serif; font-size: clamp(2.5rem, 6vw, 5rem); font-weight: 900; color: white; line-height: 1.05; letter-spacing: -1px; animation: fadeUp 0.8s 0.2s ease both; }
    .hero h1 span { color: var(--gold); }
    .hero-sub { font-size: 1.05rem; color: rgba(255,255,255,0.6); margin-top: 16px; font-weight: 300; letter-spacing: 0.5px; animation: fadeUp 0.8s 0.35s ease both; }
    .hero-since { display: inline-block; margin-top: 12px; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 0.8rem; padding: 5px 16px; border-radius: 4px; letter-spacing: 2px; animation: fadeUp 0.8s 0.4s ease both; }
    .hero-btns { margin-top: 40px; display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; animation: fadeUp 0.8s 0.5s ease both; }
    .btn-gold { background: var(--gold); color: var(--black); padding: 14px 32px; border-radius: 6px; font-weight: 700; font-size: 0.95rem; text-decoration: none; transition: all 0.2s; display: inline-block; font-family: 'Montserrat', sans-serif; letter-spacing: 0.5px; }
    .btn-gold:hover { background: var(--gold-dark); transform: translateY(-2px); box-shadow: 0 8px 24px rgba(245,197,24,0.3); }
    .btn-outline-gold { background: transparent; color: var(--gold); padding: 14px 32px; border-radius: 6px; font-weight: 700; font-size: 0.95rem; text-decoration: none; border: 2px solid var(--gold); transition: all 0.2s; display: inline-block; font-family: 'Montserrat', sans-serif; letter-spacing: 0.5px; }
    .btn-outline-gold:hover { background: rgba(245,197,24,0.1); transform: translateY(-2px); }
    .hero-stats { display: flex; gap: 48px; justify-content: center; flex-wrap: wrap; margin-top: 56px; animation: fadeUp 0.8s 0.6s ease both; }
    .stat { text-align: center; }
    .stat-num { font-family: 'Montserrat', sans-serif; font-size: 2.2rem; font-weight: 900; color: var(--gold); line-height: 1; }
    .stat-label { font-size: 0.78rem; color: rgba(255,255,255,0.5); margin-top: 4px; text-transform: uppercase; letter-spacing: 1px; }

    /* SECTION BASE */
    .section-dark { background: var(--dark); padding: 90px 24px; }
    .section-black { background: var(--black); padding: 90px 24px; }
    .section-inner { max-width: 1100px; margin: 0 auto; }
    .section-label { font-size: 0.72rem; font-weight: 700; letter-spacing: 3px; text-transform: uppercase; color: var(--gold); margin-bottom: 12px; }
    .section-title { font-family: 'Montserrat', sans-serif; font-size: clamp(1.8rem, 4vw, 2.6rem); font-weight: 800; color: var(--white); line-height: 1.2; }
    .section-title span { color: var(--gold); }
    .divider { width: 48px; height: 3px; background: var(--gold); margin-top: 16px; border-radius: 2px; }

    /* WHY US */
    .why-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; margin-top: 48px; }
    .why-card { background: var(--card); border: 1px solid rgba(245,197,24,0.1); border-radius: 12px; padding: 28px 24px; transition: transform 0.25s, border-color 0.25s; }
    .why-card:hover { transform: translateY(-5px); border-color: rgba(245,197,24,0.4); }
    .why-icon { font-size: 2rem; margin-bottom: 14px; }
    .why-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 1rem; color: var(--white); }
    .why-card p { color: var(--gray); font-size: 0.875rem; margin-top: 8px; line-height: 1.6; }

    /* VEHICLES */
    .vehicles-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; margin-top: 48px; }
    .vehicle-card { background: var(--card); border: 1px solid rgba(255,255,255,0.06); border-radius: 12px; padding: 24px; text-align: center; transition: all 0.25s; }
    .vehicle-card:hover { border-color: var(--gold); transform: translateY(-4px); }
    .vehicle-icon { font-size: 2.5rem; margin-bottom: 12px; }
    .vehicle-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 0.95rem; color: var(--white); }
    .vehicle-card p { color: var(--gray); font-size: 0.82rem; margin-top: 6px; }

    /* VEHICLE SHOWCASE (UPDATED) */
    .vgrid { display: grid; grid-template-columns: repeat(auto-fit, minmax(270px, 1fr)); gap: 24px; margin-top: 48px; }
    .vcard { background: var(--card); border: 1px solid rgba(255,255,255,0.06); border-radius: 16px; overflow: hidden; transition: all 0.3s; backdrop-filter: blur(2px); }
    .vcard:hover { transform: translateY(-6px); border-color: var(--gold); box-shadow: 0 12px 30px rgba(245,197,24,0.12); }
    .vcard-img-wrap { position: relative; background: #0f0f0f; display: flex; align-items: center; justify-content: center; padding: 20px 16px 12px 16px; min-height: 190px; }
    .vcard-img-wrap img { max-width: 100%; max-height: 160px; width: auto; height: auto; object-fit: contain; display: block; margin: 0 auto; filter: drop-shadow(0 4px 8px rgba(0,0,0,0.4)); transition: transform 0.3s ease; }
    .vcard:hover .vcard-img-wrap img { transform: scale(1.02); }
    .vcard-badge { position: absolute; top: 12px; left: 12px; background: rgba(0,0,0,0.65); backdrop-filter: blur(4px); border-left: 3px solid var(--gold); color: var(--gold); font-size: 0.7rem; font-weight: 700; letter-spacing: 1px; padding: 4px 10px; border-radius: 0 8px 8px 0; text-transform: uppercase; z-index: 2; }
    .vcard-info { padding: 20px; border-top: 1px solid rgba(255,255,255,0.06); background: rgba(20,20,20,0.7); }
    .vcard-info h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 1rem; color: var(--white); margin-bottom: 4px; }
    .vcard-info p { color: var(--gray); font-size: 0.8rem; margin-bottom: 14px; }
    .vcard-btn { display: inline-block; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 0.75rem; padding: 8px 18px; border-radius: 30px; text-decoration: none; transition: all 0.2s; letter-spacing: 0.5px; }
    .vcard-btn:hover { background: var(--gold-dark); transform: translateY(-1px); }

    /* CUSTOMERS (HAPPY) */
    .cust-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 20px; margin-top: 48px; }
    .cust-card { border-radius: 14px; overflow: hidden; position: relative; border: 1px solid rgba(245,197,24,0.1); transition: all 0.3s; }
    .cust-card:hover { border-color: var(--gold); transform: translateY(-5px); box-shadow: 0 12px 40px rgba(245,197,24,0.15); }
    .cust-img-wrap { position: relative; overflow: hidden; }
    .cust-img-wrap img { width: 100%; height: 380px; object-fit: cover; object-position: top; display: block; transition: transform 0.4s; }
    .cust-card:hover .cust-img-wrap img { transform: scale(1.04); }
    .cust-overlay { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.88)); padding: 28px 18px 18px; }
    .cust-badge { display: inline-block; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 0.72rem; padding: 4px 12px; border-radius: 4px; letter-spacing: 1px; margin-bottom: 6px; }
    .cust-handle { color: rgba(255,255,255,0.85); font-size: 0.85rem; margin-top: 4px; }

    /* INSTAGRAM */
    .insta-section { background: linear-gradient(135deg, #833ab4, #fd1d1d, #f77737); padding: 80px 24px; text-align: center; }
    .insta-inner { max-width: 700px; margin: 0 auto; }
    .insta-logo { width: 90px; height: 90px; border-radius: 20px; object-fit: cover; margin: 0 auto 20px; display: block; border: 3px solid white; box-shadow: 0 8px 30px rgba(0,0,0,0.3); }
    .insta-section h2 { font-family: 'Montserrat', sans-serif; font-size: clamp(1.8rem, 4vw, 2.4rem); font-weight: 800; color: white; }
    .insta-handle { font-size: 1.2rem; color: rgba(255,255,255,0.9); margin-top: 8px; font-weight: 600; letter-spacing: 1px; }
    .insta-section p { color: rgba(255,255,255,0.8); margin-top: 10px; font-size: 0.95rem; }
    .btn-white { display: inline-block; margin-top: 28px; background: white; color: #833ab4; padding: 14px 36px; border-radius: 6px; font-weight: 700; font-size: 0.95rem; text-decoration: none; transition: all 0.2s; font-family: 'Montserrat', sans-serif; }
    .btn-white:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,0,0,0.2); }

    /* CONTACT */
    .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; margin-top: 48px; }
    .contact-card { background: var(--card); border: 1px solid rgba(245,197,24,0.15); border-radius: 12px; padding: 28px 24px; display: flex; align-items: flex-start; gap: 16px; transition: border-color 0.2s; }
    .contact-card:hover { border-color: rgba(245,197,24,0.4); }
    .contact-icon { font-size: 1.6rem; margin-top: 2px; }
    .contact-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 0.85rem; color: var(--gold); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 6px; }
    .contact-card p { color: var(--gray); font-size: 0.9rem; line-height: 1.6; }
    .contact-card a { color: var(--white); text-decoration: none; font-weight: 600; font-size: 1rem; }
    .contact-card a:hover { color: var(--gold); }
    .map-btn { display: inline-block; margin-top: 32px; }

    /* FOOTER */
    footer { background: #050505; border-top: 1px solid rgba(245,197,24,0.15); text-align: center; padding: 30px 24px; }
    footer p { color: rgba(255,255,255,0.4); font-size: 0.82rem; }
    footer span { color: var(--gold); }

    @keyframes fadeUp { from { opacity: 0; transform: translateY(28px); } to { opacity: 1; transform: translateY(0); } }
    @media (max-width: 640px) { nav { padding: 12px 16px; } .nav-links { display: none; } .hero-stats { gap: 28px; } }
  </style>
</head>
<body>

<nav>
  <div class="nav-logo">
    <img src="data:image/jpeg;base64,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
