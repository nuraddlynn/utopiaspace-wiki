# Architecture

<span class="utopia-architecture-scope"></span>

UtopiaSpace is structured as a role-based internal operations platform. The application connects daily workspaces, approval flows, operational records, Supabase data, access control, and developer automation into one system.

<div class="utopia-architecture-actions">
  <a href="/developer-space">Developer Space</a>
  <a href="/database">Database</a>
  <a href="/api">API</a>
</div>

## Overview

<div class="utopia-architecture-grid">
  <section>
    <h3>Role-Based Platform</h3>
    <p>Users access spaces based on responsibility, such as Manager, HR, Accounts, Credit, OE, Indoor Sales, and Developer.</p>
  </section>

  <section>
    <h3>Workflow-Oriented Data</h3>
    <p>Claims, approvals, attendance, tasks, announcements, meetings, payments, and operational records move through structured workflows.</p>
  </section>

  <section>
    <h3>Git-Backed Documentation</h3>
    <p>Wiki documentation is maintained in Git and synced into Wiki.js through the Git storage module.</p>
  </section>
</div>

## Application Layers

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Layer</div>
  <div class="utopia-architecture-head">Responsibility</div>

  <strong>Frontend</strong>
  <p>Displays UtopiaSpace screens, role spaces, dashboards, forms, trackers, tables, and navigation. It handles user interactions and sends requests for data or workflow actions.</p>

  <strong>Backend / Application Logic</strong>
  <p>Processes submissions, approvals, workflow rules, filtering, validations, status changes, and system operations before data is stored or returned.</p>

  <strong>Supabase / Database</strong>
  <p>Stores user profiles, announcements, meetings, tasks, approvals, settings, attendance records, finance records, and operational data.</p>

  <strong>Authentication and Access</strong>
  <p>Uses Google login, Supabase authentication, role checks, permissions, and policy metadata to control what users can access.</p>

  <strong>Documentation Layer</strong>
  <p>Uses Wiki.js and GitHub-backed Markdown pages to document user guides, role spaces, developer references, and release updates.</p>
</div>

## Role Spaces

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Space</div>
  <div class="utopia-architecture-head">System Area</div>

  <strong>Personal Space</strong>
  <p>Personal tasks, claims, announcements, calendar, meeting notes, and individual workflow visibility.</p>

  <strong>Manager / Director / Supervisor</strong>
  <p>Review, approval, reporting, team monitoring, task follow-up, and escalated operational oversight.</p>

  <strong>HR Space</strong>
  <p>Employee records, leave, attendance, benefits, overtime, company structure, and HR-related approvals.</p>

  <strong>Account Space</strong>
  <p>Claims verification, supplier payment requests, backcharges, petty cash, AP processing, finance reporting, and payment history.</p>

  <strong>Credit Space</strong>
  <p>Rental accounts, repayment timelines, payment collection progress, overdue tracking, and credit follow-up.</p>

  <strong>Operations Efficiency Space</strong>
  <p>Operations attendance, workforce availability, RentalTracker, warehouse pages, item history, and backcharge support.</p>

  <strong>Indoor Space</strong>
  <p>Indoor sales documents, ceiling calculator, quotation history, customer records, and sales reference tools.</p>

  <strong>Developer Space</strong>
  <p>System health, Supabase usage, server monitoring, deployment notes, environment setup, and technical workflows.</p>
</div>

## Data Model

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Entity</div>
  <div class="utopia-architecture-head">Purpose</div>

  <strong>profiles</strong>
  <p>Stores user information such as full name, short name, phone number, and related profile details.</p>

  <strong>announcements</strong>
  <p>Stores company announcements, including title, summary, type, department, and audience information.</p>

  <strong>one_to_one</strong>
  <p>Stores meeting records, meeting titles, meeting time, business unit information, and related notes.</p>

  <strong>pbac_settings</strong>
  <p>Supports approval-based configuration and workflow changes through before-and-after record tracking.</p>

  <strong>abac_policy_metadata</strong>
  <p>Supports attribute-based access metadata used to help control role and permission behaviour.</p>
</div>

## Request Flow

