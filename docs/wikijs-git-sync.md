# Wiki.js Git Sync Setup

This repository can update Wiki.js automatically after a pull request is merged,
but only if Wiki.js is configured to use Git storage.

## How it works

1. A pull request updates one or more `.md` files in this repository.
2. After the PR is merged, GitHub Actions reads the PR text and the available wiki page catalog.
3. GitHub Actions asks OpenAI to classify the PR into one or more wiki update targets.
4. For each target, GitHub Actions creates a brand-new update page file.
5. Wiki.js pulls the latest repository changes through its Git storage module.
6. The new Markdown files become separate Wiki.js pages.

## Important

The GitHub Action does not write directly to the Wiki.js database.
Wiki.js must be configured to sync this repository.

## Required Wiki.js settings

In the Wiki.js admin area:

1. Open `Administration -> Storage`.
2. Enable the `Git` storage target.
3. Configure the Git module with this repository.
4. Set `Sync Direction` to `Bi-directional`.
5. Set `Branch` to `main`.
6. Set a sync schedule such as `5 minutes`.
7. Apply changes and confirm the Git storage status is healthy.

## First-time import

If your existing pages were created in Wiki.js before Git sync was enabled:

1. Open `Administration -> Storage -> Git`.
2. Run `Add Untracked Changes` if the database already has content that is not in Git.
3. Run `Force Sync` or wait for the next scheduled sync.

If the repository already contains the pages you want to use, run `Import Everything`
from the Git storage module.

## How page categorization works

The workflow uses OpenAI to classify the PR text into one or more existing wiki page targets.
It does not rely only on tags in the PR title.

Examples:

- if the PR describes a manager-related change, the workflow can create `manager-update-pr-<number>.md`
- if the PR describes a login-related change, the workflow can create `login-update-pr-<number>.md`
- if one PR mentions both login and manager updates, the workflow creates two separate update pages

This means the original page is not overwritten by the workflow.
Instead, each merged PR creates a new update page that Wiki.js can sync as a
separate page.

## Required repository secret

This workflow requires a GitHub Actions secret:

- `OPENAI_API_KEY`

Without that secret, the AI classification step cannot run.
