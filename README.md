# SwarmAITech - Multi-Agent Framework Portal

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-brightgreen)](https://onepersonlab.github.io/SwarmAITech/)
[![Jekyll](https://img.shields.io/badge/Jekyll-4.3-blue)](https://jekyllrb.com/)

A curated portal for exploring multi-agent AI frameworks.

## 🌐 Live Site

**URL**: https://onepersonlab.github.io/SwarmAITech/

## 📁 Project Structure

```
SwarmAITech/
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page templates
│   ├── default.html     # Base layout with header/footer
│   ├── framework.html   # Framework detail page
│   └── page.html        # Generic page layout
├── _data/               # Data files
│   └ frameworks.yml     # Framework catalog
├── assets/              # Static assets
│   ├── css/main.css     # Dark theme styles
│   └── images/          # Icons and images
├── frameworks/          # Framework pages
│   └ index.md           # Frameworks listing
├── index.md             # Homepage
├── comparison.md        # Comparison tables
├── about.md             # About page
├── Gemfile              # Ruby dependencies
└ README.md              # This file
```

## 🚀 Local Development

### Prerequisites

- Ruby 3.0+
- Bundler
- Jekyll 4.3

### Setup

```bash
# Clone the repository
git clone https://github.com/onepersonlab/SwarmAITech.git
cd SwarmAITech

# Install dependencies
bundle install

# Start local server
bundle exec jekyll serve

# Open http://localhost:4000/SwarmAITech/
```

### Build for Production

```bash
bundle exec jekyll build
# Output in _site/ directory
```

## 🎨 Design Features

- **Dark Theme** — Code-friendly, modern aesthetic
- **Responsive** — Mobile-first design
- **Accessible** — WCAG compliant, skip links, proper semantics
- **Animations** — Smooth transitions, staggered reveals
- **Data-Driven** — Framework data loaded from YAML

## 📊 Framework Data

All framework data is sourced from:
- GitHub API (stars, forks, language, license)
- Official documentation (features, use cases)
- Phase 1 data collection task (st-01)

## 🔧 Customization

### Adding New Frameworks

Edit `_data/frameworks.yml`:

```yaml
frameworks:
  - name: NewFramework
    slug: newframework
    github_url: https://github.com/org/repo
    stars: 10000
    forks: 500
    language: Python
    description: "Description here"
    topics: [ai, agents]
    license: MIT
    key_features: [Feature1, Feature2]
```

### Theme Colors

Edit `assets/css/main.css` CSS variables:

```css
:root {
  --color-accent-primary: #00ff88;
  --color-accent-secondary: #00d4ff;
}
```

## 📝 License

MIT License - See [LICENSE](LICENSE) for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

---

Built by SwarmAITech Team with Jekyll and GitHub Pages.