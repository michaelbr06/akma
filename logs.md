# Change Log

## [2026-09-04] - Made Footer Monogram Responsive and Scaled to Device Dimensions
- Increased the size of the footer monogram (`.footer-monogram`) in `index.html` from a static 100px width to responsive sizing using viewport-relative units (`clamp()` and `vw`).
- Configured mobile sizing to `clamp(150px, 35vw, 220px)` and desktop/tablet sizing (`@media (min-width: 768px)`) to `clamp(220px, 18vw, 280px)` to dynamically scale relative to device screen dimensions while maintaining visual balance.


## [2026-09-04] - Replaced Footer Text with Monogram Logo
- Replaced the footer text (`<p>AK • MA • 2026</p>`) in `index.html` with the monogram SVG logo (`monogram-svg.svg`).
- Applied the `.footer-monogram` class with centered margins (`margin: 0 auto;`) and responsive sizing for clean vertical and horizontal alignment within the footer.


## [2026-09-03] - Added Garden Screenshot Background Across Page Sections
- Applied the garden hero screenshot background (`Screenshot 2026-05-24 at 15.21.13.png`) with warm semi-transparent gradient overlay (`rgba(253, 251, 247, 0.6)`) and subtle bottom border (`1px solid var(--color-accent-light)`) to all page sections (`section.container`).
- Set `width: 100%` on `.container` and `section.container` so the garden background spans edge-to-edge across the viewport like the hero banner.
- Preserved centered, balanced content widths for all section children (`.details-grid` max 1000px, `.timeline-card` max 600px/680px, `.faq-list` max 800px, and `.rsvp-section` max 800px).
- Maintained the HTML format of all sections starting from the Details section (`<section class="container">`) with no build steps or external dependencies.


## [2026-09-03] - Horizontally Aligned When Timeline Time Slot with First Activity
- Aligned the horizontal text of `.timeline-time` with the first line of `.timeline-desc` in the When timeline grid:
  - Added `line-height: 1.5` and increased `padding-top` from `2px` to `6px` on `.timeline-time` for mobile screens, resolving the offset caused by font-size and line-height disparity.
  - Added `padding-top: 7px` to desktop `.timeline-time` (`@media (min-width: 768px)`) to keep optical alignment precise with the `1.2rem` description text.
  - Adjusted `.timeline-dot` `margin-top` from `6px` to `8px` to center the marker with the aligned first line of text while preserving the continuous stem.


## [2026-09-03] - Updated When Section Schedule
- Updated the "When" itinerary timeline in `index.html` to reflect the latest schedule:
  - 12:30 PM: Assembly / Start of Ceremony
  - 02:30 PM: End of Ceremony / Pictorial
  - 03:00 PM: Travel to Reception
  - 03:30 PM: Cocktail Hour / Registration
  - 04:30 PM: Start of Program
  - 05:00 PM: Dinner
  - 06:30 PM: End of Program / Party time
- Split comma-separated activities onto separate lines using `<br />` breaks for clean multi-line presentation.


## [2026-09-03] - Centered When Timeline on Larger Screens
- Updated `.timeline-item` grid template columns on desktop (`min-width: 768px`) to `1fr 24px 1fr`, creating a balanced, centered layout with times right-aligned and descriptions left-aligned relative to the central timeline rail.
- Adjusted desktop `.timeline-card` `max-width` to `600px` for balanced visual proportions.
- Preserved the left-aligned vertical flow (`84px 22px 1fr`) on mobile devices to ensure full responsiveness across smaller screens.


## [2026-09-03] - Formatted 4:00 PM and 6:30 PM Multi-Line Activities
- Applied multi-line formatting with `<br />` breaks to 4:00 PM ("Registration" / "Start of Program") and 6:30 PM ("End of Program" / "After Party").
- Maintained the bold, prominent styling (`.timeline-item.major`) for the 4:00 PM activity and preserved standard weight for 6:30 PM.
- Maintained seamless connection of the timeline stem across all multi-line items.

