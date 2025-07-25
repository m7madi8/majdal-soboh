# 🤝 Contributing to Majdal Soboh Portfolio

Thank you for your interest in contributing to the Majdal Soboh Yoga Portfolio project! This document provides guidelines and information for contributors.

## 📋 Table of Contents

- [Types of Contributions](#types-of-contributions)
- [How to Contribute](#how-to-contribute)
- [Local Development Setup](#local-development-setup)
- [Code Standards](#code-standards)
- [Development Workflow](#development-workflow)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [FAQs](#faqs)

## 🎯 Types of Contributions

We welcome various types of contributions:

### 🐛 Bug Reports
- Report bugs and issues
- Provide detailed reproduction steps
- Include browser and device information

### ✨ Feature Requests
- Suggest new features
- Propose improvements
- Share ideas for enhancement

### 📝 Documentation
- Improve README files
- Add code comments
- Update documentation

### 🎨 Design & UI
- Improve visual design
- Enhance user experience
- Optimize responsive design

### 🔧 Code Improvements
- Fix bugs
- Optimize performance
- Add new features
- Improve code quality

## 🚀 How to Contribute

### Step 1: Fork the Repository
1. Go to the project repository
2. Click the "Fork" button
3. Clone your forked repository:
   ```bash
   git clone https://github.com/your-username/majdal-soboh-portfolio.git
   cd majdal-soboh-portfolio
   ```

### Step 2: Create a Branch
Create a new branch for your changes:
```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

### Step 3: Make Changes
- Make your changes
- Follow the code standards
- Test your changes thoroughly

### Step 4: Commit Changes
Commit your changes with clear messages:
```bash
git add .
git commit -m "feat: add new yoga session booking feature"
git commit -m "fix: resolve mobile navigation issue"
git commit -m "docs: update installation instructions"
```

### Step 5: Push and Create Pull Request
```bash
git push origin feature/your-feature-name
```
Then create a Pull Request on GitHub.

## 🛠️ Local Development Setup

### Prerequisites
- Node.js (v14 or higher)
- Git
- Modern web browser

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/majdal-soboh-portfolio.git
   cd majdal-soboh-portfolio
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to `http://localhost:3000`

## 📏 Code Standards

### HTML Standards
- Use semantic HTML5 elements
- Maintain proper indentation (2 spaces)
- Include alt attributes for images
- Use descriptive class names
- Follow accessibility guidelines

```html
<!-- Good -->
<section class="yoga-services">
  <h2 class="services-title">Yoga Services</h2>
  <div class="services-grid">
    <article class="service-card">
      <img src="yoga.jpg" alt="Yoga session" class="service-image">
      <h3 class="service-title">Individual Sessions</h3>
    </article>
  </div>
</section>

<!-- Avoid -->
<div class="div">
  <div class="title">Services</div>
  <div class="box">
    <img src="yoga.jpg">
    <div class="text">Individual Sessions</div>
  </div>
</div>
```

### CSS Standards
- Use CSS variables for colors and spacing
- Follow BEM methodology for class naming
- Maintain consistent indentation
- Group related styles together
- Use meaningful comments

```css
/* Good */
.yoga-services {
  padding: var(--section-padding);
  background-color: var(--secondary-color);
}

.yoga-services__title {
  font-size: var(--h2-font-size);
  color: var(--text-color);
  margin-bottom: 2rem;
}

.yoga-services__grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

/* Avoid */
.services {
  padding: 120px 0;
  background: #f8f9fa;
}

.services .title {
  font-size: 3rem;
  color: #2c3e50;
  margin-bottom: 20px;
}
```

### JavaScript Standards
- Use ES6+ features
- Follow consistent naming conventions
- Add error handling
- Include JSDoc comments for functions
- Use meaningful variable names

```javascript
// Good
/**
 * Initialize the yoga session booking system
 * @param {Object} config - Configuration object
 * @returns {Promise<void>}
 */
async function initializeBookingSystem(config) {
  try {
    const bookingForm = document.getElementById('bookingForm');
    if (!bookingForm) {
      throw new Error('Booking form not found');
    }
    
    await setupFormValidation(bookingForm);
    await setupPaymentIntegration(config.paymentApiKey);
    
    console.log('Booking system initialized successfully');
  } catch (error) {
    console.error('Failed to initialize booking system:', error);
    showNotification('Failed to initialize booking system', 'error');
  }
}

// Avoid
function init() {
  var form = document.getElementById('form');
  if (form) {
    // do something
  }
}
```

## 🔄 Development Workflow

### Git Workflow
1. **Main Branch**: Always keep main branch stable
2. **Feature Branches**: Create branches for new features
3. **Pull Requests**: Review all changes before merging
4. **Squash Commits**: Clean up commit history

### Commit Message Format
Use conventional commit format:
```
type(scope): description

[optional body]

[optional footer]
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

Examples:
```bash
git commit -m "feat(booking): add online session booking system"
git commit -m "fix(navigation): resolve mobile menu toggle issue"
git commit -m "docs(readme): update installation instructions"
git commit -m "style(css): improve responsive design for tablets"
```

### Pull Request Template
When creating a PR, use this template:

```markdown
## Description
Brief description of changes made

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Code refactoring
- [ ] Performance improvement

## Testing
- [ ] Tested on desktop browsers
- [ ] Tested on mobile devices
- [ ] Cross-browser compatibility verified
- [ ] Performance impact assessed

## Screenshots (if applicable)
Add screenshots of UI changes

## Checklist
- [ ] Code follows project standards
- [ ] Self-review completed
- [ ] Documentation updated
- [ ] No console errors
- [ ] Responsive design maintained
```

## 🐛 Reporting Bugs

### Before Reporting
1. Check existing issues
2. Test on different browsers
3. Clear browser cache
4. Check console for errors

### Bug Report Template
```markdown
## Bug Description
Clear description of the bug

## Steps to Reproduce
1. Go to '...'
2. Click on '...'
3. Scroll down to '...'
4. See error

## Expected Behavior
What should happen

## Actual Behavior
What actually happens

## Environment
- Browser: [e.g., Chrome 90]
- OS: [e.g., Windows 10]
- Device: [e.g., Desktop/Mobile]

## Screenshots
Add screenshots if applicable

## Console Errors
Any error messages from browser console
```

## 💡 Suggesting Features

### Feature Request Template
```markdown
## Feature Description
Clear description of the feature

## Problem Statement
What problem does this feature solve?

## Proposed Solution
How should this feature work?

## Alternative Solutions
Other ways to solve the problem

## Additional Context
Any other relevant information
```

## ❓ FAQs

### Q: How do I test my changes?
A: Use the development server (`npm run dev`) and test on multiple browsers and devices.

### Q: What if my PR is not merged?
A: We'll provide feedback on why. Address the feedback and resubmit.

### Q: Can I contribute without coding experience?
A: Yes! Documentation, bug reports, and feature suggestions are valuable contributions.

### Q: How often should I update my fork?
A: Regularly sync with the main repository to avoid conflicts.

### Q: What if I find a security issue?
A: Please report security issues privately to the maintainers.

## 📞 Contact

For questions about contributing:
- Create an issue on GitHub
- Contact the maintainers
- Join our community discussions

## 🙏 Recognition

Contributors will be recognized in:
- Project README
- Release notes
- Contributor hall of fame

Thank you for contributing to making this portfolio better! 🌟 