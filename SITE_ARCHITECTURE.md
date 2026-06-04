# 📄 Multi-Page Integration Architecture

## 🔗 Page Structure & Navigation

Your site now has a complete multi-page architecture with three integrated pages:

### 1. **Home Page** (`index.md`)
- **URL**: `/Dhruv-for-All/` (Root)
- **Permalink**: `/`
- **Purpose**: Landing page with overview and statistics
- **Features**:
  - Hero banner with site title
  - Quick navigation buttons
  - Live statistics (total plays, current leader, best score)
  - Feature highlights
  - Calls-to-action for new and returning players

### 2. **Intro/Tutorial Page** (`intro.md`)
- **URL**: `/Dhruv-for-All/intro/`
- **Permalink**: `/intro/`
- **Purpose**: Player onboarding and information collection
- **Features**:
  - Detailed game explanation
  - Feature showcase with cards
  - Game statistics
  - Step-by-step instructions
  - Player information form (Name, Age, Class)
  - Tips for success
  - Saves player data to localStorage

### 3. **Game Page** (`game.md`)
- **URL**: `/Dhruv-for-All/game/`
- **Permalink**: `/game/`
- **Purpose**: Main interactive game
- **Features**:
  - Full game functionality
  - Player welcome banner
  - 15 questions across 3 levels
  - Audio feedback
  - Score card with leaderboard
  - Medal system (🥇🥈🥉✨)
  - Enhanced player tracking
  - "Go Home" button to return to homepage

---

## 📊 Data Flow Architecture

```
┌─────────────────────────────────────┐
│      index.md (Home Page)           │
│  Display stats from localStorage    │
│  Show navigation to Intro/Game      │
└────────────────┬────────────────────┘
                 │
        ┌────────┴────────┐
        ▼                 ▼
   intro.md           game.md
 (New Players)    (Game Players)
   │                  │
   │ Form Input       │ Game Logic
   │ localStorage     │ localStorage
   │                  │
   └──────────┬───────┘
              ▼
      localStorage
   (Persistent Data)
   ├─ playerName
   ├─ playerAge
   ├─ playerClass
   └─ tableLeaderboard
```

---

## 🔄 Navigation Flow

```
User Visits Site
        ↓
   HOME PAGE (index.md)
   ├─ View Statistics
   ├─ Learn About Game
   │
   ├─→ [New Player Button]
   │       ↓
   │   INTRO PAGE (intro.md)
   │   ├─ Read Instructions
   │   ├─ Enter Player Info
   │   ├─ Save to localStorage
   │   └─ Start Game
   │       ↓
   │   GAME PAGE (game.md)
   │   ├─ Play 15 Questions
   │   ├─ Get Feedback
   │   ├─ View Score Card
   │   └─ Save Score
   │       ↓
   │   [Play Again or Go Home]
   │
   └─→ [Continue to Game Button]
           ↓
       GAME PAGE (game.md)
       └─ Direct Play
```

---

## 🗂️ File Organization

```
Dhruv-for-All/
├── _config.yml                 # Jekyll configuration (global)
├── _layouts/
│   └── default.html           # Master template (all pages)
│
├── index.md                   # Home page (root)
├── intro.md                   # Introduction/onboarding page
├── game.md                    # Game page
│
├── README.md                  # Project documentation
├── VERIFICATION.md            # Verification report
├── SITE_ARCHITECTURE.md       # This file
│
└── Original Files
    └── index.html            # Original standalone version
```

---

## 🎯 Data Persistence

### localStorage Keys Used

| Key | Purpose | Used By | Example |
|-----|---------|---------|---------|
| `playerName` | Player's name | intro.md, game.md | "John" |
| `playerAge` | Player's age | intro.md, game.md | "12" |
| `playerClass` | Grade/Class | intro.md, game.md | "5th Grade" |
| `tableLeaderboard` | Top 5 scores | game.md, index.md | Array of scores |

### Data Flow Example

```
User enters "John" in intro.md form
         ↓
localStorage.setItem('playerName', 'John')
         ↓
User plays game in game.md
         ↓
Retrieves: playerName = 'John'
         ↓
Shows: "Welcome, John! 🎮"
         ↓
After game: Saves score with playerName
         ↓
Home page reads tableLeaderboard
         ↓
Displays: "Current Leader: John"
```

---

## 🔌 Integration Points

### Point 1: Config File (_config.yml)
- Sets theme for all pages
- Configures base URLs
- Defines plugins (SEO, Feed, Sitemap)

### Point 2: Layout Template (_layouts/default.html)
- Wraps all page content
- Applies consistent styling
- Injects page content via `{{ content }}`
- Uses site variables: `{{ site.title }}`, `{{ site.github_url }}`

