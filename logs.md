# Change Log

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