## [2026-09-03] - Formatted 2:30 PM Multi-Line Schedule Text & Resolved Stem Gap
- Formatted the 2:30 PM schedule description with an inline break (`<br />`) to cleanly separate "End of Ceremony" and "Travel to Reception".
- Replaced multiple adjacent `.timeline-desc` sibling containers with a single description block so CSS Grid keeps all item content within a single row.
- Resolved the timeline stem gap between 2:30 PM and 3:30 PM by allowing the `.timeline-rail` to expand to the full height of the two-line description and seamlessly bridge to the next node.

## [2026-09-03] - Connected Timeline Nodes with Continuous Line
- Updated `.timeline-rail`, `.timeline-dot`, and `.timeline-stem` styling in `index.html` so connecting stems bridge between all timeline nodes.
- Positioned the stem to extend through item padding to meet subsequent nodes, using the wedding accent color (`var(--color-accent)`).
- Layered dots above the connecting stem with `z-index: 1` to create clean intersections for both major and minor event nodes.
- Added responsive stem bottom calculation for desktop viewports (`bottom: calc(-2.1rem - 6px)`).

## [2026-09-03] - Added When Timeline Section to Index Page
- Added a new "When" schedule section to `index.html` featuring a responsive timeline.
- Styled timeline with wedding theme tokens, including custom markers, connecting line, and responsive card container.
- Added responsive layout: desktop displays balanced side-by-side time and event schedule, while mobile provides a clean left-aligned vertical flow.
- Included complete wedding day itinerary: Ceremony (12:30 PM), Reception travel (2:30 PM), Cocktail hour (3:30 PM), Registration/Program (4:00 PM), Dinner (5:00 PM), After party (6:30 PM), and End (8:00 PM).

## [2026-06-05] - Added Bank QR Codes to Registry
- Integrated bank transfer QR codes (`BPI_AKMA.png`, `GT_AKMA.png`, `bdo-qr.jpeg`) into the `registry.html` page.
- Implemented a responsive `.qr-codes` container with flex-wrap and consistent styling.
- Added hover effects and shadows to the QR code images for a polished UI.
- Positioned the QR codes within the "A Note on Gifts" section for better context.

## [2026-06-03] - Fixed iOS Carousel Skipping Issue
- Resolved "image skipping" bug on iOS Safari by removing `scroll-behavior: smooth` from CSS and relying on JavaScript `scrollTo`.
- Updated carousel logic to use discrete target index calculations instead of relative `scrollBy`.
- Changed `scroll-snap-align` to `start` and added `scroll-snap-stop: always` to ensure more stable snapping on mobile browsers.

## [2026-06-03] - Optimized Entourage Dress Code Images
- Implemented `max-height: 75vh` and `width: auto` on dress code carousel images in `entourage.html`.
- This ensures the entire image height is visible within the viewport on all devices, including laptops.
- Maintained responsive scaling and aspect ratio for the portrait-style palette images.

## [2026-06-03] - Updated Entourage Color Palettes
- Updated `entourage.html` with new, high-quality color palette images for the wedding party.
- Replaced `moh-color.jpeg` with `moh-palette.jpeg` (Maids of Honor).
- Replaced `bm-color.jpeg` with `bmaids-color-palette.jpeg` (Bridesmaids).
- Replaced `bestman-grooms-color.jpeg` with `bm-dresscode-new.jpeg` (Bestman & Groomsmen).
- Maintained carousel functionality and responsiveness for the updated images.

## [2026-05-31] - Enhanced Dress Code Gallery in Entourage Page
- Replaced the single Dress Code palette image with a custom carousel in `entourage.html`.
- Implemented single-image display with navigation arrows (previous/next).
- Optimized image responsiveness by capping the carousel width at 500px and centering it.
- Added logic to dynamically show/hide arrows based on the carousel position.
- Integrated new color palette images: `parents-color.jpeg`, `nin-colors.jpeg`, `moh-color.jpeg`, `bm-color.jpeg`, and `bestman-grooms-color.jpeg`.
- Used CSS scroll-snap and smooth scrolling for a native carousel feel.

