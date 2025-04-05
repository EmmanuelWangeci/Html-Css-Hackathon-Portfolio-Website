# My PLP Hackathon Project

## Overview

Welcome to my Power Learn Project hackathon submission! This project showcases my skills in building a responsive, modern website using only HTML and CSS (no JavaScript frameworks). I challenged myself to create an interactive and engaging user experience while maintaining clean, semantic code.

## Project Description

This website is a portfolio/showcase platform that I created during the 48-hour Power Learn Project hackathon. I wanted to demonstrate that impressive web experiences can be created with just the core technologies of the web - HTML and CSS.

### Features

- Fully responsive design that works smoothly on mobile, tablet, and desktop
- Custom CSS animations and transitions for an interactive feel
- CSS Grid and Flexbox for modern layouts
- Semantic HTML5 structure for accessibility
- Pure CSS dropdown menus and interactive components
- Custom form styling with validation indicators
- Dark/light mode toggle using CSS variables

## Technical Implementation

### HTML Structure

I used semantic HTML5 elements throughout the site:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My PLP Hackathon Project</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">
            <h1>DevPortfolio</h1>
        </div>
        <nav>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="theme-toggle">
                <label for="theme-switch" class="switch">
                    <input type="checkbox" id="theme-switch">
                    <span class="slider round"></span>
                </label>
            </div>
        </nav>
    </header>

    <main>
        <section id="hero">
            <div class="hero-content">
                <h2>Hello, I'm <span class="highlight">Your Name</span></h2>
                <p>A passionate web developer creating modern experiences with clean code</p>
                <a href="#contact" class="cta-button">Get In Touch</a>
            </div>
        </section>

        <section id="about">
            <!-- About section content -->
        </section>

        <section id="projects">
            <!-- Projects grid with hover effects -->
        </section>

        <section id="skills">
            <!-- Skills with CSS-only progress bars -->
        </section>

        <section id="contact">
            <!-- Contact form with CSS validation -->
        </section>
    </main>

    <footer>
        <p>Created for Power Learn Project Hackathon 2025</p>
    </footer>
</body>
</html>
```

### CSS Techniques

I relied heavily on modern CSS techniques to create interactive elements without JavaScript:

```css
:root {
    /* Color variables for theming */
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --dark-bg: #2c3e50;
    --light-bg: #ecf0f1;
    --text-dark: #2c3e50;
    --text-light: #ecf0f1;
}

/* Dark theme settings */
body.dark-theme {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --bg-color: var(--dark-bg);
    --text-color: var(--text-light);
}

/* Light theme settings (default) */
body {
    --bg-color: var(--light-bg);
    --text-color: var(--text-dark);
    
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    transition: background-color 0.3s ease;
}

/* Responsive navigation with CSS only dropdown */
.nav-links {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
}

@media (max-width: 768px) {
    .nav-links {
        position: absolute;
        flex-direction: column;
        background-color: var(--bg-color);
        width: 100%;
        top: 60px;
        left: 0;
        padding: 20px 0;
        clip-path: circle(0px at 90% -10%);
        transition: all 0.5s ease-out;
    }
    
    .nav-links.active {
        clip-path: circle(1000px at 90% -10%);
    }
}

/* Project card with hover effects */
.project-card {
    position: relative;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.2);
}

.project-card .overlay {
    position: absolute;
    bottom: -100%;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,0.8));
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 20px;
    transition: bottom 0.3s ease;
}

.project-card:hover .overlay {
    bottom: 0;
}

/* CSS-only form validation indicators */
input:invalid {
    border-color: #e74c3c;
}

input:valid {
    border-color: #2ecc71;
}

/* Pure CSS animation for loading state */
@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

.cta-button:active {
    animation: pulse 0.5s ease infinite;
}
```

## Challenges and Solutions

One of the biggest challenges was creating interactive elements without JavaScript. I implemented:

1. A responsive hamburger menu using the `:checked` pseudo-class and `label` targeting
2. Form validation indicators with CSS `:valid` and `:invalid` pseudo-classes
3. A theme toggle using CSS variables and a checkbox input
4. Animated hover states for project cards using CSS transitions

## Lessons Learned

This hackathon taught me to appreciate the power of pure CSS. I deepened my understanding of:

- CSS animations and transitions
- Custom properties (variables)
- Advanced selectors and pseudo-elements
- Responsive design without media query bloat
- Performance optimization for CSS animations

## Future Improvements

If I had more time, I would add:
- More accessibility features 
- Optimized images with the picture element
- Additional animation sequences
- Print stylesheet optimization

## Conclusion

This hackathon pushed me to explore the limits of what's possible with HTML and CSS alone. I'm proud of creating an interactive experience without relying on JavaScript, which demonstrates that core web technologies are incredibly powerful when used creatively.

---

*Created with ❤️ for the Power Learn Project Hackathon 2025*
