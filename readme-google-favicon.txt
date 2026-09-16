GETTING THE FAVICON TO SHOW IN GOOGLE SEARCH RESULTS
====================================================

The grey globe means Google has not yet indexed a valid favicon for
pointalpha.co. The favicon Google shows in SEARCH is separate from the
browser-tab favicon and has stricter rules.

WHAT GOOGLE REQUIRES
--------------------
1. The favicon must be a SQUARE image whose size is a multiple of 48px
   (48x48, 96x96, etc.). Google may ignore tiny 16/32 icons for search.
2. It must be referenced in the <head> of your HOME PAGE (the root URL
   https://pointalpha.co/), not only on subpages.
3. The favicon file AND the home page must be crawlable (not blocked by
   robots.txt, returns HTTP 200).
4. The <link> rel must be one of: icon, shortcut icon, apple-touch-icon.
5. Google only updates the search favicon when it RE-CRAWLS your site.
   This can take several days to a few weeks. You cannot force it, but
   you can speed it up (step 3 below).

STEP 1 - UPLOAD THESE FILES TO YOUR SITE ROOT
---------------------------------------------
   favicon.svg            (modern browser tabs)
   favicon-96x96.png      (Google search - preferred)
   favicon-48x48.png      (Google search - minimum)
   favicon-32x32.png      (browser tabs)
   favicon-16x16.png      (browser tabs)
   apple-touch-icon.png   (iOS, 180x180)

Put them in the same folder as your index/home HTML (the web root).

STEP 2 - PUT THIS IN THE <head> OF THE HOME PAGE
------------------------------------------------
   <link rel="icon" type="image/png" sizes="96x96" href="https://pointalpha.co/favicon-96x96.png" />
   <link rel="icon" type="image/png" sizes="48x48" href="https://pointalpha.co/favicon-48x48.png" />
   <link rel="icon" type="image/svg+xml" href="https://pointalpha.co/favicon.svg" />
   <link rel="icon" type="image/png" sizes="32x32" href="https://pointalpha.co/favicon-32x32.png" />
   <link rel="apple-touch-icon" sizes="180x180" href="https://pointalpha.co/apple-touch-icon.png" />

   Use the FULL https://pointalpha.co/... URLs (absolute paths). Google's
   crawler is happier with absolute URLs for the search favicon.

STEP 3 - ASK GOOGLE TO RE-CRAWL (speeds it up)
----------------------------------------------
   a. Go to Google Search Console (search.google.com/search-console).
   b. Add / verify the pointalpha.co property if you have not already.
   c. Use the "URL Inspection" tool on https://pointalpha.co/ and click
      "Request Indexing".
   d. Wait. The favicon usually appears within a few days to ~2 weeks
      after the next crawl.

NOTE ON THE TITLE/DESCRIPTION
-----------------------------
Your search result still shows the OLD title ("Student-led closed
capital management"). That is also cached from a previous crawl. Once
Google re-crawls (step 3), it will pick up the new title
("Closed hedge fund & equity research firm") and the new favicon
together.

TROUBLESHOOTING
---------------
- Make sure https://pointalpha.co/favicon-96x96.png opens directly in a
  browser and shows the pa mark. If it 404s, the path is wrong.
- Make sure robots.txt does not disallow the favicon files or the home page.
- The favicon background is the brand black (#09090b). On Google's white
  card it will sit inside a circle - that is normal and matches how other
  finance firms (Citadel, etc.) appear.
