# Afif Rahman - Personal Website

A professional personal showcase website for Afif Rahman, a Computer Science & Engineering undergraduate at BRAC University. This website showcases projects, research interests, blog posts, and provides contact information.

## 🌐 Live Website

Visit the live website at: [https://afifrahman.github.io](https://afifrahman.github.io)

## ✨ Features

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Modern UI**: Clean, professional design suitable for academic and professional purposes
- **Sections**:
  - Home: Introduction and professional summary
  - About: Academic background and interests
  - Projects: Portfolio showcase with project cards
  - Research: Research interests and areas of focus
  - Blog: Platform for sharing thoughts and insights
  - Contact: Contact form and social links

## 🚀 How to Update Content

### Updating Personal Information

1. Open `index.html`
2. Find the relevant section you want to update
3. Edit the text content directly

#### Update Email and Social Links

Search for these lines in `index.html` and update with your actual links:

```html
<a href="mailto:afif.rahman@g.bracu.ac.bd">
<a href="https://github.com/afifrahman">
<a href="https://linkedin.com/in/afifrahman">
<a href="https://scholar.google.com">
```

### Adding Projects

Find the `<!-- Projects Section -->` and duplicate a project card:

```html
<div class="project-card">
    <div class="project-header">
        <i class="fas fa-laptop-code"></i>
    </div>
    <h3>Your Project Title</h3>
    <p>Your project description here.</p>
    <div class="project-tags">
        <span class="tag">Technology 1</span>
        <span class="tag">Technology 2</span>
    </div>
    <div class="project-links">
        <a href="your-github-link" class="project-link">
            <i class="fab fa-github"></i> Code
        </a>
        <a href="your-demo-link" class="project-link">
            <i class="fas fa-external-link-alt"></i> Demo
        </a>
    </div>
</div>
```

### Adding Blog Posts

Find the `<!-- Blog Section -->` and add a new blog card:

```html
<article class="blog-card">
    <div class="blog-date">
        <span class="date-day">15</span>
        <span class="date-month">Dec</span>
    </div>
    <div class="blog-content">
        <h3>Your Blog Title</h3>
        <p>Your blog post preview text.</p>
        <a href="link-to-full-post" class="read-more">Read More <i class="fas fa-arrow-right"></i></a>
    </div>
</article>
```

### Customizing Colors

To change the color scheme, edit `styles.css` and update the CSS variables at the top:

```css
:root {
    --primary-color: #2563eb;  /* Main brand color */
    --secondary-color: #1e40af; /* Darker shade */
    --accent-color: #3b82f6;   /* Accent color */
    /* ... other colors */
}
```

## 🛠️ Technology Stack

- **HTML5**: Structure and content
- **CSS3**: Styling with modern features (Grid, Flexbox, CSS Variables)
- **JavaScript**: Interactive functionality and animations
- **Font Awesome**: Icons
- **Google Fonts**: Inter font family

## 📝 File Structure

```
afifrahman.github.io/
├── index.html          # Main HTML file
├── styles.css          # All styles and responsive design
├── script.js           # JavaScript for interactivity
└── README.md           # This file
```

## 🎨 Customization Tips

1. **Icons**: Change Font Awesome icons by updating the class names. Find icons at [fontawesome.com](https://fontawesome.com/icons)
2. **About Section**: Update your biography, education, interests, and goals
3. **Research Interests**: Add or modify research areas to match your focus
4. **Contact Form**: The current form shows an alert. For a working form, integrate with a backend service or use services like Formspree, EmailJS, or Netlify Forms

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📄 License

This is a personal website. All content is © 2026 Afif Rahman.

## 🤝 Contributing

This is a personal portfolio website, but suggestions and feedback are welcome!

## 📧 Contact

For any questions or collaborations, feel free to reach out:
- Email: afif.rahman@g.bracu.ac.bd
- GitHub: [@afifrahman](https://github.com/afifrahman)

---

Built with ❤️ by Afif Rahman