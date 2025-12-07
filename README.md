# Piyush Malpure - Personal Portfolio

A modern, responsive personal portfolio website showcasing projects, experience, publications, and technical skills in Robotics and AI Engineering.

## Features

- **Dark/Light Mode Toggle** - Seamless theme switching with persistence
- **Project Showcase** - Beautiful project grid with filtering capabilities
- **Media Support** - Automatic loading of project images, GIFs, and videos
- **Smooth Animations** - Elegant fade-in and scroll reveal effects
- **Responsive Design** - Mobile-optimized for all screen sizes
- **Professional Layout** - Clean, modern design with smooth interactions

## Quick Start

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/PiyushMalpure/piyushmalpure.github.io.git
cd piyushmalpure.github.io
```

2. Open the portfolio locally:
   - Simply open `index.html` in your browser
   - Or use a local server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```

3. Visit `http://localhost:8000` in your browser

### File Structure

```
piyushmalpure.github.io/
├── index.html              # Main portfolio page (all styles & scripts embedded)
├── README.md              # This file
├── LICENSE                # MIT License
└── assets/
    └── projects/          # Project media files (add your media here)
        ├── bimodal-quadruped/
        │   └── preview.{jpg|png|gif|mp4}
        ├── multi-robot-task/
        │   └── preview.{jpg|png|gif|mp4}
        └── [other-project-ids]/
            └── preview.{jpg|png|gif|mp4}
```

**Note**: Legacy folders (`css/`, `js/`, `images/`) have been removed to keep the project clean. All styles and scripts are now embedded in `index.html` for optimal performance.

## Customization

### Adding Projects

1. Add a new project card in `index.html` in the projects section:

```html
<div class="project-card" 
     data-tags="python,ai" 
     data-project-id="my-new-project">
  <div class="project-media loading"></div>
  <div class="project-top">
    <i class="far fa-folder folder-icon"></i>
    <a href="https://github.com/PiyushMalpure/repo-name" 
       class="github-link" target="_blank">
      <i class="fab fa-github"></i>
    </a>
  </div>
  <h3>Project Title</h3>
  <p>Project description goes here...</p>
  <div class="tech-stack">
    <span>Python</span>
    <span>ROS</span>
  </div>
</div>
```

2. Add project media (optional):
   - Create folder: `assets/projects/my-new-project/`
   - Add preview file: `preview.jpg` (or `.gif`, `.mp4`, etc.)
   - Supported formats: jpg, jpeg, png, gif, webp, mp4, webm

3. Update filter tags if needed (in the filter bar HTML)

### Adding Skills

Update the skills section in `index.html` with your technical skills:

```html
<div class="skill-group">
  <div class="skill-title">New Skill Category</div>
  <div class="skill-list">
    <span class="skill-pill">Skill 1</span>
    <span class="skill-pill">Skill 2</span>
  </div>
</div>
```

### Adding Publications

Add new publications in the publications section:

```html
<div class="pub-item">
  <div class="pub-content">
    <div>Publication Title</div>
    <div class="pub-venue">Venue/Journal (Year)</div>
  </div>
  <a href="publication-link" style="color:var(--text-muted)">
    <i class="fas fa-external-link-alt"></i>
  </a>
</div>
```

## Styling & Themes

### Color Variables

The portfolio uses CSS custom properties for theming. Modify in the `:root` section:

**Light Mode (Default):**
```css
:root {
  --bg-body: #f8fafc;
  --bg-card: #ffffff;
  --text-main: #0f172a;
  --text-muted: #64748b;
  --accent: #2563eb;
  --border: #e2e8f0;
}
```

**Dark Mode:**
```css
[data-theme="dark"] {
  --bg-body: #0f172a;
  --bg-card: #1e293b;
  --text-main: #f1f5f9;
  --text-muted: #94a3b8;
  --accent: #38bdf8;
  --border: #334155;
}
```

### Modifying Styles

All styles are embedded in `index.html` within the `<style>` tag. Key style sections:

- **Navigation**: `.nav-*` classes
- **Hero Section**: `header` styles
- **Project Grid**: `.project-*` classes
- **Skills**: `.skill-*` classes
- **Animations**: `@keyframes` definitions

## Responsive Design

The portfolio is fully responsive with breakpoints at:

- **Desktop**: Full layout with 3-column project grid
- **Tablet**: Adjusted spacing and 2-column grid
- **Mobile**: Single column layout, optimized for touch

Media queries are included for screens under 768px width.

## Links & Social

Update the following in `index.html`:

- **Email**: Change `malpurepiyush07@gmail.com` to your email
- **GitHub**: Update `https://github.com/PiyushMalpure`
- **LinkedIn**: Update `https://linkedin.com/in/piyushmalpure07`
- **Resume**: Add link to your resume PDF

## Deployment

### GitHub Pages

This repository is configured for GitHub Pages deployment:

1. Ensure repository name is `yourusername.github.io`
2. Push to `master` branch
3. Visit `https://yourusername.github.io`

### Custom Domain

To use a custom domain:

1. Create a `CNAME` file in the repository root
2. Add your domain: `yourdomain.com`
3. Configure DNS records to point to GitHub Pages

## Performance

- **Fast Load**: Single HTML file with embedded CSS/JS
- **No Dependencies**: Pure HTML/CSS/JavaScript (no frameworks)
- **Optimized**: Minimal network requests, smooth animations
- **Accessible**: Semantic HTML, ARIA labels

## Privacy

This portfolio contains public professional information only. No personal data is collected or tracked.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Feel free to fork this project and customize it for your own portfolio!

## Tips

- Use WebP images for better compression
- Test on mobile devices before deployment
- Keep media files under 500KB for faster loading
- Update your work and achievements regularly
- Use descriptive project names and IDs (lowercase with hyphens)

## Contact

For questions about this portfolio template or setup, feel free to reach out!

---

**Built by Piyush Malpure**
