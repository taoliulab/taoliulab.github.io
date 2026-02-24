# AGENTS.md — taoliulab.github.io

This file defines how the assistant should maintain the Taoliu Lab website repo.

## Scope

- Repository: `~/Projects/Github/taoliulab.github.io`
- Production site: `https://lab.biomisc.org/`
- Deployment trigger: any push to `origin/master` (GitHub Pages)

## Core rules

1. **Build before push**
   - Always run:
     - `bundle exec jekyll build`
   - Do not push if build fails.

2. **Keep edits minimal and reviewable**
   - Prefer small commits with clear messages.
   - Avoid unrelated formatting churn.

3. **Preserve site structure**
   - Do not rename/move top-level folders or key files unless requested.
   - Keep `CNAME` as `lab.biomisc.org` unless explicitly changed.

4. **Protect publishing settings**
   - `_config.yml` fields should remain consistent unless requested:
     - `url: "https://lab.biomisc.org"`
     - `baseurl: ""`

5. **No destructive git actions without confirmation**
   - Ask before `git reset --hard`, force-push, branch deletion, or history rewrite.

## Local sandbox workflow

Use repo-local gems to isolate dependencies:

```bash
bundle config set --local path '.bundle/vendor'
bundle config set --local without 'development'
bundle install
```

Build and preview:

```bash
bundle exec jekyll build
bundle exec jekyll serve --host 0.0.0.0 --port 4000 --livereload
```

## Optional UI debugging workflow

When layout/interaction issues appear:

1. Start local server.
2. Use Playwright checks on key pages.
3. Capture screenshot + console errors.
4. Fix and re-run until clean.

## Suggested pre-push checklist

- [ ] `git status` clean except intended changes
- [ ] `bundle exec jekyll build` passes
- [ ] changed pages render correctly
- [ ] links/assets for edited pages work
- [ ] commit message explains what changed and why

## Commit style

Use concise, semantic messages, e.g.:

- `content: update team member bios`
- `home: refresh hero text and CTA`
- `news: add Feb 2026 lab highlights`
- `fix: correct broken publication links`
- `style: improve mobile spacing on homepage`

## Notes for assistant behavior

- Prefer action over long narration.
- Report exactly what changed, where, and how to verify.
- If uncertain about content tone (scientific messaging, lab announcements), ask Dr. Liu before publishing.
