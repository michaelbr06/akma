# Change Log

## [2026-05-27] - Optimized Attire Images for Mobile
- Switched from aspect-ratio cropping to `max-height: 500px` and `object-fit: contain` in `attire.html`.
- Added 1.5rem margin/padding around images to give them more breathing room.
- This ensures images are not "too tall" on mobile while preventing any cropping.

## [2026-05-27] - Optimized RSVP Form for Mobile
- Fixed nested media query bug in `index.html`.
- Adjusted RSVP iframe height for mobile devices to prevent excessive vertical space.
- Removed fixed height from `.rsvp-section` to allow it to grow naturally with its content.
- Cleaned up redundant `.rsvp-iframe-wrapper` CSS blocks.
