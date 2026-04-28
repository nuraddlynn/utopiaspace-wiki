# Wiki.js Stripe-Inspired UI Polish

Use this when you want the wiki to use the same blue as the existing UtopiaSpace action buttons, while making the home page feel closer to Stripe Docs: clearer navigation, tighter typography, card-like tables, code-friendly spacing, and a cleaner content surface.

Most of the visual polish below is scoped to the home page only. The brand-blue overrides are global so the website blue matches the button color shown in the UtopiaSpace UI.

```html
<span class="utopia-home-scope"></span>
```

The current `home.md` page already has that marker.

## Where to Add It

In Wiki.js:

1. Open `Administration`.
2. Go to `Theme` or `Rendering`, depending on your Wiki.js admin layout.
3. Find `Custom CSS` / `Inject CSS`.
4. Paste the CSS below.
5. Save and refresh the wiki.

## Custom CSS

Copy everything inside this CSS block. Do not copy the opening or closing triple backticks.

```css
.utopia-home-scope {
  display: none;
}

:root {
  --utopia-brand-blue: #1976d2;
  --utopia-brand-blue-hover: #1565c0;
  --utopia-brand-blue-soft: #e8f2fd;
  --utopia-page-bg: #ffffff;
  --utopia-sidebar-bg: #ffffff;
  --utopia-sidebar-hover: #f6f9fc;
  --utopia-sidebar-text: #22324a;
  --utopia-sidebar-muted: #4b5568;
  --utopia-bg: #ffffff;
  --utopia-surface: #ffffff;
  --utopia-surface-soft: #f9fbfd;
  --utopia-row-soft: #f7f9fc;
  --utopia-text: #0a2540;
  --utopia-muted: #5b6b7f;
  --utopia-border: #dbe4ef;
  --utopia-accent: var(--utopia-brand-blue);
  --utopia-accent-strong: var(--utopia-brand-blue);
  --utopia-code-bg: #0a2540;
  --utopia-code-text: #e6edf7;
  --utopia-inline-code-bg: #eef4ff;
  --utopia-inline-code-text: #334155;
  --utopia-shadow: 0 1px 2px rgba(10, 37, 64, 0.04);
  --utopia-shadow-strong: 0 18px 45px rgba(10, 37, 64, 0.14);
}

@media (prefers-color-scheme: dark) {
  :root {
    --utopia-brand-blue: #1976d2;
    --utopia-brand-blue-hover: #1565c0;
    --utopia-brand-blue-soft: #112b46;
    --utopia-accent: var(--utopia-brand-blue);
    --utopia-accent-strong: var(--utopia-brand-blue);
  }
}

.theme--dark.v-application,
body.theme--dark,
html.theme--dark {
  --utopia-brand-blue: #1976d2;
  --utopia-brand-blue-hover: #1565c0;
  --utopia-brand-blue-soft: #112b46;
  --utopia-page-bg: #0b1220;
  --utopia-sidebar-bg: #0b1220;
  --utopia-sidebar-hover: #111827;
  --utopia-sidebar-text: #dbe7f6;
  --utopia-sidebar-muted: #9aa8bc;
  --utopia-bg: #0b1220;
  --utopia-surface: #111827;
  --utopia-surface-soft: #172033;
  --utopia-row-soft: #0f172a;
  --utopia-text: #f8fafc;
  --utopia-muted: #b6c2d1;
  --utopia-border: #263247;
  --utopia-accent: var(--utopia-brand-blue);
  --utopia-accent-strong: #64b5f6;
  --utopia-code-bg: #050816;
  --utopia-code-text: #e6edf7;
  --utopia-inline-code-bg: #1b2638;
  --utopia-inline-code-text: #dbeafe;
  --utopia-shadow: 0 18px 45px rgba(0, 0, 0, 0.26);
  --utopia-shadow-strong: 0 18px 45px rgba(0, 0, 0, 0.36);
}

html,
body,
.v-application {
  background: var(--utopia-page-bg) !important;
  color: var(--utopia-text) !important;
  font-family: Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif !important;
}

.v-application,
.v-application .v-main,
.v-application main {
  background: var(--utopia-page-bg) !important;
}

.v-application h1,
.v-application h2,
.v-application h3,
.v-application h4,
.v-application h5,
.v-application h6,
.v-application p,
.v-application a,
.v-application li,
.v-application td,
.v-application th,
.v-application .v-list-item__title {
  font-family: Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif !important;
}

.v-application .primary,
.v-application .blue,
.v-application .info,
.v-application .v-btn.primary,
.v-application .v-btn.blue,
.v-application .v-btn.info {
  background-color: var(--utopia-brand-blue) !important;
  border-color: var(--utopia-brand-blue) !important;
}

.v-application .primary--text,
.v-application .blue--text,
.v-application .info--text,
.v-application a:not(.v-btn):not(.v-list-item) {
  color: var(--utopia-brand-blue) !important;
  caret-color: var(--utopia-brand-blue) !important;
}

.v-application .v-btn.primary:hover,
.v-application .v-btn.blue:hover,
.v-application .v-btn.info:hover {
  background-color: var(--utopia-brand-blue-hover) !important;
  border-color: var(--utopia-brand-blue-hover) !important;
}

.v-application .v-tabs-slider,
.v-application .v-progress-linear__determinate,
.v-application .v-pagination__item--active {
  background-color: var(--utopia-brand-blue) !important;
  border-color: var(--utopia-brand-blue) !important;
}

.v-application .v-list-item--active,
.v-application .v-chip.primary {
  background-color: var(--utopia-brand-blue-soft) !important;
}

.v-application .v-navigation-drawer,
.v-application .v-navigation-drawer.primary,
.v-application .v-navigation-drawer.blue,
.v-application .v-navigation-drawer.info,
.v-application .v-navigation-drawer.theme--dark,
.v-application .v-navigation-drawer .v-navigation-drawer__content,
.v-application .v-navigation-drawer .v-sheet,
.v-application .v-navigation-drawer .v-toolbar,
.v-application .v-navigation-drawer .v-card {
  background: var(--utopia-sidebar-bg) !important;
  background-color: var(--utopia-sidebar-bg) !important;
  border-right: 1px solid var(--utopia-border) !important;
  box-shadow: none !important;
}

.v-application .v-navigation-drawer .v-list,
.v-application .v-navigation-drawer .v-list-group,
.v-application .v-navigation-drawer .v-list-item,
.v-application .v-navigation-drawer .primary,
.v-application .v-navigation-drawer .blue,
.v-application .v-navigation-drawer .info,
.v-application .v-navigation-drawer .v-list-item.primary,
.v-application .v-navigation-drawer .v-list-item.blue,
.v-application .v-navigation-drawer .v-list-item.info,
.v-application .v-navigation-drawer .v-list-group__header,
.v-application .v-navigation-drawer .v-list-group__items,
.v-application .v-navigation-drawer .theme--dark,
.v-application .v-navigation-drawer .v-item-group,
.v-application .v-navigation-drawer .v-btn-toggle,
.v-application .v-navigation-drawer .v-slide-group,
.v-application .v-navigation-drawer .v-slide-group__wrapper,
.v-application .v-navigation-drawer .v-slide-group__content,
.v-application .v-navigation-drawer .v-tabs-bar,
.v-application .v-navigation-drawer .v-toolbar__content,
.v-application .v-navigation-drawer .v-card__text,
.v-application .v-navigation-drawer .v-card__actions {
  background: transparent !important;
  background-color: transparent !important;
}

.v-application .v-navigation-drawer .v-item-group:first-of-type,
.v-application .v-navigation-drawer .v-btn-toggle:first-of-type,
.v-application .v-navigation-drawer .v-slide-group:first-of-type {
  display: none !important;
}

.v-application .v-navigation-drawer .v-navigation-drawer__content > div:nth-child(2),
.v-application .v-navigation-drawer .v-navigation-drawer__content > nav:first-of-type,
.v-application .v-navigation-drawer .v-navigation-drawer__content > .v-list:first-of-type {
  display: none !important;
}

.v-application .v-navigation-drawer .v-list-item {
  min-height: 38px !important;
  margin: 1px 12px !important;
  padding: 0 8px !important;
  border-radius: 0 !important;
  color: var(--utopia-sidebar-text) !important;
}

.v-application .v-navigation-drawer .v-list-item__title,
.v-application .v-navigation-drawer .v-list-item__subtitle,
.v-application .v-navigation-drawer .v-list-group__header,
.v-application .v-navigation-drawer .v-icon {
  color: var(--utopia-sidebar-text) !important;
}

.v-application .v-navigation-drawer .v-list-item__title {
  font-size: 14.5px !important;
  font-weight: 500 !important;
  line-height: 1.35 !important;
}

.v-application .v-navigation-drawer .v-subheader,
.v-application .v-navigation-drawer .v-list-item--disabled .v-list-item__title {
  color: var(--utopia-sidebar-muted) !important;
  font-size: 12px !important;
  font-weight: 700 !important;
  letter-spacing: 0.04em !important;
  text-transform: uppercase !important;
}

.v-application .v-navigation-drawer .v-subheader {
  margin-top: 18px !important;
  margin-bottom: 0 !important;
  min-height: 24px !important;
}

.v-application .v-navigation-drawer .v-list-item:hover {
  background: transparent !important;
  background-color: transparent !important;
  color: #000000 !important;
}

.v-application .v-navigation-drawer .v-list-item:hover .v-list-item__title,
.v-application .v-navigation-drawer .v-list-item:hover .v-icon {
  color: var(--utopia-brand-blue) !important;
}

.v-application .v-navigation-drawer .v-list-item--active,
.v-application .v-navigation-drawer .v-list-item.v-list-item--active {
  background: transparent !important;
  background-color: transparent !important;
  color: var(--utopia-brand-blue) !important;
  font-weight: 700 !important;
}

.v-application .v-navigation-drawer .v-list-item--active .v-list-item__title,
.v-application .v-navigation-drawer .v-list-item--active .v-icon {
  color: var(--utopia-brand-blue) !important;
  font-weight: 700 !important;
}

.v-application .v-navigation-drawer .v-btn,
.v-application .v-navigation-drawer .v-btn.primary,
.v-application .v-navigation-drawer .v-btn.blue,
.v-application .v-navigation-drawer .v-btn.info,
.v-application .v-navigation-drawer .v-btn--active,
.v-application .v-navigation-drawer .v-item--active,
.v-application .v-navigation-drawer button,
.v-application .v-navigation-drawer .v-btn-toggle,
.v-application .v-navigation-drawer .v-btn-toggle .v-btn,
.v-application .v-navigation-drawer .v-tabs,
.v-application .v-navigation-drawer .v-tab {
  background: transparent !important;
  background-color: transparent !important;
  box-shadow: none !important;
  color: var(--utopia-sidebar-text) !important;
}

.v-application .v-navigation-drawer .v-btn .v-btn__content,
.v-application .v-navigation-drawer .v-btn .v-icon {
  color: var(--utopia-sidebar-text) !important;
}

.v-application .v-navigation-drawer .v-btn::before,
.v-application .v-navigation-drawer .v-btn::after,
.v-application .v-navigation-drawer .v-list-item::before,
.v-application .v-navigation-drawer .v-list-item::after,
.v-application .v-navigation-drawer .v-tab::before,
.v-application .v-navigation-drawer .v-tab::after {
  background: transparent !important;
  background-color: transparent !important;
  opacity: 0 !important;
}

.v-application .v-navigation-drawer .v-btn:hover,
.v-application .v-navigation-drawer button:hover,
.v-application .v-navigation-drawer .v-tab:hover {
  background: transparent !important;
  background-color: transparent !important;
  color: var(--utopia-brand-blue) !important;
}

.v-application .v-navigation-drawer .v-btn:hover .v-btn__content,
.v-application .v-navigation-drawer .v-btn:hover .v-icon,
.v-application .v-navigation-drawer .v-tab:hover,
.v-application .v-navigation-drawer .v-tab:hover .v-icon {
  color: var(--utopia-brand-blue) !important;
}

.v-application .v-navigation-drawer hr,
.v-application .v-navigation-drawer .v-divider {
  border-color: var(--utopia-border) !important;
  opacity: 1 !important;
  margin: 8px 16px 14px !important;
}

.v-application .v-navigation-drawer .v-subheader + hr,
.v-application .v-navigation-drawer .v-subheader + .v-divider,
.v-application .v-navigation-drawer .v-list-item--disabled + hr,
.v-application .v-navigation-drawer .v-list-item--disabled + .v-divider {
  margin-top: 2px !important;
}

main:has(.utopia-home-scope),
.contents:has(.utopia-home-scope),
.page-contents:has(.utopia-home-scope),
.v-main:has(.utopia-home-scope) {
  background: var(--utopia-page-bg);
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

main:has(.utopia-home-scope) h3,
.contents:has(.utopia-home-scope) h3,
.page-contents:has(.utopia-home-scope) h3,
.v-main:has(.utopia-home-scope) h3 {
  margin-top: 30px;
  margin-bottom: 14px;
}

main:has(.utopia-home-scope) p,
main:has(.utopia-home-scope) li,
main:has(.utopia-home-scope) td,
main:has(.utopia-home-scope) th,
.contents:has(.utopia-home-scope) p,
.contents:has(.utopia-home-scope) li,
.contents:has(.utopia-home-scope) td,
.contents:has(.utopia-home-scope) th,
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

main:has(.utopia-home-scope) a,
.contents:has(.utopia-home-scope) a,
.page-contents:has(.utopia-home-scope) a,
.v-main:has(.utopia-home-scope) a {
  color: var(--utopia-accent-strong);
  font-weight: 600;
  text-decoration: none;
}

main:has(.utopia-home-scope) a:hover,
.contents:has(.utopia-home-scope) a:hover,
.page-contents:has(.utopia-home-scope) a:hover,
.v-main:has(.utopia-home-scope) a:hover {
  color: #000000 !important;
  text-decoration: none !important;
}

main:has(.utopia-home-scope) .utopia-home-actions,
.contents:has(.utopia-home-scope) .utopia-home-actions,
.page-contents:has(.utopia-home-scope) .utopia-home-actions,
.v-main:has(.utopia-home-scope) .utopia-home-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 22px 0 32px;
}

main:has(.utopia-home-scope) .utopia-home-actions a,
.contents:has(.utopia-home-scope) .utopia-home-actions a,
.page-contents:has(.utopia-home-scope) .utopia-home-actions a,
.v-main:has(.utopia-home-scope) .utopia-home-actions a {
  display: inline-flex;
  align-items: center;
  min-height: 36px;
  padding: 8px 14px;
  color: #ffffff !important;
  background: var(--utopia-brand-blue);
  border: 1px solid var(--utopia-brand-blue);
  border-radius: 6px;
  font-weight: 700;
  line-height: 1.2;
  text-decoration: none;
  box-shadow: 0 10px 24px rgba(25, 118, 210, 0.22);
}

main:has(.utopia-home-scope) .utopia-home-actions a:hover,
.contents:has(.utopia-home-scope) .utopia-home-actions a:hover,
.page-contents:has(.utopia-home-scope) .utopia-home-actions a:hover,
.v-main:has(.utopia-home-scope) .utopia-home-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

main:has(.utopia-home-scope) .utopia-quickstart-table,
.contents:has(.utopia-home-scope) .utopia-quickstart-table,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
  margin: 18px 0 30px;
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-home-scope) .utopia-quickstart-head,
.contents:has(.utopia-home-scope) .utopia-quickstart-head,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-head,
.v-main:has(.utopia-home-scope) .utopia-quickstart-head {
  padding: 14px 20px;
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

main:has(.utopia-home-scope) .utopia-quickstart-table a,
.contents:has(.utopia-home-scope) .utopia-quickstart-table a,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table a,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table a,
main:has(.utopia-home-scope) .utopia-quickstart-table p,
.contents:has(.utopia-home-scope) .utopia-quickstart-table p,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table p,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table p {
  min-height: 62px;
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
  background: var(--utopia-surface);
}

main:has(.utopia-home-scope) .utopia-quickstart-table > a:nth-of-type(odd),
main:has(.utopia-home-scope) .utopia-quickstart-table > p:nth-of-type(odd),
.contents:has(.utopia-home-scope) .utopia-quickstart-table > a:nth-of-type(odd),
.contents:has(.utopia-home-scope) .utopia-quickstart-table > p:nth-of-type(odd),
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table > a:nth-of-type(odd),
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table > p:nth-of-type(odd),
.v-main:has(.utopia-home-scope) .utopia-quickstart-table > a:nth-of-type(odd),
.v-main:has(.utopia-home-scope) .utopia-quickstart-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft) !important;
  background-color: var(--utopia-row-soft) !important;
}

main:has(.utopia-home-scope) .utopia-quickstart-table a:nth-last-child(2),
.contents:has(.utopia-home-scope) .utopia-quickstart-table a:nth-last-child(2),
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table a:nth-last-child(2),
.v-main:has(.utopia-home-scope) .utopia-quickstart-table a:nth-last-child(2),
main:has(.utopia-home-scope) .utopia-quickstart-table p:last-child,
.contents:has(.utopia-home-scope) .utopia-quickstart-table p:last-child,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table p:last-child,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table p:last-child {
  border-bottom: 0;
}

main:has(.utopia-home-scope) .utopia-quickstart-table a,
.contents:has(.utopia-home-scope) .utopia-quickstart-table a,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table a,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table a {
  display: flex;
  align-items: center;
  color: var(--utopia-accent-strong) !important;
  font-size: 15px;
  font-weight: 600;
  line-height: 1.35;
  box-shadow: none !important;
  outline: 0 !important;
  text-decoration: none !important;
}

main:has(.utopia-home-scope) .utopia-quickstart-table a::before,
main:has(.utopia-home-scope) .utopia-quickstart-table a::after,
.contents:has(.utopia-home-scope) .utopia-quickstart-table a::before,
.contents:has(.utopia-home-scope) .utopia-quickstart-table a::after,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table a::before,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table a::after,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table a::before,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table a::after {
  display: none !important;
}

main:has(.utopia-home-scope) .utopia-quickstart-table a:hover,
.contents:has(.utopia-home-scope) .utopia-quickstart-table a:hover,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table a:hover,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table a:hover {
  color: #000000 !important;
  text-decoration: none !important;
}

main:has(.utopia-home-scope) .utopia-quickstart-table p,
.contents:has(.utopia-home-scope) .utopia-quickstart-table p,
.page-contents:has(.utopia-home-scope) .utopia-quickstart-table p,
.v-main:has(.utopia-home-scope) .utopia-quickstart-table p {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

@media (max-width: 720px) {
  main:has(.utopia-home-scope) .utopia-quickstart-table,
  .contents:has(.utopia-home-scope) .utopia-quickstart-table,
  .page-contents:has(.utopia-home-scope) .utopia-quickstart-table,
  .v-main:has(.utopia-home-scope) .utopia-quickstart-table {
    grid-template-columns: 1fr;
  }

  main:has(.utopia-home-scope) .utopia-quickstart-head:nth-child(2),
  .contents:has(.utopia-home-scope) .utopia-quickstart-head:nth-child(2),
  .page-contents:has(.utopia-home-scope) .utopia-quickstart-head:nth-child(2),
  .v-main:has(.utopia-home-scope) .utopia-quickstart-head:nth-child(2) {
    display: none;
  }

  main:has(.utopia-home-scope) .utopia-quickstart-table a,
  .contents:has(.utopia-home-scope) .utopia-quickstart-table a,
  .page-contents:has(.utopia-home-scope) .utopia-quickstart-table a,
  .v-main:has(.utopia-home-scope) .utopia-quickstart-table a {
    min-height: 0;
    padding-bottom: 6px;
    border-bottom: 0;
  }

  main:has(.utopia-home-scope) .utopia-quickstart-table p,
  .contents:has(.utopia-home-scope) .utopia-quickstart-table p,
  .page-contents:has(.utopia-home-scope) .utopia-quickstart-table p,
  .v-main:has(.utopia-home-scope) .utopia-quickstart-table p {
    min-height: 0;
    padding-top: 0;
  }
}

main:has(.utopia-home-scope) p:first-of-type,
.contents:has(.utopia-home-scope) > p:first-of-type,
.page-contents:has(.utopia-home-scope) > p:first-of-type,
.v-main:has(.utopia-home-scope) p:first-of-type {
  max-width: 760px;
  color: var(--utopia-muted);
  font-size: 18px;
}

main:has(.utopia-home-scope) table,
.contents:has(.utopia-home-scope) table,
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
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-updates-scope),
.contents:has(.utopia-updates-scope),
.page-contents:has(.utopia-updates-scope),
.v-main:has(.utopia-updates-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

main:has(.utopia-updates-scope) h1,
.contents:has(.utopia-updates-scope) h1,
.page-contents:has(.utopia-updates-scope) h1,
.v-main:has(.utopia-updates-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 6px;
}

main:has(.utopia-updates-scope) .utopia-updates-hero,
.contents:has(.utopia-updates-scope) .utopia-updates-hero,
.page-contents:has(.utopia-updates-scope) .utopia-updates-hero,
.v-main:has(.utopia-updates-scope) .utopia-updates-hero {
  max-width: 760px;
  margin: 0 0 24px;
}

main:has(.utopia-updates-scope) .utopia-updates-hero p,
.contents:has(.utopia-updates-scope) .utopia-updates-hero p,
.page-contents:has(.utopia-updates-scope) .utopia-updates-hero p,
.v-main:has(.utopia-updates-scope) .utopia-updates-hero p {
  color: var(--utopia-muted);
  font-size: 16px;
  line-height: 1.55;
  margin: 0 0 8px;
}

main:has(.utopia-updates-scope) .utopia-updates-date,
.contents:has(.utopia-updates-scope) .utopia-updates-date,
.page-contents:has(.utopia-updates-scope) .utopia-updates-date,
.v-main:has(.utopia-updates-scope) .utopia-updates-date {
  color: var(--utopia-brand-blue) !important;
  font-size: 13px !important;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  margin-top: 0 !important;
}

main:has(.utopia-updates-scope) .utopia-updates-grid,
.contents:has(.utopia-updates-scope) .utopia-updates-grid,
.page-contents:has(.utopia-updates-scope) .utopia-updates-grid,
.v-main:has(.utopia-updates-scope) .utopia-updates-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
  margin: 22px 0 18px;
}

main:has(.utopia-updates-scope) .utopia-updates-card,
.contents:has(.utopia-updates-scope) .utopia-updates-card,
.page-contents:has(.utopia-updates-scope) .utopia-updates-card,
.v-main:has(.utopia-updates-scope) .utopia-updates-card,
main:has(.utopia-updates-scope) .utopia-updates-trigger,
.contents:has(.utopia-updates-scope) .utopia-updates-trigger,
.page-contents:has(.utopia-updates-scope) .utopia-updates-trigger,
.v-main:has(.utopia-updates-scope) .utopia-updates-trigger {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

main:has(.utopia-updates-scope) .utopia-updates-wide,
.contents:has(.utopia-updates-scope) .utopia-updates-wide,
.page-contents:has(.utopia-updates-scope) .utopia-updates-wide,
.v-main:has(.utopia-updates-scope) .utopia-updates-wide,
main:has(.utopia-updates-scope) .utopia-updates-trigger,
.contents:has(.utopia-updates-scope) .utopia-updates-trigger,
.page-contents:has(.utopia-updates-scope) .utopia-updates-trigger,
.v-main:has(.utopia-updates-scope) .utopia-updates-trigger {
  margin-top: 16px;
}

main:has(.utopia-updates-scope) .utopia-updates-card h2,
.contents:has(.utopia-updates-scope) .utopia-updates-card h2,
.page-contents:has(.utopia-updates-scope) .utopia-updates-card h2,
.v-main:has(.utopia-updates-scope) .utopia-updates-card h2,
main:has(.utopia-updates-scope) .utopia-updates-trigger h2,
.contents:has(.utopia-updates-scope) .utopia-updates-trigger h2,
.page-contents:has(.utopia-updates-scope) .utopia-updates-trigger h2,
.v-main:has(.utopia-updates-scope) .utopia-updates-trigger h2 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.3;
  margin: 0 0 12px;
  padding: 0;
  border: 0;
}

main:has(.utopia-updates-scope) .utopia-updates-card ul,
.contents:has(.utopia-updates-scope) .utopia-updates-card ul,
.page-contents:has(.utopia-updates-scope) .utopia-updates-card ul,
.v-main:has(.utopia-updates-scope) .utopia-updates-card ul {
  margin: 0;
  padding-left: 18px;
}

main:has(.utopia-updates-scope) .utopia-updates-card li,
.contents:has(.utopia-updates-scope) .utopia-updates-card li,
.page-contents:has(.utopia-updates-scope) .utopia-updates-card li,
.v-main:has(.utopia-updates-scope) .utopia-updates-card li,
main:has(.utopia-updates-scope) .utopia-updates-trigger p,
.contents:has(.utopia-updates-scope) .utopia-updates-trigger p,
.page-contents:has(.utopia-updates-scope) .utopia-updates-trigger p,
.v-main:has(.utopia-updates-scope) .utopia-updates-trigger p {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.55;
}

main:has(.utopia-updates-scope) .utopia-updates-card a,
.contents:has(.utopia-updates-scope) .utopia-updates-card a,
.page-contents:has(.utopia-updates-scope) .utopia-updates-card a,
.v-main:has(.utopia-updates-scope) .utopia-updates-card a {
  color: var(--utopia-brand-blue) !important;
  font-weight: 600;
  text-decoration: none;
}

main:has(.utopia-updates-scope) .utopia-updates-card a:hover,
.contents:has(.utopia-updates-scope) .utopia-updates-card a:hover,
.page-contents:has(.utopia-updates-scope) .utopia-updates-card a:hover,
.v-main:has(.utopia-updates-scope) .utopia-updates-card a:hover {
  color: #000000 !important;
  text-decoration: none;
}

@media (max-width: 900px) {
  main:has(.utopia-updates-scope) .utopia-updates-grid,
  .contents:has(.utopia-updates-scope) .utopia-updates-grid,
  .page-contents:has(.utopia-updates-scope) .utopia-updates-grid,
  .v-main:has(.utopia-updates-scope) .utopia-updates-grid {
    grid-template-columns: 1fr;
  }
}

main:has(.utopia-overview-scope),
.contents:has(.utopia-overview-scope),
.page-contents:has(.utopia-overview-scope),
.v-main:has(.utopia-overview-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

main:has(.utopia-overview-scope) h1,
.contents:has(.utopia-overview-scope) h1,
.page-contents:has(.utopia-overview-scope) h1,
.v-main:has(.utopia-overview-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

main:has(.utopia-overview-scope) h2,
.contents:has(.utopia-overview-scope) h2,
.page-contents:has(.utopia-overview-scope) h2,
.v-main:has(.utopia-overview-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

main:has(.utopia-overview-scope) p,
main:has(.utopia-overview-scope) li,
.contents:has(.utopia-overview-scope) p,
.contents:has(.utopia-overview-scope) li,
.page-contents:has(.utopia-overview-scope) p,
.page-contents:has(.utopia-overview-scope) li,
.v-main:has(.utopia-overview-scope) p,
.v-main:has(.utopia-overview-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

main:has(.utopia-overview-scope) > p:first-of-type,
.contents:has(.utopia-overview-scope) > p:first-of-type,
.page-contents:has(.utopia-overview-scope) > p:first-of-type,
.v-main:has(.utopia-overview-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

main:has(.utopia-overview-scope) .utopia-overview-actions,
.contents:has(.utopia-overview-scope) .utopia-overview-actions,
.page-contents:has(.utopia-overview-scope) .utopia-overview-actions,
.v-main:has(.utopia-overview-scope) .utopia-overview-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

main:has(.utopia-overview-scope) .utopia-overview-actions a,
.contents:has(.utopia-overview-scope) .utopia-overview-actions a,
.page-contents:has(.utopia-overview-scope) .utopia-overview-actions a,
.v-main:has(.utopia-overview-scope) .utopia-overview-actions a {
  display: inline-flex;
  align-items: center;
  min-height: 36px;
  padding: 8px 14px;
  color: #ffffff !important;
  background: var(--utopia-brand-blue);
  border: 1px solid var(--utopia-brand-blue);
  border-radius: 6px;
  font-weight: 700;
  line-height: 1.2;
  text-decoration: none;
}

main:has(.utopia-overview-scope) .utopia-overview-actions a:hover,
.contents:has(.utopia-overview-scope) .utopia-overview-actions a:hover,
.page-contents:has(.utopia-overview-scope) .utopia-overview-actions a:hover,
.v-main:has(.utopia-overview-scope) .utopia-overview-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

main:has(.utopia-overview-scope) .utopia-overview-grid,
.contents:has(.utopia-overview-scope) .utopia-overview-grid,
.page-contents:has(.utopia-overview-scope) .utopia-overview-grid,
.v-main:has(.utopia-overview-scope) .utopia-overview-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}

main:has(.utopia-overview-scope) .utopia-overview-grid section,
.contents:has(.utopia-overview-scope) .utopia-overview-grid section,
.page-contents:has(.utopia-overview-scope) .utopia-overview-grid section,
.v-main:has(.utopia-overview-scope) .utopia-overview-grid section,
main:has(.utopia-overview-scope) .utopia-overview-next a,
.contents:has(.utopia-overview-scope) .utopia-overview-next a,
.page-contents:has(.utopia-overview-scope) .utopia-overview-next a,
.v-main:has(.utopia-overview-scope) .utopia-overview-next a {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

main:has(.utopia-overview-scope) .utopia-overview-grid h3,
.contents:has(.utopia-overview-scope) .utopia-overview-grid h3,
.page-contents:has(.utopia-overview-scope) .utopia-overview-grid h3,
.v-main:has(.utopia-overview-scope) .utopia-overview-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

main:has(.utopia-overview-scope) .utopia-overview-grid p,
.contents:has(.utopia-overview-scope) .utopia-overview-grid p,
.page-contents:has(.utopia-overview-scope) .utopia-overview-grid p,
.v-main:has(.utopia-overview-scope) .utopia-overview-grid p {
  margin: 0;
}

main:has(.utopia-overview-scope) .utopia-overview-flow,
.contents:has(.utopia-overview-scope) .utopia-overview-flow,
.page-contents:has(.utopia-overview-scope) .utopia-overview-flow,
.v-main:has(.utopia-overview-scope) .utopia-overview-flow,
main:has(.utopia-overview-scope) .utopia-overview-table,
.contents:has(.utopia-overview-scope) .utopia-overview-table,
.page-contents:has(.utopia-overview-scope) .utopia-overview-table,
.v-main:has(.utopia-overview-scope) .utopia-overview-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-overview-scope) .utopia-overview-flow div,
.contents:has(.utopia-overview-scope) .utopia-overview-flow div,
.page-contents:has(.utopia-overview-scope) .utopia-overview-flow div,
.v-main:has(.utopia-overview-scope) .utopia-overview-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-overview-scope) .utopia-overview-flow div:nth-child(odd),
.contents:has(.utopia-overview-scope) .utopia-overview-flow div:nth-child(odd),
.page-contents:has(.utopia-overview-scope) .utopia-overview-flow div:nth-child(odd),
.v-main:has(.utopia-overview-scope) .utopia-overview-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-overview-scope) .utopia-overview-flow div:last-child,
.contents:has(.utopia-overview-scope) .utopia-overview-flow div:last-child,
.page-contents:has(.utopia-overview-scope) .utopia-overview-flow div:last-child,
.v-main:has(.utopia-overview-scope) .utopia-overview-flow div:last-child {
  border-bottom: 0;
}

main:has(.utopia-overview-scope) .utopia-overview-flow strong,
.contents:has(.utopia-overview-scope) .utopia-overview-flow strong,
.page-contents:has(.utopia-overview-scope) .utopia-overview-flow strong,
.v-main:has(.utopia-overview-scope) .utopia-overview-flow strong {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 30px;
  height: 30px;
  color: #ffffff;
  background: var(--utopia-brand-blue);
  border-radius: 999px;
  font-size: 13px;
}

main:has(.utopia-overview-scope) .utopia-overview-flow span,
.contents:has(.utopia-overview-scope) .utopia-overview-flow span,
.page-contents:has(.utopia-overview-scope) .utopia-overview-flow span,
.v-main:has(.utopia-overview-scope) .utopia-overview-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

main:has(.utopia-overview-scope) .utopia-overview-table,
.contents:has(.utopia-overview-scope) .utopia-overview-table,
.page-contents:has(.utopia-overview-scope) .utopia-overview-table,
.v-main:has(.utopia-overview-scope) .utopia-overview-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

main:has(.utopia-overview-scope) .utopia-overview-head,
.contents:has(.utopia-overview-scope) .utopia-overview-head,
.page-contents:has(.utopia-overview-scope) .utopia-overview-head,
.v-main:has(.utopia-overview-scope) .utopia-overview-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

main:has(.utopia-overview-scope) .utopia-overview-table a,
main:has(.utopia-overview-scope) .utopia-overview-table p,
.contents:has(.utopia-overview-scope) .utopia-overview-table a,
.contents:has(.utopia-overview-scope) .utopia-overview-table p,
.page-contents:has(.utopia-overview-scope) .utopia-overview-table a,
.page-contents:has(.utopia-overview-scope) .utopia-overview-table p,
.v-main:has(.utopia-overview-scope) .utopia-overview-table a,
.v-main:has(.utopia-overview-scope) .utopia-overview-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-overview-scope) .utopia-overview-table > a:nth-of-type(odd),
main:has(.utopia-overview-scope) .utopia-overview-table > p:nth-of-type(odd),
.contents:has(.utopia-overview-scope) .utopia-overview-table > a:nth-of-type(odd),
.contents:has(.utopia-overview-scope) .utopia-overview-table > p:nth-of-type(odd),
.page-contents:has(.utopia-overview-scope) .utopia-overview-table > a:nth-of-type(odd),
.page-contents:has(.utopia-overview-scope) .utopia-overview-table > p:nth-of-type(odd),
.v-main:has(.utopia-overview-scope) .utopia-overview-table > a:nth-of-type(odd),
.v-main:has(.utopia-overview-scope) .utopia-overview-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-overview-scope) .utopia-overview-table a,
.contents:has(.utopia-overview-scope) .utopia-overview-table a,
.page-contents:has(.utopia-overview-scope) .utopia-overview-table a,
.v-main:has(.utopia-overview-scope) .utopia-overview-table a {
  color: var(--utopia-brand-blue) !important;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
}

main:has(.utopia-overview-scope) .utopia-overview-table a:hover,
.contents:has(.utopia-overview-scope) .utopia-overview-table a:hover,
.page-contents:has(.utopia-overview-scope) .utopia-overview-table a:hover,
.v-main:has(.utopia-overview-scope) .utopia-overview-table a:hover,
main:has(.utopia-overview-scope) .utopia-overview-next a:hover strong,
.contents:has(.utopia-overview-scope) .utopia-overview-next a:hover strong,
.page-contents:has(.utopia-overview-scope) .utopia-overview-next a:hover strong,
.v-main:has(.utopia-overview-scope) .utopia-overview-next a:hover strong {
  color: #000000 !important;
  text-decoration: none;
}

main:has(.utopia-overview-scope) .utopia-overview-next,
.contents:has(.utopia-overview-scope) .utopia-overview-next,
.page-contents:has(.utopia-overview-scope) .utopia-overview-next,
.v-main:has(.utopia-overview-scope) .utopia-overview-next {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

main:has(.utopia-overview-scope) .utopia-overview-next a,
.contents:has(.utopia-overview-scope) .utopia-overview-next a,
.page-contents:has(.utopia-overview-scope) .utopia-overview-next a,
.v-main:has(.utopia-overview-scope) .utopia-overview-next a {
  display: block;
  text-decoration: none;
}

main:has(.utopia-overview-scope) .utopia-overview-next strong,
.contents:has(.utopia-overview-scope) .utopia-overview-next strong,
.page-contents:has(.utopia-overview-scope) .utopia-overview-next strong,
.v-main:has(.utopia-overview-scope) .utopia-overview-next strong {
  display: block;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  margin-bottom: 6px;
}

main:has(.utopia-overview-scope) .utopia-overview-next span,
.contents:has(.utopia-overview-scope) .utopia-overview-next span,
.page-contents:has(.utopia-overview-scope) .utopia-overview-next span,
.v-main:has(.utopia-overview-scope) .utopia-overview-next span {
  color: var(--utopia-muted);
  font-size: 14px;
  line-height: 1.5;
}

@media (max-width: 900px) {
  main:has(.utopia-overview-scope) .utopia-overview-grid,
  .contents:has(.utopia-overview-scope) .utopia-overview-grid,
  .page-contents:has(.utopia-overview-scope) .utopia-overview-grid,
  .v-main:has(.utopia-overview-scope) .utopia-overview-grid,
  main:has(.utopia-overview-scope) .utopia-overview-next,
  .contents:has(.utopia-overview-scope) .utopia-overview-next,
  .page-contents:has(.utopia-overview-scope) .utopia-overview-next,
  .v-main:has(.utopia-overview-scope) .utopia-overview-next {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  main:has(.utopia-overview-scope) .utopia-overview-table,
  .contents:has(.utopia-overview-scope) .utopia-overview-table,
  .page-contents:has(.utopia-overview-scope) .utopia-overview-table,
  .v-main:has(.utopia-overview-scope) .utopia-overview-table {
    grid-template-columns: 1fr;
  }

  main:has(.utopia-overview-scope) .utopia-overview-head:nth-child(2),
  .contents:has(.utopia-overview-scope) .utopia-overview-head:nth-child(2),
  .page-contents:has(.utopia-overview-scope) .utopia-overview-head:nth-child(2),
  .v-main:has(.utopia-overview-scope) .utopia-overview-head:nth-child(2) {
    display: none;
  }
}

main:has(.utopia-home-scope) th,
.contents:has(.utopia-home-scope) th,
.page-contents:has(.utopia-home-scope) th,
.v-main:has(.utopia-home-scope) th {
  background: var(--utopia-surface-soft);
  color: var(--utopia-text);
  font-size: 13px;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}

main:has(.utopia-home-scope) th,
main:has(.utopia-home-scope) td,
.contents:has(.utopia-home-scope) th,
.contents:has(.utopia-home-scope) td,
.page-contents:has(.utopia-home-scope) th,
.page-contents:has(.utopia-home-scope) td,
.v-main:has(.utopia-home-scope) th,
.v-main:has(.utopia-home-scope) td {
  border-bottom: 1px solid var(--utopia-border);
  padding: 16px 18px;
  vertical-align: top;
}

main:has(.utopia-home-scope) tr:last-child td,
.contents:has(.utopia-home-scope) tr:last-child td,
.page-contents:has(.utopia-home-scope) tr:last-child td,
.v-main:has(.utopia-home-scope) tr:last-child td {
  border-bottom: 0;
}

main:has(.utopia-home-scope) code,
.contents:has(.utopia-home-scope) code,
.page-contents:has(.utopia-home-scope) code,
.v-main:has(.utopia-home-scope) code {
  color: var(--utopia-inline-code-text);
  background: var(--utopia-inline-code-bg);
  border: 1px solid var(--utopia-border);
  border-radius: 6px;
  padding: 2px 6px;
}

main:has(.utopia-home-scope) pre,
.contents:has(.utopia-home-scope) pre,
.page-contents:has(.utopia-home-scope) pre,
.v-main:has(.utopia-home-scope) pre {
  color: var(--utopia-code-text);
  background: var(--utopia-code-bg);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow-strong);
}

main:has(.utopia-home-scope) blockquote,
.contents:has(.utopia-home-scope) blockquote,
.page-contents:has(.utopia-home-scope) blockquote,
.v-main:has(.utopia-home-scope) blockquote {
  margin: 24px 0;
  padding: 18px 20px;
  background: var(--utopia-surface);
  border-left: 4px solid var(--utopia-accent);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-home-scope) hr,
.contents:has(.utopia-home-scope) hr,
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

## Content Pattern

For pages to look less basic, use this structure:

- One clear page title.
- One short intro paragraph.
- Three to six task links near the top.
- Tables for guide indexes and comparisons.
- Short sections grouped by user goal.
- Keep updates at the bottom so they do not bury the main guide.
