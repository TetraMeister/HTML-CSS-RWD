
# Responsive Landing Page - RWD Project

A fully responsive landing page template showcasing mobile-first design principles and modern CSS techniques. Built with semantic HTML5 and CSS3 (SCSS) to demonstrate proficiency in responsive web design.

**Main features**:
- Fully responsive design adapting to mobile, tablet, and desktop screens
- Mobile-first CSS approach with progressive enhancement
- Pure CSS hamburger menu (no JavaScript required)
- Smooth animations and interactive hover effects
- Custom typography with multiple font weights
- Semantic HTML structure for better accessibility


&nbsp;

## 💡 Technologies
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white)


&nbsp;

## 💿 Installation

No installation required. Simply open [index.html](index.html) in your browser to view the project (remember to have "src" directory inside your root folder).

If you want to work with SCSS files, you'll need [node](https://nodejs.org/en/) and [npm](https://www.npmjs.com/). Having them installed, type into the terminal: `npm i`.


&nbsp;

## 🤔 Solutions provided in the project

- **Mobile-first responsive design** - breakpoints implemented progressively from smallest to largest screens:
```css
/* Base mobile styles */
.container {
  padding: 0 1em;
}

/* Tablet */
@media (min-width: 600px) {
  .container {
    padding: 0 3em;
  }
}

/* Desktop */
@media (min-width: 1280px) {
  .container {
    padding: 0 2em;
    max-width: 1600px;
  }
}
```

 &nbsp;

- **Pure CSS hamburger menu** - toggle functionality without JavaScript using CSS checkbox hack:
```css
.heading__burger-checkbox:checked + .heading__menu-list {
  display: block;
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background-color: #2C2C2C;
}
```
 &nbsp;

- **Custom font implementation** using @font-face with multiple weights for professional typography:
```css
@font-face {
  font-family: Poppins;
  src: url('./../fonts/Poppins-Light.ttf');
  font-weight: 300;
  font-display: swap;
}
```

 &nbsp;

- **BEM methodology** - Block Element Modifier naming convention for maintainable and scalable CSS:
```html
<section class="features row">
  <div class="features__container container">
    <div class="features__message cell">
      <!-- Block: features, Element: container, message -->
    </div>
  </div>
</section>
```

 &nbsp;

- **SCSS mixins for theming** - reusable color variations for pricing cards maintaining DRY principles:
```scss
@mixin pricing-card-color($colors) {
  @each $key, $color in $colors {
    &--#{$key} .pricing__price {
      color: $color;
    }
  }
}

.pricing__item {
  @include pricing-card-color($pricing-colors);
}
```

 &nbsp;

- **Smooth transitions and hover effects** enhancing user experience with visual feedback on interactive elements:
```css
.heading__hero-btn {
  transition: scale 250ms ease-in-out;
}

.heading__hero-btn:hover,
.heading__hero-btn:focus-visible {
  scale: 1.1;
}
```

&nbsp;

## 💭 Conclusions for future projects

Areas for improvement and further learning:

#### Font optimization:
```css
/* Consider using variable fonts to reduce file size */
/* and improve loading performance */
@font-face {
  font-family: 'Poppins Variable';
  src: url('Poppins-Variable.woff2');
  font-weight: 100 900;
}
```

#### JavaScript enhancements:
Add intersection observer for scroll animations and lazy loading images to improve performance on slower connections.


&nbsp;

## 👏 Thanks / Special thanks / Credits
Thanks to my [Mentor - devmentor.pl](https://devmentor.pl/) – for providing me with this task and for code review.
