# Nav update — add "Sold" link to all 4 existing pages

In index.html, macdonald.html, mcnell.html, and resources.html,
find the nav <ul> and add this <li> right after the Listings link:

  <li><a href="sold.html">Sold</a></li>

Also add "Sold" to the footer <nav> in each file:

  <a href="sold.html">Sold</a>

Place it right after the Listings link in both nav and footer.

---

## sitemap.xml — add this <url> block

  <url>
    <loc>https://sherylnexthome.com/sold.html</loc>
    <lastmod>2026-04-22</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>

---

## Photos

The sold cards currently show placeholder text where photos will go.
To add real photos, replace each:

  <div class="card-img-placeholder">
    <span class="placeholder-address">...</span>
  </div>

with:

  <img src="images/sold/1340-grand.jpg" alt="1340 Grand Ave, Ojai CA" class="card-img" />

Put sold property photos in /images/sold/ in the repo.
MLS photos are typically public record and fine to use for a past-sale reference page,
but confirm with Jeri if you want to be cautious.
