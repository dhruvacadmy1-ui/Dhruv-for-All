---
layout: default
title: Dhruv for All - Welcome
---

<div class="intro-container">
    <div class="intro-header">
        <h1>🎮 Welcome to Dhruv for All</h1>
        <p class="subtitle">Master Multiplication Tables 5-16</p>
    </div>
    
    <div class="intro-content">
        <div class="intro-info">
            <h2>📚 About This Game</h2>
            <p>An interactive educational game designed to help you master multiplication tables in a fun and engaging way. Progress through three difficulty levels and challenge yourself to get the highest score!</p>
        </div>
        
        <div class="intro-features">
            <h2>✨ Features</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <span class="feature-icon">🌱</span>
                    <h3>Easy Start</h3>
                    <p>Begin with tables 1-4</p>
                </div>
                <div class="feature-card">
                    <span class="feature-icon">🌿</span>
                    <h3>Progressive</h3>
                    <p>Medium level gets tougher</p>
                </div>
                <div class="feature-card">
                    <span class="feature-icon">🔥</span>
                    <h3>Challenge</h3>
                    <p>Super level tests your skills</p>
                </div>
                <div class="feature-card">
                    <span class="feature-icon">🎵</span>
                    <h3>Audio Feedback</h3>
                    <p>Sound effects for answers</p>
                </div>
                <div class="feature-card">
                    <span class="feature-icon">🏆</span>
                    <h3>Leaderboard</h3>
                    <p>Track your top 5 scores</p>
                </div>
                <div class="feature-card">
                    <span class="feature-icon">📱</span>
                    <h3>Mobile Ready</h3>
                    <p>Play on any device</p>
                </div>
            </div>
        </div>
        
        <div class="intro-stats">
            <h2>📊 Game Statistics</h2>
            <div class="stats-grid">
                <div class="stat-box">
                    <div class="stat-number">12</div>
                    <div class="stat-label">Multiplication Tables</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">15</div>
                    <div class="stat-label">Total Questions</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">3</div>
                    <div class="stat-label">Difficulty Levels</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">∞</div>
                    <div class="stat-label">Replay Times</div>
                </div>
            </div>
        </div>
        
        <div class="intro-how-to">
            <h2>🎯 How to Play</h2>
            <ol class="steps-list">
                <li><strong>Enter Your Name</strong> - Click the button below to start</li>
                <li><strong>Choose Your Level</strong> - Game selects your difficulty automatically</li>
                <li><strong>Answer Questions</strong> - Solve multiplication problems quickly</li>
                <li><strong>Get Feedback</strong> - Hear audio cues and see visual feedback</li>
                <li><strong>Complete All Levels</strong> - Finish 15 questions across 3 levels</li>
                <li><strong>View Your Score</strong> - Check the leaderboard and play again!</li>
            </ol>
        </div>
        
        <div class="intro-player-section">
            <h2>👤 Player Information</h2>
            <form id="playerForm" class="player-form">
                <div class="form-group">
                    <label for="playerName">Your Name:</label>
                    <input 
                        type="text" 
                        id="playerName" 
                        placeholder="Enter your name" 
                        required
                        autocomplete="off"
                        maxlength="20"
                    >
                </div>
                
                <div class="form-group">
                    <label for="playerAge">Age (Optional):</label>
                    <input 
                        type="number" 
                        id="playerAge" 
                        placeholder="Enter your age" 
                        min="5"
                        max="100"
                        autocomplete="off"
                    >
                </div>
                
                <div class="form-group">
                    <label for="playerClass">Class/Grade (Optional):</label>
                    <input 
                        type="text" 
                        id="playerClass" 
                        placeholder="e.g., 3rd Grade, Class 5" 
                        autocomplete="off"
                        maxlength="20"
                    >
                </div>
                
                <button type="button" class="start-button" onclick="startGameWithPlayer()">
                    🚀 Start Game Now
                </button>
            </form>
        </div>
        
        <div class="intro-tips">
            <h2>💡 Tips for Success</h2>
            <ul class="tips-list">
                <li>🎧 Use headphones for better audio feedback</li>
                <li>⏱️ Answer quickly - there's no time limit but speed helps!</li>
                <li>📝 Pay attention to each question carefully</li>
                <li>🎯 Try to beat your previous high score</li>
                <li>🔄 Practice makes perfect - play multiple times</li>
            </ul>
        </div>
    </div>
</div>

