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

- **Round 2 Performance & Animation Overhaul (June 2026)**
  - **Linear Onboarding Counter**: Rewrote the progress counter to tick linearly from 1 to 100 over the 2.4s duration, ensuring every percentage point is visible without jumps.
  - **3,900 CSS Animation Elimination**: Replaced individual staggered animations on all week dots with a single, high-performance opacity fade-in on the grid container, reducing concurrent DOM animations from 3,900 to 0.
  - **GPU Spotlight Acceleration**: Replaced layout-triggering `left`/`top` CSS mutations on mouse spotlight with hardware-accelerated `transform` updates, throttled to 60fps using `requestAnimationFrame`.
  - **Static Grain Overlay**: Converted the grain noise animation to a static overlay, avoiding constant full-screen GPU compositing overhead.
  - **Font Preloading**: Preloaded the Google Fonts stylesheet to accelerate font rendering and reduce initial text flash (FOUT).
- **Final Visual Polish (June 2026)**
  - **Loader Formatting**: Restructured the loader HTML to absolute position the `%` symbol outside of the flex container, perfectly centering the "100" counter without horizontal layout shifting.
  - **Loader Duration & Completion**: Lengthened the fake loading duration to 3.6s and added a subtle, satisfying cubic-bezier scale/color pulse when reaching 100%, holding for 1s before dismissing.
  - **Dynamic Grid Stats**: Fixed a bug where LIVED, LEFT, and SPENT % text was hardcoded to weeks. The stats now instantly update and recalculate dynamically when the user toggles between Weeks, Months, and Years.
