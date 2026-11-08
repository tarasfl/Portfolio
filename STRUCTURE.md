# Portfolio Structure Overview

## 🎨 Visual Layout

```
┌─────────────────────────────────────────────────────────┐
│                      HEADER / NAV                       │
│  [Logo] [Home] [About] [Research] [Notes] [Exp] [CV]   │
├─────────────────────────────────────────────────────────┤
│                                                          │
│                  🏠 HERO / LANDING                      │
│                      Your Name                          │
│                   Research & Engineering               │
│                                                          │
│            [GitHub Button] [LinkedIn Button]           │
│                                                          │
├─────────────────────────────────────────────────────────┤
│  📋 ABOUT SECTION                                       │
│  ┌──────────────────────┐    ┌──────────────────────┐  │
│  │ Name & University    │    │ Quick Links          │  │
│  │ Focus: Research Area │    │ [CV] [GitHub]        │  │
│  │ Research Statement   │    │ [LinkedIn]           │  │
│  └──────────────────────┘    └──────────────────────┘  │
├─────────────────────────────────────────────────────────┤
│  🔬 RESEARCH & PROJECTS                                 │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐    │
│  │  Project 1  │  │  Project 2  │  │  Project 3  │    │
│  │ Description │  │ Description │  │ Description │    │
│  │ Tags • Tags │  │ Tags • Tags │  │ Tags • Tags │    │
│  └─────────────┘  └─────────────┘  └─────────────┘    │
├─────────────────────────────────────────────────────────┤
│  📝 TECHNICAL NOTES                                     │
│  ┌─────────────────────────────────────────────┐       │
│  │ Note Title 1                        5 min  │       │
│  │ Excerpt of the article...                  │       │
│  │ Read More →                                 │       │
│  └─────────────────────────────────────────────┘       │
│  ┌─────────────────────────────────────────────┐       │
│  │ Note Title 2                        8 min  │       │
│  │ Excerpt of the article...                  │       │
│  │ Read More →                                 │       │
│  └─────────────────────────────────────────────┘       │
├─────────────────────────────────────────────────────────┤
│  💼 EXPERIENCE & ACTIVITIES (TIMELINE)                  │
│  ● Position 1 — Company A (2023)                       │
│    • Achievement 1                                     │
│    • Achievement 2                                     │
│                                                         │
│  ● Position 2 — Company B (2022)                       │
│    • Achievement 1                                     │
│    • Achievement 2                                     │
├─────────────────────────────────────────────────────────┤
│  🎓 ACADEMIC CV                                         │
│  ┌──────────────────────┐    ┌──────────────────────┐  │
│  │ EDUCATION            │    │ SKILLS               │  │
│  │ Degree • University  │    │ Programming: Lang1.. │  │
│  │ Field of Study       │    │ Tools: Frame1...     │  │
│  │                      │    │                      │  │
│  │ CONTACT              │    │ PUBLICATIONS         │  │
│  │ email@example.com    │    │ • Publication 1      │  │
│  │ +1-234-567-8900      │    │ • Publication 2      │  │
│  └──────────────────────┘    └──────────────────────┘  │
├─────────────────────────────────────────────────────────┤
│                      FOOTER                             │
│            © 2024 | [Links] [Links] [Links]            │
└─────────────────────────────────────────────────────────┘
```

## 🔄 Component Hierarchy

```
Layout (Global wrapper)
├── Header
│   └── Navigation Links (smooth scroll)
├── Hero
│   └── CTA Buttons (GitHub, LinkedIn)
├── About
│   └── Social Links
├── Research
│   └── ProjectCard (multiple)
├── TechnicalNotes
│   └── Note Items (multiple)
├── Experience
│   └── Timeline Items (multiple)
├── CV
│   └── Education, Skills, Publications, Contact
└── Footer
    └── Footer Links
```

## 🎯 Data Flow

```
index.astro (Data Source)
├── portfolioData → Hero, About
├── projects → Research (ProjectCard[])
├── technicalNotes → TechnicalNotes
├── experiences → Experience
├── education, skills, contact → CV
└── All → Layout (passes to components)
```

## 🔗 Navigation Flow

```
Header Navigation Anchor Links:
  #home   ──→ Hero Section
  #about  ──→ About Section
  #research ──→ Research & Projects
  #notes  ──→ Technical Notes
  #experience ──→ Experience Timeline
  #cv ──→ CV Section
```

## 📱 Responsive Breakpoints

```
Desktop (> 768px)
├── Multi-column layouts
├── Full spacing and typography
├── Hover effects enabled
└── All sections at full width

Mobile/Tablet (≤ 768px)
├── Single column layouts
├── Optimized spacing
├── Touch-friendly buttons
├── Responsive typography
└── Adjusted navigation
```

## 💾 Data Structure Template

### Portfolio Data
```javascript
{
  name: string
  title: string
  subtitle: string
  university: string
  academicFocus: string
  researchStatement: string
  cvLink: string (URL)
  githubLink: string (URL)
  linkedinLink: string (URL)
}
```

### Projects
```javascript
[
  {
    title: string
    description: string
    tags: string[]
    link: string (URL)
    github: string (URL)
  }
]
```

### Experiences
```javascript
[
  {
    title: string
    organization: string
    period: string
    description: string
    highlights: string[]
  }
]
```

### Technical Notes
```javascript
[
  {
    title: string
    excerpt: string
    date: string
    readTime: string
    link: string (URL)
  }
]
```

### Education
```javascript
[
  {
    degree: string
    field: string
    school: string
    year: string
  }
]
```

### Skills
```javascript
[
  {
    category: string
    items: string[]
  }
]
```

---

**Ready to customize?** Edit `src/pages/index.astro` with your information!
