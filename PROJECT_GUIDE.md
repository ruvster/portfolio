# Project Page Update Guide

## Overview
Project detail pages are located in `projects/` folder. The Broker Digital project page is at `projects/broker-digital.html`.

## Structure
Each project page has these main sections:
1. **Hero** - Project title, role, duration, team
2. **Sections** - Content organized with headings, text, images, and quotes

## How to Update Content

### Text Content
Edit any section text directly in the HTML file. Look for:
- `.project-section-title` - Section headings
- `.project-section-text` - Paragraph text
- `.project-quote` - Quoted text

Example:
```html
<div class="project-section-text">
  <p>Your text here</p>
</div>
```

### Adding/Updating Images

#### Image Directory
Place all project images in: `assets/projects/broker-digital/`

#### Single Image
```html
<div class="project-image">
  <img src="../assets/projects/broker-digital/your-image.png" alt="Description">
</div>
```

#### Image with Caption
```html
<div class="project-figure">
  <div class="project-figure-image">
    <img src="../assets/projects/broker-digital/your-image.png" alt="Description">
  </div>
  <div class="project-figure-caption">Your caption here</div>
</div>
```

#### 2-Column Grid
```html
<div class="project-grid-2">
  <div class="project-figure">
    <div class="project-figure-image">
      <img src="../assets/projects/broker-digital/image-1.png" alt="Description 1">
    </div>
    <div class="project-figure-caption">Caption 1</div>
  </div>
  <div class="project-figure">
    <div class="project-figure-image">
      <img src="../assets/projects/broker-digital/image-2.png" alt="Description 2">
    </div>
    <div class="project-figure-caption">Caption 2</div>
  </div>
</div>
```

#### 3-Column Grid (for multiple small images)
```html
<div class="project-grid-3">
  <div class="project-figure">
    <div class="project-figure-image">
      <img src="../assets/projects/broker-digital/image-1.png" alt="Description">
    </div>
  </div>
  <!-- More figures -->
</div>
```

### Quotes/Callouts
```html
<div class="project-quote">
  "Your quoted text here"
</div>
```

### Meta Information (Top of page)
Update the duration, role, and team in the meta section:
```html
<div class="project-meta">
  <div class="meta-item">
    <div class="meta-label">Duration</div>
    <div class="meta-value">Your dates here</div>
  </div>
  <!-- More meta items -->
</div>
```

## Image Naming Convention
Use descriptive names:
- `customer-journey.png` - Full width journey map
- `sketch-1.jpg`, `sketch-2.jpg` - Individual sketches
- `stakeholder-interview-1.jpg` - Photos
- `usability-testing.png` - Testing screenshots
- `prototype-1.png` - Prototype screens

## Required Images for Broker Digital
Current project expects these images (place in `assets/projects/broker-digital/`):
- customer-journey.png
- stakeholder-interview-1.jpg
- stakeholder-interview-2.jpg
- affinity-mapping.jpg
- workshop-wall.jpg
- sketch-1.jpg through sketch-6.jpg
- prototype-1.png
- registration-sketch-1.jpg through registration-sketch-6.jpg
- prototype-2.png
- usability-testing.png
- login-screen.png

## Creating New Project Pages

1. Copy `projects/broker-digital.html` to `projects/your-project.html`
2. Update all `../assets/projects/broker-digital/` to `../assets/projects/your-project/`
3. Create directory: `assets/projects/your-project/`
4. Update project title, meta info, and content
5. Add the project card link to `projects.html`

Example project card:
```html
<a href="projects/your-project.html" class="work-card">
  <div class="card-bg" style="background: linear-gradient(135deg, #color1 0%, #color2 50%, #color3 100%);"></div>
  <div class="card-content">
    <span class="card-tag">Category • Year</span>
    <h3 class="card-title">Project Name</h3>
    <p class="card-brief">Brief description</p>
  </div>
  <div class="card-arrow">→</div>
</a>
```

## Styling Notes

- Max content width for text: 860px (set automatically)
- Responsive images: automatically scale with container
- Grids automatically adjust on mobile (2-col → 1-col, 3-col → 1-col)
- Quotes have subtle background and accent border
- Captions use monospace gray text

## File Structure
```
portfolio/
├── styles.css              (Main stylesheet)
├── projects/
│   ├── broker-digital.html
│   └── [your-projects].html
├── assets/
│   └── projects/
│       ├── broker-digital/
│       │   ├── image-1.png
│       │   ├── image-2.jpg
│       │   └── ...
│       └── [your-projects]/
│           └── ...
├── index.html
├── projects.html           (Edit this to add new project links)
└── about.html
```

## Tips
- Keep image file sizes reasonable (compress images)
- Use PNG for screenshots, JPG for photos
- Provide descriptive alt text for all images
- Test responsive view on mobile
- Keep captions concise
- Use quotes to highlight key feedback/insights
