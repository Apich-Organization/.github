# .github

Organization-level files for [Apich Organization](https://github.com/Apich-Organization).

| Path | What it is |
| --- | --- |
| `profile/README.md` | The profile rendered on the organization page, with the logo files it references. |
| `index.html` | The legacy homepage, still served at apich.org until the domain points at the new site. |
| `sitemap.xml` | The URL set for apich.org, copied from the site build so the two cannot drift. |
| `CNAME`, `BingSiteAuth.xml` | Domain and search-console files for the same legacy deployment. |

The site itself lives in [main-website](https://github.com/Apich-Organization/main-website),
which generates `sitemap.xml`, `robots.txt`, `llms.txt` and the structured data
for every page. When `apich.org` moves to that deployment, `index.html`,
`sitemap.xml`, `CNAME` and `BingSiteAuth.xml` are removed from this repository
and it becomes profile-only.

To refresh the sitemap in the meantime:

```bash
cp ../main-website/dist/sitemap.xml sitemap.xml
```
