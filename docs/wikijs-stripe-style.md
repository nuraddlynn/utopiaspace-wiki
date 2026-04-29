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

main:has(.utopia-overview-scope) .utopia-overview-table:has(.utopia-overview-row),
.contents:has(.utopia-overview-scope) .utopia-overview-table:has(.utopia-overview-row),
.page-contents:has(.utopia-overview-scope) .utopia-overview-table:has(.utopia-overview-row),
.v-main:has(.utopia-overview-scope) .utopia-overview-table:has(.utopia-overview-row) {
  display: block;
}

main:has(.utopia-overview-scope) .utopia-overview-row,
.contents:has(.utopia-overview-scope) .utopia-overview-row,
.page-contents:has(.utopia-overview-scope) .utopia-overview-row,
.v-main:has(.utopia-overview-scope) .utopia-overview-row {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-overview-scope) .utopia-overview-row:last-child,
.contents:has(.utopia-overview-scope) .utopia-overview-row:last-child,
.page-contents:has(.utopia-overview-scope) .utopia-overview-row:last-child,
.v-main:has(.utopia-overview-scope) .utopia-overview-row:last-child {
  border-bottom: 0;
}

main:has(.utopia-overview-scope) .utopia-overview-row:nth-child(even),
.contents:has(.utopia-overview-scope) .utopia-overview-row:nth-child(even),
.page-contents:has(.utopia-overview-scope) .utopia-overview-row:nth-child(even),
.v-main:has(.utopia-overview-scope) .utopia-overview-row:nth-child(even) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-overview-scope) .utopia-overview-row > a,
main:has(.utopia-overview-scope) .utopia-overview-row > p,
.contents:has(.utopia-overview-scope) .utopia-overview-row > a,
.contents:has(.utopia-overview-scope) .utopia-overview-row > p,
.page-contents:has(.utopia-overview-scope) .utopia-overview-row > a,
.page-contents:has(.utopia-overview-scope) .utopia-overview-row > p,
.v-main:has(.utopia-overview-scope) .utopia-overview-row > a,
.v-main:has(.utopia-overview-scope) .utopia-overview-row > p {
  display: flex;
  align-items: center;
  min-height: 72px;
  border-bottom: 0 !important;
  background: transparent !important;
}

