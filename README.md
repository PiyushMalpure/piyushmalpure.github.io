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

### Adding Custom Sections

The portfolio is flexible and supports custom sections. Follow these steps to add a new section:

#### 1. Add Navigation Link

Update the navigation bar in the `<nav>` section:

```html
<div class="nav-links">
  <a href="#about">About</a>
  <a href="#experience">Experience</a>
  <a href="#projects">Work</a>
  <a href="#patents">Patents</a>
  <a href="#publications">Research</a>
  <a href="#awards">Awards</a>  <!-- New section -->
</div>
```

#### 2. Create Section HTML

Add your section in the `<main>` element with a unique `id` matching your navigation link:

```html
<section id="awards">
  <h2 class="section-title">Awards & Recognition</h2>
  
  <div class="award-item" style="background: var(--bg-card); border: 1px solid var(--border); padding: 1.5rem; border-radius: 8px; margin-bottom: 1rem; box-shadow: var(--shadow);">
    <div style="display: flex; justify-content: space-between; align-items: center;">
      <div>
        <h3 style="margin: 0 0 0.5rem 0; color: var(--text-main);">Award Name</h3>
        <p style="margin: 0; color: var(--text-muted); font-size: 0.9rem;">Organization, Year</p>
      </div>
      <span style="background: rgba(37, 99, 235, 0.1); color: var(--accent); padding: 0.5rem 1rem; border-radius: 20px; font-size: 0.85rem; font-weight: 500;">Category</span>
    </div>
  </div>
  
</section>
```

#### 3. Style Considerations

The portfolio uses CSS custom properties that automatically respond to light/dark mode:

- `--bg-body`: Section background
- `--bg-card`: Card/item background
- `--text-main`: Primary text color
- `--text-muted`: Secondary text color
- `--accent`: Highlight/link color
- `--border`: Border color
- `--shadow`: Box shadow

Use these variables for consistent styling:

```html
<div style="background: var(--bg-card); color: var(--text-main); border: 1px solid var(--border); box-shadow: var(--shadow);">
  Content here
</div>
```

#### 4. Section Title Format

All sections use the same title format for consistency:

```html
<h2 class="section-title">Section Name</h2>
```

This automatically includes:
- Accent bar on the left
- Horizontal line on the right
- Consistent font size and spacing
- Slide-in animation

#### 5. Example: Adding a Testimonials Section

```html
<section id="testimonials">
  <h2 class="section-title">Testimonials</h2>
  
  <div class="pub-item">
    <div class="pub-content">
      <div style="font-style: italic; margin-bottom: 0.5rem;">"Your quote here"</div>
      <div style="font-weight: 600; color: var(--text-main);">Person Name</div>
      <div class="pub-venue">Title/Company</div>
    </div>
  </div>
  
  <div class="pub-item">
    <div class="pub-content">
      <div style="font-style: italic; margin-bottom: 0.5rem;">"Another quote"</div>
      <div style="font-weight: 600; color: var(--text-main);">Another Person</div>
      <div class="pub-venue">Their Title/Company</div>
    </div>
  </div>
  
</section>
```

#### 6. Example: Adding a Timeline Section

```html
<section id="certifications">
  <h2 class="section-title">Certifications</h2>
  
  <div class="timeline">
    <div class="job-item">
      <div class="job-header">
        <span class="job-title">Certification Name</span>
        <span class="job-company">@ Issuing Organization</span>
        <span class="job-date">Month Year</span>
      </div>
      <div class="job-details">
        <p style="margin: 0; color: var(--text-muted);">Brief description of the certification and what you learned.</p>
      </div>
    </div>
  </div>
  
</section>
```

#### 7. Reusing Existing Components

The portfolio provides several reusable component classes:

**Items with Icons (like publications):**
```html
<div class="pub-item">
  <div class="pub-content">
    <div>Main Title</div>
    <div class="pub-venue">Subtitle/Venue</div>
  </div>
  <span class="badge">Label</span>
</div>
```

**Timeline Items (with left border and dot):**
```html
<div class="timeline">
  <div class="job-item">
    <div class="job-header">
      <span class="job-title">Title</span>
      <span class="job-company">@ Organization</span>
      <span class="job-date">Date</span>
    </div>
    <div class="job-details">Content</div>
  </div>
</div>
```

**Skill/Tag Pills:**
```html
<span class="skill-pill">Tag Name</span>
```

#### 8. Adding Section-Specific Styles

If you need custom styling for your new section, add CSS inside the `<style>` tag before the closing `</style>`:

```css
/* Custom section styling */
.custom-item {
  background: var(--bg-card);
  border: 1px solid var(--border);
  padding: 1.5rem;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.custom-item:hover {
  border-color: var(--accent);
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(37, 99, 235, 0.15);
}
```

Then use in HTML:
```html
<div class="custom-item">Your content</div>
```

#### 9. Mobile Responsiveness

The portfolio uses a breakpoint at 768px. Add mobile-specific styles:

```css
@media (max-width: 768px) {
  .custom-section-grid {
    grid-template-columns: 1fr;  /* Single column on mobile */
  }
}
```

#### 10. Common Inline Styles Reference

For quick styling without adding CSS classes:

```html
<!-- Centered badge/tag -->
<span style="background: rgba(37, 99, 235, 0.1); color: var(--accent); padding: 0.5rem 1rem; border-radius: 20px; font-size: 0.9rem; font-weight: 500;">Tag</span>

<!-- Subtle text -->
<p style="color: var(--text-muted); font-size: 0.9rem;">Muted text</p>

<!-- Card container -->
<div style="background: var(--bg-card); border: 1px solid var(--border); padding: 1.5rem; border-radius: 8px; box-shadow: var(--shadow);">
  Card content
</div>

<!-- Flexible header -->
<div style="display: flex; justify-content: space-between; align-items: center;">
  <div>Left content</div>
  <div>Right content</div>
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
