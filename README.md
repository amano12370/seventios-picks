<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seventios Sports Picks</title>
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID" crossorigin="anonymous"></script>
    <style>
        :root {
            --primary-color: #1e3a8a;
            --secondary-color: #facc15;
            --background-color: #0f172a;
            --text-color: #f8fafc;
            --card-bg: #1e293b;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 600px;
            margin: 0 auto;
            padding: 1rem;
        }
        
        header {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 1.5rem 0;
            text-align: center;
            border-bottom: 2px solid var(--secondary-color);
            margin-bottom: 1.5rem;
        }
        
        header h1 {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            color: var(--secondary-color);
        }
        
        header p {
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .tab-container {
            display: flex;
            justify-content: center;
            margin-bottom: 1.5rem;
        }
        
        .tab {
            padding: 0.75rem 1rem;
            background-color: var(--card-bg);
            border: none;
            color: var(--text-color);
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            text-align: center;
        }
        
        .tab.active {
            background-color: var(--primary-color);
            color: var(--secondary-color);
            border-bottom: 3px solid var(--secondary-color);
        }
        
        .content {
            display: none;
        }
        
        .content.active {
            display: block;
        }
        
        .pick-card {
            background-color: var(--card-bg);
            border-radius: 8px;
            padding: 1rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            border-left: 4px solid var(--secondary-color);
        }
        
        .pick-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.75rem;
            padding-bottom: 0.5rem;
            border-bottom: 1px solid #334155;
        }
        
        .pick-header h3 {
            color: var(--secondary-color);
            font-size: 1.2rem;
        }
        
        .pick-body {
            margin-bottom: 0.75rem;
        }
        
        .match-teams {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        .pick-prediction {
            display: inline-block;
            background-color: var(--primary-color);
            color: var(--secondary-color);
            padding: 0.5rem;
            border-radius: 4px;
            font-weight: bold;
        }
        
        .confidence {
            display: flex;
            align-items: center;
            margin-top: 0.75rem;
        }
        
        .confidence-bar {
            flex: 1;
            height: 6px;
            background-color: #334155;
            border-radius: 3px;
            overflow: hidden;
            margin-left: 0.5rem;
        }
        
        .confidence-level {
            height: 100%;
            background-color: var(--secondary-color);
        }
        
        .ad-container {
            background-color: var(--card-bg);
            padding: 1rem;
            text-align: center;
            margin: 1.5rem 0;
            border-radius: 8px;
        }
        
        .subscription-box {
            background-color: var(--primary-color);
            border-radius: 8px;
            padding: 1.5rem;
            text-align: center;
            margin: 2rem 0;
        }
        
        .subscription-box h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }
        
        .email-input {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }
        
        .email-input input {
            padding: 0.75rem;
            border-radius: 4px;
            border: none;
            font-size: 1rem;
        }
        
        .subscribe-btn {
            padding: 0.75rem 1rem;
            background-color: var(--secondary-color);
            color: var(--primary-color);
            border: none;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .subscribe-btn:hover {
            opacity: 0.9;
        }
        
        footer {
            text-align: center;
            padding: 2rem 0;
            border-top: 1px solid #334155;
            margin-top: 2rem;
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .social-link {
            color: var(--secondary-color);
            text-decoration: none;
        }
        
        /* Notification */
        .notification {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: var(--primary-color);
            color: var(--text-color);
            padding: 1rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            display: none;
            z-index: 100;
            max-width: 90%;
            text-align: center;
        }
        
        .notification.show {
            display: block;
            animation: fadeIn 0.3s ease, fadeOut 0.3s ease 2.7s forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes fadeOut {
            from { opacity: 1; }
            to { opacity: 0; }
        }

        /* Loading animation */
        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: var(--secondary-color);
            animation: spin 1s ease-in-out infinite;
            margin-right: 10px;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        /* Responsive */
        @media (max-width: 480px) {
            header h1 {
                font-size: 1.75rem;
            }
            
            .tab {
                padding: 0.6rem 0.5rem;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Seventios Sports Picks</h1>
            <p>Daily Expert Predictions | Straight from Morocco</p>
        </header>
        
        <div class="tab-container">
            <button class="tab active" onclick="openTab('today')">TODAY'S PICKS</button>
            <button class="tab" onclick="openTab('tomorrow')">TOMORROW</button>
            <button class="tab" onclick="openTab('premium')">VIP PICKS</button>
        </div>
        
        <div id="today" class="content active">
            <div class="pick-card">
                <div class="pick-header">
                    <h3>Football Pick of the Day</h3>
                    <span>May 6, 2025</span>
                </div>
                <div class="pick-body">
                    <div class="match-teams">Barcelona vs Real Madrid</div>
                    <div class="pick-prediction">Both Teams to Score (BTTS)</div>
                    <div class="confidence">
                        <span>Confidence:</span>
                        <div class="confidence-bar">
                            <div class="confidence-level" style="width: 85%;"></div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="ad-container">
                <!-- Ad placeholder -->
                <div style="background-color: #334155; color: #94a3b8; padding: 20px; border-radius: 4px;">
                    Advertisement Space
                </div>
            </div>
            
            <div class="pick-card">
                <div class="pick-header">
                    <h3>NBA Pick</h3>
                    <span>May 6, 2025</span>
                </div>
                <div class="pick-body">
                    <div class="match-teams">Lakers vs Warriors</div>
                    <div class="pick-prediction">Under 220.5 Points</div>
                    <div class="confidence">
                        <span>Confidence:</span>
                        <div class="confidence-bar">
                            <div class="confidence-level" style="width: 75%;"></div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="pick-card">
                <div class="pick-header">
                    <h3>Tennis Pick</h3>
                    <span>May 6, 2025</span>
                </div>
                <div class="pick-body">
                    <div class="match-teams">Nadal vs Djokovic</div>
                    <div class="pick-prediction">Over 3.5 Sets</div>
                    <div class="confidence">
                        <span>Confidence:</span>
                        <div class="confidence-bar">
                            <div class="confidence-level" style="width: 90%;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="tomorrow" class="content">
            <div class="pick-card">
                <div class="pick-header">
                    <h3>Football Pick</h3>
                    <span>May 7, 2025</span>
                </div>
                <div class="pick-body">
                    <div class="match-teams">Manchester City vs Liverpool</div>
                    <div class="pick-prediction">Over 2.5 Goals</div>
                    <div class="confidence">
                        <span>Confidence:</span>
                        <div class="confidence-bar">
                            <div class="confidence-level" style="width: 80%;"></div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="ad-container">
                <!-- Ad placeholder -->
                <div style="background-color: #334155; color: #94a3b8; padding: 20px; border-radius: 4px;">
                    Advertisement Space
                </div>
            </div>
            
            <div class="pick-card">
                <div class="pick-header">
                    <h3>NBA Pick</h3>
                    <span>May 7, 2025</span>
                </div>
                <div class="pick-body">
                    <div class="match-teams">Celtics vs Bucks</div>
                    <div class="pick-prediction">Celtics -4.5</div>
                    <div class="confidence">
                        <span>Confidence:</span>
                        <div class="confidence-bar">
                            <div class="confidence-level" style="width: 70%;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="premium" class="content">
            <div style="text-align: center; padding: 2rem 0;">
                <h2 style="color: var(--secondary-color); margin-bottom: 1rem;">VIP Premium Picks</h2>
                <p style="margin-bottom: 1.5rem;">Get access to our high-confidence premium picks with an 85%+ success rate!</p>
                <button class="subscribe-btn" onclick="showNotification('Premium feature coming soon!')">UNLOCK VIP ACCESS</button>
            </div>
            
            <div class="ad-container">
                <!-- Ad placeholder -->
                <div style="background-color: #334155; color: #94a3b8; padding: 20px; border-radius: 4px;">
                    Advertisement Space
                </div>
            </div>
        </div>
        
        <div class="subscription-box">
            <h3>Never Miss a Winning Pick!</h3>
            <div class="email-input">
                <input type="email" placeholder="Your Email Address" id="email">
                <button class="subscribe-btn" onclick="subscribe()">
                    <span id="subscribe-text">SUBSCRIBE</span>
                    <span id="loading-spinner" style="display: none;">
                        <span class="loading"></span>Subscribing...
                    </span>
                </button>
            </div>
        </div>
        
        <footer>
            <p>© 2025 Seventios Sports Picks. All rights reserved.</p>
            <p>Follow us on <a href="https://instagram.com/Seventios" class="social-link">Instagram</a> for updates.</p>
        </footer>
    </div>
    
    <div class="notification" id="notification"></div>
    
    <script>
        // Tab functionality
        function openTab(tabName) {
            const contents = document.getElementsByClassName('content');
            for (let i = 0; i < contents.length; i++) {
                contents[i].classList.remove('active');
            }
            
            const tabs = document.getElementsByClassName('tab');
            for (let i = 0; i < tabs.length; i++) {
                tabs[i].classList.remove('active');
            }
            
            document.getElementById(tabName).classList.add('active');
            event.currentTarget.classList.add('active');
        }
        
        // Notification functionality
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.classList.add('show');
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, 3000);
        }
        
        // Subscribe functionality
        function subscribe() {
            const email = document.getElementById('email').value;
            const subscribeText = document.getElementById('subscribe-text');
            const loadingSpinner = document.getElementById('loading-spinner');
            
            if (!email || !validateEmail(email)) {
                showNotification('Please enter a valid email address.');
                return;
            }
            
            // Show loading state
            subscribeText.style.display = 'none';
            loadingSpinner.style.display = 'inline-block';
            
            // Simulate subscription (would connect to your email service)
            setTimeout(() => {
                // Hide loading state
                subscribeText.style.display = 'inline-block';
                loadingSpinner.style.display = 'none';
                
                // Clear input and show success
                document.getElementById('email').value = '';
                showNotification('Subscribed successfully! Thank you.');
                
                // Save to localStorage for demonstration
                localStorage.setItem('subscribed', email);
            }, 1500);
        }
        
        // Validate email format
        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(String(email).toLowerCase());
        }
        
        // Push notification permission (will work on HTTPS)
        function requestNotificationPermission() {
            if ('Notification' in window) {
                Notification.requestPermission().then(permission => {
                    if (permission === 'granted') {
                        showNotification('Notifications enabled!');
                    }
                });
            }
        }
        
        // Check if user is already subscribed (demo)
        window.onload = function() {
            const subscribed = localStorage.getItem('subscribed');
            if (subscribed) {
                document.getElementById('email').value = subscribed;
            }
            
            // Request notification permission after a delay
            setTimeout(() => {
                requestNotificationPermission();
            }, 5000);
        };
    </script>
</body>
</html>
