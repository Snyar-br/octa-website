# Octa website

A single-page, front-end-only website. No backend, no database, no forms.

## Files
- index.html: the page
- styles.css, main.js: all styling and scripts (kept out of the HTML so the strict security policy works)
- favicon.svg: browser tab icon
- _headers: security headers for Cloudflare Pages or Netlify
- .htaccess: the same headers for Apache / cPanel hosting
- robots.txt, sitemap.xml: for search engines (replace YOUR-DOMAIN with your real domain)
- .well-known/security.txt: tells security researchers how to reach you (renew the Expires date yearly)

## Deploy on Cloudflare Pages (recommended, free)
1. Create a free account at dash.cloudflare.com.
2. Go to Workers & Pages, choose Create, then Pages, then "Upload assets".
3. Drag in this whole folder (including the hidden _headers and .well-known files).
4. Connect your domain under Custom domains. HTTPS is turned on automatically.
5. In your domain's SSL/TLS settings choose "Full (strict)" and turn on "Always Use HTTPS".

## Deploy on Netlify
Drag the folder onto app.netlify.com/drop. The _headers file is applied automatically.

## Check the security
After the site is live, test it at:
- https://securityheaders.com
- https://developer.mozilla.org/en-US/observatory
Both should give an A or A+.

## Editing
Change text directly in index.html. Do not add inline <script> or style="" attributes,
because the security policy blocks them. Put new styles in styles.css and new code in main.js.