main:has(.utopia-overview-scope) .utopia-overview-row-head .utopia-overview-head,
.contents:has(.utopia-overview-scope) .utopia-overview-row-head .utopia-overview-head,
.page-contents:has(.utopia-overview-scope) .utopia-overview-row-head .utopia-overview-head,
.v-main:has(.utopia-overview-scope) .utopia-overview-row-head .utopia-overview-head {
  border-bottom: 0;
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

main:has(.utopia-login-scope),
.contents:has(.utopia-login-scope),
.page-contents:has(.utopia-login-scope),
.v-main:has(.utopia-login-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

main:has(.utopia-login-scope) h1,
.contents:has(.utopia-login-scope) h1,
.page-contents:has(.utopia-login-scope) h1,
.v-main:has(.utopia-login-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

main:has(.utopia-login-scope) h2,
.contents:has(.utopia-login-scope) h2,
.page-contents:has(.utopia-login-scope) h2,
.v-main:has(.utopia-login-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

main:has(.utopia-login-scope) p,
main:has(.utopia-login-scope) li,
.contents:has(.utopia-login-scope) p,
.contents:has(.utopia-login-scope) li,
.page-contents:has(.utopia-login-scope) p,
.page-contents:has(.utopia-login-scope) li,
.v-main:has(.utopia-login-scope) p,
.v-main:has(.utopia-login-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

main:has(.utopia-login-scope) > p:first-of-type,
.contents:has(.utopia-login-scope) > p:first-of-type,
.page-contents:has(.utopia-login-scope) > p:first-of-type,
.v-main:has(.utopia-login-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

main:has(.utopia-login-scope) .utopia-login-hero,
.contents:has(.utopia-login-scope) .utopia-login-hero,
.page-contents:has(.utopia-login-scope) .utopia-login-hero,
.v-main:has(.utopia-login-scope) .utopia-login-hero {
  display: grid;
  grid-template-columns: minmax(280px, 0.95fr) minmax(320px, 1.05fr);
  gap: 28px;
  align-items: center;
  min-height: 280px;
  margin: 8px 0 34px;
  padding-bottom: 28px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-login-scope) .utopia-login-copy p,
.contents:has(.utopia-login-scope) .utopia-login-copy p,
.page-contents:has(.utopia-login-scope) .utopia-login-copy p,
.v-main:has(.utopia-login-scope) .utopia-login-copy p {
  max-width: 540px;
  color: var(--utopia-muted);
  font-size: 20px;
  line-height: 1.55;
  margin: 0;
}

main:has(.utopia-login-scope) .utopia-login-copy pre,
.contents:has(.utopia-login-scope) .utopia-login-copy pre,
.page-contents:has(.utopia-login-scope) .utopia-login-copy pre,
.v-main:has(.utopia-login-scope) .utopia-login-copy pre {
  display: none !important;
}

main:has(.utopia-login-scope) .utopia-login-visual,
.contents:has(.utopia-login-scope) .utopia-login-visual,
.page-contents:has(.utopia-login-scope) .utopia-login-visual,
.v-main:has(.utopia-login-scope) .utopia-login-visual {
  position: relative;
  min-height: 380px;
  overflow: hidden;
}

main:has(.utopia-login-scope) .utopia-login-image,
.contents:has(.utopia-login-scope) .utopia-login-image,
.page-contents:has(.utopia-login-scope) .utopia-login-image,
.v-main:has(.utopia-login-scope) .utopia-login-image {
  position: absolute;
  display: block;
  width: min(440px, 72%);
  height: auto;
  aspect-ratio: 1366 / 768;
  object-fit: cover;
  padding: 0;
  overflow: hidden;
  background-color: var(--utopia-surface);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border: 1px solid var(--utopia-border);
  border-radius: 10px;
  box-shadow: 0 22px 55px rgba(10, 37, 64, 0.16);
}

.theme--dark.v-application main:has(.utopia-login-scope) .utopia-login-image,
body.theme--dark main:has(.utopia-login-scope) .utopia-login-image,
html.theme--dark main:has(.utopia-login-scope) .utopia-login-image {
  background-color: var(--utopia-surface);
  box-shadow: 0 22px 55px rgba(0, 0, 0, 0.32);
}

main:has(.utopia-login-scope) .utopia-login-image::before,
.contents:has(.utopia-login-scope) .utopia-login-image::before,
.page-contents:has(.utopia-login-scope) .utopia-login-image::before,
.v-main:has(.utopia-login-scope) .utopia-login-image::before {
  display: none;
}

main:has(.utopia-login-scope) .utopia-login-image::after,
.contents:has(.utopia-login-scope) .utopia-login-image::after,
.page-contents:has(.utopia-login-scope) .utopia-login-image::after,
.v-main:has(.utopia-login-scope) .utopia-login-image::after {
  display: none;
}

main:has(.utopia-login-scope) .utopia-login-image-back,
.contents:has(.utopia-login-scope) .utopia-login-image-back,
.page-contents:has(.utopia-login-scope) .utopia-login-image-back,
.v-main:has(.utopia-login-scope) .utopia-login-image-back {
  top: 24px;
  left: clamp(0px, 4%, 28px);
  right: auto;
  z-index: 1;
  background-image: url("/assets/login/login-dark.jpeg");
}

main:has(.utopia-login-scope) .utopia-login-image-front,
.contents:has(.utopia-login-scope) .utopia-login-image-front,
.page-contents:has(.utopia-login-scope) .utopia-login-image-front,
.v-main:has(.utopia-login-scope) .utopia-login-image-front {
  top: 118px;
  left: clamp(80px, 22%, 150px);
  right: auto;
  z-index: 2;
  transform: none;
  background-image: url("/assets/login/login-light.jpeg");
}

main:has(.utopia-login-scope) .utopia-login-image span,
main:has(.utopia-login-scope) .utopia-login-image strong,
main:has(.utopia-login-scope) .utopia-login-image small,
.contents:has(.utopia-login-scope) .utopia-login-image span,
.contents:has(.utopia-login-scope) .utopia-login-image strong,
.contents:has(.utopia-login-scope) .utopia-login-image small,
.page-contents:has(.utopia-login-scope) .utopia-login-image span,
.page-contents:has(.utopia-login-scope) .utopia-login-image strong,
.page-contents:has(.utopia-login-scope) .utopia-login-image small,
.v-main:has(.utopia-login-scope) .utopia-login-image span,
.v-main:has(.utopia-login-scope) .utopia-login-image strong,
.v-main:has(.utopia-login-scope) .utopia-login-image small {
  display: none !important;
}

main:has(.utopia-login-scope) .utopia-login-actions,
.contents:has(.utopia-login-scope) .utopia-login-actions,
.page-contents:has(.utopia-login-scope) .utopia-login-actions,
.v-main:has(.utopia-login-scope) .utopia-login-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  max-width: none;
  margin: 20px 0 28px;
}

main:has(.utopia-login-scope) .utopia-login-actions a,
.contents:has(.utopia-login-scope) .utopia-login-actions a,
.page-contents:has(.utopia-login-scope) .utopia-login-actions a,
.v-main:has(.utopia-login-scope) .utopia-login-actions a {
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

main:has(.utopia-login-scope) .utopia-login-actions a:hover,
.contents:has(.utopia-login-scope) .utopia-login-actions a:hover,
.page-contents:has(.utopia-login-scope) .utopia-login-actions a:hover,
.v-main:has(.utopia-login-scope) .utopia-login-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

main:has(.utopia-login-scope) .utopia-login-flow,
.contents:has(.utopia-login-scope) .utopia-login-flow,
.page-contents:has(.utopia-login-scope) .utopia-login-flow,
.v-main:has(.utopia-login-scope) .utopia-login-flow,
main:has(.utopia-login-scope) .utopia-login-table,
.contents:has(.utopia-login-scope) .utopia-login-table,
.page-contents:has(.utopia-login-scope) .utopia-login-table,
.v-main:has(.utopia-login-scope) .utopia-login-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-login-scope) .utopia-login-flow div,
.contents:has(.utopia-login-scope) .utopia-login-flow div,
.page-contents:has(.utopia-login-scope) .utopia-login-flow div,
.v-main:has(.utopia-login-scope) .utopia-login-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-login-scope) .utopia-login-flow div:nth-child(odd),
.contents:has(.utopia-login-scope) .utopia-login-flow div:nth-child(odd),
.page-contents:has(.utopia-login-scope) .utopia-login-flow div:nth-child(odd),
.v-main:has(.utopia-login-scope) .utopia-login-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-login-scope) .utopia-login-flow div:last-child,
.contents:has(.utopia-login-scope) .utopia-login-flow div:last-child,
.page-contents:has(.utopia-login-scope) .utopia-login-flow div:last-child,
.v-main:has(.utopia-login-scope) .utopia-login-flow div:last-child {
  border-bottom: 0;
}

main:has(.utopia-login-scope) .utopia-login-flow strong,
.contents:has(.utopia-login-scope) .utopia-login-flow strong,
.page-contents:has(.utopia-login-scope) .utopia-login-flow strong,
.v-main:has(.utopia-login-scope) .utopia-login-flow strong {
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

main:has(.utopia-login-scope) .utopia-login-flow span,
.contents:has(.utopia-login-scope) .utopia-login-flow span,
.page-contents:has(.utopia-login-scope) .utopia-login-flow span,
.v-main:has(.utopia-login-scope) .utopia-login-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

main:has(.utopia-login-scope) .utopia-login-flow a,
.contents:has(.utopia-login-scope) .utopia-login-flow a,
.page-contents:has(.utopia-login-scope) .utopia-login-flow a,
.v-main:has(.utopia-login-scope) .utopia-login-flow a {
  color: var(--utopia-brand-blue) !important;
  font-weight: 600;
  text-decoration: none;
}

main:has(.utopia-login-scope) .utopia-login-grid,
.contents:has(.utopia-login-scope) .utopia-login-grid,
.page-contents:has(.utopia-login-scope) .utopia-login-grid,
.v-main:has(.utopia-login-scope) .utopia-login-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

main:has(.utopia-login-scope) .utopia-login-grid section,
.contents:has(.utopia-login-scope) .utopia-login-grid section,
.page-contents:has(.utopia-login-scope) .utopia-login-grid section,
.v-main:has(.utopia-login-scope) .utopia-login-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

main:has(.utopia-login-scope) .utopia-login-grid h3,
.contents:has(.utopia-login-scope) .utopia-login-grid h3,
.page-contents:has(.utopia-login-scope) .utopia-login-grid h3,
.v-main:has(.utopia-login-scope) .utopia-login-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

main:has(.utopia-login-scope) .utopia-login-grid p,
.contents:has(.utopia-login-scope) .utopia-login-grid p,
.page-contents:has(.utopia-login-scope) .utopia-login-grid p,
.v-main:has(.utopia-login-scope) .utopia-login-grid p {
  margin: 0;
}

main:has(.utopia-login-scope) .utopia-login-table,
.contents:has(.utopia-login-scope) .utopia-login-table,
.page-contents:has(.utopia-login-scope) .utopia-login-table,
.v-main:has(.utopia-login-scope) .utopia-login-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

main:has(.utopia-login-scope) .utopia-login-head,
.contents:has(.utopia-login-scope) .utopia-login-head,
.page-contents:has(.utopia-login-scope) .utopia-login-head,
.v-main:has(.utopia-login-scope) .utopia-login-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

main:has(.utopia-login-scope) .utopia-login-table strong,
main:has(.utopia-login-scope) .utopia-login-table p,
.contents:has(.utopia-login-scope) .utopia-login-table strong,
.contents:has(.utopia-login-scope) .utopia-login-table p,
.page-contents:has(.utopia-login-scope) .utopia-login-table strong,
.page-contents:has(.utopia-login-scope) .utopia-login-table p,
.v-main:has(.utopia-login-scope) .utopia-login-table strong,
.v-main:has(.utopia-login-scope) .utopia-login-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-login-scope) .utopia-login-table > strong:nth-of-type(odd),
main:has(.utopia-login-scope) .utopia-login-table > p:nth-of-type(odd),
.contents:has(.utopia-login-scope) .utopia-login-table > strong:nth-of-type(odd),
.contents:has(.utopia-login-scope) .utopia-login-table > p:nth-of-type(odd),
.page-contents:has(.utopia-login-scope) .utopia-login-table > strong:nth-of-type(odd),
.page-contents:has(.utopia-login-scope) .utopia-login-table > p:nth-of-type(odd),
.v-main:has(.utopia-login-scope) .utopia-login-table > strong:nth-of-type(odd),
.v-main:has(.utopia-login-scope) .utopia-login-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-login-scope) .utopia-login-table strong,
.contents:has(.utopia-login-scope) .utopia-login-table strong,
.page-contents:has(.utopia-login-scope) .utopia-login-table strong,
.v-main:has(.utopia-login-scope) .utopia-login-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-text);
  font-size: 15px;
  font-weight: 600;
  line-height: 1.35;
}

