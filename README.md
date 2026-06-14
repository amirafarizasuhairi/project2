# project2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amira's Mobile Programming Portfolio | SDG 2 Zero Hunger</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #E5A93B;
            --primary-dark: #C68B23;
            --secondary: #1F2937;
            --bg-light: #F9FAFB;
            --card-bg: #FFFFFF;
            --accent-green: #2ECC71;
            --nav-height: 70px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: calc(var(--nav-height) + 20px);
        }

        body {
            background-color: var(--bg-light);
            color: var(--secondary);
            line-height: 1.6;
        }

        nav {
            background: var(--secondary);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            height: var(--nav-height);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-logo {
            color: white;
            font-weight: 800;
            font-size: 1.2rem;
            letter-spacing: 0.5px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .nav-logo span {
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 5px;
        }

        nav ul li a {
            color: #9CA3AF;
            text-decoration: none;
            font-weight: 600;
            padding: 10px 18px;
            transition: 0.3s;
            border-radius: 8px;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        nav ul li a:hover, nav ul li a.active {
            color: white;
            background: var(--primary);
        }

        header {
            background: linear-gradient(135deg, #E5A93B 0%, #D35400 100%);
            color: white;
            padding: 90px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 8px solid var(--secondary);
        }

        header::before {
            content: "🍔 🌾 🍲 🍏";
            position: absolute;
            font-size: 6rem;
            opacity: 0.08;
            bottom: -10px;
            right: 10px;
            letter-spacing: 25px;
        }

        .profile-card {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            max-width: 750px;
            margin: 0 auto;
            padding: 35px;
            border-radius: 24px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            border: 1px solid rgba(255,255,255,0.2);
        }

        .profile-img-container {
            position: relative;
            width: 130px;
            height: 130px;
            margin: 0 auto 20px;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.8rem;
            border: 4px solid white;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .app-badge {
            position: absolute;
            bottom: -5px;
            right: -5px;
            background: var(--secondary);
            color: var(--primary);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
            border: 3px solid white;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }

        .container {
            max-width: 1200px;
            margin: 60px auto;
            padding: 0 20px;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 800;
            margin-bottom: 40px;
            text-align: center;
            position: relative;
            color: var(--secondary);
        }

        .section-title i {
            color: var(--primary);
            margin-right: 10px;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 5px;
            background: var(--primary);
            margin: 12px auto 0;
            border-radius: 4px;
        }

        .grid-layout {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 30px;
        }

        .custom-card {
            background: var(--card-bg);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.05);
            border: 1px solid #E5E7EB;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .custom-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(229, 169, 59, 0.15);
            border-color: var(--primary);
        }

        .card-header-badge {
            background: #FEF3C7;
            color: #D97706;
            padding: 6px 14px;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            margin-bottom: 12px;
        }

        .card-body {
            padding: 25px;
        }

        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 14px;
            margin-top: 15px;
            background: #E5E7EB;
            box-shadow: inset 0 2px 8px rgba(0,0,0,0.1);
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        .project-highlight-card {
            background: linear-gradient(to right, #FFFFFF, #FFFDF9);
            border-left: 6px solid var(--primary);
        }

        .btn-github {
            display: inline-flex;
            align-items: center;
            background: var(--secondary);
            color: white;
            padding: 10px 20px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            margin-top: 15px;
            transition: 0.3s;
        }

        .btn-github:hover {
            background: var(--primary);
        }

        .btn-github i {
            margin-right: 8px;
            font-size: 1.1rem;
        }

        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            margin-top: 20px;
        }

        .tech-badge {
            background: #F3F4F6;
            color: var(--secondary);
            padding: 8px 16px;
            border-radius: 12px;
            font-size: 0.85rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            border: 1px solid #E5E7EB;
        }

        .tech-badge i {
            margin-right: 6px;
            color: var(--primary);
        }

        footer {
            background: var(--secondary);
            color: #9CA3AF;
            text-align: center;
            padding: 40px 20px;
            font-size: 0.9rem;
            border-top: 4px solid var(--primary);
        }

        @media (max-width: 768px) {
            .nav-container { flex-direction: column; height: auto; padding: 10px; }
            nav { height: auto; }
            nav ul { margin-top: 10px; flex-wrap: wrap; justify-content: center; }
            html { scroll-padding-top: 140px; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="nav-container">
            <div class="nav-logo">
                <i class="fa-solid fa-utensils"></i> MEALIFY<span>.PORTFOLIO</span>
            </div>
            <ul>
                <li><a href="#profile"><i class="fa-solid fa-user"></i> Profile</a></li>
                <li><a href="#labs"><i class="fa-solid fa-flask"></i> Labs</a></li>
                <li><a href="#projects"><i class="fa-solid fa-code-branch"></i> Projects</a></li>
                <li><a href="#reflection"><i class="fa-solid fa-book-open"></i> Journey</a></li>
            </ul>
        </div>
    </nav>

    <header id="profile">
        <div class="profile-card">
            <div class="profile-img-container">
                <div class="profile-img">👩‍💻</div>
                <div class="app-badge" title="Mealify App Core"><i class="fa-solid fa-bowl-food"></i></div>
            </div>
            <h1 style="font-size: 2.5rem; font-weight: 800; margin-bottom: 5px;">AMIRA FARIZA BINTI SUHAIRI</h1>
            <p style="font-size: 1.1rem; opacity: 0.9; font-weight: 500; letter-spacing: 0.5px;">Matric No: A216295</p>
            <p style="font-size: 1rem; opacity: 0.8; margin-bottom: 20px;">Bachelor of Information Technology</p>
            
            <div style="background: rgba(0,0,0,0.2); padding: 15px 20px; border-radius: 14px; text-align: left; margin-top: 15px;">
                <h3 style="color: var(--primary); font-size: 1.1rem; margin-bottom: 6px;"><i class="fa-solid fa-wheat-awn"></i> SDG 2: Zero Hunger</h3>
                <p style="font-size: 0.9rem; opacity: 0.95; line-height: 1.5;">My digital application "Mealify" is dedicated to eliminating food waste and optimizing local food security operations. By providing instant local storage coordination and scalable cloud features, we build technical systems that make securing nutritional access for everyone a seamless reality.</p>
            </div>
        </div>
    </header>

    <div class="container">
        
        <section id="labs" style="margin-bottom: 80px;">
            <h2 class="section-title"><i class="fa-solid fa-kitchen-set"></i>Lab Task Submissions</h2>
            <div class="grid-layout">
                
                <div class="custom-card">
                    <div class="card-body">
                        <span class="card-header-badge"><i class="fa-solid fa-layer-group"></i> Exercise 1</span>
                        <h3 style="font-size: 1.25rem; margin-bottom: 8px;">Lab 1: UI Implementation</h3>
                        <p style="color: #6B7280; font-size: 0.9rem;">Exploration of declarative layout foundations inside Jetpack Compose, setting up high-fidelity text structures and theme alignment.</p>
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/K_ZLqwoBWxY?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>

                <div class="custom-card">
                    <div class="card-body">
                        <span class="card-header-badge"><i class="fa-solid fa-toggle-on"></i> Exercise 2</span>
                        <h3 style="font-size: 1.25rem; margin-bottom: 8px;">Lab 2: State & Interaction</h3>
                        <p style="color: #6B7280; font-size: 0.9rem;">Building dynamic user click handling logic, incorporating remembered mutable states to redraw the screen efficiently.</p>
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/GBF7YRdjefo?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>

                <div class="custom-card">
                    <div class="card-body">
                        <span class="card-header-badge"><i class="fa-solid fa-palette"></i> Exercise 3</span>
                        <h3 style="font-size: 1.25rem; margin-bottom: 8px;">Lab 3: Material Design</h3>
                        <p style="color: #6B7280; font-size: 0.9rem;">Implementing standard Material 3 layouts, structural Scaffold configurations, Top App Bars, and persistent buttons.</p>
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/HCDaFLcPB_M?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>

                <div class="custom-card">
                    <div class="card-body">
                        <span class="card-header-badge"><i class="fa-solid fa-route"></i> Exercise 4</span>
                        <h3 style="font-size: 1.25rem; margin-bottom: 8px;">Lab 4: Advanced Navigation</h3>
                        <p style="color: #6B7280; font-size: 0.9rem;">Developing declarative application routing control loops, establishing NavHost configurations and multi-screen state transfer pipelines.</p>
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/EXg05rhhv6Y?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>

                <div class="custom-card">
                    <div class="card-body">
                        <span class="card-header-badge"><i class="fa-solid fa-database"></i> Exercise 5</span>
                        <h3 style="font-size: 1.25rem; margin-bottom: 8px;">Lab 5: Room Data Persistence</h3>
                        <p style="color: #6B7280; font-size: 0.9rem;">Setting up persistent schema logic via local SQLite Room Entities, data access boundaries (DAOs), and asynchronous coroutines.</p>
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/NSC5CQEkoTU?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <section id="projects" style="margin-bottom: 80px;">
            <h2 class="section-title"><i class="fa-solid fa-diagram-project"></i>Major Course Projects</h2>
            <div class="grid-layout">
                
                <div class="custom-card project-highlight-card">
                    <div class="card-body">
                        <span class="card-header-badge" style="background:#E0F2FE; color:#0369A1;"><i class="fa-solid fa-boxes-stacked"></i> Project Phase 1</span>
                        <h3 style="font-size: 1.4rem; margin-bottom: 8px;">Mealify: Architectural Foundation</h3>
                        <p style="color: #4B5563; font-size: 0.95rem;">Establishing the core multi-screen framework (5 screens) using structural ViewModels to distribute unified state bindings safely across screen layers. Focuses heavily on clean navigation flow.</p>
                        
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/F-88hXKOw5o?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                        
                        <a href="https://github.com/YOUR_USERNAME" target="_blank" class="btn-github">
                            <i class="fa-brands fa-github"></i> View Project 1 Source Code
                        </a>
                    </div>
                </div>

                <div class="custom-card project-highlight-card" style="border-left-color: var(--accent-green);">
                    <div class="card-body">
                        <span class="card-header-badge" style="background:#DCFCE7; color:#15803D;"><i class="fa-solid fa-cloud-sun"></i> Project Phase 2</span>
                        <h3 style="font-size: 1.4rem; margin-bottom: 8px;">Mealify: Connected Cloud & Hardware</h3>
                        <p style="color: #4B5563; font-size: 0.95rem;">Extending Mealify into an advanced application by adding live Retrofit network queries, online Firebase Cloud synchronizations, and integrating the location GPS sensor tracking subsystem.</p>
                        
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/PLACEHOLDER_PROJECT2_VSR?modestbranding=1&rel=0" allowfullscreen></iframe>
                        </div>
                        
                        <a href="https://github.com/YOUR_USERNAME" target="_blank" class="btn-github" style="background:var(--accent-green);">
                            <i class="fa-brands fa-github"></i> View Project 2 Source Code
                        </a>
                    </div>
                </div>

            </div>
        </section>

        <section id="reflection">
            <h2 class="section-title"><i class="fa-solid fa-heart-pulse"></i>Learning Journey & Reflections</h2>
            <div class="custom-card" style="padding: 35px; border-radius: 24px;">
                <p style="font-size: 1.05rem; color: #374151; margin-bottom: 25px; text-align: justify; line-height: 1.8;">
                    "My developmental path throughout this course has been an incredible transformation in understanding enterprise-grade mobile application design. Moving from basic standalone user interfaces in Lab 1 to managing complex asynchronous live persistence loops in Project 2 allowed me to appreciate modular programming. Overcoming challenges with Kotlin Symbol Processing (KSP) and background cloud thread synchronization deeply boosted my troubleshooting intuition. Aligning my engineering work with SDG 2: Zero Hunger gave me profound satisfaction, proving that software architecture can actively solve structural societal deficiencies."
                </p>
                
                <h4 style="text-align: center; font-weight: 700; margin-bottom: 15px; color: var(--secondary);">Confidently Mastered Tech Stack</h4>
                <div class="badge-container">
                    <div class="tech-badge"><i class="fa-solid fa-cube"></i> Jetpack Compose</div>
                    <div class="tech-badge"><i class="fa-solid fa-database"></i> Room Persistence</div>
                    <div class="tech-badge"><i class="fa-solid fa-cloud"></i> Firebase Firestore</div>
                    <div class="tech-badge"><i class="fa-solid fa-cloud-arrow-down"></i> Retrofit REST API</div>
                    <div class="tech-badge"><i class="fa-solid fa-location-crosshairs"></i> GPS Location Sensor</div>
                    <div class="tech-badge"><i class="fa-solid fa-diagram-project"></i> MVVM Architecture</div>
                </div>
            </div>
        </section>

    </div>

    <footer>
        <p>© 2026 Amira (A216295) | Mobile Programming e-Portfolio Submission</p>
        <p style="font-size: 0.8rem; margin-top: 5px; opacity: 0.6;">Instructor: Cikgu Izwan | Universiti Kebangsaan Malaysia</p>
    </footer>

</body>
</html>