### Point 3: Home Page (index.md)
- Front matter: `permalink: /` (root path)
- Reads localStorage for statistics
- Provides navigation links to other pages

### Point 4: Intro Page (intro.md)
- Front matter: `permalink: /intro/`
- Form saves player data to localStorage
- JavaScript redirects to game page after form submission

### Point 5: Game Page (game.md)
- Front matter: `permalink: /game/`
- Reads player data from localStorage
- Updates leaderboard and sends data back to localStorage

---

## 📱 Responsive Design

All pages are fully responsive with:
- Mobile-first design
- Breakpoints at 768px
- Flexible grid layouts
- Touch-friendly buttons
- Readable fonts and spacing

### Tested On
- ✅ Desktop (1920px+)
- ✅ Tablet (768-1024px)
- ✅ Mobile (320-767px)

---

## 🧪 Testing the Integration

### Test Flow 1: New Player Journey
1. Visit https://dhruvacadmy1-ui.github.io/Dhruv-for-All/
2. Click "👤 New Player - Start Here"
3. Fill in player form with name (required), age, class
4. Click "🚀 Start Game Now"
5. See welcome message with your name
6. Play the game
7. View leaderboard with your score
8. Click "🏠 Go Home"
9. Home page shows you as "Current Leader"

### Test Flow 2: Returning Player
1. Visit https://dhruvacadmy1-ui.github.io/Dhruv-for-All/
2. Click "🎮 Continue to Game"
3. Game uses saved player name from localStorage
4. Play and submit new score
5. Leaderboard updates

### Test Flow 3: Statistics
1. Play multiple games as different players
2. Home page updates:
   - Total Plays count increases
   - Current Leader updates
   - Best Score updates

---

## 📊 Statistics Auto-Update

The home page statistics update every 2 seconds:

```javascript
setInterval(updateStats, 2000);

function updateStats() {
    const leaderboard = JSON.parse(localStorage.getItem('tableLeaderboard')) || [];
    
    document.getElementById('totalPlays').textContent = leaderboard.length;
    document.getElementById('currentLeader').textContent = leaderboard[0].name;
    document.getElementById('bestScore').textContent = leaderboard[0].score + '/15';
}
```

---

## 🎨 Styling Hierarchy

```
1. Browser Defaults
   ↓
2. Jekyll Theme (jekyll-theme-minimal)
   ↓
3. _layouts/default.html (Global CSS)
   - Colors, fonts, buttons
   - Container styling
   - Footer styling
   ↓
4. Page-Specific Styles (index.md, intro.md, game.md)
   - Hero sections
   - Forms
   - Game UI
```

---

## ✨ Features per Page

### Home (index.md)
- 🎨 Beautiful hero banner
- 📊 Live statistics
- 🔗 Navigation buttons
- ℹ️ Feature highlights
- 📱 Responsive grid

### Intro (intro.md)
- 📚 Feature cards
- 📝 Form with validation
- 💡 Tips section
- 🎯 Step-by-step guide
- 💾 Data persistence

### Game (game.md)
- 🎮 Interactive questions
- 🎵 Audio feedback
- 🏆 Leaderboard
- 🥇 Medal system
- 📊 Score tracking

---

## 🚀 Deployment

### Automatic Deployment
- Push to main branch
- GitHub Pages auto-builds
- Jekyll processes all .md files
- Applies _config.yml and _layouts
- Deploys to https://dhruvacadmy1-ui.github.io/Dhruv-for-All/

### URLs Generated
| Source File | Output URL |
|------------|-----------|
| index.md | / (root) |
| intro.md | /intro/ |
| game.md | /game/ |

---

## 🔐 Browser Storage

- **Type**: localStorage (persists until cleared)
- **Size Limit**: ~5-10MB per domain
- **Data Stored**: Player info & leaderboard
- **Clearing**: User can clear via browser settings

---

## ✅ Verification Checklist

- ✅ All 3 pages accessible
- ✅ Navigation working between pages
- ✅ Form data saving to localStorage
- ✅ Statistics updating correctly
- ✅ Game functionality intact
- ✅ Leaderboard persisting
- ✅ Responsive design working
- ✅ All styles applied correctly
- ✅ Jekyll building successfully
- ✅ GitHub Pages deploying

---

## 📞 Support

For detailed information about:
- Jekyll integration → See VERIFICATION.md
- Game mechanics → See README.md
- Setup instructions → See README.md

---

**Generated**: 2026-06-04
**Status**: ✅ Multi-Page Integration Complete
