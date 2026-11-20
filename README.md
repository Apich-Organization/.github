# .github

Organization-level files for [Apich Organization](https://github.com/Apich-Organization).

| Path | What it is |
| --- | --- |
| `profile/README.md` | The profile rendered on the organization page, with the logo files it references. |
| `sitemap.xml` | The URL set for apich.org: the site's pages, copied from its build, plus the properties that keep their own subdomain. |
| `robots.txt` | Points crawlers at that sitemap. |
| `CNAME`, `BingSiteAuth.xml` | Domain and search-console files, kept until the domain moves. |

The site itself lives in [main-website](https://github.com/Apich-Organization/main-website),
which generates `sitemap.xml`, `robots.txt`, `llms.txt` and the structured data
for every page. The legacy homepage has been removed: apich.org serves a 404
until the domain points at that deployment, at which point `sitemap.xml`,
`robots.txt`, `CNAME` and `BingSiteAuth.xml` go too and this repository becomes
profile-only.

`tou`, `ygs-2026`, `ncee`, `status` and the personal sites keep their own
subdomains — they were never part of the consolidation, and their URLs stay in
the sitemap.

To refresh the sitemap, replace the first block of `<url>` elements with the
ones from `main-website/dist/sitemap.xml`; the second block is the fixed list of
subdomain properties and does not change with a site build.
