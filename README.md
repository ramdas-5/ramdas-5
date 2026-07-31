<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ramdas Hembram · Goated README</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <style>
        /* ── Reset & Base ── */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;
            font-family: 'Segoe UI', 'Helvetica Neue', sans-serif;
            display: flex;
            justify-content: center;
            padding: 2rem 1rem;
            color: #e6edf3;
        }

        .readme {
            max-width: 880px;
            width: 100%;
            background: #161b22;
            border-radius: 32px;
            padding: 2.5rem 2.8rem;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7);
            border: 1px solid #30363d;
            transition: all 0.2s;
        }

        /* ── Scrollbar ── */
        .readme::-webkit-scrollbar {
            width: 6px;
        }
        .readme::-webkit-scrollbar-track {
            background: #0d1117;
        }
        .readme::-webkit-scrollbar-thumb {
            background: #58a6ff;
            border-radius: 12px;
        }

        /* ── Typography ── */
        h1,
        h2,
        h3 {
            font-weight: 600;
            letter-spacing: -0.01em;
        }

        h1 {
            font-size: 2.6rem;
            background: linear-gradient(135deg, #f0883e, #f6a85b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: inline-block;
        }

        h2 {
            font-size: 1.6rem;
            margin-top: 2.2rem;
            margin-bottom: 1.2rem;
            border-bottom: 2px solid #30363d;
            padding-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: #f0f6fc;
        }

        h2 i {
            color: #f0883e;
            font-size: 1.4rem;
        }

        h3 {
            font-size: 1.2rem;
            color: #f0f6fc;
            margin: 1.4rem 0 0.4rem;
        }

        a {
            color: #58a6ff;
            text-decoration: none;
            transition: color 0.2s;
        }
        a:hover {
            color: #79c0ff;
            text-decoration: underline;
        }

        p,
        li {
            line-height: 1.7;
            color: #c9d1d9;
        }

        ul,
        .skill-list {
            list-style: none;
            padding-left: 0;
        }

        .skill-list li {
            padding: 0.2rem 0;
        }

        .skill-list li i {
            width: 1.6rem;
            color: #f0883e;
        }

        /* ── Header / Badge row ── */
        .header-top {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 0.6rem;
        }

        .badge-group {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .badge {
            background: #21262d;
            border-radius: 40px;
            padding: 0.25rem 1rem 0.25rem 0.8rem;
            font-size: 0.8rem;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            border: 1px solid #30363d;
            color: #c9d1d9;
        }

        .badge i {
            color: #f0883e;
            font-size: 0.9rem;
        }

        .badge .count {
            font-weight: 600;
            color: #f0f6fc;
        }

        .subtitle {
            font-size: 1.05rem;
            color: #8b949e;
            margin-top: -0.2rem;
            margin-bottom: 1.2rem;
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
        }

        .subtitle i {
            color: #f0883e;
            width: 1.2rem;
        }

        /* ── Snake container ── */
        .snake-wrap {
            background: #0d1117;
            border-radius: 20px;
            padding: 0.6rem 0.2rem;
            margin: 1.8rem 0 1.2rem;
            border: 1px solid #30363d;
            text-align: center;
        }

        .snake-wrap img {
            max-width: 100%;
            height: auto;
            display: block;
            border-radius: 12px;
            background: #0d1117;
        }

        /* ── Stats grid ── */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 1.2rem;
            margin: 1.2rem 0 0.6rem;
        }

        .stats-grid img {
            width: 100%;
            height: auto;
            border-radius: 12px;
            border: 1px solid #30363d;
            background: #0d1117;
            transition: transform 0.15s ease;
        }

        .stats-grid img:hover {
            transform: scale(1.01);
        }

        /* ── Graph card ── */
        .graph-card {
            background: #0d1117;
            border-radius: 16px;
            padding: 0.8rem 0.2rem 0.4rem;
            margin: 1.2rem 0 0.8rem;
            border: 1px solid #30363d;
            text-align: center;
        }

        .graph-card img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }

        /* ── Skills chips ── */
        .skill-chips {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem 0.8rem;
            margin: 0.8rem 0 0.2rem;
        }

        .skill-chips .chip {
            background: #21262d;
            padding: 0.25rem 1rem 0.25rem 0.8rem;
            border-radius: 40px;
            font-size: 0.85rem;
            border: 1px solid #30363d;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            color: #c9d1d9;
        }

        .chip i {
            color: #f0883e;
            width: 1.1rem;
            font-size: 0.9rem;
        }

        /* ── Experience / Project cards ── */
        .exp-item,
        .project-item {
            background: #0d1117;
            border-radius: 14px;
            padding: 1rem 1.4rem;
            margin-bottom: 0.8rem;
            border-left: 4px solid #f0883e;
            border: 1px solid #30363d;
            border-left-width: 4px;
        }

        .exp-item strong,
        .project-item strong {
            color: #f0f6fc;
            font-size: 1.05rem;
        }

        .exp-item .meta,
        .project-item .meta {
            color: #8b949e;
            font-size: 0.85rem;
            display: block;
            margin: 0.2rem 0 0.4rem;
        }

        .exp-item ul,
        .project-item ul {
            list-style: disc;
            padding-left: 1.4rem;
            margin-top: 0.3rem;
        }

        .exp-item ul li,
        .project-item ul li {
            font-size: 0.95rem;
        }

        /* ── Cert badge row ── */
        .cert-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-top: 0.6rem;
        }

        .cert-row span {
            background: #21262d;
            padding: 0.2rem 1.2rem;
            border-radius: 40px;
            font-size: 0.85rem;
            border: 1px solid #30363d;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
        }

        .cert-row span i {
            color: #f0883e;
        }

        /* ── Footer social ── */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem 2rem;
            margin-top: 2rem;
            padding-top: 1.4rem;
            border-top: 2px solid #30363d;
            justify-content: center;
        }

        .social-links a {
            font-size: 1.05rem;
            color: #c9d1d9;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.2s;
        }

        .social-links a i {
            font-size: 1.4rem;
            color: #f0883e;
            transition: 0.2s;
        }

        .social-links a:hover {
            color: #f0f6fc;
        }
        .social-links a:hover i {
            color: #f6a85b;
            transform: scale(1.08);
        }

        .footer-note {
            text-align: center;
            font-size: 0.8rem;
            color: #484f58;
            margin-top: 0.8rem;
            letter-spacing: 0.3px;
        }

        /* ── Responsive ── */
        @media (max-width: 700px) {
            .readme {
                padding: 1.6rem 1.2rem;
            }
            h1 {
                font-size: 2rem;
            }
            .header-top {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.6rem;
            }
            .stats-grid {
                grid-template-columns: 1fr;
            }
            .subtitle {
                flex-direction: column;
                gap: 0.2rem;
            }
        }
    </style>
