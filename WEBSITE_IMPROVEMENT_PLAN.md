# Website Improvement Plan (Tao Liu Lab)

## Goal
Improve clarity, freshness, and maintainability of lab.biomisc.org in phased iterations.

## Phase 1 (current)

1. Homepage quick refresh
   - Add three compact sections under intro:
     - Latest News (recent posts)
     - Featured Software
     - Join / Contact
2. Publication link cleanup (priority on newest entries)
   - Replace fragile/indirect links with stable publisher/DOI-style links when available.
3. Tutorials internal-link scaffold
   - Create dedicated internal tutorial posts for key topics.
   - Update `Tutorial.md` to point to internal posts instead of external links where possible.

## Phase 2

1. Publications usability
   - Add optional tags/badges (co-corresponding, method, single-cell).
   - Improve consistency of links (DOI/PubMed/journal page).
2. Research page readability
   - Convert into clearer theme-based sections with representative outputs.
3. People page polish
   - Add role + expertise snippets and recruiting note.

## Phase 3

1. Quality and maintenance automation
   - Add periodic link-check workflow.
   - Add lightweight analytics and metadata polish.
2. Visual and navigation polish
   - Improve homepage hierarchy and call-to-action flow.

## Working notes
- Keep edits small and reviewable.
- Run local build before push (`bundle exec jekyll build`).
- Preserve compatibility with current Jekyll/minima setup.
