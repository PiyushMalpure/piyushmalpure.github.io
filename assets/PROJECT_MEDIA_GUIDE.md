# Project Media Setup Guide

## Overview
Your portfolio now supports automatic loading of project preview media (images, GIFs, or videos). Media will only display if present, with graceful fallback if missing.

## How to Add Media to Projects

### Folder Structure
Create the following structure in your `assets/projects/` directory:

```
assets/
└── projects/
    ├── bimodal-quadruped/
    │   └── preview.gif  (or .jpg, .png, .mp4, etc.)
    ├── multi-robot-task/
    │   └── preview.gif
    ├── motion-planner/
    │   └── preview.gif
    └── patent-movement/
        └── preview.gif
```

### Project IDs
Each project has a unique `data-project-id` attribute:
- `bimodal-quadruped` - Bimodal Quadruped Control
- `multi-robot-task` - Multi-Robot Task Allocation
- `motion-planner` - Centralized Motion Planner
- `patent-movement` - Patent: Multi-Dimensional Movement

### Adding New Projects
When you add new projects to the HTML, include a `data-project-id` attribute:

```html
<div class="project-card" 
     data-tags="python,ai" 
     data-project-id="your-project-id">
  <div class="project-media loading"></div>
  <!-- Rest of card content -->
</div>
```

Then create the corresponding media folder:
```
assets/projects/your-project-id/preview.{jpg|png|gif|webp|mp4|webm}
```

### Supported Media Formats

#### Images
- **JPG/JPEG**: `.jpg`, `.jpeg`
- **PNG**: `.png`
- **WebP**: `.webp` (modern format, smallest size)
- **GIF**: `.gif` (animations)

#### Videos
- **MP4**: `.mp4` (best browser support)
- **WebM**: `.webm` (modern format)

### Media Guidelines

1. **File Naming**: Always name the preview file exactly as `preview.{extension}` (lowercase)

2. **File Size**: Keep files reasonably small for web delivery
   - Images: 100-300 KB recommended
   - GIFs: 200-500 KB recommended
   - Videos: 1-3 MB recommended

3. **Dimensions**: 
   - Images/GIFs: 600x360px or similar 16:9 aspect ratio works best
   - Videos: Any size (will be fitted to 180px height container)

4. **Content**: 
   - Showcase project visuals, demos, or key features
   - Can be screenshots, animations, demos, or demo videos
   - Should be professional and representative of the project

### Production Behavior

- **With media present**: Project card displays with preview at the top
- **No media folder/file**: Media container silently hides, showing only text content
- **Missing file**: No console errors or broken images appear
- **Network issues**: Gracefully falls back to text-only display

### Testing

To test locally:
1. Create folder: `assets/projects/bimodal-quadruped/`
2. Add an image file named `preview.jpg` or `preview.gif`
3. Reload the page - it should appear in the first project card
4. The loading pulse animation will show briefly while fetching the media

### Technical Details

The media loader:
- Uses `fetch()` with HEAD requests to check file existence
- Tries media formats in this order: jpg, jpeg, png, gif, webp, mp4, webm
- Automatically detects video vs image based on file extension
- Videos autoplay, loop, and are muted (safe for auto-play in most browsers)
- Uses IntersectionObserver for scroll-based animation support
