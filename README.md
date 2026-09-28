<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AgroConsultoria — Rastreabilidade, genética e performance agronômica</title>
<meta name="description" content="Consultoria agronômica especializada em rastreabilidade, melhoramento genético, certificação e compliance para cadeias produtivas de alto valor.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300..600&family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<style>
  :root{
    /* Paleta corporativa sóbria */
    --petroleo-900:#0a1c26;
    --petroleo-800:#0f2836;
    --petroleo-700:#16394a;
    --petroleo-600:#1e4a5e;
    --petroleo-500:#2c6479;

    --oliva-900:#2d3a1f;
    --oliva-700:#4a5c31;
    --oliva-500:#6b8048;
    --oliva-300:#a4b380;
    --oliva-100:#e6ebd9;

    --ambar-700:#a8701a;
    --ambar-600:#c9871f;
    --ambar-500:#e0a233;
    --ambar-300:#f0c168;
    --ambar-100:#fdf3e0;

    --tinta:#0f1a22;
    --cinza-900:#1e2a33;
    --cinza-700:#3d4d59;
    --cinza-500:#6b7a86;
    --cinza-300:#a8b3bc;
    --cinza-100:#e8ecf0;
    --cinza-50:#f4f6f9;
    --branco:#ffffff;
    --linha:#dfe4ea;
    --linha-escura:rgba(255,255,255,.1);
  }

  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth;-webkit-font-smoothing:antialiased}
  body{
    font-family:'Inter',system-ui,sans-serif;
    color:var(--tinta);
    background:var(--branco);
    line-height:1.65;
    font-size:16px;
    overflow-x:hidden;
  }

  h1,h2,h3,h4{
    font-family:'Fraunces',Georgia,serif;
    font-weight:400;
    letter-spacing:-0.02em;
    line-height:1.15;
    color:var(--petroleo-900);
  }

  a{color:inherit;text-decoration:none}
  img{max-width:100%;display:block}

  .container{
    width:100%;
    max-width:1280px;
    margin:0 auto;
    padding:0 40px;
  }

  .eyebrow{
    font-family:'JetBrains Mono',monospace;
    font-size:.7rem;
    font-weight:500;
    letter-spacing:.22em;
    text-transform:uppercase;
    color:var(--ambar-700);
    display:inline-flex;
    align-items:center;
    gap:14px;
  }
  .eyebrow::before{
    content:'';
    width:28px;
    height:1px;
    background:var(--ambar-700);
    display:inline-block;
  }

  /* ============ HEADER ============ */
  header{
    position:fixed;
    top:0;left:0;right:0;
    z-index:1000;
    padding:20px 0;
    transition:all .3s ease;
    background:transparent;
  }
  header.scrolled{
    background:var(--branco);
    padding:14px 0;
    border-bottom:1px solid var(--linha);
    box-shadow:0 1px 3px rgba(11,31,42,.04);
  }
  .nav-inner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:48px;
  }
  .brand{
    display:flex;
    align-items:center;
    gap:12px;
    font-family:'Fraunces',serif;
    font-size:1.25rem;
    font-weight:500;
    letter-spacing:-.02em;
    color:var(--branco);
    transition:color .3s;
  }
  header.scrolled .brand{color:var(--petroleo-900)}
  .brand-mark{
    width:36px;height:36px;
    border-radius:6px;
    background:var(--ambar-500);
    display:flex;align-items:center;justify-content:center;
    color:var(--petroleo-900);
    font-size:.9rem;
  }
  header.scrolled .brand-mark{
    background:var(--petroleo-800);
    color:var(--ambar-500);
  }
  .brand em{
    font-style:normal;
    color:var(--ambar-500);
    transition:color .3s;
  }
  header.scrolled .brand em{color:var(--oliva-700)}

  nav.menu ul{
    display:flex;
    gap:36px;
    list-style:none;
  }
  nav.menu a{
    font-size:.83rem;
    font-weight:500;
    letter-spacing:.02em;
    color:rgba(255,255,255,.85);
    position:relative;
    padding:6px 0;
    transition:color .25s;
  }
  header.scrolled nav.menu a{color:var(--cinza-700)}
  nav.menu a::after{
    content:'';
    position:absolute;
    left:0;bottom:0;
    width:0;height:1.5px;
    background:var(--ambar-600);
    transition:width .3s ease;
  }
  nav.menu a:hover{color:var(--branco)}
  header.scrolled nav.menu a:hover{color:var(--petroleo-900)}
  nav.menu a:hover::after{width:100%}

  .nav-cta{
    display:inline-flex;
    align-items:center;
    gap:10px;
    font-size:.82rem;
    font-weight:600;
    letter-spacing:.02em;
    padding:12px 22px;
    border-radius:4px;
    background:var(--ambar-500);
    color:var(--petroleo-900);
    transition:all .25s ease;
    border:1px solid var(--ambar-500);
  }
  .nav-cta:hover{
    background:var(--ambar-600);
    border-color:var(--ambar-600);
  }
  header.scrolled .nav-cta{
    background:var(--petroleo-800);
    color:var(--branco);
    border-color:var(--petroleo-800);
  }
  header.scrolled .nav-cta:hover{
    background:var(--petroleo-700);
    border-color:var(--petroleo-700);
  }

  .nav-toggle{
    display:none;
    width:40px;height:40px;
    border:1px solid rgba(255,255,255,.25);
    border-radius:4px;
    background:transparent;
    color:var(--branco);
    font-size:1rem;
    align-items:center;
    justify-content:center;
    transition:all .25s;
  }
  header.scrolled .nav-toggle{
    color:var(--petroleo-900);
    border-color:var(--linha);
  }

  /* ============ HERO ============ */
  .hero{
    position:relative;
    min-height:92vh;
    display:flex;
    align-items:center;
    padding:180px 0 120px;
    color:var(--branco);
    overflow:hidden;
    background:
      linear-gradient(135deg,rgba(10,28,38,.96) 0%,rgba(15,40,54,.92) 50%,rgba(30,74,94,.86) 100%),
      url('https://images.unsplash.com/photo-1500382017468-9049fed747ef?q=80&w=2000&auto=format&fit=crop') center/cover no-repeat;
  }
  .hero::before{
    content:'';
    position:absolute;
    inset:0;
    background:
      repeating-linear-gradient(90deg,
        rgba(224,162,51,.04) 0px,
        rgba(224,162,51,.04) 1px,
        transparent 1px,
        transparent 96px);
    pointer-events:none;
    mask-image:linear-gradient(90deg,transparent,black 25%,black 75%,transparent);
    -webkit-mask-image:linear-gradient(90deg,transparent,black 25%,black 75%,transparent);
  }
  .hero::after{
    content:'';
    position:absolute;
    bottom:0;left:0;right:0;
    height:1px;
    background:linear-gradient(90deg,transparent,rgba(224,162,51,.4),transparent);
  }

  .hero-inner{
    position:relative;
    z-index:2;
    display:grid;
    grid-template-columns:1.15fr .85fr;
    gap:90px;
    align-items:end;
    width:100%;
  }

  .hero .eyebrow{color:var(--ambar-500);margin-bottom:32px}
  .hero .eyebrow::before{background:var(--ambar-500)}

  .hero h1{
    font-size:clamp(2.4rem,4.6vw,4rem);
    color:var(--branco);
    font-weight:300;
    letter-spacing:-.03em;
    line-height:1.08;
    margin-bottom:32px;
    max-width:18ch;
  }
  .hero h1 em{
    font-style:italic;
    font-weight:400;
    color:var(--ambar-300);
  }

  .hero-lede{
    font-size:1.05rem;
    color:rgba(255,255,255,.78);
    max-width:56ch;
    margin-bottom:48px;
    font-weight:300;
    line-height:1.75;
  }

  .hero-actions{
    display:flex;
    flex-wrap:wrap;
    gap:14px;
    align-items:center;
  }

  .btn{
    display:inline-flex;
    align-items:center;
    gap:12px;
    padding:16px 30px;
    border-radius:4px;
    font-family:'Inter',sans-serif;
    font-size:.85rem;
    font-weight:600;
    letter-spacing:.02em;
    cursor:pointer;
    border:1px solid transparent;
    transition:all .25s ease;
    white-space:nowrap;
  }
  .btn i{transition:transform .25s ease;font-size:.75rem}
  .btn:hover i{transform:translateX(3px)}

  .btn-primary{
    background:var(--ambar-500);
    color:var(--petroleo-900);
    border-color:var(--ambar-500);
  }
  .btn-primary:hover{
    background:var(--ambar-600);
    border-color:var(--ambar-600);
  }

  .btn-ghost{
    background:transparent;
    color:var(--branco);
    border-color:rgba(255,255,255,.3);
  }
  .btn-ghost:hover{
    border-color:var(--branco);
    background:rgba(255,255,255,.06);
  }

  .btn-dark{
    background:var(--petroleo-800);
    color:var(--branco);
    border-color:var(--petroleo-800);
  }
  .btn-dark:hover{
    background:var(--petroleo-700);
    border-color:var(--petroleo-700);
  }

  /* Stats verticais no hero */
  .hero-stats{
    border-left:1px solid rgba(255,255,255,.15);
    padding-left:48px;
    display:flex;
    flex-direction:column;
    gap:36px;
  }
  .stat{
    display:flex;
    flex-direction:column;
    gap:6px;
  }
  .stat-num{
    font-family:'Fraunces',serif;
    font-size:2.6rem;
    font-weight:300;
    color:var(--branco);
    letter-spacing:-.03em;
    line-height:1;
  }
  .stat-num sup{
    font-size:1.15rem;
    color:var(--ambar-500);
    margin-left:2px;
    font-family:'Inter',sans-serif;
    font-weight:500;
  }
  .stat-label{
    font-family:'JetBrains Mono',monospace;
    font-size:.68rem;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:rgba(255,255,255,.55);
    font-weight:500;
  }

  /* ============ TRUST ============ */
  .trust{
    background:var(--cinza-50);
    padding:40px 0;
    border-bottom:1px solid var(--linha);
  }
  .trust-inner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:40px;
    flex-wrap:wrap;
  }
  .trust-label{
    font-family:'JetBrains Mono',monospace;
    font-size:.68rem;
    letter-spacing:.18em;
    text-transform:uppercase;
    color:var(--cinza-500);
    font-weight:500;
  }
  .trust-items{
    display:flex;
    gap:56px;
    flex-wrap:wrap;
    align-items:center;
  }
  .trust-item{
    font-family:'Fraunces',serif;
    font-size:1.08rem;
    color:var(--petroleo-700);
    opacity:.55;
    font-weight:500;
    letter-spacing:-.01em;
    transition:opacity .25s;
  }
  .trust-item:hover{opacity:1}

  /* ============ SECTION HEAD ============ */
  section.block{padding:130px 0}
  .section-head{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:80px;
    align-items:end;
    margin-bottom:88px;
  }
  .section-head h2{
    font-size:clamp(2rem,3.4vw,2.85rem);
    font-weight:300;
    letter-spacing:-.03em;
    margin-top:22px;
    line-height:1.12;
  }
  .section-head h2 em{
    font-style:italic;
    color:var(--ambar-700);
  }
  .section-head p{
    color:var(--cinza-700);
    font-size:1rem;
    line-height:1.8;
    max-width:48ch;
    font-weight:300;
  }

  /* ============ PILARES TÉCNICOS ============ */
  .pillars{background:var(--branco)}
  .pillars-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:0;
    border-top:1px solid var(--linha);
    border-left:1px solid var(--linha);
  }
  .pillar{
    position:relative;
    background:var(--branco);
    padding:52px 44px;
    display:flex;
    flex-direction:column;
    gap:20px;
    border-right:1px solid var(--linha);
    border-bottom:1px solid var(--linha);
    transition:background .3s ease;
  }
  .pillar::before{
    content:'';
    position:absolute;
    top:-1px;left:-1px;
    width:0;height:2px;
    background:var(--ambar-600);
    transition:width .4s ease;
  }
  .pillar:hover{background:var(--cinza-50)}
  .pillar:hover::before{width:calc(100% + 2px)}

  .pillar-head{
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-bottom:6px;
  }
  .pillar-tag{
    display:inline-flex;
    align-items:center;
    gap:10px;
    font-family:'JetBrains Mono',monospace;
    font-size:.68rem;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:var(--ambar-700);
    font-weight:500;
  }
  .pillar-tag::before{
    content:'';
    width:20px;height:1px;
    background:var(--ambar-700);
  }

  .pillar-icon{
    width:48px;height:48px;
    border-radius:6px;
    background:var(--petroleo-800);
    color:var(--ambar-500);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:1.05rem;
    transition:background .3s;
  }
  .pillar:hover .pillar-icon{
    background:var(--oliva-700);
    color:var(--ambar-300);
  }

  .pillar h3{
    font-size:1.5rem;
    font-weight:400;
    color:var(--petroleo-900);
    letter-spacing:-.02em;
    line-height:1.2;
  }

  .pillar > p{
    color:var(--cinza-700);
    font-size:.93rem;
    line-height:1.75;
    font-weight:300;
  }

  .pillar-list{
    list-style:none;
    margin-top:auto;
    padding-top:24px;
    border-top:1px solid var(--linha);
    display:flex;
    flex-direction:column;
    gap:10px;
  }
  .pillar-list li{
    font-size:.85rem;
    color:var(--petroleo-700);
    display:flex;
    align-items:flex-start;
    gap:10px;
    font-weight:400;
    line-height:1.55;
  }
  .pillar-list li::before{
    content:'';
    width:5px;height:5px;
    border-radius:50%;
    background:var(--oliva-500);
    flex-shrink:0;
    margin-top:8px;
  }

  /* ============ MÉTODO ============ */
  .process{
    background:var(--cinza-50);
  }
  .process-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:0;
  }
  .process-step{
    padding:40px 32px 40px 0;
    border-top:2px solid var(--petroleo-800);
    margin-right:32px;
    position:relative;
  }
  .process-step:last-child{margin-right:0}
  .process-step .step-num{
    font-family:'Fraunces',serif;
    font-size:3rem;
    font-weight:300;
    color:var(--ambar-600);
    opacity:.35;
    line-height:1;
    letter-spacing:-.04em;
    margin-bottom:22px;
  }
  .process-step h4{
    font-size:1.2rem;
    font-weight:500;
    color:var(--petroleo-900);
    margin-bottom:14px;
    letter-spacing:-.01em;
  }
  .process-step p{
    font-size:.89rem;
    color:var(--cinza-700);
    line-height:1.75;
    font-weight:300;
  }

  /* ============ DIFERENCIAIS ============ */
  .differentials{
    background:var(--petroleo-900);
    color:var(--branco);
    padding:140px 0;
    position:relative;
    overflow:hidden;
  }
  .differentials::before{
    content:'';
    position:absolute;
    inset:0;
    background:
      repeating-linear-gradient(90deg,
        rgba(255,255,255,.02) 0px,
        rgba(255,255,255,.02) 1px,
        transparent 1px,
        transparent 96px);
    pointer-events:none;
  }
  .diff-grid{
    display:grid;
    grid-template-columns:1fr 1.1fr;
    gap:100px;
    align-items:start;
    position:relative;
    z-index:2;
  }
  .diff-left .eyebrow{color:var(--ambar-500)}
  .diff-left .eyebrow::before{background:var(--ambar-500)}
  .diff-left h2{
    color:var(--branco);
    font-size:clamp(1.9rem,3.2vw,2.75rem);
    font-weight:300;
    letter-spacing:-.03em;
    margin:24px 0 28px;
    line-height:1.15;
  }
  .diff-left h2 em{font-style:italic;color:var(--ambar-300)}
  .diff-left p{
    color:rgba(255,255,255,.65);
    font-size:.98rem;
    line-height:1.85;
    font-weight:300;
    max-width:46ch;
    margin-bottom:44px;
  }
  .diff-list{
    display:flex;
    flex-direction:column;
  }
  .diff-item{
    display:grid;
    grid-template-columns:60px 1fr;
    gap:32px;
    padding:34px 0;
    border-top:1px solid var(--linha-escura);
    transition:padding-left .3s ease;
  }
  .diff-item:last-child{border-bottom:1px solid var(--linha-escura)}
  .diff-item:hover{padding-left:8px}
  .diff-item-icon{
    width:52px;height:52px;
    border-radius:6px;
    background:rgba(224,162,51,.08);
    border:1px solid rgba(224,162,51,.25);
    display:flex;align-items:center;justify-content:center;
    color:var(--ambar-500);
    font-size:1.05rem;
    transition:all .3s;
  }
  .diff-item:hover .diff-item-icon{
    background:rgba(224,162,51,.15);
    border-color:var(--ambar-500);
  }
  .diff-item h4{
    color:var(--branco);
    font-size:1.18rem;
    font-weight:400;
    letter-spacing:-.01em;
    margin-bottom:8px;
  }
  .diff-item p{
    color:rgba(255,255,255,.55);
    font-size:.9rem;
    line-height:1.75;
    font-weight:300;
    margin:0;
  }

  /* ============ DEPOIMENTOS ============ */
  .testimonials{background:var(--branco)}
  .testimonials-grid{
    display:grid;
    grid-template-columns:1fr 1fr 1fr;
    gap:0;
    border-top:1px solid var(--linha);
    border-left:1px solid var(--linha);
  }
  .testimonial{
    background:var(--branco);
    padding:44px 36px;
    border-right:1px solid var(--linha);
    border-bottom:1px solid var(--linha);
    display:flex;
    flex-direction:column;
    gap:24px;
    position:relative;
    transition:background .3s ease;
  }
  .testimonial:hover{background:var(--cinza-50)}
  .testimonial-stars{
    display:flex;gap:3px;color:var(--ambar-600);font-size:.75rem;
  }
  .testimonial-quote{
    font-family:'Fraunces',serif;
    font-size:1.05rem;
    line-height:1.6;
    color:var(--petroleo-900);
    font-weight:400;
    font-style:italic;
    letter-spacing:-.005em;
  }
  .testimonial-author{
    display:flex;
    align-items:center;
    gap:14px;
    padding-top:22px;
    border-top:1px solid var(--linha);
    margin-top:auto;
  }
  .testimonial-author img{
    width:44px;height:44px;
    border-radius:50%;
    object-fit:cover;
    filter:grayscale(100%);
    transition:filter .3s;
  }
  .testimonial:hover .testimonial-author img{filter:grayscale(0)}
  .author-meta strong{
    display:block;
    font-size:.9rem;
    font-weight:600;
    color:var(--petroleo-900);
  }
  .author-meta span{
    font-size:.76rem;
    color:var(--cinza-500);
    letter-spacing:.02em;
  }

  /* ============ CTA / CONTATO ============ */
  .cta-section{
    background:var(--petroleo-800);
    color:var(--branco);
    padding:130px 0;
    position:relative;
    overflow:hidden;
  }
  .cta-section::before{
    content:'';
    position:absolute;
    inset:0;
    background:
      repeating-linear-gradient(90deg,
        rgba(255,255,255,.02) 0px,
        rgba(255,255,255,.02) 1px,
        transparent 1px,
        transparent 96px);
    pointer-events:none;
  }
  .cta-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:100px;
    position:relative;
    z-index:2;
    align-items:start;
  }
  .cta-info .eyebrow{color:var(--ambar-500)}
  .cta-info .eyebrow::before{background:var(--ambar-500)}
  .cta-info h2{
    color:var(--branco);
    font-size:clamp(1.9rem,3.2vw,2.75rem);
    font-weight:300;
    letter-spacing:-.03em;
    margin:24px 0 28px;
    line-height:1.15;
    max-width:16ch;
  }
  .cta-info h2 em{font-style:italic;color:var(--ambar-300)}
  .cta-info > p{
    color:rgba(255,255,255,.7);
    font-size:.98rem;
    line-height:1.8;
    font-weight:300;
    max-width:46ch;
    margin-bottom:52px;
  }
  .contact-list{
    display:flex;
    flex-direction:column;
  }
  .contact-line{
    display:flex;
    align-items:center;
    gap:20px;
    padding:22px 0;
    border-top:1px solid var(--linha-escura);
  }
  .contact-line:last-child{border-bottom:1px solid var(--linha-escura)}
  .contact-line i{
    color:var(--ambar-500);
    font-size:.95rem;
    width:24px;
    text-align:center;
  }
  .contact-line .cl-label{
    font-family:'JetBrains Mono',monospace;
    font-size:.66rem;
    text-transform:uppercase;
    letter-spacing:.16em;
    color:rgba(255,255,255,.4);
    display:block;
    margin-bottom:3px;
    font-weight:500;
  }
  .contact-line .cl-value{
    color:var(--branco);
    font-size:.96rem;
    font-weight:400;
  }

  .form-card{
    background:var(--branco);
    border-radius:6px;
    padding:52px 44px;
    color:var(--tinta);
    box-shadow:0 20px 60px -30px rgba(0,0,0,.4);
  }
  .form-card h3{
    font-size:1.55rem;
    font-weight:400;
    letter-spacing:-.02em;
    color:var(--petroleo-900);
    margin-bottom:8px;
  }
  .form-card .form-sub{
    font-size:.86rem;
    color:var(--cinza-500);
    margin-bottom:36px;
    letter-spacing:.01em;
  }
  .field{
    position:relative;
    margin-bottom:24px;
  }
  .field label{
    display:block;
    font-family:'JetBrains Mono',monospace;
    font-size:.66rem;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:var(--cinza-700);
    font-weight:500;
    margin-bottom:10px;
  }
  .field input,
  .field select,
  .field textarea{
    width:100%;
    border:none;
    border-bottom:1px solid var(--linha);
    background:transparent;
    padding:10px 0 12px;
    font-family:'Inter',sans-serif;
    font-size:.96rem;
    color:var(--tinta);
    transition:border-color .25s;
    border-radius:0;
    font-weight:400;
  }
  .field select{
    appearance:none;
    background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 12 12'%3E%3Cpath fill='%233d4d59' d='M6 9L1 4h10z'/%3E%3C/svg%3E");
    background-repeat:no-repeat;
    background-position:right 4px center;
    cursor:pointer;
  }
  .field textarea{resize:none;min-height:80px}
  .field input:focus,
  .field select:focus,
  .field textarea:focus{
    outline:none;
    border-bottom-color:var(--petroleo-600);
  }
  .field input::placeholder,
  .field textarea::placeholder{
    color:#b8c0c8;
    font-weight:300;
  }
  .field.valid input,
  .field.valid select{border-bottom-color:var(--oliva-500)}
  .field.invalid input,
  .field.invalid select{border-bottom-color:#c0392b}
  .field .error-msg{
    font-size:.72rem;
    color:#c0392b;
    margin-top:6px;
    display:none;
  }
  .field.invalid .error-msg{display:block}

  .form-card .btn{
    width:100%;
    justify-content:center;
    margin-top:12px;
    padding:18px;
  }
  .form-note{
    font-size:.73rem;
    color:var(--cinza-500);
    margin-top:18px;
    text-align:center;
    line-height:1.65;
  }

  /* ============ FOOTER ============ */
  footer{
    background:var(--petroleo-900);
    color:rgba(255,255,255,.65);
    padding:88px 0 40px;
  }
  .footer-top{
    display:grid;
    grid-template-columns:1.6fr 1fr 1fr 1fr;
    gap:60px;
    padding-bottom:56px;
    border-bottom:1px solid var(--linha-escura);
  }
  .footer-brand{
    display:flex;
    align-items:center;
    gap:12px;
    font-family:'Fraunces',serif;
    font-size:1.25rem;
    color:var(--branco);
    font-weight:400;
    margin-bottom:22px;
  }
  .footer-brand em{font-style:normal;color:var(--ambar-500)}
  .footer-brand .brand-mark{
    background:var(--petroleo-700);
    color:var(--ambar-500);
  }
  .footer-desc{
    font-size:.88rem;
    line-height:1.8;
    font-weight:300;
    max-width:34ch;
    color:rgba(255,255,255,.5);
    margin-bottom:30px;
  }
  .footer-social{
    display:flex;
    gap:10px;
  }
  .footer-social a{
    width:40px;height:40px;
    border:1px solid rgba(255,255,255,.15);
    border-radius:4px;
    display:flex;align-items:center;justify-content:center;
    color:rgba(255,255,255,.65);
    font-size:.88rem;
    transition:all .25s;
  }
  .footer-social a:hover{
    background:var(--ambar-500);
    border-color:var(--ambar-500);
    color:var(--petroleo-900);
  }
  .footer-col h5{
    font-family:'JetBrains Mono',monospace;
    font-size:.66rem;
    letter-spacing:.18em;
    text-transform:uppercase;
    color:var(--ambar-500);
    font-weight:500;
    margin-bottom:24px;
  }
  .footer-col ul{list-style:none;display:flex;flex-direction:column;gap:13px}
  .footer-col a{
    font-size:.88rem;
    color:rgba(255,255,255,.6);
    font-weight:300;
    transition:color .25s;
    display:inline-block;
  }
  .footer-col a:hover{color:var(--ambar-300)}
  .footer-bottom{
    padding-top:32px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:20px;
    font-size:.76rem;
    color:rgba(255,255,255,.4);
    letter-spacing:.02em;
  }
  .footer-bottom a{color:rgba(255,255,255,.55);transition:color .25s}
  .footer-bottom a:hover{color:var(--ambar-300)}

  /* ============ WHATSAPP ============ */
  .wa-float{
    position:fixed;
    bottom:32px;right:32px;
    width:56px;height:56px;
    border-radius:6px;
    background:var(--ambar-500);
    color:var(--petroleo-900);
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:1.4rem;
    z-index:900;
    box-shadow:0 10px 30px -10px rgba(224,162,51,.5);
    transition:all .25s ease;
  }
  .wa-float:hover{
    background:var(--ambar-600);
    transform:translateY(-2px);
  }
  .wa-float .tooltip{
    position:absolute;
    right:calc(100% + 14px);
    top:50%;
    transform:translateY(-50%) translateX(6px);
    background:var(--petroleo-900);
    color:var(--branco);
    font-size:.76rem;
    font-weight:500;
    padding:8px 14px;
    border-radius:4px;
    white-space:nowrap;
    opacity:0;
    pointer-events:none;
    transition:all .25s ease;
    box-shadow:0 10px 24px -8px rgba(0,0,0,.4);
  }
  .wa-float .tooltip::after{
    content:'';
    position:absolute;
    left:100%;top:50%;
    transform:translateY(-50%);
    border:5px solid transparent;
    border-left-color:var(--petroleo-900);
  }
  .wa-float:hover .tooltip{
    opacity:1;
    transform:translateY(-50%) translateX(0);
  }

  /* ============ ANIMAÇÕES (sutis) ============ */
  .reveal{
    opacity:0;
    transform:translateY(20px);
    transition:opacity .8s cubic-bezier(.2,.8,.2,1),transform .8s cubic-bezier(.2,.8,.2,1);
  }
  .reveal.visible{opacity:1;transform:none}
  .reveal-delay-1{transition-delay:.1s}
  .reveal-delay-2{transition-delay:.18s}
  .reveal-delay-3{transition-delay:.26s}

  /* Barra de progresso no topo */
  .scroll-progress{
    position:fixed;
    top:0;left:0;
    height:2px;
    background:var(--ambar-600);
    z-index:1001;
    width:0;
    transition:width .1s linear;
  }

  /* Menu mobile */
  .mobile-menu{
    position:fixed;
    inset:0;
    background:var(--petroleo-900);
    z-index:999;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    gap:6px;
    opacity:0;
    pointer-events:none;
    transition:opacity .3s ease;
  }
  .mobile-menu.open{opacity:1;pointer-events:auto}
  .mobile-menu a{
    font-family:'Fraunces',serif;
    font-size:1.5rem;
    color:var(--branco);
    padding:14px 28px;
    border-radius:4px;
    transition:all .25s;
    transform:translateY(14px);
    opacity:0;
  }
  .mobile-menu.open a{
    transform:translateY(0);
    opacity:1;
  }
  .mobile-menu a:nth-child(1){transition-delay:.08s}
  .mobile-menu a:nth-child(2){transition-delay:.12s}
  .mobile-menu a:nth-child(3){transition-delay:.16s}
  .mobile-menu a:nth-child(4){transition-delay:.2s}
  .mobile-menu a:nth-child(5){transition-delay:.24s}
  .mobile-menu a:hover{color:var(--ambar-500)}
  .mobile-menu .close-btn{
    position:absolute;
    top:24px;right:24px;
    width:44px;height:44px;
    border:1px solid rgba(255,255,255,.2);
    border-radius:4px;
    background:transparent;
    color:var(--branco);
    font-size:1.1rem;
    display:flex;align-items:center;justify-content:center;
    transition:all .25s;
  }
  .mobile-menu .close-btn:hover{
    background:var(--ambar-500);
    color:var(--petroleo-900);
    border-color:var(--ambar-500);
  }

  /* ============ RESPONSIVO ============ */
  @media (max-width:1080px){
    .hero-inner{grid-template-columns:1fr;gap:56px;align-items:start}
    .hero-stats{
      flex-direction:row;
      flex-wrap:wrap;
      gap:40px;
      padding-left:0;
      border-left:none;
      border-top:1px solid rgba(255,255,255,.15);
      padding-top:40px;
    }
    .pillars-grid{grid-template-columns:1fr}
    .diff-grid{grid-template-columns:1fr;gap:60px}
    .cta-grid{grid-template-columns:1fr;gap:60px}
    .footer-top{grid-template-columns:1fr 1fr}
    .section-head{grid-template-columns:1fr;gap:32px;margin-bottom:64px}
    .process-grid{grid-template-columns:1fr 1fr;gap:0}
    .process-step{margin-right:24px;padding:36px 24px 36px 0}
    .testimonials-grid{grid-template-columns:1fr 1fr}
  }
  @media (max-width:820px){
    .container{padding:0 24px}
    nav.menu{display:none}
    .nav-toggle{display:flex}
    .nav-cta{display:none}
    .testimonials-grid{grid-template-columns:1fr}
    .form-card{padding:44px 30px}
    section.block{padding:90px 0}
    .differentials,.cta-section{padding:90px 0}
    .footer-top{grid-template-columns:1fr;gap:44px}
    .pillar{padding:40px 32px}
    .hero{padding:140px 0 90px;min-height:auto}
  }
  @media (max-width:560px){
    .hero h1{font-size:2.1rem}
    .hero-actions{flex-direction:column;align-items:stretch}
    .hero-actions .btn{justify-content:center}
    .hero-stats{gap:28px}
    .stat-num{font-size:2rem}
    .process-grid{grid-template-columns:1fr}
    .process-step{margin-right:0;padding:30px 0}
    .trust-items{gap:24px}
    .trust-item{font-size:.95rem}
    .wa-float{width:50px;height:50px;bottom:22px;right:22px;font-size:1.25rem}
    .wa-float .tooltip{display:none}
    .brand{font-size:1.1rem}
    .brand-mark{width:32px;height:32px}
    .form-card{padding:36px 24px}
  }
</style>
</head>
<body>

<!-- Scroll progress -->
<div class="scroll-progress" id="scrollProgress"></div>

<!-- ================= MOBILE MENU ================= -->
<div class="mobile-menu" id="mobileMenu">
  <button class="close-btn" id="closeMenu" aria-label="Fechar menu"><i class="fas fa-times"></i></button>
  <a href="#pilares">Pilares técnicos</a>
  <a href="#metodo">Método</a>
  <a href="#diferenciais">Diferenciais</a>
  <a href="#depoimentos">Resultados</a>
  <a href="#contato">Contato</a>
</div>

<!-- ================= HEADER ================= -->
<header id="site-header">
  <div class="container nav-inner">
    <a href="#" class="brand">
      <span class="brand-mark"><i class="fas fa-seedling"></i></span>
      Agro<em>Consultoria</em>
    </a>

    <nav class="menu">
      <ul>
        <li><a href="#pilares">Pilares técnicos</a></li>
        <li><a href="#metodo">Método</a></li>
        <li><a href="#diferenciais">Diferenciais</a></li>
        <li><a href="#depoimentos">Resultados</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>

    <a href="#contato" class="nav-cta">
      Agendar diagnóstico <i class="fas fa-arrow-right"></i>
    </a>

    <button class="nav-toggle" id="openMenu" aria-label="Abrir menu">
      <i class="fas fa-bars"></i>
    </button>
  </div>
</header>

<!-- ================= HERO ================= -->
<section class="hero">
  <div class="container hero-inner">
    <div class="reveal">
      <span class="eyebrow">Rastreabilidade · Genética · Performance</span>
      <h1>Do grão ao mercado, <em>cada etapa</em> sob controle técnico.</h1>
      <p class="hero-lede">
        Consultoria agronômica especializada em rastreabilidade de cadeia produtiva, melhoramento genético e compliance para produtores que acessam mercados exigentes — exportação, certificação e programas de sustentabilidade.
      </p>
      <div class="hero-actions">
        <a href="#contato" class="btn btn-primary">
          Solicitar diagnóstico <i class="fas fa-arrow-right"></i>
        </a>
        <a href="#pilares" class="btn btn-ghost">Pilares técnicos</a>
      </div>
    </div>

    <div class="hero-stats reveal reveal-delay-1">
      <div class="stat">
        <span class="stat-num">100<sup>%</sup></span>
        <span class="stat-label">Lotes rastreáveis</span>
      </div>
      <div class="stat">
        <span class="stat-num">42<sup>mil</sup></span>
        <span class="stat-label">Hectares monitorados</span>
      </div>
      <div class="stat">
        <span class="stat-num">18<sup>%</sup></span>
        <span class="stat-label">Ganho médio de produtividade</span>
      </div>
    </div>
  </div>
</section>

<!-- ================= TRUST ================= -->
<section class="trust">
  <div class="container trust-inner">
    <span class="trust-label">Certificações e parcerias técnicas</span>
    <div class="trust-items">
      <span class="trust-item">GlobalG.A.P.</span>
      <span class="trust-item">Rainforest Alliance</span>
      <span class="trust-item">RTRS</span>
      <span class="trust-item">ProTerra</span>
      <span class="trust-item">Embrapa</span>
    </div>
  </div>
</section>

<!-- ================= PILARES TÉCNICOS ================= -->
<section class="block pillars" id="pilares">
  <div class="container">
    <div class="section-head reveal">
      <div>
        <span class="eyebrow">Pilares técnicos</span>
        <h2>Quatro frentes que sustentam a <em>alta performance</em> no campo.</h2>
      </div>
      <p>
        Atuamos onde a agronomia encontra a exigência de mercado: rastrear cada lote, escolher a genética certa, monitorar com precisão e comprovar conformidade. Tudo com indicadores claros e auditáveis.
      </p>
    </div>

    <div class="pillars-grid">

      <article class="pillar reveal">
        <div class="pillar-head">
          <span class="pillar-tag">Pilar 01</span>
          <div class="pillar-icon"><i class="fas fa-qrcode"></i></div>
        </div>
        <h3>Rastreabilidade de ponta a ponta</h3>
        <p>
          Estruturamos sistemas que registram cada etapa da produção — do lote de semente ao produto final — com dados auditáveis e conformes às exigências de compradores nacionais e internacionais.
        </p>
        <ul class="pillar-list">
          <li>Identificação de talhões e lotes</li>
          <li>Registro digital de insumos e operações</li>
          <li>Rastreio por QR Code e blockchain</li>
          <li>Conformidade com EUDR e exigências de exportação</li>
        </ul>
      </article>

      <article class="pillar reveal reveal-delay-1">
        <div class="pillar-head">
          <span class="pillar-tag">Pilar 02</span>
          <div class="pillar-icon"><i class="fas fa-dna"></i></div>
        </div>
        <h3>Melhoramento genético e cultivares</h3>
        <p>
          Selecionamos cultivares e híbridos com base em desempenho regional, histórico de produtividade e tolerância a estresses. A genética certa no ambiente certo.
        </p>
        <ul class="pillar-list">
          <li>Ensaio e seleção de cultivares por ambiente</li>
          <li>Análise de adaptabilidade e estabilidade</li>
          <li>Recomendação por zoneamento e histórico</li>
          <li>Programas de melhoramento participativo</li>
        </ul>
      </article>

      <article class="pillar reveal reveal-delay-2">
        <div class="pillar-head">
          <span class="pillar-tag">Pilar 03</span>
          <div class="pillar-icon"><i class="fas fa-satellite"></i></div>
        </div>
        <h3>Monitoramento e agricultura de precisão</h3>
        <p>
          Drones, imagens de satélite e sensores em campo para transformar dados brutos em decisões agronômicas no tempo certo, com mapas de produtividade e alertas precoces.
        </p>
        <ul class="pillar-list">
          <li>Índices de vegetação (NDVI, NDRE)</li>
          <li>Mapas de produtividade e fertilidade</li>
          <li>Alertas fitossanitários e climáticos</li>
          <li>Taxa variável de insumos</li>
        </ul>
      </article>

      <article class="pillar reveal reveal-delay-3">
        <div class="pillar-head">
          <span class="pillar-tag">Pilar 04</span>
          <div class="pillar-icon"><i class="fas fa-clipboard-check"></i></div>
        </div>
        <h3>Certificação e compliance socioambiental</h3>
        <p>
          Preparamos a propriedade para auditorias, certificações e exigências de compradores. Do diagnóstico de conformidade à manutenção do selo, com documentação organizada.
        </p>
        <ul class="pillar-list">
          <li>Diagnóstico de conformidade legal</li>
          <li>Preparação para auditorias (GlobalG.A.P., RTRS)</li>
          <li>Compliance socioambiental e trabalhista</li>
          <li>Regularização ambiental e CAR</li>
        </ul>
      </article>

    </div>
  </div>
</section>

<!-- ================= MÉTODO ================= -->
<section class="block process" id="metodo">
  <div class="container">
    <div class="section-head reveal">
      <div>
        <span class="eyebrow">Como trabalhamos</span>
        <h2>Um método <em>auditável</em>, do diagnóstico à colheita.</h2>
      </div>
      <p>
        Cada etapa é documentada e mensurável. Você acompanha o que está sendo feito, por que está sendo feito e qual o impacto esperado em produtividade e conformidade.
      </p>
    </div>

    <div class="process-grid">
      <div class="process-step reveal">
        <div class="step-num">01</div>
        <h4>Diagnóstico técnico</h4>
        <p>Levantamento de solo, histórico produtivo, conformidade legal e análise de rastreabilidade atual da propriedade.</p>
      </div>
      <div class="process-step reveal reveal-delay-1">
        <div class="step-num">02</div>
        <h4>Plano agronômico</h4>
        <p>Definição de cultivares, metas de produtividade, cronograma de operações e estrutura de rastreabilidade.</p>
      </div>
      <div class="process-step reveal reveal-delay-2">
        <div class="step-num">03</div>
        <h4>Execução assistida</h4>
        <p>Acompanhamento em campo e remoto, ajustes fitossanitários e registro digital de cada etapa do ciclo.</p>
      </div>
      <div class="process-step reveal reveal-delay-3">
        <div class="step-num">04</div>
        <h4>Verificação e relatório</h4>
        <p>Mensuração de resultados, relatório de rastreabilidade e revisão do plano para a próxima safra.</p>
      </div>
    </div>
  </div>
</section>

<!-- ================= DIFERENCIAIS ================= -->
<section class="differentials" id="diferenciais">
  <div class="container diff-grid">
    <div class="diff-left reveal">
      <span class="eyebrow">Nossos diferenciais</span>
      <h2>Agronomia de precisão com <em>visão de mercado</em>.</h2>
      <p>
        Não entregamos apenas recomendações técnicas. Entregamos a capacidade de comprovar, rastrear e valorizar cada lote produzido — do campo à mesa do comprador.
      </p>
    </div>

    <div class="diff-list">
      <div class="diff-item reveal">
        <div class="diff-item-icon"><i class="fas fa-user-graduate"></i></div>
        <div>
          <h4>Equipe sênior multidisciplinar</h4>
          <p>Agrônomos, geneticistas, especialistas em rastreabilidade e auditores com vivência em cadeias exportadoras.</p>
        </div>
      </div>
      <div class="diff-item reveal reveal-delay-1">
        <div class="diff-item-icon"><i class="fas fa-fingerprint"></i></div>
        <div>
          <h4>Rastreabilidade auditável</h4>
          <p>Estrutura de dados que resiste a auditorias de certificadoras e exigências de compradores internacionais.</p>
        </div>
      </div>
      <div class="diff-item reveal reveal-delay-2">
        <div class="diff-item-icon"><i class="fas fa-microscope"></i></div>
        <div>
          <h4>Genética orientada a resultado</h4>
          <p>Seleção de cultivares baseada em dados regionais, não em catálogos genéricos de fornecedores.</p>
        </div>
      </div>
      <div class="diff-item reveal reveal-delay-3">
        <div class="diff-item-icon"><i class="fas fa-globe"></i></div>
        <div>
          <h4>Prontidão para exportação</h4>
          <p>Preparação técnica e documental para atender EUDR, GlobalG.A.P., RTRS e exigências de mercados premium.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ================= DEPOIMENTOS ================= -->
<section class="block testimonials" id="depoimentos">
  <div class="container">
    <div class="section-head reveal">
      <div>
        <span class="eyebrow">Resultados comprovados</span>
        <h2>Quem rastreia, <em>vale mais</em>.</h2>
      </div>
      <p>
        Produtores que estruturaram rastreabilidade e melhoraram a base genética acessaram contratos melhores, reduziram perdas e elevaram a rentabilidade por hectare.
      </p>
    </div>

    <div class="testimonials-grid">
      <article class="testimonial reveal">
        <div class="testimonial-stars">
          <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
        </div>
        <p class="testimonial-quote">
          A rastreabilidade que estruturaram nos abriu a porta de um comprador europeu que exige conformidade com a EUDR. Sem isso, estaríamos fora.
        </p>
        <div class="testimonial-author">
          <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Carlos Mendes">
          <div class="author-meta">
            <strong>Carlos Mendes</strong>
            <span>Soja · Sorriso, MT</span>
          </div>
        </div>
      </article>

      <article class="testimonial reveal reveal-delay-1">
        <div class="testimonial-stars">
          <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
        </div>
        <p class="testimonial-quote">
          Trocaram nossas cultivares com base em ensaios regionais e o ganho foi imediato. Melhoramento genético com critério técnico, não com palpite.
        </p>
        <div class="testimonial-author">
          <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Juliana Rocha">
          <div class="author-meta">
            <strong>Juliana Rocha</strong>
            <span>Café especial · Patrocínio, MG</span>
          </div>
        </div>
      </article>

      <article class="testimonial reveal reveal-delay-2">
        <div class="testimonial-stars">
          <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
        </div>
        <p class="testimonial-quote">
          Passamos na auditoria GlobalG.A.P. na primeira tentativa. A documentação e o monitoramento digital fizeram toda a diferença.
        </p>
        <div class="testimonial-author">
          <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Ricardo Almeida">
          <div class="author-meta">
            <strong>Ricardo Almeida</strong>
            <span>Fruticultura · Petrolina, PE</span>
          </div>
        </div>
      </article>
    </div>
  </div>
</section>

<!-- ================= CTA / CONTATO ================= -->
<section class="cta-section" id="contato">
  <div class="container cta-grid">
    <div class="cta-info reveal">
      <span class="eyebrow">Vamos conversar</span>
      <h2>Pronto para tornar sua produção <em>rastreável</em> e competitiva?</h2>
      <p>
        Preencha o formulário e receba um diagnóstico inicial gratuito. Nossa equipe técnica entrará em contato em até 24 horas úteis para entender sua operação, sua cadeia produtiva e seus objetivos de mercado.
      </p>

      <div class="contact-list">
        <div class="contact-line">
          <i class="fas fa-phone"></i>
          <div>
            <span class="cl-label">Telefone</span>
            <span class="cl-value">+55 (11) 4002-8922</span>
          </div>
        </div>
        <div class="contact-line">
          <i class="fas fa-envelope"></i>
          <div>
            <span class="cl-label">E-mail</span>
            <span class="cl-value">contato@agroconsultoria.com.br</span>
          </div>
        </div>
        <div class="contact-line">
          <i class="fas fa-location-dot"></i>
          <div>
            <span class="cl-label">Escritório</span>
            <span class="cl-value">Av. das Palmeiras, 1200 — Campinas, SP</span>
          </div>
        </div>
      </div>
    </div>

    <div class="form-card reveal reveal-delay-1">
      <h3>Solicitar diagnóstico</h3>
      <p class="form-sub">Retornamos em até 24h úteis.</p>

      <form id="lead-form" novalidate>
        <div class="field">
          <label for="nome">Nome completo</label>
          <input type="text" id="nome" name="nome" placeholder="Como podemos chamá-lo" required>
          <span class="error-msg">Informe seu nome.</span>
        </div>

        <div class="field">
          <label for="email">E-mail profissional</label>
          <input type="email" id="email" name="email" placeholder="seu@email.com" required>
          <span class="error-msg">Informe um e-mail válido.</span>
        </div>

        <div class="field">
          <label for="telefone">Telefone / WhatsApp</label>
          <input type="tel" id="telefone" name="telefone" placeholder="(00) 00000-0000">
        </div>

        <div class="field">
          <label for="cultura">Cultura principal</label>
          <select id="cultura" name="cultura">
            <option value="">Selecione</option>
            <option>Soja</option>
            <option>Milho</option>
            <option>Café</option>
            <option>Cana-de-açúcar</option>
            <option>Algodão</option>
            <option>Fruticultura</option>
            <option>Pecuária</option>
            <option>Outra</option>
          </select>
        </div>

        <div class="field">
          <label for="interesse">Principal interesse</label>
          <select id="interesse" name="interesse">
            <option value="">Selecione</option>
            <option>Rastreabilidade de cadeia produtiva</option>
            <option>Melhoramento genético e cultivares</option>
            <option>Monitoramento e agricultura de precisão</option>
            <option>Certificação e compliance</option>
            <option>Diagnóstico completo</option>
          </select>
        </div>

        <div class="field">
          <label for="area">Área cultivada (hectares)</label>
          <input type="text" id="area" name="area" placeholder="Ex.: 500 ha">
        </div>

        <button type="submit" class="btn btn-dark">
          Enviar solicitação <i class="fas fa-arrow-right"></i>
        </button>

        <p class="form-note">
          Ao enviar, você concorda em ser contatado pela nossa equipe técnica. Seus dados estão protegidos conforme a LGPD.
        </p>
      </form>
    </div>
  </div>
</section>

<!-- ================= FOOTER ================= -->
<footer>
  <div class="container">
    <div class="footer-top">
      <div>
        <div class="footer-brand">
          <span class="brand-mark"><i class="fas fa-seedling"></i></span>
          Agro<em>Consultoria</em>
        </div>
        <p class="footer-desc">
          Rastreabilidade, genética e performance agronômica para produtores que acessam os mercados mais exigentes do mundo.
        </p>
        <div class="footer-social">
          <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
          <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
          <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
          <a href="#" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
        </div>
      </div>

      <div class="footer-col">
        <h5>Pilares técnicos</h5>
        <ul>
          <li><a href="#pilares">Rastreabilidade</a></li>
          <li><a href="#pilares">Melhoramento genético</a></li>
          <li><a href="#pilares">Monitoramento</a></li>
          <li><a href="#pilares">Compliance</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h5>Empresa</h5>
        <ul>
          <li><a href="#">Sobre nós</a></li>
          <li><a href="#">Equipe técnica</a></li>
          <li><a href="#">Publicações</a></li>
          <li><a href="#">Trabalhe conosco</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h5>Contato</h5>
        <ul>
          <li><a href="mailto:contato@agroconsultoria.com.br">contato@agroconsultoria.com.br</a></li>
          <li><a href="tel:+551140028922">+55 (11) 4002-8922</a></li>
          <li><a href="#">Av. das Palmeiras, 1200 — SP</a></li>
        </ul>
      </div>
    </div>

    <div class="footer-bottom">
      <span>© 2025 AgroConsultoria. Todos os direitos reservados. CNPJ 12.345.678/0001-90.</span>
      <span><a href="#">Política de Privacidade</a> · <a href="#">Termos de Uso</a></span>
    </div>
  </div>
</footer>

<a href="#" class="wa-float" aria-label="Falar no WhatsApp">
  <i class="fab fa-whatsapp"></i>
  <span class="tooltip">Fale conosco</span>
</a>

<!-- ================= SCRIPTS ================= -->
<script>
  /* ---------- Scroll Progress ---------- */
  const scrollProgress = document.getElementById('scrollProgress');
  window.addEventListener('scroll', () => {
    const total = document.documentElement.scrollHeight - window.innerHeight;
    const progress = (window.scrollY / total) * 100;
    scrollProgress.style.width = progress + '%';
  }, {passive:true});

  /* ---------- Header ---------- */
  const header = document.getElementById('site-header');
  const onScroll = () => {
    if (window.scrollY > 40) header.classList.add('scrolled');
    else header.classList.remove('scrolled');
  };
  window.addEventListener('scroll', onScroll, {passive:true});
  onScroll();

  /* ---------- Mobile Menu ---------- */
  const mobileMenu = document.getElementById('mobileMenu');
  const openMenu = document.getElementById('openMenu');
  const closeMenu = document.getElementById('closeMenu');

  openMenu.addEventListener('click', () => mobileMenu.classList.add('open'));
  closeMenu.addEventListener('click', () => mobileMenu.classList.remove('open'));
  mobileMenu.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', () => mobileMenu.classList.remove('open'));
  });

  /* ---------- Reveal on Scroll ---------- */
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        io.unobserve(entry.target);
      }
    });
  }, {threshold: 0.1, rootMargin: '0px 0px -50px 0px'});
  revealEls.forEach(el => io.observe(el));

  /* ---------- Form ---------- */
  const form = document.getElementById('lead-form');
  const nomeField = document.getElementById('nome').closest('.field');
  const emailField = document.getElementById('email').closest('.field');

  const validateField = (input, field) => {
    const value = input.value.trim();
    if (input.hasAttribute('required') && !value) {
      field.classList.add('invalid');
      field.classList.remove('valid');
      return false;
    }
    if (input.type === 'email' && value && !/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(value)) {
      field.classList.add('invalid');
      field.classList.remove('valid');
      return false;
    }
    field.classList.remove('invalid');
    field.classList.add('valid');
    return true;
  };

  ['nome', 'email'].forEach(id => {
    const input = document.getElementById(id);
    input.addEventListener('blur', () => validateField(input, input.closest('.field')));
    input.addEventListener('input', () => {
      if (input.closest('.field').classList.contains('invalid')) {
        validateField(input, input.closest('.field'));
      }
    });
  });

  form.addEventListener('submit', (e) => {
    e.preventDefault();
    const nomeOk = validateField(document.getElementById('nome'), nomeField);
    const emailOk = validateField(document.getElementById('email'), emailField);

    if (!nomeOk || !emailOk) {
      const firstInvalid = form.querySelector('.field.invalid input');
      if (firstInvalid) firstInvalid.focus();
      return;
    }

    const btn = form.querySelector('button[type="submit"]');
    const original = btn.innerHTML;
    btn.innerHTML = 'Enviando...';
    btn.disabled = true;

    setTimeout(() => {
      btn.innerHTML = 'Solicitação recebida <i class="fas fa-check" style="margin-left:6px"></i>';
      form.reset();
      document.querySelectorAll('.field').forEach(f => f.classList.remove('valid', 'invalid'));
      setTimeout(() => {
        btn.innerHTML = original;
        btn.disabled = false;
      }, 2400);
    }, 900);
  });

  /* ---------- Smooth anchor offset ---------- */
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      const targetId = this.getAttribute('href');
      if (targetId === '#') return;
      const target = document.querySelector(targetId);
      if (target) {
        e.preventDefault();
        const offset = 80;
        const top = target.getBoundingClientRect().top + window.scrollY - offset;
        window.scrollTo({top, behavior: 'smooth'});
      }
    });
  });
</script>

</body>
</html>
