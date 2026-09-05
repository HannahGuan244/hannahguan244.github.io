# Personal Academic Website

A clean, minimal Jekyll site for GitHub Pages.

## Quick Start

1. **Create your GitHub repo** named `yourusername.github.io`
2. Copy all these files into the repo
3. Edit `_config.yml` with your name, email, and social links
4. Replace `assets/photo.jpg` with your headshot
5. Edit `index.html` (bio) and `research/index.html` (projects)
6. Push to `main` — your site goes live in ~2 minutes

## Local Development

```bash
gem install bundler jekyll
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## File Structure

```
├── _config.yml          # Site settings & navigation
├── _layouts/
│   └── default.html     # Base HTML template
├── assets/
│   ├── css/style.css    # All styles
│   └── photo.jpg        # Your headshot
├── index.html           # Bio / About page
├── research/
│   └── index.html       # Research & Projects page
└── Gemfile              # Ruby dependencies
```

## Adding a New Project

Open `research/index.html` and duplicate a `<div class="project-card">` block.

## Custom Domain

1. Add a `CNAME` file containing your domain (e.g. `yourname.com`)
2. Configure DNS with your registrar (A records or CNAME to GitHub)
3. Enable HTTPS in repo Settings → Pages
