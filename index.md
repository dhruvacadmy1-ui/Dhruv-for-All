---
layout: default
title: Missing Tables Game - Home
permalink: /
---

<div class="home-welcome">
    <div class="hero-section">
        <h1>🎮 Dhruv for All</h1>
        <p class="hero-subtitle">Master Multiplication Tables 5-16</p>
        <p class="hero-description">An interactive educational game designed for students</p>
    </div>
    
    <div class="quick-links">
        <a href="{{ '/Dhruv-for-All/intro/' | relative_url }}" class="btn btn-primary btn-large">
            👤 New Player - Start Here
        </a>
        <a href="{{ '/Dhruv-for-All/game/' | relative_url }}" class="btn btn-secondary btn-large">
            🎮 Continue to Game
        </a>
    </div>
    
    <div class="home-info">
        <div class="info-card">
            <h3>🌟 Quick Start</h3>
            <p>Click "New Player" to introduce yourself and learn about the game before diving in!</p>
        </div>
        
        <div class="info-card">
            <h3>🏆 Features</h3>
            <ul>
                <li>✅ 3 Progressive Difficulty Levels</li>
                <li>✅ 15 Questions Total</li>
                <li>✅ Audio Feedback</li>
                <li>✅ Leaderboard System</li>
            </ul>
        </div>
        
        <div class="info-card">
            <h3>📱 Accessibility</h3>
            <p>Works on desktop, tablet, and mobile devices. Perfect for practicing anytime, anywhere!</p>
        </div>
    </div>
    
    <div class="stats-section">
        <h2>📊 Player Statistics</h2>
        <div id="stats-container" class="stats-display">
            <div class="stat-item">
                <span class="stat-label">Total Plays:</span>
                <span class="stat-value" id="totalPlays">0</span>
            </div>
            <div class="stat-item">
                <span class="stat-label">Current Leader:</span>
                <span class="stat-value" id="currentLeader">-</span>
            </div>
            <div class="stat-item">
                <span class="stat-label">Best Score:</span>
                <span class="stat-value" id="bestScore">0/15</span>
            </div>
        </div>
    </div>
</div>

<style>
    .home-welcome {
        animation: slideIn 0.6s ease-out;
    }
    
    @keyframes slideIn {
        from { opacity: 0; transform: translateY(30px); }
        to { opacity: 1; transform: translateY(0); }
    }
    
    .hero-section {
        text-align: center;
        padding: 40px 20px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        border-radius: 15px;
        color: white;
        margin-bottom: 40px;
        box-shadow: 0 8px 25px rgba(102, 126, 234, 0.3);
    }
    
    .hero-section h1 {
        font-size: 56px;
        margin: 0 0 10px 0;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
    }
    
    .hero-subtitle {
        font-size: 28px;
        margin: 10px 0;
        opacity: 0.95;
    }
    
    .hero-description {
        font-size: 18px;
        margin: 10px 0 0 0;
        opacity: 0.9;
    }
    
    .quick-links {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-bottom: 40px;
    }
    
    .btn {
        display: inline-block;
        padding: 15px 30px;
        text-align: center;
        text-decoration: none;
        border-radius: 10px;
        font-weight: bold;
        font-size: 18px;
        transition: all 0.3s ease;
        cursor: pointer;
        border: none;
    }
    
    .btn-primary {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
    }
    
    .btn-primary:hover {
        transform: translateY(-3px);
        box-shadow: 0 6px 20px rgba(102, 126, 234, 0.6);
    }
    
    .btn-secondary {
        background: white;
        color: #667eea;
        border: 2px solid #667eea;
        box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    }
    
    .btn-secondary:hover {
        transform: translateY(-3px);
        background: #f8f9fa;
        box-shadow: 0 6px 20px rgba(0,0,0,0.15);
    }
    
    .btn-large {
        padding: 18px 35px;
        font-size: 20px;
    }
    
    .home-info {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 25px;
        margin-bottom: 40px;
    }
    
    .info-card {
        background: #f8f9fa;
        padding: 30px;
        border-radius: 15px;
        border-left: 5px solid #3498db;
        box-shadow: 0 4px 10px rgba(0,0,0,0.08);
        transition: transform 0.3s ease;
    }
    
    .info-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 15px rgba(0,0,0,0.12);
    }
    
    .info-card h3 {
        color: #2c3e50;
        margin-top: 0;
        margin-bottom: 15px;
        font-size: 22px;
    }
    
    .info-card p {
        color: #555;
        line-height: 1.6;
        margin: 0;
    }
    
    .info-card ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }
    
    .info-card li {
        color: #555;
        padding: 8px 0;
        line-height: 1.6;
    }
    
    .stats-section {
        background: #f8f9fa;
        padding: 30px;
        border-radius: 15px;
        border-top: 5px solid #3498db;
        box-shadow: 0 4px 10px rgba(0,0,0,0.08);
    }
    
    .stats-section h2 {
        color: #2c3e50;
        text-align: center;
        margin-top: 0;
        margin-bottom: 25px;
        font-size: 28px;
    }
    
    .stats-display {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 20px;
    }
    
    .stat-item {
        background: white;
        padding: 20px;
        border-radius: 10px;
        text-align: center;
        box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    }
    
    .stat-label {
        display: block;
        color: #7f8c8d;
        font-size: 14px;
        font-weight: 600;
        margin-bottom: 10px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }
    
    .stat-value {
        display: block;
        color: #3498db;
        font-size: 32px;
        font-weight: bold;
    }
    
    @media (max-width: 768px) {
        .hero-section h1 {
            font-size: 40px;
        }
        
        .hero-subtitle {
            font-size: 22px;
        }
        
        .hero-description {
            font-size: 16px;
        }
        
        .quick-links {
            grid-template-columns: 1fr;
        }
        
        .home-info {
            grid-template-columns: 1fr;
        }
        
        .stats-display {
            grid-template-columns: 1fr;
        }
    }
</style>

<script>
    // Update statistics on page load
    function updateStats() {
        const leaderboard = JSON.parse(localStorage.getItem('tableLeaderboard')) || [];
        
        // Total plays
        document.getElementById('totalPlays').textContent = leaderboard.length;
        
        // Current leader
        if (leaderboard.length > 0) {
            document.getElementById('currentLeader').textContent = leaderboard[0].name;
        } else {
            document.getElementById('currentLeader').textContent = '-';
        }
        
        // Best score
        if (leaderboard.length > 0) {
            document.getElementById('bestScore').textContent = leaderboard[0].score + '/15';
        } else {
            document.getElementById('bestScore').textContent = '0/15';
        }
    }
    
    // Update stats when page loads
    window.addEventListener('DOMContentLoaded', updateStats);
    
    // Update stats every 2 seconds to reflect any changes
    setInterval(updateStats, 2000);
</script>
