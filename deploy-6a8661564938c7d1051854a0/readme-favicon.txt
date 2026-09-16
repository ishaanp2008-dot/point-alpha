POINT ALPHA — FAVICON PACKAGE
=============================

Files
-----
favicon.svg            Vector favicon (modern browsers, crispest)
favicon-32x32.png      Standard tab icon
favicon-16x16.png      Small tab icon
apple-touch-icon.png   180x180, iOS home-screen icon
favicon-512.png        Large master / PWA icon

How to install on pointalpha.co
-------------------------------
1. Upload all of these files to the same folder as your site's HTML
   (usually the site root).

2. Put this inside the <head> of your HTML:

   <link rel="icon" type="image/svg+xml" href="favicon.svg" />
   <link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png" />
   <link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png" />
   <link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png" />

3. Hard-refresh (Cmd/Ctrl + Shift + R) or clear cache to see the new icon.
   Browsers cache favicons aggressively, so it may take a moment.

Notes
-----
- The SVG favicon is already wired into your site's working HTML head.
- If your host wants a classic favicon.ico, rename/convert favicon-32x32.png
  to favicon.ico, or use any .ico converter — the PNGs above are the source.
