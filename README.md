# 🎮 Dhruv for All - Missing Tables Game

An interactive educational game built with **Jekyll** and **HTML5** to help students master multiplication tables 5-16.

## 📚 Features

- ✅ **Three Progressive Difficulty Levels**
  - 🌱 Very Easy Level (Tables × 1-4)
  - 🌿 Medium Level (Tables × 5-8)
  - 🔥 Super Level (Tables × 9-12)

- 🎵 **Audio Feedback** - Sounds for correct/wrong answers
- 🏆 **Leaderboard System** - Top 5 scores stored locally
- 📱 **Responsive Design** - Works on mobile and desktop
- ⚡ **Interactive Animations** - Engaging user experience

## 🚀 Live Demo

Visit: **https://dhruvacadmy1-ui.github.io/Dhruv-for-All/**

## 🛠️ Technology Stack

- **Jekyll** - Static site generator with theme support
- **HTML5** - Semantic markup
- **CSS3** - Responsive styling with animations
- **JavaScript** - Game logic and interactivity
- **GitHub Pages** - Hosting

## 📂 Project Structure

```
Dhruv-for-All/
├── _config.yml              # Jekyll configuration with theme settings
├── _layouts/
│   └── default.html         # Main layout template (interconnects all components)
├── index.md                 # Home page with game content (uses default layout)
├── index.html               # Original standalone version
└── README.md                # This file
```

## ⚙️ File Interconnection

### 1. **_config.yml** (Configuration Hub)
```yaml
theme: jekyll-theme-minimal
plugins:
  - jekyll-seo-tag
  - jekyll-feed
  - jekyll-sitemap
baseurl: /Dhruv-for-All
url: https://dhruvacadmy1-ui.github.io/Dhruv-for-All/
```
- Defines Jekyll theme and plugins
- Sets base URL for GitHub Pages
- Configures markdown processor (kramdown)

### 2. **_layouts/default.html** (Template Layer)
```html
<!DOCTYPE html>
<html>
  <head>
    {{ content from _config.yml }}
  </head>
  <body>
    {{ content from index.md }}
  </body>
</html>
```
- Wraps index.md content with proper HTML structure
- Applies consistent styling to all pages
- Injects SEO metadata from jekyll-seo-tag plugin
- Renders as final HTML served by GitHub Pages

### 3. **index.md** (Content Layer)
```markdown
---
layout: default        # References _layouts/default.html
title: Missing Tables Game
---

<!-- Game HTML and JavaScript -->
```
- YAML front matter specifies layout to use
- Contains game UI and logic
- Gets wrapped by default.html during Jekyll build

## ✅ How It All Works Together

```
index.md (Content)
     ↓
   (references layout: default)
     ↓
_layouts/default.html (Template)
     ↓
   (reads settings from)
     ↓
_config.yml (Configuration)
     ↓
   (builds into)
     ↓
index.html (Served by GitHub Pages)
```

## 🎯 How to Play

1. Visit https://dhruvacadmy1-ui.github.io/Dhruv-for-All/
2. Click **"Start Game"** button
3. Enter your answer for each multiplication problem
4. Press **Enter** or click **"Submit"**
5. Complete all 3 levels (15 questions total)
6. Enter your name on the Score Card
7. View your rank on the leaderboard

## 📊 Scoring System

- **Total Questions**: 15 (5 per level)
- **Score**: Number of correct answers out of 15
- **Leaderboard**: Tracks top 5 all-time scores (localStorage)

## 🔧 Development

To run locally:

```bash
# Clone the repository
git clone https://github.com/dhruvacadmy1-ui/Dhruv-for-All.git
cd Dhruv-for-All

# Install Jekyll (requires Ruby)
gem install jekyll bundler

# Build and serve locally
jekyll serve
```

Visit `http://localhost:4000/Dhruv-for-All/` in your browser.

## 🛠️ Customization

### Change Theme
Edit `_config.yml`:
```yaml
theme: jekyll-theme-cayman  # Or any other theme
```

### Modify Game Settings
Edit `index.md` - JavaScript section:
```javascript
let tables = [5,6,7,8,9,10,11,12,13,14,15,16];  // Change tables
levels[0].questions.slice(0,5)  // Change number of questions
```

### Update Styling
Edit `_layouts/default.html` - `<style>` section

## 🧪 Testing Checklist

- ✅ `_config.yml` validates YAML syntax
- ✅ `_layouts/default.html` uses proper Jekyll template tags
- ✅ `index.md` has valid front matter
- ✅ Game functions work correctly
- ✅ Leaderboard persists data
- ✅ Audio feedback plays
- ✅ Responsive design works
- ✅ GitHub Pages deployment successful

## 📝 License

This project is open source and available under the MIT License.

---

**Made with ❤️ by DigiDhruv**

For more projects, visit: https://github.com/dhruvacadmy1-ui
