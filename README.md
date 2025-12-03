[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner-direct.svg)](https://savelife.in.ua/en/)


PhotoSwipe v5 — JavaScript image gallery and lightbox

**[Demo](https://photoswipe.com)** | **[Documentation](https://photoswipe.com/getting-started/)**

[![Sponsor via OpenCollective](https://img.shields.io/opencollective/all/photoswipe?label=Sponsor%20via%20OpenCollective)](https://opencollective.com/photoswipe)
[![Follow on Twitter](https://img.shields.io/twitter/follow/photoswipe?style=social)](https://twitter.com/intent/user?screen_name=photoswipe)

## About This Fork

This is a fork of the original [PhotoSwipe](https://github.com/dimsemenov/PhotoSwipe) library. It includes additional enhancements for smoother user interactions:

- **Smooth Transition Animations**: Added animated transitions for slide navigation via arrow buttons and keyboard arrow keys
- **Rapid Input Handling**: Properly manages rapid button/key presses to prevent animation conflicts
- **Accessibility Support**: Respects `prefers-reduced-motion` for users who prefer reduced animations
- **Dynamic Timing**: Uses the CSS custom property `--pswp-transition-duration` for consistent timing
- **Dark Theme Support**: Includes `basic-dark.css` for easy dark theme implementation

These changes maintain full compatibility with the original PhotoSwipe API and behavior.

### About Basic Dark Theme

The `basic-dark.css` file provides a complete dark theme for PhotoSwipe with the following features:

- **CSS Custom Properties**: 
  - `--pswp-theme-background-base`: Controls the base background color (default: black)
  - `--pswp-theme-foreground-base`: Controls text and icon colors (default: white)  
  - `--pswp-theme-radius`: Controls border radius for UI elements (default: 0.3rem)

- **Enhanced UI Elements**: 
  - Semi-transparent backgrounds with backdrop blur effects
  - Improved button styling with hover states
  - Responsive arrow button design
  - Modern glassmorphism aesthetic

- **Animation Support**: Includes blur animations for opening/closing transitions using the `pswp--closing` class

To use the dark theme, simply include `basic-dark.css` after the main PhotoSwipe CSS:

```javascript
import '@juji/photoswipe/basic-dark.css';
```

### Screenshots

**Dark Theme Example:**
![Dark Theme Demo](https://previews.jumpshare.com/gif/815bc01b796dd6f1733c957c5af19493511ccf0584b26ba18adfd0f74cce5ea970b083294177afdc56ab7b86b6e8860a04b3b3467dad2b044333cb443be27b75acb5865d07d9ef1944b1554b5f39b11b)


### Repo structure

- `dist/` - main JS and CSS
- `src/` - source JS and CSS.
  - `src/js/photoswipe.js` - entry for PhotoSwipe Core.
  - `src/js/lightbox/lightbox.js` - entry for PhotoSwipe Lightbox.
- `docs/` - documentation markdown files.
- `demo-docs-website/` - website with documentation, demos and manual tests.
- `build/` - rollup build config.

To build JS and CSS in `dist/` directory, run `npm run build`.

To run the demo website and automatically rebuild files during development, run `npm install` in `demo-docs-website/` and `npm run watch` in the root directory.

### Older versions

Documentation for the old version (v4) can be found [here](https://photoswipe.com/v4-docs/getting-started.html) and [the code for 4.1.3 is here](https://github.com/dimsemenov/PhotoSwipe/tree/v4.1.3).

---

This project is tested with [BrowserStack](https://www.browserstack.com/).