main:has(.utopia-login-scope) .utopia-login-table p,
.contents:has(.utopia-login-scope) .utopia-login-table p,
.page-contents:has(.utopia-login-scope) .utopia-login-table p,
.v-main:has(.utopia-login-scope) .utopia-login-table p {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

main:has(.utopia-login-scope) .utopia-login-table strong::before,
main:has(.utopia-login-scope) .utopia-login-table strong::after,
.contents:has(.utopia-login-scope) .utopia-login-table strong::before,
.contents:has(.utopia-login-scope) .utopia-login-table strong::after,
.page-contents:has(.utopia-login-scope) .utopia-login-table strong::before,
.page-contents:has(.utopia-login-scope) .utopia-login-table strong::after,
.v-main:has(.utopia-login-scope) .utopia-login-table strong::before,
.v-main:has(.utopia-login-scope) .utopia-login-table strong::after {
  display: none !important;
}

@media (max-width: 900px) {
  main:has(.utopia-login-scope) .utopia-login-hero,
  .contents:has(.utopia-login-scope) .utopia-login-hero,
  .page-contents:has(.utopia-login-scope) .utopia-login-hero,
  .v-main:has(.utopia-login-scope) .utopia-login-hero {
    grid-template-columns: 1fr;
  }

  main:has(.utopia-login-scope) .utopia-login-visual,
  .contents:has(.utopia-login-scope) .utopia-login-visual,
  .page-contents:has(.utopia-login-scope) .utopia-login-visual,
  .v-main:has(.utopia-login-scope) .utopia-login-visual {
    min-height: 300px;
  }

  main:has(.utopia-login-scope) .utopia-login-image,
  .contents:has(.utopia-login-scope) .utopia-login-image,
  .page-contents:has(.utopia-login-scope) .utopia-login-image,
  .v-main:has(.utopia-login-scope) .utopia-login-image {
    width: min(400px, 74%);
  }

  main:has(.utopia-login-scope) .utopia-login-image-front,
  .contents:has(.utopia-login-scope) .utopia-login-image-front,
  .page-contents:has(.utopia-login-scope) .utopia-login-image-front,
  .v-main:has(.utopia-login-scope) .utopia-login-image-front {
    top: 96px;
    left: clamp(72px, 20%, 120px);
  }

  main:has(.utopia-login-scope) .utopia-login-grid,
  .contents:has(.utopia-login-scope) .utopia-login-grid,
  .page-contents:has(.utopia-login-scope) .utopia-login-grid,
  .v-main:has(.utopia-login-scope) .utopia-login-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  main:has(.utopia-login-scope) .utopia-login-table,
  .contents:has(.utopia-login-scope) .utopia-login-table,
  .page-contents:has(.utopia-login-scope) .utopia-login-table,
  .v-main:has(.utopia-login-scope) .utopia-login-table {
    grid-template-columns: 1fr;
  }

  main:has(.utopia-login-scope) .utopia-login-head:nth-child(2),
  .contents:has(.utopia-login-scope) .utopia-login-head:nth-child(2),
  .page-contents:has(.utopia-login-scope) .utopia-login-head:nth-child(2),
  .v-main:has(.utopia-login-scope) .utopia-login-head:nth-child(2) {
    display: none;
  }
}

main:has(.utopia-navigation-scope),
.contents:has(.utopia-navigation-scope),
.page-contents:has(.utopia-navigation-scope),
.v-main:has(.utopia-navigation-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

main:has(.utopia-navigation-scope) h1,
.contents:has(.utopia-navigation-scope) h1,
.page-contents:has(.utopia-navigation-scope) h1,
.v-main:has(.utopia-navigation-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

main:has(.utopia-navigation-scope) h2,
.contents:has(.utopia-navigation-scope) h2,
.page-contents:has(.utopia-navigation-scope) h2,
.v-main:has(.utopia-navigation-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

main:has(.utopia-navigation-scope) p,
main:has(.utopia-navigation-scope) li,
.contents:has(.utopia-navigation-scope) p,
.contents:has(.utopia-navigation-scope) li,
.page-contents:has(.utopia-navigation-scope) p,
.page-contents:has(.utopia-navigation-scope) li,
.v-main:has(.utopia-navigation-scope) p,
.v-main:has(.utopia-navigation-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

main:has(.utopia-navigation-scope) > p:first-of-type,
.contents:has(.utopia-navigation-scope) > p:first-of-type,
.page-contents:has(.utopia-navigation-scope) > p:first-of-type,
.v-main:has(.utopia-navigation-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

main:has(.utopia-navigation-scope) .utopia-navigation-actions,
.contents:has(.utopia-navigation-scope) .utopia-navigation-actions,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-actions,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

main:has(.utopia-navigation-scope) .utopia-navigation-actions a,
.contents:has(.utopia-navigation-scope) .utopia-navigation-actions a,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-actions a,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-actions a {
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

main:has(.utopia-navigation-scope) .utopia-navigation-actions a:hover,
.contents:has(.utopia-navigation-scope) .utopia-navigation-actions a:hover,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-actions a:hover,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

main:has(.utopia-navigation-scope) .utopia-navigation-grid,
.contents:has(.utopia-navigation-scope) .utopia-navigation-grid,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-grid,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

main:has(.utopia-navigation-scope) .utopia-navigation-grid section,
.contents:has(.utopia-navigation-scope) .utopia-navigation-grid section,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-grid section,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

main:has(.utopia-navigation-scope) .utopia-navigation-grid h3,
.contents:has(.utopia-navigation-scope) .utopia-navigation-grid h3,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-grid h3,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

main:has(.utopia-navigation-scope) .utopia-navigation-grid p,
.contents:has(.utopia-navigation-scope) .utopia-navigation-grid p,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-grid p,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-grid p {
  margin: 0;
}

main:has(.utopia-navigation-scope) .utopia-navigation-flow,
.contents:has(.utopia-navigation-scope) .utopia-navigation-flow,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-flow,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-flow,
main:has(.utopia-navigation-scope) .utopia-navigation-table,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-navigation-scope) .utopia-navigation-flow div,
.contents:has(.utopia-navigation-scope) .utopia-navigation-flow div,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-flow div,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-navigation-scope) .utopia-navigation-flow div:nth-child(odd),
.contents:has(.utopia-navigation-scope) .utopia-navigation-flow div:nth-child(odd),
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-flow div:nth-child(odd),
.v-main:has(.utopia-navigation-scope) .utopia-navigation-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-navigation-scope) .utopia-navigation-flow div:last-child,
.contents:has(.utopia-navigation-scope) .utopia-navigation-flow div:last-child,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-flow div:last-child,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-flow div:last-child {
  border-bottom: 0;
}

main:has(.utopia-navigation-scope) .utopia-navigation-flow strong,
.contents:has(.utopia-navigation-scope) .utopia-navigation-flow strong,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-flow strong,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-flow strong {
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

main:has(.utopia-navigation-scope) .utopia-navigation-flow span,
.contents:has(.utopia-navigation-scope) .utopia-navigation-flow span,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-flow span,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

main:has(.utopia-navigation-scope) .utopia-navigation-table,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

main:has(.utopia-navigation-scope) .utopia-navigation-head,
.contents:has(.utopia-navigation-scope) .utopia-navigation-head,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-head,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

main:has(.utopia-navigation-scope) .utopia-navigation-table a,
main:has(.utopia-navigation-scope) .utopia-navigation-table strong,
main:has(.utopia-navigation-scope) .utopia-navigation-table p,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table a,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table strong,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table p,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table a,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table strong,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table p,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table a,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table strong,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-navigation-scope) .utopia-navigation-table > a:nth-of-type(odd),
main:has(.utopia-navigation-scope) .utopia-navigation-table > strong:nth-of-type(odd),
main:has(.utopia-navigation-scope) .utopia-navigation-table > p:nth-of-type(odd),
.contents:has(.utopia-navigation-scope) .utopia-navigation-table > a:nth-of-type(odd),
.contents:has(.utopia-navigation-scope) .utopia-navigation-table > strong:nth-of-type(odd),
.contents:has(.utopia-navigation-scope) .utopia-navigation-table > p:nth-of-type(odd),
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table > a:nth-of-type(odd),
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table > strong:nth-of-type(odd),
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table > p:nth-of-type(odd),
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table > a:nth-of-type(odd),
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table > strong:nth-of-type(odd),
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-navigation-scope) .utopia-navigation-table a,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table a,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table a,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table a {
  color: var(--utopia-brand-blue) !important;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
}

main:has(.utopia-navigation-scope) .utopia-navigation-table strong,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table strong,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table strong,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-text);
  font-size: 15px;
  font-weight: 600;
  line-height: 1.35;
}

main:has(.utopia-navigation-scope) .utopia-navigation-table a:hover,
.contents:has(.utopia-navigation-scope) .utopia-navigation-table a:hover,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table a:hover,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table a:hover {
  color: #000000 !important;
  text-decoration: none;
}

main:has(.utopia-navigation-scope) .utopia-navigation-table:has(.utopia-navigation-row),
.contents:has(.utopia-navigation-scope) .utopia-navigation-table:has(.utopia-navigation-row),
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-table:has(.utopia-navigation-row),
.v-main:has(.utopia-navigation-scope) .utopia-navigation-table:has(.utopia-navigation-row) {
  display: block;
}

main:has(.utopia-navigation-scope) .utopia-navigation-row,
.contents:has(.utopia-navigation-scope) .utopia-navigation-row,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-navigation-scope) .utopia-navigation-row:last-child,
.contents:has(.utopia-navigation-scope) .utopia-navigation-row:last-child,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row:last-child,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row:last-child {
  border-bottom: 0;
}

