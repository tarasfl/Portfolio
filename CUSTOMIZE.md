# Quick Customization Guide

## 🎯 Customize in 5 Minutes

### Step 1: Edit Your Basic Info
Open `src/pages/index.astro` and find this section:

```javascript
const portfolioData = {
  name: 'Your Name',                    // ← Change this
  title: 'Research & Engineering',      // ← Change this
  subtitle: 'Your subtitle here',       // ← Change this
  university: 'Your University',        // ← Change this
  academicFocus: 'Your focus',          // ← Change this
  researchStatement: 'Your statement',  // ← Change this
  cvLink: '#cv',                        // ← Add CV link
  githubLink: 'https://github.com/yourprofile',    // ← Your GitHub
  linkedinLink: 'https://linkedin.com/in/yourprofile', // ← Your LinkedIn
};
```

### Step 2: Add Your Projects
Replace the projects array:

```javascript
const projects = [
  {
    title: 'My First Project',
    description: 'What you built and key achievements',
    tags: ['Python', 'TensorFlow', 'Deep Learning'],
    link: 'https://project-website.com',
    github: 'https://github.com/you/project',
  },
  {
    title: 'Another Project',
    description: 'Another impressive project description',
    tags: ['React', 'Node.js', 'MongoDB'],
    link: 'https://another-project.com',
    github: 'https://github.com/you/another',
  },
];
```

### Step 3: Add Your Experience
Replace the experiences array:

```javascript
const experiences = [
  {
    title: 'Software Engineer Intern',
    organization: 'Tech Company Inc.',
    period: 'Jun 2023 - Aug 2023',
    description: 'Worked on full-stack development of user dashboard',
    highlights: [
      'Built React components with 95% test coverage',
      'Optimized API endpoints, reducing latency by 40%',
      'Led code review sessions with team of 5 engineers',
    ],
  },
  {
    title: 'Research Assistant',
    organization: 'University Lab',
    period: 'Jan 2023 - May 2023',
    description: 'Conducted research on machine learning models',
    highlights: [
      'Published 2 papers in peer-reviewed conferences',
      'Developed novel algorithm achieving 92% accuracy',
    ],
  },
];
```

### Step 4: Add Technical Notes (Articles)
Replace the technicalNotes array:

```javascript
const technicalNotes = [
  {
    title: 'Understanding Attention Mechanisms in Transformers',
    excerpt: 'A deep dive into how self-attention works in transformer architectures.',
    date: 'Nov 2024',
    readTime: '8 min read',
    link: '/blog/transformers',
  },
  {
    title: 'Optimization Techniques for Deep Learning',
    excerpt: 'Exploring SGD, Adam, and other optimization algorithms.',
    date: 'Oct 2024',
    readTime: '6 min read',
    link: '/blog/optimization',
  },
];
```

### Step 5: Update Education & Skills
Replace education and skills:

```javascript
const education = [
  {
    degree: 'B.S. in Computer Science',
    field: 'Artificial Intelligence & Robotics',
    school: 'Your University',
    year: '2021 - 2025',
  },
];

const skills = [
  {
    category: 'Programming Languages',
    items: ['Python', 'JavaScript', 'C++', 'Java'],
  },
  {
    category: 'ML & Data Science',
    items: ['TensorFlow', 'PyTorch', 'Pandas', 'NumPy'],
  },
  {
    category: 'Web Development',
    items: ['React', 'Astro', 'Node.js', 'PostgreSQL'],
  },
];
```

### Step 6: Update Contact Info
```javascript
const contact = {
  email: 'your.email@example.com',
  phone: '+1 (555) 123-4567',
  location: 'San Francisco, CA',
};
```

## 🎨 Change Colors

Open `src/layouts/Layout.astro` and modify the color variables:

```css
:root {
  --color-bg: #ffffff;           /* Background color */
  --color-text: #1a1a1a;         /* Text color */
  --color-accent: #0066cc;       /* Main accent color (blue) */
  --color-secondary: #666666;    /* Secondary text color */
  --color-border: #e0e0e0;       /* Border color */
  --spacing-unit: 1rem;          /* Base spacing */
}
```

### Popular Color Schemes

**Dark Modern:**
```css
--color-bg: #0a0e27;
--color-text: #ffffff;
--color-accent: #00d9ff;
--color-secondary: #b0b0b0;
--color-border: #2a2a3e;
```

