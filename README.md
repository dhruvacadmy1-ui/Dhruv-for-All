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
├── _config.yml           # Jekyll configuration
├── _layouts/
│   └── default.html      # Main layout template
├── index.md              # Home page with embedded game
├── index.html            # Original standalone version
└── README.md             # This file
```

## ⚙️ Jekyll Theme Configuration

The site uses the **jekyll-theme-minimal** with custom styling:

```yaml
theme: jekyll-theme-minimal
plugins:
  - jekyll-seo-tag
  - jekyll-feed
  - jekyll-sitemap
```

## 🎯 How to Play

1. Click **"Start Game"** button
2. Enter your answer for each multiplication problem
3. Press **Enter** or click **"Submit"**
4. Complete all 3 levels (15 questions total)
5. Enter your name on the Score Card
6. View your rank on the leaderboard

## ✅ Verification

The site is properly configured with:
- ✅ `_config.yml` with Jekyll theme settings
- ✅ `_layouts/default.html` for theme integration
- ✅ `index.md` with YAML front matter
- ✅ GitHub Pages enabled
- ✅ SEO plugins active
- ✅ Responsive design
- ✅ Full game functionality preserved

## 📊 Scoring System

- **Total Questions**: 15 (5 per level)
- **Score**: Number of correct answers out of 15
- **Leaderboard**: Tracks top 5 all-time scores

## 🔧 Development

To run locally:

```bash
# Clone the repository
git clone https://github.com/dhruvacadmy1-ui/Dhruv-for-All.git

# Install Jekyll (requires Ruby)
gem install jekyll bundler

# Build and serve locally
jekyll serve
```

Visit `http://localhost:4000/Dhruv-for-All/` in your browser.

## 📝 License

This project is open source and available under the MIT License.

---

**Made with ❤️ by DigiDhruv**