main:has(.utopia-navigation-scope) .utopia-navigation-row:nth-child(even),
.contents:has(.utopia-navigation-scope) .utopia-navigation-row:nth-child(even),
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row:nth-child(even),
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row:nth-child(even) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-navigation-scope) .utopia-navigation-row > a,
main:has(.utopia-navigation-scope) .utopia-navigation-row > strong,
main:has(.utopia-navigation-scope) .utopia-navigation-row > p,
.contents:has(.utopia-navigation-scope) .utopia-navigation-row > a,
.contents:has(.utopia-navigation-scope) .utopia-navigation-row > strong,
.contents:has(.utopia-navigation-scope) .utopia-navigation-row > p,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row > a,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row > strong,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row > p,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row > a,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row > strong,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row > p {
  display: flex;
  align-items: center;
  min-height: 72px;
  border-bottom: 0 !important;
  background: transparent !important;
}

main:has(.utopia-navigation-scope) .utopia-navigation-row-head .utopia-navigation-head,
.contents:has(.utopia-navigation-scope) .utopia-navigation-row-head .utopia-navigation-head,
.page-contents:has(.utopia-navigation-scope) .utopia-navigation-row-head .utopia-navigation-head,
.v-main:has(.utopia-navigation-scope) .utopia-navigation-row-head .utopia-navigation-head {
  border-bottom: 0;
}

