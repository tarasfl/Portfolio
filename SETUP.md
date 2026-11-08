# Portfolio Website Setup Guide

## 📋 Project Structure

Your Astro portfolio is organized as follows:

```
Portfolio/
├── src/
│   ├── components/        # Reusable UI components
│   │   ├── Header.astro          # Sticky navigation with scroll links
│   │   ├── Hero.astro            # Landing section
│   │   ├── About.astro           # About you section
│   │   ├── Research.astro        # Research & Projects section
│   │   ├── ProjectCard.astro     # Individual project card
│   │   ├── TechnicalNotes.astro  # Technical articles section
│   │   ├── Experience.astro      # Timeline of experiences
│   │   ├── CV.astro              # Academic CV section
│   │   └── Footer.astro          # Footer with links
│   ├── layouts/           # Page templates
│   │   └── Layout.astro          # Main layout wrapper
│   ├── pages/             # Routes (automatically creates URLs)
│   │   └── index.astro           # Home page
│   └── styles/            # Global stylesheets (optional)
├── astro.config.mjs       # Astro configuration
├── package.json           # Project dependencies
└── README.md              # Project documentation
```

## 🎯 Sections Overview

### 1. **Header with Navigation**
- Sticky header that stays visible while scrolling
- Smooth scroll navigation to each section
- Hover effects on links
- Responsive mobile menu

### 2. **Landing Page (Hero)**
- Large introductory section with your name and title
- Call-to-action buttons (GitHub, LinkedIn, CV)
- Professional gradient background

### 3. **About Section**
- Personal introduction
- University and academic focus
- Research statement
- Quick links to CV, GitHub, and LinkedIn

### 4. **Research & Projects**
- Grid layout for project cards
- Each project shows:
  - Title and description
  - Technology tags
  - Links to project and GitHub repo
  - Hover effects

### 5. **Technical Notes**
- Article list with titles and excerpts
- Metadata (date, read time)
- "Read More" links
- Timeline-style layout

### 6. **Experience & Activities**
- Interactive timeline of your experiences
- Each item includes:
  - Position title and organization
  - Duration
  - Description
  - Key highlights
- Animated timeline markers

### 7. **Academic CV**
- Education history
- Skills by category
- Publications
- Contact information

## 🚀 Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Customize Content
Edit `src/pages/index.astro` and update the data objects:

```javascript
const portfolioData = {
  name: 'Your Name',
  title: 'Your Title',
  subtitle: 'Your Subtitle',
  university: 'Your University',
  academicFocus: 'Your Focus Area',
  researchStatement: 'Your research statement...',
  cvLink: 'link-to-your-cv',
  githubLink: 'https://github.com/yourusername',
  linkedinLink: 'https://linkedin.com/in/yourusername',
};
```

### 3. Add Your Projects
Update the `projects` array with your projects:

```javascript
const projects = [
  {
    title: 'Project Name',
    description: 'What you built and why',
    tags: ['Technology1', 'Technology2'],
    link: 'https://project-link.com',
    github: 'https://github.com/yourprojects',
  },
];
```

### 4. Add Experiences
Update the `experiences` array:

```javascript
const experiences = [
  {
    title: 'Software Engineer',
    organization: 'Company Name',
    period: 'Jan 2023 - Dec 2023',
    description: 'What you did...',
    highlights: ['Achievement 1', 'Achievement 2'],
  },
];
```

### 5. Add Education & Skills
Update `education` and `skills` arrays with your background.

### 6. Run Development Server
```bash
npm run dev
```

Open `http://localhost:3000` in your browser.

## 🎨 Customization

### Colors
Global colors are defined in `src/layouts/Layout.astro`:

```css
:root {
  --color-bg: #ffffff;
  --color-text: #1a1a1a;
  --color-accent: #0066cc;
  --color-secondary: #666666;
  --color-border: #e0e0e0;
  --spacing-unit: 1rem;
}
```

### Fonts
The default uses system fonts for performance. Change in `Layout.astro`:

```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, ...;
```

### Spacing & Typography
Modify spacing and text sizes in component styles to match your preferences.

## 🔗 Navigation

The header provides smooth scroll navigation to all sections:
- **Home** → `#home` (Hero section)
- **About** → `#about`
- **Research & Projects** → `#research`
- **Technical Notes** → `#notes`
- **Experience** → `#experience`
- **CV** → `#cv`

## 📱 Responsive Design

All components are fully responsive:
- Desktop: Full layout with multiple columns
- Tablet: Adjusted spacing and font sizes
- Mobile: Single column, optimized touch targets

## 🏗️ Building for Production

```bash
npm run build
```

This creates an optimized `dist/` folder ready for deployment.

## 🚀 Deployment

### Netlify
```bash
npm run build
# Deploy dist/ folder
```

### Vercel
```bash
npm run build
# Connect repository and Vercel will auto-deploy
```

### GitHub Pages
1. Update `astro.config.mjs` with your repo name
2. Add GitHub Pages deployment workflow
3. Push to main branch

## 📝 Adding New Pages

Create new files in `src/pages/`:
```bash
src/pages/blog.astro      # Creates /blog route
src/pages/projects.astro  # Creates /projects route
```

## 🔍 SEO Best Practices

- Update meta descriptions in the Layout component
- Use semantic HTML headings (h1, h2, h3, etc.)
- Add alt text to images
- Structure content with proper heading hierarchy

## 🛠️ Common Customizations

### Add Social Links
Update the Hero section's button links or add more in the footer.

### Add Blog Posts
Create a blog section using Markdown files in `src/content/`.

### Change Theme
Modify CSS variables in `Layout.astro` for dark mode or custom colors.

### Add Analytics
Add Google Analytics or Plausible tracking to `Layout.astro` head.

## 📚 Astro Resources

- [Astro Documentation](https://docs.astro.build)
- [Astro Components](https://docs.astro.build/en/basics/astro-components/)
- [Astro Deployment](https://docs.astro.build/en/guides/deploy/)

## ✨ Tips

1. **Keep content organized** - Edit data in index.astro, not component files
2. **Use consistent styling** - Follow the existing component styles
3. **Test responsiveness** - Check on mobile, tablet, and desktop
4. **Optimize images** - Use WebP format for faster loading
5. **Monitor performance** - Use Lighthouse to check PageSpeed

---

Happy building! 🚀
