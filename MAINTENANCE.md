# MAINTENANCE.md — Taoliu Lab website

Recurring maintenance checklist for `taoliulab.github.io`.

## Weekly (light pass)

1. News and announcements
   - Add new lab news items.
   - Remove outdated time-sensitive notices.

2. Publication links sanity check
   - Spot-check newest publication entries.
   - Fix broken DOI/PubMed/journal links.

3. Homepage freshness
   - Confirm hero text, featured highlights, and calls-to-action are current.

## Monthly (full pass)

1. People page
   - Update members, roles, photos, and profile links.

2. Publications
   - Add newly accepted/published papers.
   - Ensure citation formatting is consistent.

3. Grants / projects / resources
   - Update project status and external resource links.

4. Site quality checks
   - Run full local build.
   - Verify key pages on desktop + mobile.
   - Check for console errors on main pages.

## Pre-push release checklist

- `bundle exec jekyll build` succeeds.
- No unintended file changes in `git status`.
- Updated pages render correctly.
- Commit message is clear and scoped.
- Push to `origin/master`.

## Suggested cadence reminder

- Weekly quick update: every Monday morning.
- Monthly full review: first weekend of each month.

## Ownership

- Final content decisions: Dr. Liu
- Technical implementation and QA: assistant