@media (max-width: 900px) {
  main:has(.utopia-navigation-scope) .utopia-navigation-grid,
  .contents:has(.utopia-navigation-scope) .utopia-navigation-grid,
  .page-contents:has(.utopia-navigation-scope) .utopia-navigation-grid,
  .v-main:has(.utopia-navigation-scope) .utopia-navigation-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  main:has(.utopia-navigation-scope) .utopia-navigation-table,
  .contents:has(.utopia-navigation-scope) .utopia-navigation-table,
  .page-contents:has(.utopia-navigation-scope) .utopia-navigation-table,
  .v-main:has(.utopia-navigation-scope) .utopia-navigation-table {
    grid-template-columns: 1fr;
  }

  main:has(.utopia-navigation-scope) .utopia-navigation-head:nth-child(2),
  .contents:has(.utopia-navigation-scope) .utopia-navigation-head:nth-child(2),
  .page-contents:has(.utopia-navigation-scope) .utopia-navigation-head:nth-child(2),
  .v-main:has(.utopia-navigation-scope) .utopia-navigation-head:nth-child(2) {
    display: none;
  }
}

main:has(.utopia-personal-scope),
.contents:has(.utopia-personal-scope),
.page-contents:has(.utopia-personal-scope),
.v-main:has(.utopia-personal-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

main:has(.utopia-personal-scope) h1,
.contents:has(.utopia-personal-scope) h1,
.page-contents:has(.utopia-personal-scope) h1,
.v-main:has(.utopia-personal-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

main:has(.utopia-personal-scope) h2,
.contents:has(.utopia-personal-scope) h2,
.page-contents:has(.utopia-personal-scope) h2,
.v-main:has(.utopia-personal-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

main:has(.utopia-personal-scope) p,
main:has(.utopia-personal-scope) li,
.contents:has(.utopia-personal-scope) p,
.contents:has(.utopia-personal-scope) li,
.page-contents:has(.utopia-personal-scope) p,
.page-contents:has(.utopia-personal-scope) li,
.v-main:has(.utopia-personal-scope) p,
.v-main:has(.utopia-personal-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

main:has(.utopia-personal-scope) > p:first-of-type,
.contents:has(.utopia-personal-scope) > p:first-of-type,
.page-contents:has(.utopia-personal-scope) > p:first-of-type,
.v-main:has(.utopia-personal-scope) > p:first-of-type {
  max-width: 760px;
  font-size: 18px;
}

main:has(.utopia-personal-scope) .utopia-personal-actions,
.contents:has(.utopia-personal-scope) .utopia-personal-actions,
.page-contents:has(.utopia-personal-scope) .utopia-personal-actions,
.v-main:has(.utopia-personal-scope) .utopia-personal-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

main:has(.utopia-personal-scope) .utopia-personal-actions a,
.contents:has(.utopia-personal-scope) .utopia-personal-actions a,
.page-contents:has(.utopia-personal-scope) .utopia-personal-actions a,
.v-main:has(.utopia-personal-scope) .utopia-personal-actions a {
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

main:has(.utopia-personal-scope) .utopia-personal-actions a:hover,
.contents:has(.utopia-personal-scope) .utopia-personal-actions a:hover,
.page-contents:has(.utopia-personal-scope) .utopia-personal-actions a:hover,
.v-main:has(.utopia-personal-scope) .utopia-personal-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

main:has(.utopia-personal-scope) .utopia-personal-grid,
.contents:has(.utopia-personal-scope) .utopia-personal-grid,
.page-contents:has(.utopia-personal-scope) .utopia-personal-grid,
.v-main:has(.utopia-personal-scope) .utopia-personal-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

main:has(.utopia-personal-scope) .utopia-personal-grid section,
.contents:has(.utopia-personal-scope) .utopia-personal-grid section,
.page-contents:has(.utopia-personal-scope) .utopia-personal-grid section,
.v-main:has(.utopia-personal-scope) .utopia-personal-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

main:has(.utopia-personal-scope) .utopia-personal-grid h3,
.contents:has(.utopia-personal-scope) .utopia-personal-grid h3,
.page-contents:has(.utopia-personal-scope) .utopia-personal-grid h3,
.v-main:has(.utopia-personal-scope) .utopia-personal-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

main:has(.utopia-personal-scope) .utopia-personal-grid p,
.contents:has(.utopia-personal-scope) .utopia-personal-grid p,
.page-contents:has(.utopia-personal-scope) .utopia-personal-grid p,
.v-main:has(.utopia-personal-scope) .utopia-personal-grid p {
  margin: 0;
}

main:has(.utopia-personal-scope) .utopia-personal-flow,
.contents:has(.utopia-personal-scope) .utopia-personal-flow,
.page-contents:has(.utopia-personal-scope) .utopia-personal-flow,
.v-main:has(.utopia-personal-scope) .utopia-personal-flow,
main:has(.utopia-personal-scope) .utopia-personal-table,
.contents:has(.utopia-personal-scope) .utopia-personal-table,
.page-contents:has(.utopia-personal-scope) .utopia-personal-table,
.v-main:has(.utopia-personal-scope) .utopia-personal-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

main:has(.utopia-personal-scope) .utopia-personal-flow div,
.contents:has(.utopia-personal-scope) .utopia-personal-flow div,
.page-contents:has(.utopia-personal-scope) .utopia-personal-flow div,
.v-main:has(.utopia-personal-scope) .utopia-personal-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-personal-scope) .utopia-personal-flow div:nth-child(odd),
.contents:has(.utopia-personal-scope) .utopia-personal-flow div:nth-child(odd),
.page-contents:has(.utopia-personal-scope) .utopia-personal-flow div:nth-child(odd),
.v-main:has(.utopia-personal-scope) .utopia-personal-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-personal-scope) .utopia-personal-flow div:last-child,
.contents:has(.utopia-personal-scope) .utopia-personal-flow div:last-child,
.page-contents:has(.utopia-personal-scope) .utopia-personal-flow div:last-child,
.v-main:has(.utopia-personal-scope) .utopia-personal-flow div:last-child {
  border-bottom: 0;
}

main:has(.utopia-personal-scope) .utopia-personal-flow strong,
.contents:has(.utopia-personal-scope) .utopia-personal-flow strong,
.page-contents:has(.utopia-personal-scope) .utopia-personal-flow strong,
.v-main:has(.utopia-personal-scope) .utopia-personal-flow strong {
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

main:has(.utopia-personal-scope) .utopia-personal-flow span,
.contents:has(.utopia-personal-scope) .utopia-personal-flow span,
.page-contents:has(.utopia-personal-scope) .utopia-personal-flow span,
.v-main:has(.utopia-personal-scope) .utopia-personal-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

main:has(.utopia-personal-scope) .utopia-personal-table,
.contents:has(.utopia-personal-scope) .utopia-personal-table,
.page-contents:has(.utopia-personal-scope) .utopia-personal-table,
.v-main:has(.utopia-personal-scope) .utopia-personal-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

main:has(.utopia-personal-scope) .utopia-personal-head,
.contents:has(.utopia-personal-scope) .utopia-personal-head,
.page-contents:has(.utopia-personal-scope) .utopia-personal-head,
.v-main:has(.utopia-personal-scope) .utopia-personal-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

main:has(.utopia-personal-scope) .utopia-personal-table strong,
main:has(.utopia-personal-scope) .utopia-personal-table p,
.contents:has(.utopia-personal-scope) .utopia-personal-table strong,
.contents:has(.utopia-personal-scope) .utopia-personal-table p,
.page-contents:has(.utopia-personal-scope) .utopia-personal-table strong,
.page-contents:has(.utopia-personal-scope) .utopia-personal-table p,
.v-main:has(.utopia-personal-scope) .utopia-personal-table strong,
.v-main:has(.utopia-personal-scope) .utopia-personal-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

main:has(.utopia-personal-scope) .utopia-personal-table > strong:nth-of-type(odd),
main:has(.utopia-personal-scope) .utopia-personal-table > p:nth-of-type(odd),
.contents:has(.utopia-personal-scope) .utopia-personal-table > strong:nth-of-type(odd),
.contents:has(.utopia-personal-scope) .utopia-personal-table > p:nth-of-type(odd),
.page-contents:has(.utopia-personal-scope) .utopia-personal-table > strong:nth-of-type(odd),
.page-contents:has(.utopia-personal-scope) .utopia-personal-table > p:nth-of-type(odd),
.v-main:has(.utopia-personal-scope) .utopia-personal-table > strong:nth-of-type(odd),
.v-main:has(.utopia-personal-scope) .utopia-personal-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

main:has(.utopia-personal-scope) .utopia-personal-table strong,
.contents:has(.utopia-personal-scope) .utopia-personal-table strong,
.page-contents:has(.utopia-personal-scope) .utopia-personal-table strong,
.v-main:has(.utopia-personal-scope) .utopia-personal-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  main:has(.utopia-personal-scope) .utopia-personal-grid,
  .contents:has(.utopia-personal-scope) .utopia-personal-grid,
  .page-contents:has(.utopia-personal-scope) .utopia-personal-grid,
  .v-main:has(.utopia-personal-scope) .utopia-personal-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  main:has(.utopia-personal-scope) .utopia-personal-table,
  .contents:has(.utopia-personal-scope) .utopia-personal-table,
  .page-contents:has(.utopia-personal-scope) .utopia-personal-table,
  .v-main:has(.utopia-personal-scope) .utopia-personal-table {
    grid-template-columns: 1fr;
  }

  main:has(.utopia-personal-scope) .utopia-personal-head:nth-child(2),
  .contents:has(.utopia-personal-scope) .utopia-personal-head:nth-child(2),
  .page-contents:has(.utopia-personal-scope) .utopia-personal-head:nth-child(2),
  .v-main:has(.utopia-personal-scope) .utopia-personal-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-announcements-scope) .utopia-announcements-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-calendar-scope) .utopia-calendar-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-meeting-scope) .utopia-meeting-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-taskboard-scope) .utopia-taskboard-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-manager-scope) .utopia-manager-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-director-scope) .utopia-director-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-supervisor-scope) .utopia-supervisor-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-hr-scope) .utopia-hr-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-account-scope) .utopia-account-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-credit-scope) .utopia-credit-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-oe-scope) .utopia-oe-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-indoor-scope) .utopia-indoor-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-developer-scope) .utopia-developer-head:nth-child(2) {
    display: none;
  }
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) {
  background: var(--utopia-page-bg);
  color: var(--utopia-text);
  padding: 28px;
  border-radius: 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) h1 {
  color: var(--utopia-text);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0;
  margin-bottom: 10px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) h2 {
  color: var(--utopia-text);
  border-top: 1px solid var(--utopia-border);
  font-size: 22px;
  line-height: 1.3;
  margin-top: 34px;
  margin-bottom: 16px;
  padding-top: 26px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) p,
:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) li {
  color: var(--utopia-muted);
  font-size: 15px;
  line-height: 1.6;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) > p:first-of-type {
  max-width: 780px;
  font-size: 18px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0 28px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-actions a {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-actions a:hover {
  background: var(--utopia-brand-blue-hover);
  border-color: var(--utopia-brand-blue-hover);
  text-decoration: none;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-grid section {
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
  padding: 18px 20px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-grid h3 {
  color: var(--utopia-text);
  font-size: 16px;
  line-height: 1.35;
  margin: 0 0 8px;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-grid p {
  margin: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-flow,
:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table {
  overflow: hidden;
  background: var(--utopia-surface);
  border: 1px solid var(--utopia-border);
  border-radius: 8px;
  box-shadow: var(--utopia-shadow);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-flow div {
  display: grid;
  grid-template-columns: 44px 1fr;
  gap: 14px;
  align-items: center;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-flow div:nth-child(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-flow div:last-child {
  border-bottom: 0;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-flow strong {
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

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-flow span {
  color: var(--utopia-text);
  font-size: 15px;
  line-height: 1.5;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table {
  display: grid;
  grid-template-columns: minmax(190px, 34%) 1fr;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-head {
  color: var(--utopia-muted);
  background: transparent;
  border-bottom: 1px solid var(--utopia-border);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.04em;
  padding: 14px 20px;
  text-transform: uppercase;
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table strong,
:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table p {
  margin: 0;
  padding: 16px 20px;
  border-bottom: 1px solid var(--utopia-border);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table > strong:nth-of-type(odd),
:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table > p:nth-of-type(odd) {
  background: var(--utopia-row-soft);
}

:is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table strong {
  display: flex;
  align-items: center;
  color: var(--utopia-brand-blue);
  font-size: 15px;
  font-weight: 700;
  line-height: 1.35;
}

@media (max-width: 900px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  :is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-table {
    grid-template-columns: 1fr;
  }

  :is(main, .contents, .page-contents, .v-main):has(.utopia-user-management-scope) .utopia-user-management-head:nth-child(2) {
    display: none;
  }
}

:is(
  .utopia-quickstart-table,
  .utopia-overview-table,
  .utopia-login-table,
  .utopia-navigation-table,
  .utopia-personal-table,
  .utopia-announcements-table,
  .utopia-calendar-table,
  .utopia-meeting-table,
  .utopia-taskboard-table,
  .utopia-manager-table,
  .utopia-director-table,
  .utopia-supervisor-table,
  .utopia-hr-table,
  .utopia-account-table,
  .utopia-credit-table,
  .utopia-oe-table,
  .utopia-indoor-table,
  .utopia-developer-table,
  .utopia-user-management-table
) > :is(a, strong, p) {
  width: 100%;
  box-sizing: border-box;
  align-self: stretch;
}

:is(
  .utopia-quickstart-table,
  .utopia-overview-table,
  .utopia-navigation-table,
  .utopia-personal-table,
  .utopia-announcements-table,
  .utopia-calendar-table,
  .utopia-meeting-table,
  .utopia-taskboard-table,
  .utopia-manager-table,
  .utopia-director-table,
  .utopia-supervisor-table,
  .utopia-hr-table,
  .utopia-account-table,
  .utopia-credit-table,
  .utopia-oe-table,
  .utopia-indoor-table,
  .utopia-developer-table,
  .utopia-user-management-table
) > :is(a, strong) {
  display: flex;
  align-items: center;
}

:is(
  .utopia-quickstart-table,
  .utopia-overview-table,
  .utopia-navigation-table,
  .utopia-personal-table,
  .utopia-announcements-table,
  .utopia-calendar-table,
  .utopia-meeting-table,
  .utopia-taskboard-table,
  .utopia-manager-table,
  .utopia-director-table,
  .utopia-supervisor-table,
  .utopia-hr-table,
  .utopia-account-table,
  .utopia-credit-table,
  .utopia-oe-table,
  .utopia-indoor-table,
  .utopia-developer-table,
  .utopia-user-management-table
) > :is(a, strong)::before,
:is(
  .utopia-quickstart-table,
  .utopia-overview-table,
  .utopia-navigation-table,
  .utopia-personal-table,
  .utopia-announcements-table,
  .utopia-calendar-table,
  .utopia-meeting-table,
  .utopia-taskboard-table,
  .utopia-manager-table,
  .utopia-director-table,
  .utopia-supervisor-table,
  .utopia-hr-table,
  .utopia-account-table,
  .utopia-credit-table,
  .utopia-oe-table,
  .utopia-indoor-table,
  .utopia-developer-table,
  .utopia-user-management-table
) > :is(a, strong)::after {
  display: none !important;
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
