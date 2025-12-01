<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #ffffff;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .language-switcher {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .lang-btn {
            background: linear-gradient(45deg, #FF6B35, #FF8E53);
            color: white;
            border: none;
            padding: 15px 40px;
            margin: 10px;
            border-radius: 50px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
        }
        
        .lang-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 107, 53, 0.5);
        }
        
        .lang-btn.active {
            background: linear-gradient(45deg, #2D3047, #419D78);
            box-shadow: 0 4px 15px rgba(65, 157, 120, 0.4);
        }
        
        .profile-section {
            display: none;
            animation: fadeIn 0.8s ease;
        }
        
        .profile-section.active {
            display: block;
        }
        
        .profile-header {
            text-align: center;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 25px;
            margin-bottom: 40px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .profile-pic {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 5px solid #FF6B35;
            margin-bottom: 20px;
            object-fit: cover;
            box-shadow: 0 0 30px rgba(255, 107, 53, 0.5);
        }
        
        .name {
            font-size: 3em;
            background: linear-gradient(45deg, #FF6B35, #00C9FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        
        .title {
            font-size: 1.5em;
            color: #B0B0B0;
            margin-bottom: 20px;
        }
        
        .quote {
            font-style: italic;
            color: #FF8E53;
            margin: 20px 0;
            padding: 0 20px;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .stats-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease;
        }
        
        .stats-card:hover {
            transform: translateY(-5px);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 40px 0;
        }
        
        .social-btn {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px 25px;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            color: white;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .social-btn:hover {
            background: rgba(255, 107, 53, 0.2);
            transform: translateY(-3px);
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 30px 0;
        }
        
        .tech-badge {
            background: linear-gradient(45deg, #419D78, #2D3047);
            padding: 12px 25px;
            border-radius: 50px;
            font-weight: 600;
            box-shadow: 0 4px 10px rgba(65, 157, 120, 0.3);
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 20px;
            margin: 30px 0;
            border-left: 5px solid #FF6B35;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @media (max-width: 768px) {
            .name { font-size: 2.2em; }
            .title { font-size: 1.2em; }
            .lang-btn { padding: 12px 25px; font-size: 16px; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- زبان‌ها -->
        <div class="language-switcher">
            <button class="lang-btn active" onclick="switchLanguage('farsi')">🇮🇷 فارسی</button>
            <button class="lang-btn" onclick="switchLanguage('english')">🇺🇸 English</button>
        </div>

        <!-- بخش فارسی -->
        <div id="farsi-section" class="profile-section active">
            <div class="profile-header">
                <img src="https://avatars.githubusercontent.com/AtaKral1387s?v=4" class="profile-pic" alt="عکس پروفایل">
                <h1 class="name">عطا</h1>
                <p class="title">🚀 طراح فرانت‌اند | توسعه‌دهنده وب ریسپانسیو</p>
                <p class="quote">"کد زدن هنر منه، و مرورگر بوم نقاشی‌م"</p>
            </div>

            <div class="stats-grid">
                <div class="stats-card">
                    <h2>📊 آمار گیت‌هاب</h2>
                    <img src="https://github-readme-stats.vercel.app/api?username=AtaKral1387s&show_icons=true&theme=radical&locale=fa&hide_border=true" alt="آمار گیت‌هاب" style="width:100%; margin-top:15px;">
                </div>
                
                <div class="stats-card">
                    <h2>💻 زبان‌های پرکاربرد</h2>
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AtaKral1387s&layout=compact&theme=radical&locale=fa&hide_border=true" alt="زبان‌های پرکاربرد" style="width:100%; margin-top:15px;">
                </div>
            </div>

            <div class="stats-card">
                <h2>🛠 فن‌آوری‌ها و مهارت‌ها</h2>
                <div class="tech-stack">
                    <span class="tech-badge">HTML5</span>
                    <span class="tech-badge">CSS3</span>
                    <span class="tech-badge">JavaScript</span>
                    <span class="tech-badge">Responsive Design</span>
                    <span class="tech-badge">Git & GitHub</span>
                    <span class="tech-badge">VS Code</span>
                    <span class="tech-badge">Figma</span>
                </div>
            </div>

            <div class="project-card">
                <h2>🌟 پروژه شاخص: سایت ایستاژن</h2>
                <p>🎓 پلتفرم آموزش کامپیوتر، موبایل، سرگرمی و موسیقی</p>
                <p><strong>🛠 تکنولوژی:</strong> HTML خالص، CSS، JavaScript</p>
                <p><strong>✨ ویژگی:</strong> طراحی کاملاً ریسپانسیو و رابط کاربری مدرن</p>
                <p><strong>🌐 لینک:</strong> <a href="https://istagen.ir" style="color:#FF6B35;">istagen.ir</a></p>
                <p><em>کدهای پروژه به زودی روی گیت‌هاب منتشر می‌شه!</em></p>
            </div>

            <div class="stats-card">
                <h2>📚 در حال یادگیری و توسعه</h2>
                <ul style="padding-right:20px;">
                    <li>مطالعه عمیق‌تر جاوااسکریپت (الگوها و بهینه‌سازی)</li>
                    <li>آماده‌سازی برای یادگیری React.js و Next.js</li>
                    <li>ساخت پروژه‌های بیشتر برای تقویت رزومه</li>
                    <li>هدف: توسعه‌دهنده فول‌استک حرفه‌ای</li>
                </ul>
            </div>

            <div class="social-links">
                <a href="https://istagen.ir" class="social-btn" target="_blank">
                    <span>🌐</span> وبسایت شخصی
                </a>
                <a href="https://www.linkedin.com/in/ata1387s" class="social-btn" target="_blank">
                    <span>💼</span> لینکدین
                </a>
                <a href="https://t.me/Age1bat" class="social-btn" target="_blank">
                    <span>📱</span> تلگرام
                </a>
                <a href="https://instagram.com/mr1ata1" class="social-btn" target="_blank">
                    <span>📸</span> اینستاگرام
                </a>
                <a href="mailto:mxkral1401@gmail.com" class="social-btn">
                    <span>📧</span> ایمیل
                </a>
            </div>

            <div class="profile-header" style="margin-top:40px;">
                <p style="color:#FF8E53;">🔥 عاشق کد و کد زدن</p>
                <p>🎵 علاقه‌مند به موسیقی | 📚 معتقدم به یادگیری مستمر</p>
                <p style="margin-top:20px; font-size:0.9em; color:#B0B0B0;">
                    "نبوغ یک درصد الهام و نود و نه درصد عرق ریختنه" – توماس ادیسون
                </p>
            </div>
        </div>

        <!-- بخش انگلیسی -->
        <div id="english-section" class="profile-section">
            <div class="profile-header">
                <img src="https://avatars.githubusercontent.com/AtaKral1387s?v=4" class="profile-pic" alt="Profile Picture">
                <h1 class="name">Ata</h1>
                <p class="title">🚀 Front-End Developer | Responsive Web Designer</p>
                <p class="quote">"Coding is my art, and the browser is my canvas"</p>
            </div>

            <div class="stats-grid">
                <div class="stats-card">
                    <h2>📊 GitHub Statistics</h2>
                    <img src="https://github-readme-stats.vercel.app/api?username=AtaKral1387s&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats" style="width:100%; margin-top:15px;">
                </div>
                
                <div class="stats-card">
                    <h2>💻 Top Languages</h2>
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AtaKral1387s&layout=compact&theme=radical&hide_border=true" alt="Top Languages" style="width:100%; margin-top:15px;">
                </div>
            </div>

            <div class="stats-card">
                <h2>🛠️ Tech Stack & Skills</h2>
                <div class="tech-stack">
                    <span class="tech-badge">HTML5</span>
                    <span class="tech-badge">CSS3</span>
                    <span class="tech-badge">JavaScript</span>
                    <span class="tech-badge">Responsive Design</span>
                    <span class="tech-badge">Git & GitHub</span>
                    <span class="tech-badge">VS Code</span>
                    <span class="tech-badge">Figma</span>
                </div>
            </div>

            <div class="project-card">
                <h2>🌟 Featured Project: Istagen Website</h2>
                <p>🎓 Computer, Mobile, Entertainment & Music Learning Platform</p>
                <p><strong>🛠 Technologies:</strong> Pure HTML, CSS, JavaScript</p>
                <p><strong>✨ Features:</strong> Fully responsive design & modern UI</p>
                <p><strong>🌐 Live:</strong> <a href="https://istagen.ir" style="color:#FF6B35;">istagen.ir</a></p>
                <p><em>Project code will be published on GitHub soon!</em></p>
            </div>

            <div class="stats-card">
                <h2>📚 Currently Learning & Growing</h2>
                <ul style="padding-left:20px;">
                    <li>Deep dive into JavaScript (patterns & optimization)</li>
                    <li>Preparing for React.js & Next.js journey</li>
                    <li>Building more portfolio projects</li>
                    <li>Goal: Professional Full-Stack Developer</li>
                </ul>
            </div>

            <div class="social-links">
                <a href="https://istagen.ir" class="social-btn" target="_blank">
                    <span>🌐</span> Personal Website
                </a>
                <a href="https://www.linkedin.com/in/ata1387s" class="social-btn" target="_blank">
                    <span>💼</span> LinkedIn
                </a>
                <a href="https://t.me/Age1bat" class="social-btn" target="_blank">
                    <span>📱</span> Telegram
                </a>
                <a href="https://instagram.com/mr1ata1" class="social-btn" target="_blank">
                    <span>📸</span> Instagram
                </a>
                <a href="mailto:mxkral1401@gmail.com" class="social-btn">
                    <span>📧</span> Email
                </a>
            </div>

            <div class="profile-header" style="margin-top:40px;">
                <p style="color:#FF8E53;">🔥 Passionate Coder & Tech Enthusiast</p>
                <p>🎵 Music Lover | 📚 Continuous Learner</p>
                <p style="margin-top:20px; font-size:0.9em; color:#B0B0B0;">
                    "Genius is one percent inspiration and ninety-nine percent perspiration" – Thomas Edison
                </p>
            </div>
        </div>
    </div>

    <script>
        function switchLanguage(lang) {
            // مخفی کردن همه بخش‌ها
            document.getElementById('farsi-section').classList.remove('active');
            document.getElementById('english-section').classList.remove('active');
            
            // نمایش بخش انتخاب شده
            document.getElementById(lang + '-section').classList.add('active');
            
            // به‌روزرسانی دکمه‌های فعال
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');
            
            // اسکرول به بالا
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
        
        // تنظیم اولیه
        document.addEventListener('DOMContentLoaded', function() {
            // پیش‌فرض فارسی
            document.getElementById('farsi-section').classList.add('active');
            document.querySelector('.lang-btn').classList.add('active');
        });
    </script>
</body>
</html>
