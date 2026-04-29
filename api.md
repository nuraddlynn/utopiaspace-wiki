---
title: API
description: Describe how UtopiaSpace and the wiki communicate between frontend, backend, Supabase, GitHub, and Wiki.js using requests and integrations.
published: true
date: 2026-04-20T08:37:40.679Z
tags: api, backend, supabase, request, response, integration, wikijs
editor: markdown
dateCreated: 2026-04-20T02:39:22.311Z
---

# API

<span class="utopia-api-scope"></span>

This page explains how API-style communication works across UtopiaSpace and the wiki: frontend actions, backend logic, Supabase requests, authentication, workflow processing, GitHub automation, and Wiki.js sync.

<div class="utopia-api-actions">
  <a href="/architecture">Architecture</a>
  <a href="/database">Database</a>
  <a href="/developer-space">Developer Space</a>
</div>

## Overview

<div class="utopia-api-grid">
  <section>
    <h3>Application Requests</h3>
    <p>UtopiaSpace screens send requests when users create records, update workflows, approve submissions, or load reports.</p>
  </section>

  <section>
    <h3>Supabase Communication</h3>
    <p>Application logic reads and writes structured data through Supabase tables, authentication, and security policies.</p>
  </section>

  <section>
    <h3>Wiki Automation</h3>
    <p>GitHub and Wiki.js use Git-based sync and workflow triggers to keep documentation pages updated.</p>
  </section>
</div>

## Request Flow

<div class="utopia-api-flow">
  <div>
    <strong>1</strong>
    <span>User performs an action, such as creating a task, submitting a claim, approving leave, or publishing an announcement.</span>
  </div>
  <div>
    <strong>2</strong>
    <span>The frontend sends a request with the required payload and user session context.</span>
  </div>
  <div>
    <strong>3</strong>
    <span>The application validates the request, role access, required fields, and workflow state.</span>
  </div>
  <div>
    <strong>4</strong>
    <span>The backend or Supabase client reads, inserts, updates, or deletes data where allowed.</span>
  </div>
  <div>
    <strong>5</strong>
    <span>The response returns success, failure, validation errors, or updated records to the frontend.</span>
  </div>
</div>

## API Types

<div class="utopia-api-table">
  <div class="utopia-api-head">Type</div>
  <div class="utopia-api-head">Use</div>

  <strong>CRUD Operations</strong>
  <p>Create, read, update, and delete records such as tasks, announcements, meeting notes, claims, settings, and reference data.</p>

  <strong>Authentication API</strong>
  <p>Handles Google sign-in, session management, profile lookup, and role verification.</p>

  <strong>Workflow API</strong>
  <p>Moves records through statuses such as submitted, pending review, approved, rejected, processed, or completed.</p>

  <strong>Reporting API</strong>
  <p>Fetches filtered data for dashboards, histories, trackers, summaries, attendance records, and analytics.</p>

  <strong>Integration API</strong>
  <p>Supports cross-system actions such as GitHub repository dispatch, update generation, and Wiki.js Git sync.</p>
</div>

## UtopiaSpace Examples

<div class="utopia-api-table">
  <div class="utopia-api-head">Example</div>
  <div class="utopia-api-head">What Happens</div>

  <strong>Create Task</strong>
  <p>User creates a task, the request validates assignee and required fields, then the task is stored and shown in Taskboard.</p>

  <strong>Submit Claim</strong>
  <p>User submits claim details and supporting information, then the claim moves into the correct approval workflow.</p>

  <strong>Approve Leave</strong>
  <p>Manager, Supervisor, HR, or Director reviews the request, permission is checked, and status is updated.</p>

  <strong>Publish Announcement</strong>
  <p>Announcement details, audience, department, and publish settings are saved so targeted users can view it.</p>

  <strong>Track Supplier Payment</strong>
  <p>Finance users load supplier payment records, update verification status, and track processing history.</p>
</div>

## CRUD Mapping

<div class="utopia-api-table">
  <div class="utopia-api-head">Action</div>
  <div class="utopia-api-head">Example in UtopiaSpace</div>

  <strong>Create</strong>
  <p>Add a new task, announcement, claim, leave request, supplier payment request, backcharge, or meeting note.</p>

  <strong>Read</strong>
  <p>Load calendar items, taskboard rows, payment trackers, user profiles, attendance records, or quotation history.</p>

  <strong>Update</strong>
  <p>Change task status, approve or reject a request, update profile details, edit settings, or process payment status.</p>

  <strong>Delete</strong>
  <p>Remove data only where the module and permissions allow deletion. Many workflow records should be archived or status-updated instead.</p>
