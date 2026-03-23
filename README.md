
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shadow Reapers - Gaming Tournaments</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700;800;900&family=Rajdhani:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Base Styles */
        :root {
            --bg: #050507;
            --panel: #0b0b0d;
            --neon: #00fff7;
            --neon-dim: #0fe8df;
            --neon-glow: rgba(0, 255, 247, 0.5);
            --accent: #aefcff;
            --muted: #9fe3e0;
            --danger: #ff6b6b;
            --success: #6bff8d;
            --warning: #ffd166;
            --info: #4ecdc4;
            --purple: #9d4edd;
            --pink: #ff5c8a;
            --glass: rgba(255, 255, 255, 0.02);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            --gradient-1: linear-gradient(135deg, #00fff7 0%, #9d4edd 100%);
            --gradient-2: linear-gradient(135deg, #ff5c8a 0%, #ffd166 100%);
            --gradient-3: linear-gradient(135deg, #4ecdc4 0%, #6bff8d 100%);
            --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.1);
            --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);
            --shadow-xl: 0 20px 25px rgba(0, 0, 0, 0.1);
            --shadow-neon: 0 0 5px var(--neon-glow), 0 0 10px var(--neon-glow), 0 0 15px var(--neon-glow);
            --border-radius: 12px;
            --border-radius-lg: 16px;
            --border-radius-xl: 24px;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        html, body {
            height: 100%;
            margin: 0;
            font-family: 'Rajdhani', 'Orbitron', sans-serif;
            background: linear-gradient(180deg, #050507 0%, #070317 100%);
            color: #e9feff;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }
        
        /* Typography */
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Orbitron', sans-serif;
            font-weight: 700;
            margin-bottom: 0.5rem;
            line-height: 1.2;
        }
        
        h1 {
            font-size: 3.5rem;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(157, 78, 221, 0.3);
        }
        
        h2 {
            font-size: 2.5rem;
            color: var(--neon);
            text-shadow: 0 0 10px rgba(0, 255, 247, 0.3);
        }
        
        h3 {
            font-size: 1.75rem;
            color: var(--accent);
        }
        
        p {
            margin-bottom: 1rem;
            line-height: 1.6;
        }
        
        a {
            color: var(--neon);
            text-decoration: none;
            transition: var(--transition);
        }
        
        a:hover {
            color: var(--accent);
            text-shadow: 0 0 10px rgba(0, 255, 247, 0.5);
        }
        
        /* Layout */
        .app-shell {
            min-height: 100vh;
            position: relative;
            overflow: hidden;
        }
        
        .container {
            max-width: 1320px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .section {
            padding: 80px 0;
        }
        
        .center {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .flex {
            display: flex;
            gap: 24px;
            align-items: flex-start;
        }
        
        .col {
            flex: 1;
        }
        
        .text-center {
            text-align: center;
        }
        
        /* Landing Animation */
        .landing-wrap {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            background: radial-gradient(ellipse at center, rgba(9, 11, 38, 0.8) 0%, rgba(5, 5, 7, 0.9) 70%);
        }
        
        .logo-blob {
            position: absolute;
            inset: 0;
            background: radial-gradient(circle at 50% 40%, rgba(0, 255, 247, 0.1), transparent 30%);
            animation: pulse 8s infinite alternate;
        }
        
        .neon-logo {
            font-size: 5rem;
            font-weight: 900;
            color: var(--neon);
            text-shadow: 0 0 10px rgba(0, 255, 247, 0.5), 0 0 20px rgba(0, 255, 247, 0.3), 0 0 30px rgba(0, 255, 247, 0.1);
            transform-origin: center;
            letter-spacing: 6px;
            position: relative;
            z-index: 2;
        }
        
        .tagline {
            color: var(--muted);
            margin-top: 16px;
            font-size: 1.25rem;
            font-weight: 300;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        
        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background: var(--neon);
            color: #061014;
            border: none;
            padding: 12px 24px;
            border-radius: var(--border-radius);
            cursor: pointer;
            font-weight: 600;
            font-family: 'Orbitron', sans-serif;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 14px 40px rgba(0, 255, 247, 0.2);
        }
        
        .btn-ghost {
            background: transparent;
            border: 1px solid rgba(0, 255, 247, 0.3);
            color: var(--neon);
            padding: 10px 20px;
            border-radius: var(--border-radius);
            transition: var(--transition);
        }
        
        .btn-ghost:hover {
            background: rgba(0, 255, 247, 0.1);
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(0, 255, 247, 0.15);
        }
        
        .btn-success {
            background: var(--success);
            color: #061014;
        }
        
        .btn-danger {
            background: var(--danger);
            color: #fff;
        }
        
        /* Cards */
        .card {
            background: var(--panel);
            border-radius: var(--border-radius-lg);
            padding: 24px;
            border: 1px solid rgba(255, 255, 255, 0.03);
            box-shadow: var(--shadow-lg);
            transition: var(--transition);
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            border-color: rgba(0, 255, 247, 0.1);
        }
        
        /* Tournament Box */
        .tournament-box {
            background: linear-gradient(180deg, rgba(255, 255, 255, 0.02), rgba(255, 255, 255, 0.01));
            border: 1px solid rgba(0, 255, 247, 0.08);
            padding: 24px;
            border-radius: var(--border-radius);
            margin: 16px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: var(--transition);
        }
        
        .tournament-box:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 255, 247, 0.1);
            border-color: rgba(0, 255, 247, 0.15);
        }
        
        .tournament-left {
            flex: 1;
        }
        
        .tournament-meta {
            color: var(--muted);
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 16px;
            flex-wrap: wrap;
            margin: 8px 0;
        }
        
        .tournament-desc {
            color: #bff9f6;
            margin-top: 12px;
            line-height: 1.5;
        }
        
        /* Forms */
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-label {
            display: block;
            margin-bottom: 8px;
            color: var(--muted);
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            background: #061018;
            border: 1px solid rgba(0, 255, 247, 0.1);
            padding: 12px 16px;
            border-radius: var(--border-radius);
            color: var(--neon);
            transition: var(--transition);
            font-family: inherit;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--neon);
            box-shadow: 0 0 0 3px rgba(0, 255, 247, 0.1);
        }
        
        .form-row {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
            margin: 16px 0;
        }
        
        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(5, 5, 7, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            z-index: 1000;
            padding: 16px 0;
            transition: var(--transition);
        }
        
        .navbar.scrolled {
            padding: 10px 0;
            background: rgba(5, 5, 7, 0.95);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .navbar-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            max-width: 1320px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .navbar-brand {
            font-family: 'Orbitron', sans-serif;
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--neon);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .navbar-nav {
            display: flex;
            align-items: center;
            gap: 24px;
        }
        
        .nav-link {
            color: var(--muted);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }
        
        .nav-link::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--neon);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover {
            color: var(--neon);
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        /* Chat & Leaderboard */
        .chat-window {
            height: 400px;
            overflow-y: auto;
            padding: 16px;
            border-radius: var(--border-radius);
            background: linear-gradient(180deg, #070707, #0b0b0b);
            border: 1px solid rgba(0, 255, 247, 0.05);
        }
        
        .chat-msg {
            background: linear-gradient(90deg, var(--neon), var(--neon-dim));
            color: #031416;
            padding: 12px;
            border-radius: var(--border-radius);
            margin: 12px 0;
            font-weight: 600;
            transition: var(--transition);
        }
        
        .leaderboard {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .leaderboard li {
            padding: 12px;
            border-bottom: 1px dashed rgba(255, 255, 255, 0.05);
            display: flex;
            justify-content: space-between;
            font-weight: 600;
            color: var(--muted);
            transition: var(--transition);
        }
        
        .leaderboard li:hover {
            background: rgba(0, 255, 247, 0.05);
        }
        
        /* Modals */
        .modal-overlay {
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            padding: 20px;
            backdrop-filter: blur(5px);
        }
        
        .modal-content {
            background: #071014;
            border-radius: var(--border-radius-lg);
            padding: 32px;
            border: 1px solid rgba(0, 255, 247, 0.1);
            max-width: 500px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 24px;
        }
        
        .modal-close {
            background: none;
            border: none;
            color: var(--muted);
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
            width: 32px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }
        
        .modal-close:hover {
            color: var(--neon);
            background: rgba(0, 255, 247, 0.1);
        }
        
        /* Badges */
        .badge {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .badge-success {
            background: var(--success);
            color: #061014;
        }
        
        .badge-info {
            background: var(--info);
            color: #061014;
        }
        
        .badge-danger {
            background: var(--danger);
            color: #fff;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes fadeUp {
            0% { transform: translateY(40px) scale(0.6); opacity: 0; }
            70% { transform: translateY(-10px) scale(1.08); opacity: 1; }
            100% { transform: translateY(-120px) scale(1); opacity: 1; }
        }
        
        @keyframes pulse {
            0% { opacity: 0.5; }
            50% { opacity: 1; }
            100% { opacity: 0.5; }
        }
        
        @keyframes glow {
            0% { text-shadow: 0 0 5px rgba(0, 255, 247, 0.5); }
            50% { text-shadow: 0 0 20px rgba(0, 255, 247, 0.8), 0 0 30px rgba(0, 255, 247, 0.5); }
            100% { text-shadow: 0 0 5px rgba(0, 255, 247, 0.5); }
        }
        
        /* Utilities */
        .mt-1 { margin-top: 8px; }
        .mt-2 { margin-top: 16px; }
        .mt-3 { margin-top: 24px; }
        
        .mb-1 { margin-bottom: 8px; }
        .mb-2 { margin-bottom: 16px; }
        .mb-3 { margin-bottom: 24px; }
        
        .small { font-size: 0.9rem; color: var(--muted); }
        .muted { color: var(--muted); }
        
        /* Hero Section */
        .hero-section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: radial-gradient(ellipse at center, rgba(9, 11, 38, 0.8) 0%, rgba(5, 5, 7, 0.9) 70%);
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
        }
        
        .hero-title {
            font-size: 4rem;
            margin-bottom: 24px;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: glow 3s infinite;
        }
        
        .hero-subtitle {
            font-size: 1.5rem;
            color: var(--muted);
            margin-bottom: 32px;
            line-height: 1.6;
        }
        
        .hero-cta {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }
        
        /* Features Section */
        .features-section {
            position: relative;
        }
        
        .feature-box {
            text-align: center;
            padding: 32px 24px;
            border-radius: var(--border-radius-lg);
            background: rgba(11, 11, 13, 0.5);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
            height: 100%;
        }
        
        .feature-box:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            border-color: rgba(0, 255, 247, 0.1);
        }
        
        .feature-icon {
            font-size: 3rem;
            margin-bottom: 24px;
            color: var(--neon);
        }
        
        .feature-title {
            font-size: 1.5rem;
            margin-bottom: 16px;
            color: var(--accent);
        }
        
        .feature-description {
            color: var(--muted);
            line-height: 1.6;
        }
        
        /* Tournaments Section */
        .tournaments-section {
            background: linear-gradient(180deg, #050507 0%, #070317 100%);
            position: relative;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 16px;
        }
        
        .section-title p {
            font-size: 1.2rem;
            color: var(--muted);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .tournament-filters {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
            justify-content: center;
            margin-bottom: 40px;
        }
        
        .filter-btn {
            background: transparent;
            border: 1px solid rgba(0, 255, 247, 0.2);
            color: var(--muted);
            padding: 8px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .filter-btn:hover, .filter-btn.active {
            background: var(--neon);
            color: #061014;
            border-color: var(--neon);
        }
        
        /* Payment Methods */
        .payment-methods {
            display: flex;
            gap: 12px;
            margin-bottom: 20px;
        }
        
        .payment-method {
            flex: 1;
            padding: 16px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: var(--border-radius);
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .payment-method:hover {
            border-color: var(--neon);
        }
        
        .payment-method.active {
            border-color: var(--neon);
            background: rgba(0, 255, 247, 0.1);
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .flex {
                flex-direction: column;
            }
            
            .hero-title {
                font-size: 3rem;
            }
        }
        
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .tournament-box {
                flex-direction: column;
                align-items: flex-start;
                gap: 16px;
            }
            
            .navbar-nav {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div id="app" class="app-shell">
        <!-- Landing Animation -->
        <div id="landing" class="landing-wrap">
            <div class="logo-blob"></div>
            <div style="text-align: center;">
                <div class="neon-logo">SHADOW REAPERS</div>
                <div class="tagline">GEAR UP. COMPETE. CONQUER GLOBAL ARENAS.</div>
            </div>
        </div>

        <!-- Main Content (initially hidden) -->
        <div id="main-content" style="display: none;">
            <!-- Navigation -->
            <nav class="navbar">
                <div class="navbar-container">
                    <a href="#" class="navbar-brand">
                        <span>SHADOW</span> <span style="color: var(--accent);">REAPERS</span>
                    </a>
                    
                    <div class="navbar-nav">
                        <a href="#" class="nav-link active">Home</a>
                        <a href="#tournaments" class="nav-link">Tournaments</a>
                        <a href="#" class="nav-link">Leaderboard</a>
                        <a href="#" class="nav-link">FAQ</a>
                        <button class="btn btn-sm" id="admin-btn">Admin Login</button>
                    </div>
                </div>
            </nav>

            <!-- Hero Section -->
            <section class="hero-section">
                <div class="container">
                    <div class="hero-content">
                        <h1 class="hero-title">DOMINATE THE ARENA</h1>
                        <p class="hero-subtitle">
                            Join the ultimate gaming platform where champions are made. 
                            Compete in tournaments, climb leaderboards, and earn rewards in a 
                            community built for gamers.
                        </p>
                        <div class="hero-cta">
                            <button class="btn btn-lg" id="explore-tournaments">Explore Tournaments</button>
                            <button class="btn btn-ghost btn-lg">How It Works</button>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Features Section -->
            <section class="features-section section">
                <div class="container">
                    <div class="section-title">
                        <h2>WHY CHOOSE SHADOW REAPERS?</h2>
                        <p>We provide everything you need to compete at the highest level</p>
                    </div>
                    
                    <div class="flex">
                        <div class="col">
                            <div class="feature-box">
                                <div class="feature-icon">🏆</div>
                                <h3 class="feature-title">Competitive Tournaments</h3>
                                <p class="feature-description">
                                    Join daily tournaments with cash prizes and exclusive rewards for top performers.
                                    Our platform is designed to prepare you for international competition.
                                </p>
                            </div>
                        </div>
                        
                        <div class="col">
                            <div class="feature-box">
                                <div class="feature-icon">📊</div>
                                <h3 class="feature-title">Real-time Leaderboards</h3>
                                <p class="feature-description">
                                    Track your progress and compare your skills with players from around the world.
                                    Climb the ranks and prove you're among the best.
                                </p>
                            </div>
                        </div>
                        
                        <div class="col">
                            <div class="feature-box">
                                <div class="feature-icon">💬</div>
                                <h3 class="feature-title">Community Chat</h3>
                                <p class="feature-description">
                                    Coordinate with your team and chat with other players in dedicated tournament rooms.
                                    Build your squad and strategize for victory.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Tournaments Section -->
            <section id="tournaments" class="tournaments-section section">
                <div class="container">
                    <div class="section-title">
                        <h2>UPCOMING TOURNAMENTS</h2>
                        <p>Join upcoming tournaments and prove your skills</p>
                    </div>
                    
                    <div class="tournament-filters">
                        <button class="filter-btn active" data-game="all">All Games</button>
                        <button class="filter-btn" data-game="freefire">FreeFire</button>
                        <button class="filter-btn" data-game="bgmi">BGMI</button>
                        <button class="filter-btn" data-game="cod">COD</button>
                        <button class="filter-btn" data-game="pubg">PUBG</button>
                        <button class="filter-btn" data-game="valorant">Valorant</button>
                        <button class="filter-btn" data-game="coc">COC</button>
                    </div>
                    
                    <div id="tournaments-container">
                        <!-- Tournaments will be loaded here -->
                    </div>
                </div>
            </section>

            <!-- Footer -->
            <footer style="background: #050507; border-top: 1px solid rgba(255,255,255,0.05); padding: 60px 0 30px;">
                <div class="container">
                    <div class="text-center">
                        <p class="muted">© Shadow Reapers. All rights reserved.</p>
                        <p class="small muted">This is a demo platform. For production use, implement proper backend and payment processing.</p>
                    </div>
                </div>
            </footer>
        </div>

        <!-- Admin Login Modal -->
        <div id="admin-modal" class="modal-overlay" style="display: none;">
            <div class="modal-content">
                <div class="modal-header">
                    <h2>Admin Login</h2>
                    <button class="modal-close" id="close-admin">×</button>
                </div>
                <div class="modal-body">
                    <p class="small muted">Enter admin password to manage tournaments</p>
                    <div class="form-group">
                        <input type="password" class="form-control" placeholder="Admin Password" id="admin-password">
                    </div>
                    <div class="form-group">
                        <button class="btn btn-success w-100" id="admin-login">Login</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Join Tournament Modal -->
        <div id="join-modal" class="modal-overlay" style="display: none;">
            <div class="modal-content">
                <div class="modal-header">
                    <h2>Join Tournament</h2>
                    <button class="modal-close" id="close-join">×</button>
                </div>
                <div class="modal-body">
                    <div id="join-form">
                        <div class="form-group">
                            <label class="form-label">Full Name</label>
                            <input type="text" class="form-control" placeholder="Your Name" id="player-name">
                        </div>
                        <div class="form-group">
                            <label class="form-label">Game ID</label>
                            <input type="text" class="form-control" placeholder="Your Game ID" id="game-id">
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label">Age</label>
                                <input type="number" class="form-control" placeholder="Age" id="player-age">
                            </div>
                            <div class="form-group">
                                <label class="form-label">Date of Birth</label>
                                <input type="date" class="form-control" id="player-dob">
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label">Max Kills (Optional)</label>
                                <input type="number" class="form-control" placeholder="Maximum kills" id="max-kills">
                            </div>
                            <div class="form-group">
                                <label class="form-label">Total Matches (Optional)</label>
                                <input type="number" class="form-control" placeholder="Total matches played" id="total-matches">
                            </div>
                        </div>
                        <div class="form-group">
                            <button class="btn btn-success w-100" id="proceed-to-payment">Proceed to Payment</button>
                        </div>
                    </div>

                    <div id="payment-form" style="display: none;">
                        <div class="payment-summary">
                            <h4>Tournament: <span id="payment-tournament-name"></span></h4>
                            <p>Entry Fee: <strong>₹<span id="payment-amount"></span></strong></p>
                        </div>

                        <div class="form-group">
                            <label class="form-label">Select Payment Method</label>
                            <div class="payment-methods">
                                <div class="payment-method active" data-method="upi">
                                    <span>UPI</span>
                                </div>
                                <div class="payment-method" data-method="card">
                                    <span>Card</span>
                                </div>
                                <div class="payment-method" data-method="wallet">
                                    <span>Wallet</span>
                                </div>
                            </div>
                        </div>

                        <div class="form-group">
                            <label class="form-label">UPI ID</label>
                            <input type="text" class="form-control" placeholder="yourname@upi" id="upi-id">
                        </div>

                        <div class="form-group">
                            <button class="btn btn-success w-100" id="complete-payment">Pay Now</button>
                        </div>

                        <div style="text-align: center; margin-top: 20px; padding-top: 20px; border-top: 1px solid rgba(255,255,255,0.1);">
                            <p class="small muted">
                                🔒 Your payment is secure and encrypted
                            </p>
                        </div>
                    </div>

                    <div id="payment-success" style="display: none; text-align: center;">
                        <div style="font-size: 4rem; color: var(--success);">✓</div>
                        <h3>Payment Successful!</h3>
                        <p>You have successfully registered for <strong id="success-tournament-name"></strong></p>
                        <div class="payment-details">
                            <p><strong>Transaction ID:</strong> <span id="transaction-id"></span></p>
                            <p><strong>Amount Paid:</strong> ₹<span id="success-amount"></span></p>
                        </div>
                        <button class="btn btn-success mt-3" id="enter-tournament">Enter Tournament Room</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Tournament Room Modal -->
        <div id="tournament-room" class="modal-overlay" style="display: none;">
            <div class="modal-content" style="max-width: 1000px;">
                <div class="modal-header">
                    <h2>Tournament Room: <span id="room-tournament-name"></span></h2>
                    <button class="modal-close" id="close-room">×</button>
                </div>
                <div class="modal-body">
                    <div class="flex">
                        <div class="col">
                            <h3>Group Chat</h3>
                            <div class="chat-window">
                                <div class="chat-msg">
                                    <strong>Admin:</strong> Welcome to the tournament! Matches will begin in 15 minutes.
                                </div>
                                <div class="chat-msg" style="background: linear-gradient(90deg, #9ff, #70eaf0);">
                                    <strong>ProPlayer99:</strong> Good luck everyone!
                                </div>
                                <!-- More chat messages will be added here -->
                            </div>
                            <div class="form-group mt-2">
                                <input type="text" class="form-control" placeholder="Type your message...">
                                <button class="btn btn-sm mt-1">Send</button>
                            </div>
                        </div>
                        <div class="col">
                            <h3>Leaderboard</h3>
                            <ul class="leaderboard">
                                <li>
                                    <span>1. ShadowHunter</span>
                                    <span>Kills: 12</span>
                                </li>
                                <li>
                                    <span>2. ProPlayer99</span>
                                    <span>Kills: 10</span>
                                </li>
                                <li>
                                    <span>3. GameMaster</span>
                                    <span>Kills: 8</span>
                                </li>
                                <li>
                                    <span>4. NewPlayer</span>
                                    <span>Kills: 5</span>
                                </li>
                                <!-- More leaderboard entries will be added here -->
                            </ul>
                            <div class="mt-3">
                                <h4>Your Stats</h4>
                                <div class="form-row">
                                    <div class="form-group">
                                        <label class="form-label">Kills</label>
                                        <input type="number" class="form-control" value="0" id="player-kills">
                                    </div>
                                    <div class="form-group">
                                        <label class="form-label">Deaths</label>
                                        <input type="number" class="form-control" value="0" id="player-deaths">
                                    </div>
                                </div>
                                <button class="btn btn-sm">Update Stats</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Sample tournament data
            const tournaments = [
                {
                    id: 1,
                    name: "FreeFire Summer Cup",
                    game: "freefire",
                    date: "2023-09-15",
                    fee: 50,
                    prize: 5000,
                    description: "Hot summer cup—fast matches, big rewards. Join now for an exciting tournament experience with cash prizes and exclusive rewards.",
                    status: "upcoming",
                    participants: 32,
                    maxParticipants: 64
                },
                {
                    id: 2,
                    name: "Valorant Masters",
                    game: "valorant",
                    date: "2023-09-25",
                    fee: 120,
                    prize: 10000,
                    description: "Tactical 5v5 - international format practice. Perfect your strategies and compete against the best teams.",
                    status: "upcoming",
                    participants: 16,
                    maxParticipants: 32
                },
                {
                    id: 3,
                    name: "PUBG Mobile Championship",
                    game: "pubg",
                    date: "2023-10-05",
                    fee: 80,
                    prize: 8000,
                    description: "Battle royale championship with intense action. Show your survival skills and claim victory.",
                    status: "live",
                    participants: 48,
                    maxParticipants: 100
                },
                {
                    id: 4,
                    name: "COC Clan Wars",
                    game: "coc",
                    date: "2023-10-12",
                    fee: 40,
                    prize: 3000,
                    description: "Strategic clan wars for Clash of Clans players. Bring your best strategies and dominate the battlefield.",
                    status: "upcoming",
                    participants: 20,
                    maxParticipants: 40
                },
                {
                    id: 5,
                    name: "COD Mobile Mayhem",
                    game: "cod",
                    date: "2023-10-18",
                    fee: 60,
                    prize: 6000,
                    description: "Fast-paced action in Call of Duty Mobile. Test your skills in various game modes and maps.",
                    status: "upcoming",
                    participants: 28,
                    maxParticipants: 50
                },
                {
                    id: 6,
                    name: "BGMI Challenge",
                    game: "bgmi",
                    date: "2023-10-25",
                    fee: 70,
                    prize: 7000,
                    description: "The ultimate BGMI challenge for Indian players. Prove you're the best in the battlegrounds.",
                    status: "upcoming",
                    participants: 35,
                    maxParticipants: 75
                }
            ];

            // DOM Elements
            const landingElement = document.getElementById('landing');
            const mainContentElement = document.getElementById('main-content');
            const tournamentsContainer = document.getElementById('tournaments-container');
            const adminModal = document.getElementById('admin-modal');
            const joinModal = document.getElementById('join-modal');
            const tournamentRoom = document.getElementById('tournament-room');
            const adminBtn = document.getElementById('admin-btn');
            const closeAdmin = document.getElementById('close-admin');
            const closeJoin = document.getElementById('close-join');
            const closeRoom = document.getElementById('close-room');
            const exploreTournaments = document.getElementById('explore-tournaments');
            const filterButtons = document.querySelectorAll('.filter-btn');
            const joinForm = document.getElementById('join-form');
            const paymentForm = document.getElementById('payment-form');
            const paymentSuccess = document.getElementById('payment-success');
            const proceedToPayment = document.getElementById('proceed-to-payment');
            const completePayment = document.getElementById('complete-payment');
            const enterTournament = document.getElementById('enter-tournament');
            const paymentMethods = document.querySelectorAll('.payment-method');
            
            // Current selection variables
            let currentTournament = null;
            let currentPaymentMethod = 'upi';

            // Initialize the page
            function init() {
                // Show landing animation first
                setTimeout(() => {
                    landingElement.querySelector('.neon-logo').style.animation = 'fadeUp 1s forwards';
                }, 1000);
                
                // Then show main content after animation completes
                setTimeout(() => {
                    landingElement.style.display = 'none';
                    mainContentElement.style.display = 'block';
                    loadTournaments('all');
                    initEventListeners();
                }, 3000);
            }

            // Initialize event listeners
            function initEventListeners() {
                // Admin modal
                adminBtn.addEventListener('click', () => adminModal.style.display = 'flex');
                closeAdmin.addEventListener('click', () => adminModal.style.display = 'none');
                
                // Join modal
                closeJoin.addEventListener('click', () => joinModal.style.display = 'none');
                
                // Tournament room
                closeRoom.addEventListener('click', () => tournamentRoom.style.display = 'none');
                
                // Explore tournaments button
                exploreTournaments.addEventListener('click', () => {
                    document.getElementById('tournaments').scrollIntoView({ behavior: 'smooth' });
                });
                
                // Filter buttons
                filterButtons.forEach(btn => {
                    btn.addEventListener('click', () => {
                        filterButtons.forEach(b => b.classList.remove('active'));
                        btn.classList.add('active');
                        loadTournaments(btn.dataset.game);
                    });
                });
                
                // Payment methods
                paymentMethods.forEach(method => {
                    method.addEventListener('click', () => {
                        paymentMethods.forEach(m => m.classList.remove('active'));
                        method.classList.add('active');
                        currentPaymentMethod = method.dataset.method;
                    });
                });
                
                // Proceed to payment
                proceedToPayment.addEventListener('click', () => {
                    // Basic validation
                    const playerName = document.getElementById('player-name').value;
                    const gameId = document.getElementById('game-id').value;
                    
                    if (!playerName || !gameId) {
                        alert('Please enter your name and game ID');
                        return;
                    }
                    
                    joinForm.style.display = 'none';
                    paymentForm.style.display = 'block';
                    
                    // Set payment details
                    document.getElementById('payment-tournament-name').textContent = currentTournament.name;
                    document.getElementById('payment-amount').textContent = currentTournament.fee;
                });
                
                // Complete payment
                completePayment.addEventListener('click', () => {
                    // Validate UPI ID if UPI selected
                    if (currentPaymentMethod === 'upi') {
                        const upiId = document.getElementById('upi-id').value;
                        if (!upiId || !upiId.includes('@')) {
                            alert('Please enter a valid UPI ID');
                            return;
                        }
                    }
                    
                    // Simulate payment processing
                    paymentForm.style.display = 'none';
                    paymentSuccess.style.display = 'block';
                    
                    // Set success details
                    document.getElementById('success-tournament-name').textContent = currentTournament.name;
                    document.getElementById('success-amount').textContent = currentTournament.fee;
                    document.getElementById('transaction-id').textContent = 'TXN' + Math.random().toString(36).substr(2, 9).toUpperCase();
                });
                
                // Enter tournament room
                enterTournament.addEventListener('click', () => {
                    joinModal.style.display = 'none';
                    tournamentRoom.style.display = 'flex';
                    document.getElementById('room-tournament-name').textContent = currentTournament.name;
                });
                
                // Admin login
                document.getElementById('admin-login').addEventListener('click', () => {
                    const password = document.getElementById('admin-password').value;
                    if (password === 'admin123') {
                        alert('Admin login successful! Tournament management would be implemented here.');
                        adminModal.style.display = 'none';
                    } else {
                        alert('Incorrect password. Try "admin123" for demo.');
                    }
                });
            }

            // Load tournaments based on filter
            function loadTournaments(gameFilter) {
                tournamentsContainer.innerHTML = '';
                
                const filteredTournaments = gameFilter === 'all' 
                    ? tournaments 
                    : tournaments.filter(t => t.game === gameFilter);
                
                // Sort by date (upcoming first)
                filteredTournaments.sort((a, b) => new Date(a.date) - new Date(b.date));
                
                if (filteredTournaments.length === 0) {
                    tournamentsContainer.innerHTML = `
                        <div class="text-center">
                            <p class="muted">No tournaments found for this game.</p>
                        </div>
                    `;
                    return;
                }
                
                filteredTournaments.forEach(tournament => {
                    const progress = (tournament.participants / tournament.maxParticipants) * 100;
                    const tournamentElement = document.createElement('div');
                    tournamentElement.className = 'tournament-box';
                    tournamentElement.innerHTML = `
                        <div class="tournament-left">
                            <div style="display: flex; align-items: center; gap: 12px; flex-wrap: wrap;">
                                <div>
                                    <strong style="color: var(--neon);">${tournament.name}</strong>
                                    <div class="tournament-meta">
                                        ${tournament.game.toUpperCase()} • ${formatDate(tournament.date)} • ₹${tournament.fee}
                                        <span class="badge ${tournament.status === 'live' ? 'badge-success' : 'badge-info'}">
                                            ${tournament.status}
                                        </span>
                                    </div>
                                </div>
                            </div>
                            <div class="tournament-desc">${tournament.description}</div>
                            <div class="tournament-progress" style="margin-top: 16px;">
                                <div style="background: rgba(255,255,255,0.1); height: 8px; border-radius: 4px; overflow: hidden;">
                                    <div style="background: var(--neon); width: ${progress}%; height: 100%;"></div>
                                </div>
                                <div style="display: flex; justify-content: space-between; margin-top: 8px;">
                                    <span class="small">${tournament.participants} / ${tournament.maxParticipants} Participants</span>
                                    <span class="small">Prize: ₹${tournament.prize}</span>
                                </div>
                            </div>
                        </div>
                        <div>
                            <button class="btn join-btn" data-id="${tournament.id}">Join Tournament</button>
                            <div style="margin-top: 8px;"><small class="muted">Organized by Admin</small></div>
                        </div>
                    `;
                    
                    tournamentsContainer.appendChild(tournamentElement);
                });
                
                // Add event listeners to join buttons
                document.querySelectorAll('.join-btn').forEach(btn => {
                    btn.addEventListener('click', () => {
                        const tournamentId = parseInt(btn.dataset.id);
                        currentTournament = tournaments.find(t => t.id === tournamentId);
                        openJoinModal();
                    });
                });
            }

            // Open join modal
            function openJoinModal() {
                joinModal.style.display = 'flex';
                joinForm.style.display = 'block';
                paymentForm.style.display = 'none';
                paymentSuccess.style.display = 'none';
                
                // Reset form
                document.getElementById('player-name').value = '';
                document.getElementById('game-id').value = '';
                document.getElementById('player-age').value = '';
                document.getElementById('player-dob').value = '';
                document.getElementById('max-kills').value = '';
                document.getElementById('total-matches').value = '';
                document.getElementById('upi-id').value = '';
            }

            // Format date
            function formatDate(dateString) {
                const options = { year: 'numeric', month: 'short', day: 'numeric' };
                return new Date(dateString).toLocaleDateString(undefined, options);
            }

            // Initialize the app
            init();
        });
    </script>
</body>
</html>
