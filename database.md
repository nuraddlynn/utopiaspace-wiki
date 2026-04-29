# Database

<span class="utopia-database-scope"></span>

This page documents two related but separate data areas: the UtopiaSpace application database, which stores operational system data in Supabase, and the Wiki.js documentation storage flow, which syncs Markdown pages from Git into the wiki.

<div class="utopia-database-actions">
  <a href="/architecture">Architecture</a>
  <a href="/api">API</a>
  <a href="/docs/wikijs-git-sync">Wiki.js Git Sync</a>
</div>

## Overview

<div class="utopia-database-grid">
  <section>
    <h3>Application Data</h3>
    <p>UtopiaSpace uses Supabase PostgreSQL to store user, workflow, approval, attendance, finance, and operations records.</p>
  </section>

  <section>
    <h3>Documentation Data</h3>
    <p>The wiki uses Git-backed Markdown files as the source of truth for pages, guides, update records, and developer documentation.</p>
  </section>

  <section>
    <h3>Access and Security</h3>
    <p>Authentication, roles, permissions, RLS, and policy metadata protect both data access and workflow visibility.</p>
  </section>
</div>

## UtopiaSpace Application Database

<div class="utopia-database-table">
  <div class="utopia-database-head">Area</div>
  <div class="utopia-database-head">Purpose</div>

  <strong>Supabase PostgreSQL</strong>
  <p>Stores structured operational data in relational tables and supports queries from the application backend and frontend.</p>

  <strong>Authentication</strong>
  <p>Connects logged-in users to profile records, sessions, roles, and access checks.</p>

  <strong>Workflow Storage</strong>
  <p>Stores submissions, approvals, tasks, claims, attendance, announcements, meetings, finance records, and operational trackers.</p>

  <strong>Realtime and Integration</strong>
  <p>Supports application modules that need quick updates, shared data, and integration with frontend and backend logic.</p>
</div>

## Core Data Entities

<div class="utopia-database-table">
  <div class="utopia-database-head">Table / Entity</div>
  <div class="utopia-database-head">What It Stores</div>

  <strong>profiles</strong>
  <p>User information such as full name, short name, phone number, and related profile details.</p>

  <strong>announcements</strong>
  <p>Company announcements, including title, summary, type, department, target audience, and publishing details.</p>

  <strong>one_to_one</strong>
  <p>Meeting records and notes, including meeting title, time, business unit, linked tasks, and follow-up information.</p>

  <strong>pbac_settings</strong>
  <p>Approval-based workflow settings, including user references and before/after JSON values for controlled changes.</p>

  <strong>abac_policy_metadata</strong>
  <p>Attribute-based access metadata used to support role and permission behaviour across the system.</p>
</div>

## Module Data Coverage

<div class="utopia-database-table">
  <div class="utopia-database-head">Module</div>
  <div class="utopia-database-head">Data Examples</div>

  <strong>Personal Space</strong>
  <p>Personal tasks, general claims, calendars, announcements, meeting notes, and user activity records.</p>

  <strong>HR Space</strong>
  <p>Employee records, attendance, leave, overtime, benefit claims, salary advance approvals, and company structure data.</p>

  <strong>Account Space</strong>
  <p>Supplier payment requests, backcharges, claims verification, petty cash, AP records, payment history, and finance trackers.</p>

  <strong>Credit Space</strong>
  <p>Rental accounts, payment collection progress, repayment timelines, overdue status, and follow-up tracking.</p>

  <strong>Operations Efficiency</strong>
  <p>Operations attendance, workforce availability, RentalTracker records, warehouse pages, item history, and backcharge support data.</p>

  <strong>Indoor Space</strong>
  <p>Sales documents, ceiling calculator records, quotation history, customer references, and indoor sales records.</p>

  <strong>Developer / Admin</strong>
  <p>System settings, user management, roles, permissions, technical monitoring, and support/debugging records.</p>
</div>

## Application Data Flow

<div class="utopia-database-flow">
  <div>
    <strong>1</strong>
    <span>User performs an action, such as submitting a task, claim, announcement, leave request, or payment request.</span>
  </div>
  <div>
    <strong>2</strong>
    <span>The frontend sends a request through the application logic or API layer.</span>
  </div>
  <div>
    <strong>3</strong>
    <span>The application validates input, role access, workflow rules, and required permissions.</span>
  </div>
  <div>
    <strong>4</strong>
    <span>Supabase stores, updates, or retrieves the relevant records.</span>
  </div>
  <div>
    <strong>5</strong>
    <span>The updated data is returned to the user interface for review, approval, tracking, or reporting.</span>
  </div>
</div>

## Relationships

