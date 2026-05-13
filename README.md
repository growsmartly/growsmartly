<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GrowSmartly — Engineered to Grow</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Inter', sans-serif; color: #0A2540; line-height: 1.6; }
        
        /* Colors */
        :root {
            --primary: #0A2540;
            --accent: #00D26A;
            --light: #F6F9FC;
            --white: #FFFFFF;
        }

        /* Header */
        header {
            background: var(--white);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        .logo { font-size: 1.5rem; font-weight: 800; color: var(--primary); }
        .logo span { color: var(--accent); }
        nav a { margin-left: 2rem; text-decoration: none; color: var(--primary); font-weight: 600; }
        .whatsapp-btn {
            background: var(--accent);
            color: var(--white);
            padding: 0.5rem 1rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
        }

        /* Hero */
        .hero {
            background: var(--primary);
            color: var(--white);
            padding: 5rem 5%;
            text-align: center;
        }
        .hero h1 { font-size: 3rem; font-weight: 800; margin-bottom: 1rem; }
        .hero p { font-size: 1.2rem; max-width: 600px; margin: 0 auto 2rem; opacity: 0.9; }
        .btn-group { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
        .btn-primary {
            background: var(--accent);
            color: var(--primary);
            padding: 1rem 2rem;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
        }
        .btn-secondary {
            border: 2px solid var(--white);
            color: var(--white);
            padding: 1rem 2rem;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 600;
        }

        /* Sections */
        section { padding: 4rem 5%; }
        .section-title { font-size: 2rem; font-weight: 800; text-align: center; margin-bottom: 3rem; }

        /* Why Us */
        .why-us { background: var(--light); }
        .edge-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1000px;
            margin: 0 auto;
        }
        .edge-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 12px;
            border-left: 4px solid var(--accent);
        }
        .edge-card h3 { margin-bottom: 0.5rem; }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1100px;
            margin: 0 auto;
        }
        .service-card {
            background: var(--white);
            border: 2px solid var(--light);
            padding: 2rem;
            border-radius: 12px;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        .badge {
            display: inline-block;
            background: var(--accent);
            color: var(--primary);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        /* Founding Clients */
        .founding {
            background: var(--primary);
            color: var(--white);
            text-align: center;
        }
        .founding h2 { margin-bottom: 1rem; }
        .founding p { max-width: 600px; margin: 0 auto 2rem; opacity: 0.9; }

        /* Pricing */
        .pricing { background: var(--light); }
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1100px;
            margin: 0 auto;
        }
        .price-card {
            background: var(--white);
            padding: 2.5rem;
            border-radius: 16px;
            text-align: center;
            position: relative;
        }
        .price-card.featured {
            border: 3px solid var(--accent);
            transform: scale(1.05);
        }
        .price-tag {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary);
            margin: 1rem 0;
        }
        .price-tag span {
            font-size: 1rem;
            color: #666;
            text-decoration: line-through;
            display: block;
            margin-bottom: 0.3rem;
        }
        .popular-badge {
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--accent);
            color: var(--primary);
            padding: 0.3rem 1rem;
            border-radius: 20px;
            font-weight: 700;
            font-size: 0.85rem;
        }
        .price-card ul { list-style: none; margin: 1.5rem 0; }
        .price-card li { padding: 0.5rem 0; border-bottom: 1px solid var(--light); }

        /* Contact */
        .contact { text-align: center; }
        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }
        .contact-box {
            background: var(--light);
            padding: 2rem;
            border-radius: 12px;
            min-width: 250px;
        }
        .contact-box a {
            color: var(--primary);
            text-decoration: none;
            font-weight: 700;
            font-size: 1.2rem;
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: var(--white);
            text-align: center;
            padding: 2rem;
        }

        /* Mobile */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            nav { display: none; }
            .price-card.featured { transform: none; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">Grow<span>Smartly</span></div>
        <nav>
            <a href="#home">Home</a>
            <a href="#services">Services</a>
            <a href="#why">Why Us</a>
            <a href="#pricing">Pricing</a>
            <a href="#contact">Contact</a>
        </nav>
        <a href="https://wa.me/918725040390" class="whatsapp-btn">📱 WhatsApp</a>
    </header>

    <!-- Hero -->
    <section class="hero" id="home">
        <h1>We Engineer Growth.<br>Not Just Websites.</h1>
        <p>Web design, development, digital marketing & brand identity — built by engineers who understand how algorithms rank, recommend, and convert.</p>
        <div class="btn-group">
            <a href="#contact" class="btn-primary">Get Free Growth Audit</a>
            <a href="https://wa.me/918725040390" class="btn-secondary">WhatsApp Us → 8725040390</a>
        </div>
    </section>

    <!-- Why Us -->
    <section class="why-us" id="why">
        <h2 class="section-title">The Engineering Edge</h2>
        <div class="edge-grid">
            <div class="edge-card">
                <h3>🔍 How Google Crawls</h3>
                <p>SEO that actually works from day one — clean code, semantic structure, Core Web Vitals optimized.</p>
            </div>
            <div class="edge-card">
                <h3>📱 How Algorithms Push</h3>
                <p>Meta, TikTok, YouTube — we engineer content that platforms want to distribute.</p>
            </div>
            <div class="edge-card">
                <h3>⚡ How Speed Converts</h3>
                <p>Every millisecond counts. We build sites that load in under 2 seconds.</p>
            </div>
            <div class="edge-card">
                <h3>🎯 How Users Behave</h3>
                <p>Data-driven layouts that turn visitors into leads, not just traffic.</p>
            </div>
        </div>
        <p style="text-align:center; margin-top:2rem; font-style:italic; font-weight:600;">"Most agencies follow trends. We follow the math. Be first to grow."</p>
    </section>

    <!-- Services -->
    <section id="services">
        <h2 class="section-title">What We Build</h2>
        <div class="services-grid">
            <div class="service-card">
                <span class="badge">UI/UX</span>
                <h3>Web Design</h3>
                <p>Algorithm-friendly layouts, mobile-first, conversion-optimized interfaces that turn visitors into customers.</p>
            </div>
            <div class="service-card">
                <span class="badge">&lt;Code/&gt;</span>
                <h3>Web Development</h3>
                <p>Clean semantic code, Core Web Vitals optimized, scalable architecture that search engines love.</p>
            </div>
            <div class="service-card">
                <span class="badge">SEO/ADS</span>
                <h3>Digital Marketing</h3>
                <p>SEO + paid ads engineered around platform algorithms. Not guessing — engineering visibility.</p>
            </div>
            <div class="service-card">
                <span class="badge">Brand</span>
                <h3>Brand Identity</h3>
                <p>Visual systems algorithms recognize & humans remember. Logo, colors, typography, guidelines.</p>
            </div>
        </div>
    </section>

    <!-- Founding Clients -->
    <section class="founding">
        <h2>We're Building Our First Success Stories</h2>
        <p>We're engineers starting fresh — looking for 5 founding clients. You get premium work at launch pricing. We get proof of what we can do.</p>
        <a href="https://wa.me/918725040390" class="btn-primary">Claim Founding Client Spot</a>
    </section>

    <!-- Pricing -->
    <section class="pricing" id="pricing">
        <h2 class="section-title">Investment Plans</h2>
        <div class="pricing-grid">
            <div class="price-card">
                <h3>Starter</h3>
                <div class="price-tag">
                    <span>₹7,999</span>
                    ₹5,599
                </div>
                <p>Founding Client Price</p>
                <ul>
                    <li>5-page website</li>
                    <li>Mobile responsive</li>
                    <li>Basic SEO</li>
                    <li>1 revision</li>
                </ul>
                <a href="https://wa.me/918725040390?text=Hi! I'm interested in the Starter plan." class="btn-primary">Get Started</a>
            </div>
            <div class="price-card featured">
                <div class="popular-badge">MOST POPULAR</div>
                <h3>Growth</h3>
                <div class="price-tag">
                    <span>₹14,999</span>
                    ₹10,499
                </div>
                <p>Founding Client Price</p>
                <ul>
                    <li>Everything in Starter</li>
                    <li>SEO setup & optimization</li>
                    <li>Social media setup</li>
                    <li>Google Business Profile</li>
                    <li>3 revisions</li>
                </ul>
                <a href="https://wa.me/918725040390?text=Hi! I'm interested in the Growth plan." class="btn-primary">Get Started</a>
            </div>
            <div class="price-card">
                <h3>Scale</h3>
                <div class="price-tag">
                    <span>₹29,999</span>
                    ₹20,999
                </div>
                <p>Founding Client Price</p>
                <ul>
                    <li>Everything in Growth</li>
                    <li>Google & Meta Ads setup</li>
                    <li>Free logo & brand kit</li>
                    <li>Monthly optimization</li>
                    <li>Priority support</li>
                    <li>Unlimited revisions</li>
                </ul>
                <a href="https://wa.me/918725040390?text=Hi! I'm interested in the Scale plan." class="btn-primary">Get Started</a>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section class="contact" id="contact">
        <h2 class="section-title">Let's Engineer Your Growth</h2>
        <p>Tell us your business. We'll explain exactly how algorithms are affecting your visibility right now — free.</p>
        <div class="contact-info">
            <div class="contact-box">
                <p>📱 WhatsApp (Primary)</p>
                <a href="https://wa.me/918725040390">87250 40390</a>
            </div>
            <div class="contact-box">
                <p>📞 Call Us</p>
                <a href="tel:+916283706612">62837 06612</a>
            </div>
        </div>
        <div style="margin-top:2rem;">
            <a href="https://wa.me/918725040390?text=Hi GrowSmartly! I want a free growth audit for my business." class="btn-primary">Get Free Audit Now</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <h3>GrowSmartly</h3>
        <p>Engineered to Grow</p>
        <p style="margin-top:1rem; opacity:0.7;">
            📱 87250 40390 | 📞 62837 06612<br>
            © 2026 GrowSmartly. All rights reserved.
        </p>
    </footer>

</body>
</html>