<div class="utopia-architecture-flow">
  <div>
    <strong>1</strong>
    <span>User opens a role space or page from the UtopiaSpace navigation.</span>
  </div>
  <div>
    <strong>2</strong>
    <span>The frontend loads the relevant screen, form, table, tracker, or dashboard.</span>
  </div>
  <div>
    <strong>3</strong>
    <span>The application verifies authentication, role access, and required permissions.</span>
  </div>
  <div>
    <strong>4</strong>
    <span>The request is processed through application logic, validation, workflow rules, and API communication.</span>
  </div>
  <div>
    <strong>5</strong>
    <span>Supabase stores or retrieves the required records.</span>
  </div>
  <div>
    <strong>6</strong>
    <span>The frontend updates the page so the user can continue the workflow.</span>
  </div>
</div>

## Workflow Patterns

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Pattern</div>
  <div class="utopia-architecture-head">Where It Appears</div>

  <strong>Submission Flow</strong>
  <p>Used for claims, supplier payment requests, backcharges, leave requests, advance salary requests, incidents, and tasks.</p>

  <strong>Approval Flow</strong>
  <p>Used by Manager, Director, Supervisor, HR, Account, and AP workflows where requests require review before processing.</p>

  <strong>Tracking Flow</strong>
  <p>Used by taskboard, rental tracker, supplier payment tracker, backcharge history, attendance records, and quotation history.</p>

  <strong>Reference Data Flow</strong>
  <p>Used by supplier list, item code list, company directory, user profiles, roles, permissions, and system settings.</p>

  <strong>Reporting Flow</strong>
  <p>Used by dashboards, summaries, analytics, attendance records, payment history, and operational reports.</p>
</div>

## Access Control

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Control</div>
  <div class="utopia-architecture-head">Role in Architecture</div>

  <strong>Google Sign-In</strong>
  <p>Users access UtopiaSpace using their official company Google account.</p>

  <strong>Supabase Authentication</strong>
  <p>Manages sessions and helps connect logged-in users to profile and access data.</p>

  <strong>Roles and Permissions</strong>
  <p>Determine whether a user can view, create, edit, approve, reject, process, or debug specific records.</p>

  <strong>Row Level Security</strong>
  <p>Protects data at database level so sensitive rows are only available to authorised users.</p>

  <strong>Policy Metadata</strong>
  <p>Supports rule-driven access decisions and helps keep access behaviour consistent across modules.</p>
</div>

## Developer and Release Flow

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Area</div>
  <div class="utopia-architecture-head">How It Fits</div>

  <strong>Development, Staging, Production</strong>
  <p>Changes move through environment promotion flows such as development to staging and staging to production.</p>

  <strong>Branch Sync and Back-Merge</strong>
  <p>Branch-sync conventions and auto back-merge workflows reduce drift between development, staging, and production branches.</p>

  <strong>Infisical Environment</strong>
  <p>Environment setup is documented for secure configuration and deployment consistency.</p>

  <strong>Service Worker Denylist</strong>
  <p>Static assets such as images are excluded from SPA fallback routing so files can be accessed directly.</p>

  <strong>Reusable Hooks and Components</strong>
  <p>Shared plumbing includes hooks like workspace and leave filter utilities, date range filters, and workflow status constants.</p>
</div>

## Wiki and Update Automation

<div class="utopia-architecture-table">
  <div class="utopia-architecture-head">Component</div>
  <div class="utopia-architecture-head">Purpose</div>

  <strong>Wiki.js Git Storage</strong>
  <p>Pulls Markdown documentation from the GitHub wiki repository into Wiki.js pages.</p>

  <strong>GitHub Actions</strong>
  <p>Reads merged PR details, rebuilds update pages, and supports automated wiki update dispatch.</p>

  <strong>Gemini Classification</strong>
  <p>Classifies PR content into matching wiki update targets and generates update records.</p>

  <strong>Updates Page</strong>
  <p>Summarises generated update records into big updates, improvements, fixes, and detail links.</p>
</div>

## Key Characteristics

<div class="utopia-architecture-grid">
  <section>
    <h3>Modular</h3>
    <p>Each space owns a clear operational area while still sharing user, access, and workflow foundations.</p>
  </section>

  <section>
    <h3>Role-Aware</h3>
    <p>Navigation, data access, and actions are shaped by the user's role and permissions.</p>
  </section>

  <section>
    <h3>Documentation-Driven</h3>
    <p>Developer and user documentation follows the same Git-backed release and sync workflow.</p>
  </section>
</div>

## 🚀 Latest Updates

### April 24, 2026 at 12:31 PM - Service Worker Denylist for Static Assets

Improved service worker routing to bypass SPA fallback for static assets, ensuring direct access to files like `/ApprovedSample.png`.
