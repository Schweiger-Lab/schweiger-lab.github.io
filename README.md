# Schweiger Lab Website

This is the official website for the Schweiger Lab at Montana State University.

## File Structure

```
├── _config.yml              # Site configuration
├── index.md                 # Home page
├── pages/                   # All website pages
│   ├── people.md           # Team members
│   ├── publications.md     # Lab publications
│   ├── research.md         # Research areas and projects
│   ├── positions.md        # Available positions
│   ├── news.md            # News and blog posts
│   └── contact.md         # Contact information
├── _posts/                 # Blog posts/news articles
├── _data/                  # Data files
│   ├── people.yml         # Team member information
│   ├── publications.yml   # Publication data
│   └── positions.yml      # Position information
├── _layouts/               # Page templates
│   ├── default.html       # Main layout
│   └── post.html          # Blog post layout
├── assets/                 # Static assets
│   ├── css/style.css      # Main stylesheet
│   └── img/               # Images
└── _research/             # Research project pages
```

## Editing Content

- **Home page**: Edit `index.md`
- **Other pages**: Edit files in `pages/` folder
- **Team members**: Edit `_data/people.yml`
- **Publications**: Edit `_data/publications.yml`
- **News posts**: Add new files to `_posts/`
- **Styling**: Edit `assets/css/style.css`

## Local Development

```bash
jekyll serve --port 4000
```

Then visit `http://localhost:4000`

## Live Site

https://schweiger-lab.github.io