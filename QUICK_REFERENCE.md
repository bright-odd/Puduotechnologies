# Modern Neon-Gradient Project Page - Quick Reference

## 🎨 Color Palette

### Primary Neon Colors
```
Neon Pink:     #FF006E  (RGB: 255, 0, 110)
Neon Magenta:  #F72585  (RGB: 247, 37, 133)
Neon Violet:   #B5179E  (RGB: 181, 23, 158)
Purple Accent: #9D4EDD  (RGB: 157, 78, 221)
Cyan Blue:     #00D9FF  (RGB: 0, 217, 255)
Neon Cyan:     #00F5FF  (RGB: 0, 245, 255)
```

### Background Colors
```
Dark Background:        #0E0E16 (Almost black)
Dark Background Alt 1:  #1A1A2E (Very dark blue)
Dark Background Alt 2:  #111118 (Nearly black)
```

### Text Colors
```
Primary Text:   #FFFFFF (White)
Secondary Text: rgba(255, 255, 255, 0.7) (70% opacity white)
Tertiary Text:  rgba(255, 255, 255, 0.5) (50% opacity white)
```

---

## 🌟 Key Components

### Hero Section
```html
<section class="projects-hero">
    <div class="projects-hero-bg"></div>
    <div class="container">
        <h1 class="projects-hero-title">
            Our <span class="gradient-text-neon">Projects</span>
        </h1>
        <p class="projects-hero-sub">Subheading text...</p>
    </div>
</section>
```
**Styles**: 
- Title: 64px bold white
- Gradient span: Animated neon gradient
- Padding: 160px top, 80px bottom
- Background: Radial gradient overlays

### Filter Buttons
```html
<button class="filter-btn active" data-filter="all">View All</button>
<button class="filter-btn" data-filter="web">Web</button>
```
**Styles**:
- Default: Semi-transparent gray button
- Hover: Pink background + glow
- Active: Full gradient + strong glow
- Transition: 300ms ease

### Project Card Structure
```html
<article class="project-card" data-category="web" data-industry="tech">
    <div class="project-image-wrapper">
        <img src="..." alt="..." class="project-image">
        <div class="project-image-overlay"></div>
        <div class="project-category-label">Web App</div>
    </div>
    <div class="project-body">
        <div class="project-tags">
            <span class="project-tag">Category</span>
        </div>
        <h3 class="project-title">Project Name</h3>
        <p class="project-desc">Description...</p>
        <div class="project-stack">
            <span class="stack-badge">Tech Stack</span>
        </div>
    </div>
</article>
```

---

## ✨ Animation Effects

### Gradient Animation (Hero Title)
```css
@keyframes gradientShift {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
}
```
- Duration: 6 seconds
- Timing: ease (smooth)
- Loop: Infinite

### Card Fade-In
```css
@keyframes cardFadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```
- Duration: 400ms
- Staggered: 0ms to 500ms delays
- Easing: ease-out

### Card Fade-Out
```css
@keyframes cardFadeOut {
    from {
        opacity: 1;
        transform: translateY(0);
    }
    to {
        opacity: 0;
        transform: translateY(20px);
    }
}
```
- Duration: 300ms
- Used during filtering
- Smooth exit effect

---

## 🔆 Glow Effects

### Pink Glow
```css
box-shadow: 0 0 20px rgba(255, 0, 110, 0.5);
```

### Blue Glow
```css
box-shadow: 0 0 20px rgba(0, 217, 255, 0.5);
```

### Purple Glow
```css
box-shadow: 0 0 20px rgba(157, 78, 221, 0.5);
```

### Combined Glow (Card Hover)
```css
box-shadow: 
    0 20px 50px rgba(0, 0, 0, 0.4),
    var(--neon-glow-pink),
    inset 0 0 30px rgba(255, 0, 110, 0.1);
```

---

## 📐 Spacing & Sizing

### Typography
```
Hero Title:     64px, weight 800
Project Title:  20px, weight 700
Description:    14px, weight 400
Stack Badge:    11px, weight 600
Tags:           12px, weight 600
```

### Component Sizing
```
Card Height:        Variable (flexible)
Image Height:       240px
Card Padding:       28px
Button Padding:     12px 24px
Border Radius:      12px (buttons), 16px (cards)
Gap (Grid):         32px
```

### Responsive Breakpoints
```
Large Desktop:  1024px+      (3 columns)
Tablet:         768px-1023px (2 columns)
Mobile:         480px-767px  (1 column)
Small Mobile:   <480px       (1 column, optimized)
```

---

## 🎯 Interactive States

### Button States
| State | Background | Border | Text | Shadow |
|-------|-----------|--------|------|--------|
| Default | rgba(255,255,255,0.05) | rgba(255,255,255,0.1) | rgba(255,255,255,0.8) | none |
| Hover | rgba(255,0,110,0.1) | #FF006E | #FFFFFF | Pink glow |
| Active | Linear gradient (pink-magenta) | #FF006E | #FFFFFF | Pink glow |
| Focus | Same as hover | #FF006E | #FFFFFF | Pink glow |

