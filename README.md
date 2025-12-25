# MONKEY MONK STUDIO - Anamorphic 3D Billboard Website

A premium, professional billboard advertising website featuring Monkey Monk Studio's brand identity, anamorphic 3D showcases, and cinematic VFX portfolio. Built with pure HTML and CSS with full-screen background video and responsive design.

## 🎬 About Monkey Monk Studio

**Monkey Monk Studio** is a creative motion graphics and 3D visualization studio specializing in high-impact anamorphic visuals for brands, retail spaces, and large-format LED displays.

**Tagline:** Next-Generation Advertising Experiences

**Founded by:** R Murali Krishnan (VFX Artist with 8+ years Hollywood experience)

## 🎨 Brand Identity

- **Primary Color:** Copper/Bronze (#C89563) - from logo
- **Secondary Colors:** Charcoal (#1a1a1a), Slate Gray (#2d3748)
- **Typography:**
  - Display: Bebas Neue (bold, impactful)
  - Headings: Rajdhani (modern, technical)
  - Body: Montserrat (clean, professional)
- **Logo:** Geometric low-poly monkey head with copper accent

## ✨ Features

### Hero Section with Auto-Playing Background Video
- Full viewport coverage with responsive video
- Cinematic dark overlay for text readability
- Multiple source formats (1080p, 720p) for optimal performance
- Smooth autoplay across all devices
- Brand-aligned copper accent glow effects

### Professional Navigation
- Fixed navbar with brand logo integration
- Responsive mobile hamburger menu
- Active state tracking on scroll
- Copper accent hover effects matching brand

### Anamorphic 3D Portfolio Gallery
- 6 embedded YouTube videos in cinematic grid
- Responsive 16:9 aspect ratio video containers
- Project titles, descriptions, and VFX type tags
- Smooth hover animations with copper glow

### Services Showcase
- 6 core services with numbered cards
- Anamorphic 3D Billboards
- Motion Graphics & CGI
- LED Display Content
- VFX & Compositing
- Brand Campaigns
- Rendering & Color Grading

### Pricing Packages
- **Basic Package:** ₹4,000/sec
- **Standard Package:** ₹7,500/sec (Featured)
- **Premium Package:** ₹12,500/sec

### Fully Responsive Design
- Optimized for Desktop, Laptop, Tablet, and Mobile
- Breakpoints at 768px (tablet) and 480px (mobile)
- Collapsible mobile navigation with brand colors
- Adaptive typography and spacing

### Cinematic Aesthetics
- Dark theme with copper/bronze accents from brand
- Custom font pairing for professional feel
- Smooth CSS transitions and micro-interactions
- Staggered animations for visual impact

## 📁 File Structure

```
monkey-monk-studio/
├── index.html          # Main HTML file
├── styles.css          # Complete CSS stylesheet
├── logo.png           # Monkey Monk Studio logo
└── README.md          # This file
```

## 🎥 Background Video Setup

### Current Implementation
The website uses a free stock video from Coverr.co for demonstration:
```html
<source src="https://cdn.coverr.co/videos/coverr-aerial-view-of-a-city-at-night-9591/1080p.mp4" type="video/mp4">
<source src="https://cdn.coverr.co/videos/coverr-aerial-view-of-a-city-at-night-9591/720p.mp4" type="video/mp4">
```

### Using Your Own Videos

#### Option 1: Host Locally
1. Create a `videos` folder in your project root
2. Add your video files (recommended: MP4 H.264 codec)
3. Update the HTML video sources:

```html
<video autoplay muted loop playsinline preload="auto" id="hero-video">
    <source src="videos/hero-1080p.mp4" type="video/mp4">
    <source src="videos/hero-720p.mp4" type="video/mp4">
    <source src="videos/hero-mobile.mp4" type="video/mp4">
</video>
```

#### Option 2: Use CDN (Recommended)
Host your videos on:
- Cloudflare
- AWS S3 + CloudFront
- Vimeo Pro (with direct file access)

### Video Specifications
- **Format:** MP4 (H.264 codec)
- **Resolutions:**
  - Desktop: 1920x1080 (1080p)
  - Tablet: 1280x720 (720p)
  - Mobile: 854x480 (480p)
- **Duration:** 10-30 seconds for optimal file size
- **File Size:** Keep under 5MB for fast loading
- **Content:** LED billboard displays, cityscapes, or anamorphic 3D examples

### Compression Example (FFmpeg)
```bash
# 1080p version
ffmpeg -i input.mp4 -vcodec libx264 -crf 28 -preset slow -vf scale=1920:1080 hero-1080p.mp4

# 720p version
ffmpeg -i input.mp4 -vcodec libx264 -crf 28 -preset slow -vf scale=1280:720 hero-720p.mp4

# Mobile version
ffmpeg -i input.mp4 -vcodec libx264 -crf 30 -preset slow -vf scale=854:480 hero-mobile.mp4
```

## 📺 YouTube Embed Customization

Replace the placeholder YouTube video IDs with your own anamorphic 3D billboard work:

```html
<iframe 
    src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
    title="Your Project Title"
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>
```

Update project information:
- **work-title:** Your billboard project name
- **work-description:** Brief description of the anamorphic 3D work
- **tags:** VFX types (Anamorphic 3D, LED Display, Billboard, etc.)

## 🎨 Customization

### Brand Colors (Already Applied)
Brand colors from Monkey Monk Studio logo are already implemented:
```css
:root {
    --color-copper: #C89563;           /* Primary brand color */
    --color-copper-dark: #A67548;      /* Hover states */
    --color-copper-light: #D4A574;     /* Highlights */
    --color-slate: #2d3748;            /* Backgrounds */
    --color-charcoal: #1a1a1a;         /* Cards */
}
```

### Fonts (Already Applied)
Professional font pairing matching brand identity:
```css
:root {
    --font-display: 'Bebas Neue', sans-serif;    /* Logo & hero titles */
    --font-heading: 'Rajdhani', sans-serif;      /* Section headings */
    --font-body: 'Montserrat', sans-serif;       /* Body text */
}
```

### Content Updates
- **Studio Name:** Already set to "MONKEY MONK STUDIO"
- **Tagline:** "Next-Generation Advertising Experiences"
- **About Text:** Uses content from your proposal document
- **Mission & Vision:** Directly from your company values
- **Stats:** Update in `.stat-card` sections
- **Contact Info:** 
  - Email: monkeymonkstudio@gmail.com
  - Phone: +91 877 899 9674
  - Website: www.monkeymonkstudio.com

### Logo Integration
The logo is integrated in:
- Navigation bar (top left)
- Footer
- Update `logo.png` with your final logo file

## 🚀 Deployment

### Quick Deploy Options

1. **Netlify** (Drag & Drop)
   - Go to https://app.netlify.com/drop
   - Drag the project folder
   - Instant deployment with HTTPS

2. **GitHub Pages**
   - Create a GitHub repository
   - Push code to `main` branch
   - Enable Pages in repository settings
   - Site live at `username.github.io/repo-name`

3. **Vercel**
   - Install Vercel CLI: `npm i -g vercel`
   - Run `vercel` in project directory
   - Follow prompts for instant deployment

## ⚡ Performance Optimization

### Video Loading
- Videos set to `preload="auto"` for instant playback
- Multiple resolutions ensure optimal file size per device
- `playsinline` attribute prevents fullscreen on iOS

### Image Optimization
- Logo is SVG or optimized PNG
- Use WebP format for additional images
- Compress images with TinyPNG or Squoosh
- Keep images under 500KB

### CSS & Fonts
- Selective font weights loaded (400, 600, 700)
- CSS is optimized with no external frameworks
- Preconnect to Google Fonts for faster loading

## 📱 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile Safari (iOS 12+)
- Chrome Mobile (Android 8+)

## 🛠️ Troubleshooting

### Video Not Playing
1. Check video codec (should be H.264)
2. Ensure file paths are correct
3. Verify MIME type on server (video/mp4)
4. Some browsers block autoplay with sound (muted required)

### Logo Not Displaying
1. Verify `logo.png` is in the same directory as `index.html`
2. Check file name capitalization
3. Ensure file format is PNG or JPG

### Mobile Menu Not Working
- JavaScript is required for menu toggle
- Ensure script tag is present at bottom of HTML
- Check browser console for errors

### Slow Loading
- Compress video files (aim for <5MB)
- Optimize logo and images
- Enable GZIP compression on server
- Use CDN for video hosting

## 📞 Support & Contact

**Monkey Monk Studio**
- Email: monkeymonkstudio@gmail.com
- Phone: +91 877 899 9674
- Website: www.monkeymonkstudio.com

## 📄 License

This website template is customized for Monkey Monk Studio. Modify as needed for your business needs.

## 🎯 Credits

- **Design & Development:** Premium Billboard Advertising Website Template
- **Client:** Monkey Monk Studio - R Murali Krishnan
- **Fonts:** Google Fonts (Bebas Neue, Rajdhani, Montserrat)
- **Demo Video:** Coverr.co (free stock footage)
- **YouTube Videos:** Placeholder IDs (replace with your anamorphic 3D work)

---

**Ready to launch?** Update the YouTube video IDs with your portfolio, add your background video, and deploy!