## [2026-05-30] - Adjusted Entourage Details
- Updated Secondary Sponsors: Changed Candle sponsor from Ms. Daniela Allex Mallon to Ms. Angel Basilio.
- Simplified Bearer labels: Shortened "Ring Bearer", "Coin Bearer", and "Bible Bearer" to "Ring", "Coin", and "Bible".

## [2026-05-30] - Updated Wedding Party Names
- Replaced placeholders in `entourage.html` with the official names of the wedding party.
- Updated "Maid of Honor" to "Maids of Honor" to accommodate two names.
- Verified all names for Parents, Sponsors, Best Man, Maids of Honor, Groomsmen, Bridesmaids, Secondary Sponsors, Bearers, and Flower Girls.

## [2026-05-30] - Added Dress Code to Entourage Page
- Added a "Dress Code" section to `entourage.html` highlighting the reserved color palette.
- Included the palette image `Screenshot 2026-05-25 at 00.42.26.png` for reference.
- Specified attire requirements for gentlemen (Formal Suits / Barong Tagalog) and ladies (Long Gowns / Formal Filipiñana).

## [2026-05-30] - Added Entourage Page
- Created `entourage.html` with a placeholder structure for the wedding party.
- Implemented a design consistent with the project's color palette and typography.
- Used a responsive card-based layout for different entourage groups (Parents, Sponsors, etc.).
- Ensured the navigation bar is present but does not link to the Entourage page itself, as requested.

## [2026-05-27] - Improved Barcode Styling
- Styled the barcode image in `sm-store.html` to better match the registry card container.
- Added a white background, border, and subtle shadow to the barcode container.
- Ensured the barcode is responsive and centered within the instructions.

## [2026-05-27] - Updated SM Store Registry with Barcode
- Added the barcode image (`sm-store-registry-even-tocde.png`) to the in-store gifting instructions in `sm-store.html`.
- Styled the barcode for responsiveness and better layout.

## [2026-05-27] - Finalized SM Store Registry Details
- Updated `sm-store.html` with specific instructions for online and in-store gifting.
- Added a highlighted box for the SM Store Event Code (8245227).
- Styled the instructions for better readability on both mobile and desktop.

## [2026-05-27] - Added SM Store Registry Option
- Created `sm-store.html` page for the SM Store registry details.
- Updated `registry.html` to include the SM Store registry button with `sm-logo.png`.
- Documented registry options for both Rustan's and SM Store.

## [2026-05-27] - Optimized Rustan's Registry Instructions
- Adjusted instruction images in `rustans.html` to match the width of the registry card container.
- Ensured images are fully responsive with `max-width: 100%`.
- Updated `rustans.html` to include instruction screenshots as responsive "pages".
- Added `rustans-log.png` at the top of the page.

## [2026-05-27] - Added Rustan's Registry Option
- Added a visual button for Rustan's Registry in `registry.html` using the Rustan's logo.
- Created `rustans.html` page to provide details about the Rustan's registry.
- Implemented hover effects and responsive styling for the registry buttons.

## [2026-05-27] - UI Enhancements on Attire Page
- Centered the `.avoid-palette-container` in `attire.html` to improve layout on larger screens.
- Adjusted attire image padding and margins for better breathing room.

## [2026-05-27] - Fixed Automatic Scroll Jump on Load
- Added `window.scrollTo(0, 0)` and set `history.scrollRestoration = "manual"` in `index.html` to ensure the page starts at the top.
- Added `loading="lazy"` to the RSVP iframe to prevent it from grabbing focus/scrolling the page on load.

## [2026-05-27] - Optimized Attire Images for Mobile
- Switched from aspect-ratio cropping to `max-height: 500px` and `object-fit: contain` in `attire.html`.
- Added 1.5rem margin/padding around images to give them more breathing room.
- This ensures images are not "too tall" on mobile while preventing any cropping.

## [2026-05-27] - Optimized RSVP Form for Mobile
- Fixed nested media query bug in `index.html`.
- Adjusted RSVP iframe height for mobile devices to prevent excessive vertical space.
- Removed fixed height from `.rsvp-section` to allow it to grow naturally with its content.
- Cleaned up redundant `.rsvp-iframe-wrapper` CSS blocks.