**Minimal Light:**
```css
--color-bg: #fafbfc;
--color-text: #24292e;
--color-accent: #0366d6;
--color-secondary: #586069;
--color-border: #e1e4e8;
```

**Professional Purple:**
```css
--color-bg: #ffffff;
--color-text: #1a1a1a;
--color-accent: #7c3aed;
--color-secondary: #666666;
--color-border: #e0e0e0;
```

## 🔤 Change Fonts

Edit the `font-family` in `src/layouts/Layout.astro`:

### Import from Google Fonts
Add to `<head>` in Layout.astro:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Lato:wght@400;600&display=swap" rel="stylesheet">
```

Then update CSS:
```css
body {
  font-family: 'Lato', sans-serif;
}

h1, h2, h3, h4 {
  font-family: 'Playfair Display', serif;
}
```

## 🖼️ Add a Profile Picture

1. Add image to `src/` folder
2. In About section, add after the heading:

```astro
<img src="/profile-pic.jpg" alt="Your name" class="profile-pic">
```

Add styling in About.astro:
```css
.profile-pic {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 1rem;
}
```

## 🔗 Add More Social Links

Edit the Hero section in index.astro:

```astro
<Hero ...>
  <a href={portfolioData.githubLink} target="_blank" class="cta-button">
    GitHub
  </a>
  <a href={portfolioData.linkedinLink} target="_blank" class="cta-button secondary">
    LinkedIn
  </a>
  <a href="https://twitter.com/yourprofile" target="_blank" class="cta-button">
    Twitter
  </a>
  <a href="https://dribbble.com/yourprofile" target="_blank" class="cta-button secondary">
    Portfolio
  </a>
</Hero>
```

## 📝 Add Contact Form

Install email library:
```bash
npm install nodemailer
```

Create `src/components/ContactForm.astro`:

```astro
---
// Contact form component
---

<form class="contact-form">
  <input type="text" placeholder="Your Name" required />
  <input type="email" placeholder="Your Email" required />
  <textarea placeholder="Message" rows="5" required></textarea>
  <button type="submit">Send Message</button>
</form>

<style>
  .contact-form {
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  input, textarea {
    padding: 0.75rem;
    border: 1px solid var(--color-border);
    border-radius: 6px;
    font-family: inherit;
  }

  button {
    padding: 0.875rem;
    background-color: var(--color-accent);
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    font-weight: 600;
  }

  button:hover {
    opacity: 0.8;
  }
</style>
```

## 📱 Test on Mobile

1. Run dev server: `npm run dev`
2. Open Chrome DevTools (F12)
3. Click Mobile device toggle
4. Test navigation and responsiveness

## 🚀 Deploy After Customization

### Netlify (Easiest)
```bash
npm run build
# Drag & drop dist/ folder to Netlify
```

### GitHub Pages
1. Update `astro.config.mjs`:
```javascript
export default defineConfig({
  site: 'https://yourusername.github.io',
});
```

2. Add workflow file `.github/workflows/deploy.yml`:
```yaml
name: Deploy to GitHub Pages
on:
  push:
    branches: [ main ]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
      - run: npm ci && npm run build
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          build_dir: dist
```

### Vercel
1. Push to GitHub
2. Connect repository to Vercel
3. Vercel auto-deploys on push

## ✨ Pro Tips

- **Keep it simple** - Don't overload with too many projects initially
- **Use clear descriptions** - Explain what you built and why
- **Update regularly** - Add new projects and notes as you complete them
- **Optimize images** - Use WebP format and compress images
- **Use semantic HTML** - Improves SEO and accessibility
- **Test on mobile** - Most visitors use phones
- **Monitor performance** - Use Lighthouse (Chrome DevTools)
- **Add analytics** - Track visitors with Google Analytics or Plausible

## 🆘 Troubleshooting

### Page not updating?
- Clear cache: `Cmd/Ctrl + Shift + R`
- Restart dev server: Stop and run `npm run dev` again

### Styles not applying?
- Check for typos in CSS selectors
- Verify class names match between HTML and CSS
- Restart dev server

### Deployment issues?
- Check `npm run build` locally first
- Verify all links are correct
- Ensure images paths are absolute

---

**Now you're ready!** 🎉 Run `npm run dev` and start exploring your portfolio.