### Card States
| State | Transform | Border | Background | Shadow |
|-------|-----------|--------|-----------|---------|
| Default | none | rgba(255,0,110,0.2) | rgba(255,255,255,0.03) | none |
| Hover | scale(1.02) translateY(-8px) | #FF006E | rgba(255,255,255,0.08) | Pink glow + shadow |

### Tag States
| State | Background | Border | Color | Shadow |
|-------|-----------|--------|--------|---------|
| Default | rgba(255,0,110,0.15) | rgba(255,0,110,0.3) | #FF006E | none |
| Hover | Gradient pink-magenta | transparent | #FFFFFF | Pink glow |

---

## 🔧 CSS Custom Properties

```css
:root {
    --neon-pink: #FF006E;
    --neon-magenta: #F72585;
    --neon-violet: #B5179E;
    --neon-blue: #00D9FF;
    --neon-cyan: #00F5FF;
    --neon-purple: #9D4EDD;
    --dark-bg: #0E0E16;
    --dark-bg-secondary: #1A1A2E;
    --dark-bg-tertiary: #111118;
    --neon-glow-pink: 0 0 20px rgba(255, 0, 110, 0.5);
    --neon-glow-blue: 0 0 20px rgba(0, 217, 255, 0.5);
    --neon-glow-purple: 0 0 20px rgba(157, 78, 221, 0.5);
}
```

---

## 📱 Responsive Adjustments

### Hero Section
```
Desktop:   64px title, 160px padding-top
Tablet:    48px title, 130px padding-top
Mobile:    42px title, 120px padding-top
```

### Grid Layout
```
Desktop:   grid-template-columns: repeat(3, 1fr)
Tablet:    grid-template-columns: repeat(2, 1fr)
Mobile:    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))
```

### Filter Controls
```
Desktop:   flex-direction: row
Tablet:    flex-direction: row
Mobile:    flex-direction: column (full width)
```

---

## 🚀 JavaScript Integration

### Data Attributes for Filtering
```html
<!-- Category filter -->
<article class="project-card" data-category="web">

<!-- Industry filter -->
<article class="project-card" data-industry="finance">

<!-- Both combined -->
<article class="project-card" data-category="web" data-industry="finance">
```

### Filter Button Activation
```javascript
// Add active class
btn.classList.add('active');

// Get filter value
const filter = btn.getAttribute('data-filter');
```

### Dropdown Value
```javascript
// Listen to change
industryFilter.addEventListener('change', (e) => {
    currentIndustry = e.target.value;
});
```

---

## 🎨 Gradients Used

### Hero Title Gradient
```css
background: linear-gradient(135deg, 
    #FF006E 0%, 
    #F72585 25%, 
    #9D4EDD 50%, 
    #00D9FF 100%);
```

### Button Active State
```css
background: linear-gradient(135deg, 
    #FF006E 0%, 
    #F72585 100%);
```

### Tag Hover State
```css
background: linear-gradient(135deg, 
    #FF006E 0%, 
    #F72585 100%);
```

### Hero Background
```css
background: 
    radial-gradient(circle at 20% 50%, rgba(255, 0, 110, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(0, 217, 255, 0.15) 0%, transparent 50%);
```

---

## 📊 Data Structure

### Project Card Data
```
data-category: "web" | "mobile" | "desktop"
data-industry: "finance" | "healthcare" | "legal" | "tech" | "education"
```

### Filter Relationships
```
Category Filters:   all, web, mobile, desktop
Industry Filters:   all, finance, healthcare, legal, tech, education
Logic:             Category AND Industry (both must match)
```

---

## 🔍 Developer Tips

1. **Debugging Filters**: Open console (F12) and check:
   - `currentCategory` variable
   - `currentIndustry` variable
   - `projectCards` querySelectorAll count

2. **Adding Projects**: Just add new `<article class="project-card">` with:
   - Correct `data-category` attribute
   - Correct `data-industry` attribute
   - All required elements inside

3. **Customizing Colors**: All colors defined in `:root` at top of CSS
   - Change one variable to affect all uses
   - Search and replace for specific components

4. **Animation Timing**: All transitions are 300ms by default
   - Change `.filter-btn`, `.project-card`, etc.
   - Adjust `@keyframes` duration for entrance effects

5. **Responsive Testing**: Use Chrome DevTools (F12)
   - Device Toolbar (Ctrl+Shift+M)
   - Test all breakpoints
   - Check touch interactions

---

## ✅ Validation Checklist

- [ ] All CSS color values match specification
- [ ] All animations duration is 300ms or specified time
- [ ] Hover effects visible on all interactive elements
- [ ] Responsive design works at all breakpoints
- [ ] JavaScript filters work correctly
- [ ] No console errors
- [ ] Images load properly
- [ ] Text is readable on dark background
- [ ] Footer displays correctly
- [ ] Navigation links work

---

**Reference Guide Complete! For detailed implementation info, see PROJECT_PAGE_IMPLEMENTATION.md**