<style>
    .intro-container {
        animation: fadeIn 0.5s ease-in;
    }
    
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
    
    .intro-header {
        text-align: center;
        margin-bottom: 40px;
    }
    
    .intro-header h1 {
        font-size: 48px;
        color: #2c3e50;
        margin: 20px 0 10px 0;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
    }
    
    .subtitle {
        font-size: 24px;
        color: #7f8c8d;
        margin: 0;
    }
    
    .intro-content > div {
        background: #f8f9fa;
        padding: 25px;
        margin: 20px 0;
        border-radius: 15px;
        border-left: 5px solid #3498db;
    }
    
    .intro-content h2 {
        color: #2c3e50;
        margin-top: 0;
        margin-bottom: 20px;
        font-size: 28px;
    }
    
    .features-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: 20px;
    }
    
    .feature-card {
        background: white;
        padding: 20px;
        border-radius: 10px;
        text-align: center;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        transition: transform 0.3s ease;
    }
    
    .feature-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }
    
    .feature-icon {
        font-size: 32px;
        display: block;
        margin-bottom: 10px;
    }
    
    .feature-card h3 {
        color: #3498db;
        font-size: 18px;
        margin: 10px 0 5px 0;
    }
    
    .feature-card p {
        color: #7f8c8d;
        font-size: 14px;
        margin: 0;
    }
    
    .stats-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
        gap: 20px;
    }
    
    .stat-box {
        background: white;
        padding: 20px;
        border-radius: 10px;
        text-align: center;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    
    .stat-number {
        font-size: 36px;
        font-weight: bold;
        color: #3498db;
        margin-bottom: 10px;
    }
    
    .stat-label {
        color: #7f8c8d;
        font-size: 14px;
    }
    
    .steps-list {
        list-style: none;
        padding: 0;
    }
    
    .steps-list li {
        padding: 15px;
        margin: 10px 0;
        background: white;
        border-radius: 8px;
        border-left: 4px solid #3498db;
        line-height: 1.6;
    }
    
    .steps-list strong {
        color: #2c3e50;
    }
    
    .player-form {
        background: white;
        padding: 25px;
        border-radius: 10px;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    
    .form-group {
        margin-bottom: 20px;
    }
    
    .form-group label {
        display: block;
        margin-bottom: 8px;
        font-weight: bold;
        color: #2c3e50;
    }
    
    .form-group input {
        width: 100%;
        padding: 12px;
        border: 2px solid #ecf0f1;
        border-radius: 8px;
        font-size: 16px;
        transition: 0.3s;
        font-family: inherit;
    }
    
    .form-group input:focus {
        border-color: #3498db;
        box-shadow: 0 0 8px rgba(52, 152, 219, 0.2);
        outline: none;
    }
    
    .start-button {
        width: 100%;
        padding: 18px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        border: none;
        border-radius: 10px;
        font-size: 20px;
        font-weight: bold;
        cursor: pointer;
        transition: all 0.3s ease;
        box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
    }
    
    .start-button:hover {
        transform: scale(1.02);
        box-shadow: 0 6px 20px rgba(102, 126, 234, 0.6);
    }
    
    .start-button:active {
        transform: scale(0.98);
    }
    
    .tips-list {
        list-style: none;
        padding: 0;
    }
    
    .tips-list li {
        padding: 12px 0;
        padding-left: 30px;
        position: relative;
        color: #2c3e50;
        line-height: 1.6;
    }
    
    .tips-list li:before {
        content: "✓";
        position: absolute;
        left: 0;
        color: #27ae60;
        font-weight: bold;
    }
    
    @media (max-width: 768px) {
        .intro-header h1 {
            font-size: 36px;
        }
        
        .subtitle {
            font-size: 18px;
        }
        
        .features-grid {
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
        }
        
        .stats-grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }
</style>

<script>
    // Load saved player info if exists
    window.addEventListener('DOMContentLoaded', function() {
        const savedName = localStorage.getItem('playerName');
        if (savedName) {
            document.getElementById('playerName').value = savedName;
            document.getElementById('playerName').focus();
            document.getElementById('playerName').select();
        } else {
            document.getElementById('playerName').focus();
        }
    });
    
    function startGameWithPlayer() {
        const nameInput = document.getElementById('playerName');
        const playerName = nameInput.value.trim();
        
        if (!playerName) {
            alert('Please enter your name to start!');
            nameInput.focus();
            return;
        }
        
        // Save player info
        localStorage.setItem('playerName', playerName);
        localStorage.setItem('playerAge', document.getElementById('playerAge').value);
        localStorage.setItem('playerClass', document.getElementById('playerClass').value);
        
        // Hide intro and show game
        document.querySelector('.intro-container').style.display = 'none';
        document.getElementById('game-container').style.display = 'block';
        document.getElementById('game-container').innerHTML = `
            <div class="welcome-banner">
                <p>Welcome, <strong>${playerName}</strong>! 🎮</p>
                <p class="game-instruction">Click "Start Game" to begin your multiplication challenge!</p>
            </div>
            <div id="start-screen">
                <p>Master tables 5 to 16!</p>
                <button onclick="startGame()">Start Game</button>
            </div>
            <div id="game-ui" style="display:none;">
                <div id="level" class="level"></div>
                <div id="question"></div>
                <input type="number" id="answer" placeholder="?" onkeydown="if(event.key==='Enter') checkAnswer()">
                <br>
                <button onclick="checkAnswer()">Submit</button>
                <div id="feedback" class="feedback-box"></div>
            </div>
        `;
        
        // Add game script
        addGameScript();
    }
    
    function addGameScript() {
        // Game code will be injected here
        // This is called after intro to initialize game
    }
</script>
