<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imanka Shehan - Full Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0D1117 0%, #161B22 100%);
            color: #fff;
            overflow-x: hidden;
        }

        .stars {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 0;
            pointer-events: none;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #fff;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        header {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.1) 0%, rgba(88, 166, 255, 0.1) 100%);
            border-radius: 20px;
            margin-bottom: 40px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(0, 217, 255, 0.2);
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid #00D9FF;
            margin-bottom: 20px;
            animation: float 3s ease-in-out infinite;
            box-shadow: 0 0 30px rgba(0, 217, 255, 0.5);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        h1 {
            font-size: 3em;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #00D9FF, #58A6FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .typing-text {
            font-size: 1.2em;
            color: #00D9FF;
            margin-bottom: 20px;
        }

        .about {
            background: rgba(22, 27, 34, 0.6);
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
            border: 1px solid rgba(0, 217, 255, 0.2);
            backdrop-filter: blur(10px);
            animation: slideInLeft 1s ease-out;
        }

        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .about ul {
            list-style: none;
            padding: 20px 0;
        }

        .about li {
            padding: 10px 0;
            font-size: 1.1em;
            border-left: 3px solid #00D9FF;
            padding-left: 15px;
            margin: 10px 0;
            transition: transform 0.3s;
        }

        .about li:hover {
            transform: translateX(10px);
        }

        .section-title {
            font-size: 2em;
            margin: 40px 0 20px;
            text-align: center;
            color: #00D9FF;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #00D9FF, transparent);
            margin: 10px auto;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .skill-item {
            background: rgba(22, 27, 34, 0.8);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s;
            border: 1px solid rgba(0, 217, 255, 0.2);
            cursor: pointer;
        }

        .skill-item:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.3);
            border-color: #00D9FF;
        }

        .skill-item img {
            width: 50px;
            height: 50px;
            margin-bottom: 10px;
        }

        .contact-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 40px 0;
        }

        .contact-btn {
            padding: 15px 30px;
            border-radius: 10px;
            text-decoration: none;
            color: #fff;
            font-weight: bold;
            transition: all 0.3s;
            border: 2px solid;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .contact-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .linkedin { background: #0077B5; border-color: #0077B5; }
        .linkedin:hover { background: #005582; }

        .gmail { background: #D14836; border-color: #D14836; }
        .gmail:hover { background: #a33426; }

        .facebook { background: #1877F2; border-color: #1877F2; }
        .facebook:hover { background: #0e5dc0; }

        .instagram { background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); border-color: #E4405F; }
        .instagram:hover { opacity: 0.9; }

        .github { background: #333; border-color: #333; }
        .github:hover { background: #000; }

        .stats-container {
            background: rgba(22, 27, 34, 0.6);
            padding: 30px;
            border-radius: 15px;
            margin: 30px 0;
            border: 1px solid rgba(0, 217, 255, 0.2);
            text-align: center;
        }

        .stat-box {
            display: inline-block;
            margin: 20px;
            padding: 20px;
            background: rgba(0, 217, 255, 0.1);
            border-radius: 10px;
            min-width: 150px;
        }

        .stat-number {
            font-size: 2em;
            color: #00D9FF;
            font-weight: bold;
        }

        .stat-label {
            color: #8b949e;
            margin-top: 5px;
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            color: #8b949e;
            border-top: 1px solid rgba(0, 217, 255, 0.2);
            margin-top: 60px;
        }

        @media (max-width: 768px) {
            h1 { font-size: 2em; }
            .skills-grid { grid-template-columns: repeat(auto-fit, minmax(60px, 1fr)); }
            .contact-buttons { flex-direction: column; }
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    
    <div class="container">
        <header>
            <div class="profile-img" style="background: url('https://github.com/Ishehan-cloud.png') center/cover; width: 150px; height: 150px; margin: 0 auto 20px;"></div>
            <h1>Hi, I'm Imanka Shehan 👋</h1>
            <div class="typing-text">Full Stack Developer 🚀 | HNDIT Undergraduate 🎓</div>
            <p style="color: #8b949e; max-width: 600px; margin: 0 auto;">Always Learning New Things!</p>
        </header>

        <section class="about">
            <h2 style="color: #00D9FF; margin-bottom: 20px;">About Me</h2>
            <ul>
                <li>🎓 Second Year Undergraduate at <strong>SLIATE - HNDIT</strong></li>
                <li>🔭 Currently working on: <strong>Shop Management System</strong></li>
                <li>🌱 Learning: React.js, Node.js, Express, MongoDB, TypeScript</li>
                <li>🤝 Looking to collaborate on web development and real-world projects</li>
                <li>📫 Reach me: <a href="mailto:imankashehan629@gmail.com" style="color: #00D9FF; text-decoration: none;">imankashehan629@gmail.com</a></li>
            </ul>
        </section>

        <h2 class="section-title">💻 Skills & Technologies</h2>
        <div class="skills-grid">
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" alt="React">
                <div>React</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" alt="Node.js">
                <div>Node.js</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original.svg" alt="Express" style="filter: invert(1);">
                <div>Express</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="TypeScript">
                <div>TypeScript</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original.svg" alt="MongoDB">
                <div>MongoDB</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript">
                <div>JavaScript</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python">
                <div>Python</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java">
                <div>Java</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="PHP">
                <div>PHP</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="C#">
                <div>C#</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg" alt="MySQL">
                <div>MySQL</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" alt="PostgreSQL">
                <div>PostgreSQL</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" alt="Docker">
                <div>Docker</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" alt="HTML5">
                <div>HTML5</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" alt="CSS3">
                <div>CSS3</div>
            </div>
            <div class="skill-item">
                <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C">
                <div>C</div>
            </div>
        </div>

        <div class="stats-container">
            <h2 style="color: #00D9FF; margin-bottom: 30px;">📊 GitHub Stats</h2>
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=Ishehan-cloud&theme=black-ice&hide_border=true&stroke=0000&background=060A0CD0" alt="GitHub Streak" style="max-width: 100%; border-radius: 10px; margin: 10px;">
            <div style="margin-top: 20px;">
                <img src="https://github-readme-stats.vercel.app/api?username=Ishehan-cloud&show_icons=true&count_private=true&theme=react&hide_border=true&bg_color=0D1117" alt="GitHub Stats" style="max-width: 48%; border-radius: 10px; margin: 5px;">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ishehan-cloud&langs_count=8&count_private=true&layout=compact&theme=react&hide_border=true&bg_color=0D1117" alt="Top Languages" style="max-width: 48%; border-radius: 10px; margin: 5px;">
            </div>
        </div>

        <h2 class="section-title">🌐 Connect With Me</h2>
        <div class="contact-buttons">
            <a href="https://www.linkedin.com/in/imanka-shehan" class="contact-btn linkedin" target="_blank">
                <span>📎</span> LinkedIn
            </a>
            <a href="mailto:imankashehan629@gmail.com" class="contact-btn gmail">
                <span>📧</span> Gmail
            </a>
            <a href="https://www.facebook.com/share/1A6XwXW2Gu/?mibextid=wwXIfr" class="contact-btn facebook" target="_blank">
                <span>👤</span> Facebook
            </a>
            <a href="https://www.instagram.com/imanka_shehan?igsh=eXpoMjV4NGc3b2U5&utm_source=qr" class="contact-btn instagram" target="_blank">
                <span>📷</span> Instagram
            </a>
            <a href="https://github.com/Ishehan-cloud" class="contact-btn github" target="_blank">
                <span>💻</span> GitHub
            </a>
        </div>

        <footer>
            <p style="font-size: 1.2em; color: #00D9FF; margin-bottom: 10px;">Code . . . Learn . . . Build . . . Repeat . . .</p>
            <p>© 2025 Imanka Shehan. All rights reserved.</p>
        </footer>
    </div>

    <script>
        // Create animated stars
        const starsContainer = document.getElementById('stars');
        for (let i = 0; i < 100; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.animationDelay = Math.random() * 3 + 's';
            starsContainer.appendChild(star);
        }

        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.skill-item, .stat-box').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'all 0.5s ease-out';
            observer.observe(el);
        });
    </script>
</body>
</html>