</head>
<body>

    <div class="readme">

        <!-- ═══ TOP HEADER ═══ -->
        <div class="header-top">
            <h1>Ramdas Hembram</h1>
            <div class="badge-group">
                <span class="badge"><i class="fas fa-eye"></i> Views <span class="count">1.2k</span></span>
                <span class="badge"><i class="fas fa-code"></i> 14 repos</span>
                <span class="badge"><i class="fas fa-star"></i> 38 stars</span>
            </div>
        </div>

        <div class="subtitle">
            <span><i class="fas fa-map-pin"></i> Kolkata, India</span>
            <span><i class="fas fa-envelope"></i> ramdashembram05@gmail.com</span>
            <span><i class="fas fa-graduation-cap"></i> B.Tech CSE · pursuing</span>
        </div>

        <!-- ═══ SNAKE ═══ -->
        <div class="snake-wrap">
            <img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg"
            alt="snake animation" />
        </div>

        <!-- ═══ STATS GRID ═══ -->
        <div class="stats-grid">
            <img src="https://github-readme-stats.vercel.app/api?username=ramdas-5&show_icons=true&theme=dark&bg_color=0d1117&border_color=30363d&icon_color=f0883e&title_color=f0883e&text_color=c9d1d9&hide_border=true"
            alt="GitHub Stats" />
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ramdas-5&layout=compact&theme=dark&bg_color=0d1117&border_color=30363d&title_color=f0883e&text_color=c9d1d9&hide_border=true&langs_count=6"
            alt="Top Languages" />
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=ramdas-5&theme=dark&background=0d1117&border=30363d&ring=f0883e&fire=f0883e&currStreakLabel=f0883e&sideLabels=f0883e&hide_border=true"
            alt="GitHub Streak" />
        </div>

        <!-- ═══ ACTIVITY GRAPH ═══ -->
        <div class="graph-card">
            <img src="https://github-readme-activity-graph.vercel.app/graph?username=ramdas-5&theme=react-dark&bg_color=0d1117&color=c9d1d9&line=f0883e&point=f6a85b&area=true&hide_border=true&custom_title=📈%20Contribution%20Graph"
            alt="Activity Graph" />
        </div>

        <!-- ═══ SUMMARY ═══ -->
        <h2><i class="fas fa-user-astronaut"></i> Summary</h2>
        <p style="background:#0d1117; padding:1rem 1.4rem; border-radius:14px; border:1px solid #30363d;">
            Detail-oriented Computer Science student with a strong foundation in data accuracy and process management.
            Experienced in data handling, quality assurance, and systematic documentation from data annotation and
            fullstack development projects. Possesses excellent communication skills and a keen eye for detail, aiming to
            contribute to efficient back-office operations while leveraging technical proficiency in modern software tools.
        </p>

        <!-- ═══ SKILLS ═══ -->
        <h2><i class="fas fa-tools"></i> Skills</h2>

        <h3>📋 MS Office &amp; Reporting</h3>
        <div class="skill-chips">
            <span class="chip"><i class="fas fa-file-word"></i> Word</span>
            <span class="chip"><i class="fas fa-file-excel"></i> Excel</span>
            <span class="chip"><i class="fas fa-database"></i> Data Entry</span>
            <span class="chip"><i class="fas fa-file-alt"></i> Documentation</span>
            <span class="chip"><i class="fas fa-chart-line"></i> Reporting</span>
            <span class="chip"><i class="fas fa-check-circle"></i> Quality Control</span>
        </div>

        <h3 style="margin-top:1.2rem;">💻 Technical Skills</h3>
        <div class="skill-chips">
            <span class="chip"><i class="fab fa-python"></i> Python</span>
            <span class="chip"><i class="fab fa-java"></i> Java</span>
            <span class="chip"><i class="fab fa-js"></i> JavaScript</span>
            <span class="chip"><i class="fab fa-react"></i> React</span>
            <span class="chip"><i class="fab fa-node"></i> Node.js</span>
            <span class="chip"><i class="fas fa-server"></i> Express</span>
            <span class="chip"><i class="fas fa-leaf"></i> MongoDB</span>
            <span class="chip"><i class="fab fa-html5"></i> HTML5</span>
            <span class="chip"><i class="fab fa-css3-alt"></i> CSS3</span>
            <span class="chip"><i class="fab fa-git-alt"></i> Git</span>
            <span class="chip"><i class="fab fa-github"></i> GitHub</span>
        </div>

        <!-- ═══ EXPERIENCE ═══ -->
        <h2><i class="fas fa-briefcase"></i> Professional Experience</h2>

        <div class="exp-item">
            <strong>Data Annotator</strong> <span style="color:#8b949e; font-weight:400;">· Full-time</span>
            <span class="meta"><i class="fas fa-calendar-alt"></i> 3 months · Pripton Innovation</span>
            <ul>
                <li>Analyzed &amp; labeled data sets for AI model training, ensuring strict adherence to guidelines.</li>
                <li>Maintained high accuracy and consistency in data annotation for quality assurance.</li>
                <li>Collaborated with team members to manage workflow and meet project deadlines.</li>
                <li>Contributed to systematic documentation and reporting of data quality metrics.</li>
            </ul>
        </div>

        <!-- ═══ EDUCATION ═══ -->
        <h2><i class="fas fa-graduation-cap"></i> Education</h2>

        <div class="exp-item" style="border-left-color:#58a6ff;">
            <strong>B.Tech in Computer Science &amp; Engineering</strong>
            <span class="meta"><i class="fas fa-calendar-alt"></i> 2024 – 2028 (pursuing)</span>
        </div>

        <div class="exp-item" style="border-left-color:#58a6ff;">
            <strong>Diploma in Computer Science &amp; Technology</strong>
            <span class="meta"><i class="fas fa-calendar-alt"></i> 2023 – 2026 · Kingston Polytechnic College, Barasat</span>
        </div>

        <div class="exp-item" style="border-left-color:#58a6ff;">
            <strong>Secondary Education</strong>
            <span class="meta"><i class="fas fa-calendar-alt"></i> 2022 – 2023 · Monirampore Swami Mahadevananda Vidyatan, Monirampore</span>
        </div>

        <!-- ═══ PROJECTS ═══ -->
        <h2><i class="fas fa-code"></i> Projects</h2>

        <div class="project-item">
            <strong>Yumlytic – Recipe Discovery App</strong>
            <span class="meta"><i class="fas fa-cubes"></i> MERN Stack</span>
            <ul>
                <li>Developed full-stack application using MERN stack (MongoDB, Express, React, Node.js).</li>
                <li>Managed user data, authentication, and structured database records.</li>
            </ul>
        </div>

        <div class="project-item">
            <strong>File Server – Management System</strong>
            <span class="meta"><i class="fab fa-java"></i> Java · REST API</span>
            <ul>
                <li>Engineered Java-based file management system with structured REST API.</li>
                <li>Created interface for organized file upload, view, and download operations.</li>
            </ul>
        </div>

        <!-- ═══ CERTIFICATIONS ═══ -->
        <h2><i class="fas fa-certificate"></i> Certifications &amp; More</h2>
        <div class="cert-row">
            <span><i class="fas fa-medal"></i> MERN Stack Development</span>
            <span><i class="fas fa-brain"></i> Adaptability</span>
            <span><i class="fas fa-users"></i> Leadership</span>
            <span><i class="fas fa-clock"></i> Time Management</span>
            <span><i class="fas fa-puzzle-piece"></i> Problem Solving</span>
        </div>

        <!-- ═══ SOCIAL LINKS ═══ -->
        <div class="social-links">
            <a href="https://github.com/ramdas-5" target="_blank"><i class="fab fa-github"></i> ramdas-5</a>
            <a href="https://linkedin.com/in/dev-ramdas" target="_blank"><i class="fab fa-linkedin"></i> dev-ramdas</a>
            <a href="https://ramdas-portfolio.vercel.app/" target="_blank"><i class="fas fa-globe"></i> Portfolio</a>
            <a href="mailto:ramdashembram05@gmail.com"><i class="fas fa-envelope"></i> Email</a>
        </div>

        <div class="footer-note">
            ⚡ “Code. Build. Repeat.” &nbsp;·&nbsp; Ramdas Hembram © 2026
        </div>

    </div>

</body>
</html>
