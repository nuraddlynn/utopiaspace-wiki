---
title: What’s New This Week
description: Weekly summary of generated wiki update pages
published: true
date: 2026-04-24T13:38:39.508Z
dateCreated: 2026-04-24T13:38:39.508Z
tags: updates, ai-generated
editor: markdown
---

# 🚀 What’s New This Week

📅 April 24, 2026

## 🔥 Big Updates

- Reformatted the announcements page to function as a weekly summary.
- Added support for repository dispatch to automate wiki updates.
- Added useWorkspace, useLeaveFilterOptions hooks, DateRangeFilter component, and SUPPLIER_PAYMENT_WORKFLOW_STATUSES constant for future feature development.
- The main home page documentation has been renamed from home to docs/home for better organization.

## ⚡ Improvements

- The internal index for wiki updates has been rebuilt to ensure all generated pages are correctly reflected.
- Added Wiki.js metadata to automatically generated update pages for improved content management.
- Improved service worker routing to bypass SPA fallback for static assets (e.g., images), ensuring direct access to files like /ApprovedSample.png.
- Migrated 6 pages (e.g., TaskBoard, Developer Usage, Support) to use the standardized AppBreadcrumbs component for consistent navigation.
- Updated staff documentation note in the end user guide.
- Certain features are now disabled in deployed environments (e.g., staging) as part of recent promotions.
- Updated content on the home page.
- Updated documentation for HR backcharge management.
- Swapped page-level IconButtons to BaseBackButton on HR User Details and HR User Approval Details pages for consistent UI.
- Updated workspace metadata files.

## 🐛 Fixes

- Addressed case-sensitivity issues in IbnuSinaTemplate.ts and KakKenduriTemplate.ts imports, resolving Vercel deployment failures on Linux environments. Ensures successful builds and prevents runtime regressions for /indoor-workspace/ibnu-sina and /indoor-workspace/kak-kenduri.

## 📚 Update Details

- [announcements-update-commit-627fc77.md](/announcements-update-commit-627fc77)
- [announcements-update-commit-6bff029.md](/announcements-update-commit-6bff029)
- [announcements-update-commit-fc9e190.md](/announcements-update-commit-fc9e190)
- [architecture-update-pr-533.md](/architecture-update-pr-533)
- [basic-navigation-update-pr-533.md](/basic-navigation-update-pr-533)
- [developer-update-commit-5866a12.md](/developer-update-commit-5866a12)
- [developer-update-pr-533.md](/developer-update-pr-533)
- [developer-update-pr-544.md](/developer-update-pr-544)
- [end-user-update-commit-9b25f5b.md](/end-user-update-commit-9b25f5b)
- [end-user-update-pr-548.md](/end-user-update-pr-548)
- [home-update-commit-2f1033a.md](/home-update-commit-2f1033a)
- [home-update-commit-d274883.md](/home-update-commit-d274883)
- [hr-update-commit-505f74b.md](/hr-update-commit-505f74b)
- [hr-update-pr-533.md](/hr-update-pr-533)
- [settings-update-commit-ab7f2fb.md](/settings-update-commit-ab7f2fb)

## Latest Trigger

PR #548: promote: development -> staging (2026-04-24)

