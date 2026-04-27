# Wiki.js Stripe-Inspired UI Polish

Use this when you want the wiki home page to feel closer to Stripe Docs: clearer navigation, tighter typography, card-like tables, code-friendly spacing, and a cleaner content surface.

## Where to Add It

In Wiki.js:

1. Open `Administration`.
2. Go to `Theme` or `Rendering`, depending on your Wiki.js admin layout.
3. Find `Custom CSS` / `Inject CSS`.
4. Paste the CSS below.
5. Save and refresh the wiki.

## Custom CSS

```css
.utopia-home-scope {
  display: none;
}

:root {
  --utopia-bg: #f6f9fc;
  --utopia-surface: #ffffff;
  --utopia-text: #0a2540;
  --utopia-muted: #5b6b7f;
  --utopia-border: #dbe4ef;
  --utopia-accent: #635bff;
  --utopia-accent-strong: #4f46e5;
  --utopia-code-bg: #0a2540;
}

main:has(.utopia-home-scope),
.contents:has(.utopia-home-scope),
.page-contents:has(.utopia-home-scope),
.v-main:has(.utopia-home-scope) {
  background: var(--utopia-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

main:has(.utopia-home-scope),
main:has(.utopia-home-scope) *,
.contents:has(.utopia-home-scope),
.contents:has(.utopia-home-scope) *,
.page-contents:has(.utopia-home-scope),
.page-contents:has(.utopia-home-scope) *,
.v-main:has(.utopia-home-scope),
.v-main:has(.utopia-home-scope) * {
  font-feature-settings: "kern";
}

main:has(.utopia-home-scope) h1,
main:has(.utopia-home-scope) h2,
main:has(.utopia-home-scope) h3,
.contents:has(.utopia-home-scope) h1,
.contents:has(.utopia-home-scope) h2,
.contents:has(.utopia-home-scope) h3,
.page-contents:has(.utopia-home-scope) h1,
.page-contents:has(.utopia-home-scope) h2,
.page-contents:has(.utopia-home-scope) h3,
.v-main:has(.utopia-home-scope) h1,
.v-main:has(.utopia-home-scope) h2,
.v-main:has(.utopia-home-scope) h3 {
  color: var(--utopia-text);
  letter-spacing: 0;
}

main:has(.utopia-home-scope) h1,
.contents:has(.utopia-home-scope) h1,
.page-contents:has(.utopia-home-scope) h1,
.v-main:has(.utopia-home-scope) h1 {
  font-size: 42px;
  line-height: 1.08;
  margin-bottom: 12px;
}

main:has(.utopia-home-scope) h2,
.contents:has(.utopia-home-scope) h2,
.page-contents:has(.utopia-home-scope) h2,
.v-main:has(.utopia-home-scope) h2 {
  border-top: 1px solid var(--utopia-border);
  padding-top: 28px;
  margin-top: 36px;
}

.contents:has(.utopia-home-scope) p,
.contents:has(.utopia-home-scope) li,
.contents:has(.utopia-home-scope) td,
.contents:has(.utopia-home-scope) th,
main:has(.utopia-home-scope) p,
main:has(.utopia-home-scope) li,
main:has(.utopia-home-scope) td,
main:has(.utopia-home-scope) th,
.page-contents:has(.utopia-home-scope) p,
.page-contents:has(.utopia-home-scope) li,
.page-contents:has(.utopia-home-scope) td,
.page-contents:has(.utopia-home-scope) th,
.v-main:has(.utopia-home-scope) p,
.v-main:has(.utopia-home-scope) li,
.v-main:has(.utopia-home-scope) td,
.v-main:has(.utopia-home-scope) th {
  color: var(--utopia-muted);
  line-height: 1.65;
}

.contents:has(.utopia-home-scope) a,
main:has(.utopia-home-scope) a,
.page-contents:has(.utopia-home-scope) a,
.v-main:has(.utopia-home-scope) a {
  color: var(--utopia-accent-strong);
  font-weight: 600;
  text-decoration: none;
}

.contents:has(.utopia-home-scope) a:hover,
main:has(.utopia-home-scope) a:hover,
.page-contents:has(.utopia-home-scope) a:hover,
.v-main:has(.utopia-home-scope) a:hover {
  text-decoration: underline;
}

.contents:has(.utopia-home-scope) > p:first-of-type,
main:has(.utopia-home-scope) p:first-of-type,
.page-contents:has(.utopia-home-scope) > p:first-of-type,
.v-main:has(.utopia-home-scope) p:first-of-type {
  max-width: 760px;
  color: #425466;
  font-size: 18px;
}

.contents:has(.utopia-home-scope) table,
main:has(.utopia-home-scope) table,
.page-contents:has(.utopia-home-scope) table,
.v-main:has(.utopia-home-scope) table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  overflow: hidden;
  margin: 20px 0 28px;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: 0 18px 45px rgba(10, 37, 64, 0.08);
}

.contents:has(.utopia-home-scope) th,
main:has(.utopia-home-scope) th,
.page-contents:has(.utopia-home-scope) th,
.v-main:has(.utopia-home-scope) th {
  background: #eef4ff;
  color: var(--utopia-text);
  font-size: 13px;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}

.contents:has(.utopia-home-scope) th,
.contents:has(.utopia-home-scope) td,
main:has(.utopia-home-scope) th,
main:has(.utopia-home-scope) td,
.page-contents:has(.utopia-home-scope) th,
.page-contents:has(.utopia-home-scope) td,
.v-main:has(.utopia-home-scope) th,
.v-main:has(.utopia-home-scope) td {
  border-bottom: 1px solid var(--utopia-border);
  padding: 16px 18px;
  vertical-align: top;
}

.contents:has(.utopia-home-scope) tr:last-child td,
main:has(.utopia-home-scope) tr:last-child td,
.page-contents:has(.utopia-home-scope) tr:last-child td,
.v-main:has(.utopia-home-scope) tr:last-child td {
  border-bottom: 0;
}

.contents:has(.utopia-home-scope) code,
main:has(.utopia-home-scope) code,
.page-contents:has(.utopia-home-scope) code,
.v-main:has(.utopia-home-scope) code {
  color: #334155;
  background: #eef4ff;
  border: 1px solid #d8e2f0;
  border-radius: 6px;
  padding: 2px 6px;
}

.contents:has(.utopia-home-scope) pre,
main:has(.utopia-home-scope) pre,
.page-contents:has(.utopia-home-scope) pre,
.v-main:has(.utopia-home-scope) pre {
  background: var(--utopia-code-bg);
  border-radius: 8px;
  box-shadow: 0 18px 45px rgba(10, 37, 64, 0.14);
}

.contents:has(.utopia-home-scope) blockquote,
main:has(.utopia-home-scope) blockquote,
.page-contents:has(.utopia-home-scope) blockquote,
.v-main:has(.utopia-home-scope) blockquote {
  margin: 24px 0;
  padding: 18px 20px;
  background: #ffffff;
  border-left: 4px solid var(--utopia-accent);
  border-radius: 8px;
  box-shadow: 0 12px 32px rgba(10, 37, 64, 0.07);
}

.contents:has(.utopia-home-scope) hr,
main:has(.utopia-home-scope) hr,
.page-contents:has(.utopia-home-scope) hr,
.v-main:has(.utopia-home-scope) hr {
  border-color: var(--utopia-border);
}
```