</div>

## Request Payloads

<div class="utopia-api-table">
  <div class="utopia-api-head">Payload Area</div>
  <div class="utopia-api-head">Typical Content</div>

  <strong>User Context</strong>
  <p>User ID, session, role, department, company, workspace, and permission-related metadata.</p>

  <strong>Record Data</strong>
  <p>Title, description, status, dates, assignees, amounts, attachments, item codes, supplier references, or meeting details.</p>

  <strong>Workflow Data</strong>
  <p>Current status, next status, approval decision, rejection reason, reviewer, processor, and before/after values.</p>

  <strong>Filters</strong>
  <p>Date range, company, department, workspace, status, type, assignee, supplier, employee, or search keyword.</p>
</div>

## Example Request

```json
{
  "title": "Prepare monthly report",
  "assigned_to": "user_id",
  "priority": "medium",
  "due_date": "2026-04-30",
  "workspace": "manager-space"
}
```

## Example Response

```json
{
  "status": "success",
  "message": "Task created successfully",
  "record_id": "task_id"
}
```

## Error Response Pattern

```json
{
  "status": "error",
  "message": "You do not have permission to approve this request.",
  "code": "permission_denied"
}
```

## Supabase Interaction

<div class="utopia-api-table">
  <div class="utopia-api-head">Operation</div>
  <div class="utopia-api-head">Purpose</div>

  <strong>Insert</strong>
  <p>Create records in tables such as announcements, meeting notes, tasks, claims, or workflow requests.</p>

  <strong>Select</strong>
  <p>Fetch rows for dashboards, reports, trackers, histories, profile pages, and workspace tables.</p>

  <strong>Update</strong>
  <p>Modify records after validation, such as status changes, profile updates, approval decisions, and setting changes.</p>

  <strong>Delete</strong>
  <p>Remove records only when allowed by business rules, permissions, and database policies.</p>

  <strong>Auth</strong>
  <p>Verify session state, identify the user, and connect the session to profile and role data.</p>
</div>

## Access and Validation

<div class="utopia-api-table">
  <div class="utopia-api-head">Check</div>
  <div class="utopia-api-head">Why It Matters</div>

  <strong>Authentication</strong>
  <p>Confirms that the user is signed in with a valid company account.</p>

  <strong>Role Permission</strong>
  <p>Confirms that the user can view, create, edit, approve, reject, process, or debug the requested record.</p>

  <strong>Required Fields</strong>
  <p>Prevents incomplete submissions, missing amounts, missing assignees, invalid dates, or empty supporting details.</p>

  <strong>Workflow State</strong>
  <p>Prevents invalid transitions, such as processing a payment before verification or approving an already completed request.</p>

  <strong>RLS Policy</strong>
  <p>Protects rows at database level so sensitive data is not exposed by frontend mistakes.</p>
</div>

## Wiki and GitHub API Flow

<div class="utopia-api-table">
  <div class="utopia-api-head">Flow</div>
  <div class="utopia-api-head">Purpose</div>

  <strong>Repository Dispatch</strong>
  <p>Triggers wiki update workflows from the UtopiaSpace application repository into the wiki repository.</p>

  <strong>GitHub Actions</strong>
  <p>Reads PR or commit information and generates relevant update records for wiki pages.</p>

  <strong>Gemini Classification</strong>
  <p>Classifies release or PR summaries into the most relevant documentation pages.</p>

  <strong>Wiki.js Git Sync</strong>
  <p>Pulls Markdown pages from GitHub into Wiki.js so the documentation site reflects the repository.</p>
</div>

## API Design Guidelines

<div class="utopia-api-grid">
  <section>
    <h3>Validate Early</h3>
    <p>Check user access, required fields, status, and workflow rules before writing data.</p>
  </section>

  <section>
    <h3>Return Clear Errors</h3>
    <p>Use understandable messages for missing fields, permission issues, invalid states, and failed requests.</p>
  </section>

  <section>
    <h3>Keep Workflows Traceable</h3>
    <p>Store enough status and reviewer information so approvals, processing, and histories can be audited.</p>
  </section>
</div>
