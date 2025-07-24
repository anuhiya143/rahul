<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Rahul - Mirror of Memories</title>
    <style>
        /* CSS Styles */
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600;700&display=swap');
        
        :root {
            --primary: #ff6b6b;
            --secondary: #4ecdc4;
            --dark: #292f36;
            --light: #f7fff7;
            --accent: #ffbe0b;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--dark);
            color: var(--light);
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('IMG20231029202820.jpg') center/cover no-repeat;
        }
        
        .header-content {
            z-index: 2;
        }
        
        h1 {
            font-size: 5rem;
            margin-bottom: 20px;
            font-family: 'Dancing Script', cursive;
            color: var(--primary);
            text-shadow: 3px 3px 0 rgba(0,0,0,0.2);
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            color: var(--secondary);
        }
        
        .birthday-date {
            font-size: 1.8rem;
            margin-bottom: 40px;
            color: var(--accent);
        }
        
        .btn {
            display: inline-block;
            padding: 15px 30px;
            background: var(--primary);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
        }
        
        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        
        .btn-memories {
            background: var(--secondary);
        }
        
        .floating-balloons {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 1;
            pointer-events: none;
        }
        
        .balloon {
            position: absolute;
            width: 50px;
            height: 70px;
            border-radius: 50%;
            opacity: 0.7;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-50px) rotate(5deg);
            }
        }
        
        /* Mirror Section */
        .mirror-section {
            padding: 100px 0;
            background: linear-gradient(135deg, #292f36 0%, #1a1e23 100%);
            position: relative;
        }
        
        .section-title {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 60px;
            font-family: 'Dancing Script', cursive;
            color: var(--accent);
        }
        
        .mirror-container {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            gap: 30px;
            perspective: 1000px;
        }
        
        .mirror {
            width: 300px;
            height: 400px;
            background: rgba(255,255,255,0.1);
            border-radius: 20px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            transition: all 0.5s ease;
            transform-style: preserve-3d;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            cursor: pointer;
        }
        
        .mirror:hover {
            transform: translateY(-10px) rotateY(10deg);
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
        }
        
        .mirror-img {
            width: 100%;
            height: 70%;
            object-fit: cover;
            border-radius: 15px;
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }
        
        .mirror:hover .mirror-img {
            transform: scale(1.05);
        }
        
        .mirror-caption {
            font-size: 1.2rem;
            text-align: center;
            color: white;
            font-weight: 600;
        }
        
        /* Equality Section */
        .equality-section {
            padding: 100px 0;
            background: url('IMG20230930123453.jpg') center/cover no-repeat fixed;
            background-color: rgba(0,0,0,0.7);
            background-blend-mode: overlay;
            color: white;
            text-align: center;
        }
        
        .equality-title {
            font-size: 2.5rem;
            margin-bottom: 30px;
            font-family: 'Dancing Script', cursive;
        }
        
        /* Life Section */
        .life-section {
            padding: 100px 0;
            background: url('IMG20240303160326.jpg') center/cover no-repeat fixed;
            background-color: rgba(0,0,0,0.7);
            background-blend-mode: overlay;
            color: white;
            text-align: center;
        }
        
        .life-quote {
            font-size: 2.5rem;
            font-family: 'Dancing Script', cursive;
            margin-bottom: 30px;
        }
        
        /* Photo Grid Section */
        .photo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            padding: 50px 0;
        }
        
        .photo-item {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            height: 250px;
            transition: all 0.3s ease;
        }
        
        .photo-item:hover {
            transform: scale(1.03);
            box-shadow: 0 10px 30px rgba(0,0,0,0.4);
        }
        
        .photo-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: all 0.5s ease;
        }
        
        .photo-item:hover img {
            transform: scale(1.1);
        }
        
        .photo-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0,0,0,0.7);
            color: white;
            padding: 10px;
            transform: translateY(100%);
            transition: all 0.3s ease;
        }
        
        .photo-item:hover .photo-caption {
            transform: translateY(0);
        }
        
        /* Footer */
        footer {
            background: #1a1e23;
            padding: 30px 0;
            text-align: center;
        }
        
        .footer-text {
            font-size: 1.2rem;
            color: var(--secondary);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 3rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .mirror {
                width: 250px;
                height: 350px;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="header-content">
            <h1>Happy Birthday Rahul!</h1>
            <p class="subtitle">Mirror of Our Memories</p>
            <p class="birthday-date">Celebrating You Today and Always</p>
            <a href="#memories" class="btn btn-memories">View Our Journey</a>
        </div>
        <div class="floating-balloons" id="balloons-container"></div>
    </header>
    
    <!-- Mirror of Memories Section -->
    <section class="mirror-section" id="memories">
        <div class="container">
            <h2 class="section-title">Mirror of Memories</h2>
            <div class="mirror-container">
                <div class="mirror">
                    <img src="IMG20231029202820.jpg" alt="Birthday Celebration" class="mirror-img">
                    <p class="mirror-caption">Celebrating You</p>
                </div>
                <div class="mirror">
                    <img src="IMG20240303160326.jpg" alt="Live Your Life" class="mirror-img">
                    <p class="mirror-caption">Live Your Life</p>
                </div>
                <div class="mirror">
                    <img src="IMG20230930123453.jpg" alt="Statue of Equality" class="mirror-img">
                    <p class="mirror-caption">Equality</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Equality Section -->
    <section class="equality-section">
        <div class="container">
            <h2 class="equality-title">Statue of Equality</h2>
            <p>Just like this monument stands for balance, our friendship has always been about equality and mutual respect.</p>
        </div>
    </section>
    
    <!-- Life Section -->
    <section class="life-section">
        <div class="container">
            <h2 class="life-quote">"Live Your Life"</h2>
            <p>Wishing you a life full of adventures, happiness and wonderful moments!</p>
        </div>
    </section>
    
    <!-- Photo Grid Section -->
    <section class="container">
        <h2 class="section-title">Our Moments Together</h2>
        <div class="photo-grid">
            <div class="photo-item">
                <img src="IMG-20240724-WA0012.jpg" alt="Baco John">
                <div class="photo-caption">Baco John Moments</div>
            </div>
            <div class="photo-item">
                <img src="IMG-20240724-WA0004.jpg" alt="Contact">
                <div class="photo-caption">Always in Touch</div>
            </div>
            <div class="photo-item">
                <img src="IMG-20241024-WA0107.jpg" alt="Rich Blind">
                <div class="photo-caption">Deep Conversations</div>
            </div>
            <div class="photo-item">
                <img src="IMG-20240724-WA0016.jpg" alt="RCH">
                <div class="photo-caption">Adventure Time</div>
            </div>
            <div class="photo-item">
                <img src="IMG_20250208_134655_758.webp" alt="Motorcar">
                <div class="photo-caption">Road Trips</div>
            </div>
            <div class="photo-item">
                <img src="Screenshot_2025-07-24-18-00-21-65_7352322957d4404136654ef4adb64504~2.jpg" alt="Oho Players">
                <div class="photo-caption">Fun Times</div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p class="footer-text">Created with love for Rahul's special day © 2024</p>
        </div>
    </footer>
    
    <script>
        // JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Create floating balloons
            const balloonsContainer = document.getElementById('balloons-container');
            const colors = ['#ff6b6b', '#4ecdc4', '#ffbe0b', '#a663cc', '#5e60ce'];
            
            for (let i = 0; i < 15; i++) {
                const balloon = document.createElement('div');
                balloon.classList.add('balloon');
                balloon.style.left = ${Math.random() * 100}%;
                balloon.style.top = ${Math.random() * 100}%;
                balloon.style.background = colors[Math.floor(Math.random() * colors.length)];
                balloon.style.animationDuration = ${4 + Math.random() * 6}s;
                balloon.style.animationDelay = ${Math.random() * 5}s;
                balloon.style.width = ${30 + Math.random() * 40}px;
                balloon.style.height = ${40 + Math.random() * 60}px;
                balloonsContainer.appendChild(balloon);
            }
            
            // Mirror hover effect
            const mirrors = document.querySelectorAll('.mirror');
            mirrors.forEach(mirror => {
                mirror.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px) rotateY(10deg)';
                });
                mirror.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) rotateY(0)';
                });
            });
            
            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
            
            // Birthday confetti effect
            const header = document.querySelector('header');
            header.addEventListener('click', function() {
                createConfetti();
            });
            
            function createConfetti() {
                const confettiCount = 100;
                const confettiContainer = document.createElement('div');
                confettiContainer.style.position = 'fixed';
                confettiContainer.style.top = '0';
                confettiContainer.style.left = '0';
                confettiContainer.style.width = '100%';
                confettiContainer.style.height = '100%';
                confettiContainer.style.pointerEvents = 'none';
                confettiContainer.style.zIndex = '1000';
                document.body.appendChild(confettiContainer);
                
                for (let i = 0; i < confettiCount; i++) {
                    const confetti = document.createElement('div');
                    confetti.style.position = 'absolute';
                    confetti.style.width = '10px';
                    confetti.style.height = '10px';
                    confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.left = ${Math.random() * 100}%;
                    confetti.style.top = '-10px';
                    confetti.style.borderRadius = '50%';
                    confetti.style.opacity = '0.8';
                    
                    const animation = confetti.animate([
                        { transform: 'translateY(0) rotate(0deg)', opacity: 0.8 },
                        { transform: translateY(${window.innerHeight}px) rotate(${360 + Math.random() * 360}deg), opacity: 0 }
                    ], {
                        duration: 2000 + Math.random() * 3000,
                        easing: 'cubic-bezier(0.1, 0.8, 0.3, 1)'
                    });
                    
                    confettiContainer.appendChild(confetti);
                    
                    animation.onfinish = () => {
                        confetti.remove();
                        if (confettiContainer.children.length === 0) {
                            confettiContainer.remove();
                        }
                    };
                }
            }
        });
    </script>
</body>
</html>