<div class="utopia-database-table">
  <div class="utopia-database-head">Relationship</div>
  <div class="utopia-database-head">Example</div>

  <strong>User to Announcement</strong>
  <p>One user can create or manage many announcements depending on role and permissions.</p>

  <strong>User to Approval</strong>
  <p>One user can submit requests, while another authorised user reviews, approves, rejects, or processes them.</p>

  <strong>Meeting to Task</strong>
  <p>One meeting can contain multiple linked tasks, assignees, deadlines, and follow-up items.</p>

  <strong>Role to Data Access</strong>
  <p>Roles and policy metadata determine which rows, modules, and actions are visible to a user.</p>
</div>

## Security

<div class="utopia-database-table">
  <div class="utopia-database-head">Control</div>
  <div class="utopia-database-head">Purpose</div>

  <strong>Supabase Authentication</strong>
  <p>Manages login sessions and connects authenticated users to their profile and access information.</p>

  <strong>Row Level Security</strong>
  <p>Restricts database rows so users only access data allowed by their role, department, company, or workflow context.</p>

  <strong>Role-Based Access</strong>
  <p>Controls which modules and actions users can access, such as view, create, edit, approve, reject, process, or debug.</p>

  <strong>Policy Metadata</strong>
  <p>Supports rule-based access decisions and keeps permission behaviour consistent across modules.</p>
</div>

## Wiki.js Documentation Storage

<div class="utopia-database-table">
  <div class="utopia-database-head">Component</div>
  <div class="utopia-database-head">Role</div>

  <strong>Markdown Pages</strong>
  <p>Wiki pages are stored as `.md` files in the GitHub wiki repository, including guides, role pages, developer docs, and updates.</p>

  <strong>Wiki.js Git Storage</strong>
  <p>Pulls the Markdown files into Wiki.js so GitHub can act as the source of truth for documentation.</p>

  <strong>Update Records</strong>
  <p>Generated files in `update-records/` capture release notes, PR summaries, commit updates, and documentation changes.</p>

  <strong>Custom CSS</strong>
  <p>The Stripe-inspired wiki styling is documented in `docs/wikijs-stripe-style.md` and applied through Wiki.js custom CSS.</p>
</div>

## Wiki Sync Flow

<div class="utopia-database-flow">
  <div>
    <strong>1</strong>
    <span>A Markdown page or update record is changed in the wiki Git repository.</span>
  </div>
  <div>
    <strong>2</strong>
    <span>The change is committed and pushed to the `main` branch on GitHub.</span>
  </div>
  <div>
    <strong>3</strong>
    <span>Wiki.js Git Storage imports or syncs from GitHub.</span>
  </div>
  <div>
    <strong>4</strong>
    <span>Wiki.js renders the Markdown content as pages inside the documentation site.</span>
  </div>
  <div>
    <strong>5</strong>
    <span>If Wiki.js local edits conflict with GitHub, purge the local repository and import from Git as the source of truth.</span>
  </div>
</div>

## Wiki Automation

<div class="utopia-database-table">
  <div class="utopia-database-head">Automation</div>
  <div class="utopia-database-head">Purpose</div>

  <strong>GitHub Actions</strong>
  <p>Reads PR and commit details, then creates or updates documentation records when relevant system changes are merged.</p>

  <strong>Gemini Classification</strong>
  <p>Classifies change summaries into matching documentation targets so update pages can be generated automatically.</p>

  <strong>Repository Dispatch</strong>
  <p>Supports automated wiki update triggers from the UtopiaSpace application repository into the wiki repository.</p>

  <strong>Updates Page</strong>
  <p>Aggregates generated update records into a readable weekly summary for users and internal teams.</p>
</div>

## Maintenance Guidelines

<div class="utopia-database-grid">
  <section>
    <h3>Keep App Data Protected</h3>
    <p>Use RLS, role checks, and permission metadata so sensitive operational records remain controlled.</p>
  </section>

  <section>
    <h3>Keep Wiki Git-First</h3>
    <p>When documentation is managed from Git, avoid editing the same pages directly inside Wiki.js to prevent conflicts.</p>
  </section>

  <section>
    <h3>Monitor Sync Health</h3>
    <p>If Wiki.js reports merge conflicts, purge the local repository and import from GitHub before continuing.</p>
  </section>
</div>

## 🚀 Latest Updates

<!-- AUTO-UPDATE-START -->
<!-- AUTO-UPDATE-ENTRY-START -->
### April 27, 2026 at 11:41 AM - Fix: Backfill FT to IRIS

Fixed an issue related to backfilling FT data to IRIS.
<!-- AUTO-UPDATE-ENTRY-END -->
<!-- AUTO-UPDATE-END -->
