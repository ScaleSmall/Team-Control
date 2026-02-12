# Context

## Project
- Slug: `seo-audit-HillCoPaint`
- Website: https://www.hillcopaint.com/
- Stack: Supabase; bolt.new
- State file: `ops/STATE/seo-audit-HillCoPaint.md`

## Prior work / history
- Prior runs found in `ops/RUNS/` for this project: **none** (this is the first run).

## Constraints (must follow)
- This is **read-only** (no deploys, no PRs in this run).
- **No invented metrics**. Any numbers must be tied to a source (GSC export, crawl output, screenshot, etc.).
- Output must be **publish-ready** per `02_plan.md` acceptance criteria.

## Inputs currently available
- Public site URL only.

## Inputs needed to complete a publish-ready SEO audit
### Google Search Console (preferred)
Provide exports (CSV is fine) or screenshots for:
- Performance → Search results (last 3 months + last 28 days): queries + pages
- Indexing/Pages (or Coverage): excluded reasons + counts
- Sitemaps status
- Manual actions / Security issues (if any)

Also confirm the exact GSC property to use:
- `https://www.hillcopaint.com/` vs `sc-domain:hillcopaint.com`

### Crawl evidence (read-only)
If allowed, we’ll run a crawl of the site (or you can provide one) to capture:
- indexable pages, titles/meta, H1s
- canonicals, redirects, status codes
- internal link structure
- sitemap/robots findings

### Brand / copy context (to avoid tone/positioning misses)
- Primary service areas + target cities
- Key differentiators (warranty, years in business, specialties)
- Any words/claims to avoid

## Next actions
1) You confirm which GSC property + share the exports.
2) You confirm we can run a read-only crawl (checkbox in `03_risk_and_approvals.md`).
3) Proceed to draft `05_outputs/seo-audit.md` with evidence-backed findings.
