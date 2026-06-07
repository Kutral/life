# Memento Mori — Your Life in Weeks

A highly optimized visual representation of your life in weeks, months, or years, reminding you of the precious nature of time.

## Recent Milestones

- **Git & Deployment Setup (June 2026)**
  - Initialized git repository.
  - Linked to remote repository `https://github.com/Kutral/life`.
  - Pushed to `main` and `gh-pages` branches to enable automatic deployment on GitHub Pages.
  - Added a highly descriptive and beautifully styled `README.md` file.

- **Performance & Transition Optimizations (June 2026)**
  - **Onboarding Background**: Optimized background canvas animation by batch rendering the 2,000+ default dots. This reduced individual drawing/pathing calls from ~3,000 to <150 per frame, enabling 60fps rendering on both desktop and mobile.
  - **Reflow Prevention**: Eliminated layout thrashing during main grid initialization by replacing DOM queries (`offsetTop`/`offsetHeight`) with a mathematical formula.
  - **Tooltip Optimization**: Cached tooltip `offsetWidth` on pointer move, avoiding recalculating layout on every cursor wiggle.
  - **Throttled Scroll Progress**: Added requestAnimationFrame throttling to the window scroll handler to avoid unnecessary layout updates on scroll.
  - **CSS Containment**: Added `contain: layout paint;` to the grid container, isolating style recalculations.
  - **Premium Loading Transition**: Enhanced the fake loader duration from 4.0s to 2.4s, and introduced a cubic ease-out progress percentage counter and SVG transition curve.