## Quick Test

If the full CSS still does not visibly change anything, paste this tiny test into Custom CSS:

```css
.utopia-home-scope {
  display: block !important;
  height: 8px !important;
  background: red !important;
}
```

Then refresh the home page.

- If you see a red bar under the title, the marker works and the issue is the container selector.
- If you do not see a red bar, Wiki.js is stripping the marker or the home page has not synced yet.
- If every page changes, the CSS was pasted without the scoped selectors.

## Older Scoped CSS

This was the first version. Use the larger CSS above first.

```css
.contents:has(.utopia-home-scope) p,
.contents:has(.utopia-home-scope) li,
.contents:has(.utopia-home-scope) td,
.contents:has(.utopia-home-scope) th {
  color: var(--utopia-muted);
  line-height: 1.65;
}

.contents:has(.utopia-home-scope) a {
  color: var(--utopia-accent-strong);
  font-weight: 600;
  text-decoration: none;
}

.contents:has(.utopia-home-scope) a:hover {
  text-decoration: underline;
}

.contents:has(.utopia-home-scope) > p:first-of-type {
  max-width: 760px;
  color: #425466;
  font-size: 18px;
}

.contents:has(.utopia-home-scope) table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  overflow: hidden;
  margin: 20px 0 28px;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: 0 18px 45px rgba(10, 37, 64, 0.08);
}

.contents:has(.utopia-home-scope) th {
  background: #eef4ff;
  color: var(--utopia-text);
  font-size: 13px;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}

.contents:has(.utopia-home-scope) th,
.contents:has(.utopia-home-scope) td {
  border-bottom: 1px solid var(--utopia-border);
  padding: 16px 18px;
  vertical-align: top;
}

.contents:has(.utopia-home-scope) tr:last-child td {
  border-bottom: 0;
}

.contents:has(.utopia-home-scope) code {
  color: #334155;
  background: #eef4ff;
  border: 1px solid #d8e2f0;
  border-radius: 6px;
  padding: 2px 6px;
}

.contents:has(.utopia-home-scope) pre {
  background: var(--utopia-code-bg);
  border-radius: 8px;
  box-shadow: 0 18px 45px rgba(10, 37, 64, 0.14);
}

.contents:has(.utopia-home-scope) blockquote {
  margin: 24px 0;
  padding: 18px 20px;
  background: #ffffff;
  border-left: 4px solid var(--utopia-accent);
  border-radius: 8px;
  box-shadow: 0 12px 32px rgba(10, 37, 64, 0.07);
}

.contents:has(.utopia-home-scope) hr {
  border-color: var(--utopia-border);
}
```

This CSS only affects pages that contain:

```html
<span class="utopia-home-scope"></span>
```

The current `home.md` page already has that marker. Other pages will stay unchanged.

## Content Pattern

For pages to look less basic, use this structure:

- One clear page title.
- One short intro paragraph.
- Three to six task links near the top.
- Tables for guide indexes and comparisons.
- Short sections grouped by user goal.
- Keep updates at the bottom so they do not bury the main guide.
