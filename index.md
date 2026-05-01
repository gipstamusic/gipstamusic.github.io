---
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ site.data.site.producer_name }} | Beat Store</title>
    <script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
    <style>
    :root { --bg: #050505; --yellow: #FFDE00; --text: #ffffff; --gray: #7F7F7F; }
    body, html { margin: 0; padding: 0; font-family: 'Montserrat', sans-serif; background-color: var(--bg); color: var(--text); scroll-behavior: smooth; }
    a { text-decoration: none; color: var(--text); }
    
    /* Layout Basics */
    .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; text-align: center; }
    section { padding: 100px 0; border-bottom: 1px solid #1a1a1a; }
    h2 { font-size: 2.2rem; margin-bottom: 50px; text-transform: uppercase; letter-spacing: 2px; }

    /* Fixed Navigation */
    nav { 
        display: flex; justify-content: space-between; align-items: center; 
        padding: 15px 40px; position: fixed; width: 100%; top: 0; 
        box-sizing: border-box; z-index: 100; background: rgba(5, 5, 5, 0.95);
        border-bottom: 1px solid #1a1a1a;
    }
    .nav-logo img { height: 50px; width: auto; }
    .nav-links a { margin-left: 20px; font-size: 0.85rem; text-transform: uppercase; font-weight: bold; }
    .nav-links a:hover { color: var(--yellow); }

    /* Floating Background Hero */
    #hero { 
        position: relative; padding: 250px 0 150px; 
        background-image: url('{{ site.data.site.bg_image }}'); 
        background-size: cover; background-position: center; 
        background-attachment: fixed;
        border-bottom: none;
    }

    /* Gray Content Box (Image 4 Style) */
    .content-card {
        background: var(--gray);
        max-width: 800px;
        margin: 0 auto;
        padding: 60px;
        border-radius: 4px;
        position: relative;
        z-index: 5;
        color: #000;
        box-shadow: 0 20px 50px rgba(0,0,0,0.5);
    }
    .content-card h1 { margin: 0 0 10px; font-size: 3rem; text-transform: uppercase; }
    .content-card p { margin: 0; font-size: 1.2rem; font-weight: 500; }

    /* Uniform Grid for Kits & Services */
    .kits-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 40px; max-width: 1100px; margin: 0 auto; }
    .kit-card { background: #111; border: 1px solid #222; border-radius: 8px; overflow: hidden; transition: 0.3s; text-align: left; }
    .kit-card:hover { border-color: var(--yellow); transform: translateY(-5px); }
    .kit-card img { width: 100%; aspect-ratio: 1 / 1; object-fit: cover; border-bottom: 1px solid #222; }
    .kit-info { padding: 20px; display: flex; justify-content: space-between; align-items: center; }
    .kit-info h3 { font-size: 1rem; margin: 0; color: #fff; }
    .kit-info .price { background: var(--yellow); color: #000; padding: 5px 12px; border-radius: 4px; font-weight: bold; }

    /* Social Grid (Restored Alignment) */
    .social-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; max-width: 1000px; margin: 0 auto; }
    .social-card { background: #111; padding: 40px 20px; border-radius: 8px; border: 1px solid #222; transition: 0.3s; }
    .social-card:hover { border-color: var(--yellow); background: #161616; }
    .social-card img { width: 60px; height: 60px; margin-bottom: 20px; }

    /* Buttons & Forms */
    .btn { background: var(--yellow); color: #000; padding: 12px 30px; font-weight: bold; text-transform: uppercase; border: none; cursor: pointer; }
    input, textarea { background: #111; border: 1px solid #222; color: #fff; padding: 15px; margin-bottom: 15px; width: 100%; box-sizing: border-box; }
    
    /* Top Button */
    #topBtn {
        position: fixed; bottom: 30px; right: 30px; z-index: 99;
        background-color: var(--yellow); color: black; border: none;
        width: 50px; height: 50px; border-radius: 50%; cursor: pointer; display: none;
        font-weight: bold; font-size: 20px;
    }

    @media (max-width: 768px) {
        .social-grid { grid-template-columns: 1fr; }
        .nav-links { display: none; }
    }
    </style>
</head>
<body>

    <nav>
       <div class="nav-logo"><img src="/images/image_3.png" alt="Logo"></div>
        <div class="nav-links">
            <a href="#beats">Beats</a>
            <a href="#socials">Connect</a>
            <a href="#kits">Sound Kits</a>
            <a href="#services">Services</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <!-- 1. HERO BACKGROUND -->
    <section id="hero">
        <div class="content-card">
            <h1>{{ site.data.site.producer_name }}</h1>
            <p>{{ site.data.site.bio }}</p>
        </div>
    </section>

    <!-- 2. BEATSTARS PLAYER -->
    <section id="beats">
        <div class="container">
            <h2>Beat Store</h2>
            <div class="iframe-wrapper">
                <iframe src="https://player.beatstars.com/?storeId=96640" height="600" scrolling="no"></iframe>
            </div>
        </div>
    </section>

    <!-- 3. SOCIAL MEDIA THUMBNAILS -->
    <section id="socials">
        <div class="container">
            <h2>Connect</h2>
            <div class="social-grid">
                <a href="https://instagram.com/yourhandle" target="_blank" class="social-card">
                    <img src="/images/instagram.png" alt="Instagram">
                    <h3>Instagram</h3>
                </a>
                <a href="https://youtube.com/yourchannel" target="_blank" class="social-card">
                    <img src="/images/youtube.png" alt="YouTube">
                    <h3>YouTube</h3>
                </a>
                <a href="https://tiktok.com/@yourhandle" target="_blank" class="social-card">
                    <img src="/images/tiktok.png" alt="TikTok">
                    <h3>TikTok</h3>
                </a>
            </div>
        </div>
    </section>

    <!-- 4. BEATSTARS SOUND KITS -->
    <section id="kits">
        <div class="container">
            <h2>Sound Kits</h2>
            <div class="kits-grid">
                {% for kit in site.data.site.sound_kits %}
                <a href="{{ kit.link }}" target="_blank" class="kit-card">
                    <img src="{{ kit.image }}" alt="{{ kit.title }}">
                    <div class="kit-info">
                        <h3>{{ kit.title }}</h3>
                        <div class="price">{{ kit.price }}</div>
                    </div>
                </a>
                {% endfor %}
            </div>
        </div>
    </section>

   <!-- 5. SERVICES -->
    <section id="services">
        <div class="container">
            <h2>Services</h2>
            <div class="kits-grid"> <!-- Reusing the Kits CSS grid so it matches perfectly -->
                {% for service in site.data.site.services %}
                <a href="{{ service.link}}" target="_blank" class="kit-card">
                    <img src="{{ service.image }}" alt="{{ service.title }}">
                    <div class="kit-info">
                        <h3>{{ service.title }}</h3>
                        <div class="price">{{ service.price }}</div>
                    </div>
                </a>
                {% endfor %}
            </div>
        </div>
    </section>

    <!-- 6. CONTACT FORM -->
    <section id="contact">
        <div class="container">
            <h2>Let's Work</h2>
            <form name="contact" method="POST" data-netlify="true">
                <div style="display: flex; gap: 20px;">
                    <input type="text" name="name" placeholder="NAME" required>
                    <input type="email" name="email" placeholder="EMAIL" required>
                </div>
                <input type="text" name="subject" placeholder="SUBJECT">
                <textarea name="message" rows="5" placeholder="MESSAGE" required></textarea>
                <div style="text-align: center; margin-top: 10px;">
                    <button type="submit" class="btn">Send Message</button>
                </div>
            </form>
        </div>
    </section>

    <footer>
        <div class="container">
            © 2026 {{ site.data.site.producer_name }}. All Rights Reserved.
        </div>
    </footer>

    <script>
      if (window.netlifyIdentity) {
        window.netlifyIdentity.on("init", user => {
          if (!user) {
            window.netlifyIdentity.on("login", () => { document.location.href = "/admin/"; });
          }
        });
      }
    </script>
    <button onclick="window.scrollTo({top: 0, behavior: 'smooth'})" id="topBtn" title="Go to top">↑</button>

    <script>
        window.onscroll = function() {
            if (document.body.scrollTop > 500 || document.documentElement.scrollTop > 500) {
                document.getElementById("topBtn").style.display = "block";
            } else {
                document.getElementById("topBtn").style.display = "none";
            }
        };
    </script>
</body>
</html>