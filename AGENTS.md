# Landing Page Revamp — Agent Instructions

## Purpose

This root directory contains landing-page cloning and revamp projects.

Each landing page must live in its own child folder.

Never mix two landing-page implementations inside one child project.

## Model Policy

Use:
GPT-6.1 Sol
Reasoning: Low

Do not intentionally change the selected model or reasoning level.

If unavailable, report it instead of silently using another model.

## Mandatory Access Preflight

Before inspecting or cloning any landing page, verify:

1. Local computer access
2. Access to Documents/landing-page-revamp
3. Access to this AGENTS.md
4. Browser access
5. Ability to open and inspect the source landing page
6. Git installed
7. GitHub connected and authenticated
8. Permission to create/push repositories
9. Codex local task access
10. Website Cloner plugin available
11. clone-website skill available
12. Intended model is GPT-6.1 Sol / Low

If ANY required access is missing:

STOP.

Tell the user exactly what is missing and what must be enabled before continuing.

Do not bypass permissions.
Do not continue using guesses.
Do not silently use another method.

## Website Cloner

For landing-page cloning, reconstruction or revamp work, use the installed Website Cloner plugin and clone-website skill.

## Workflow

For every new landing page:

1. Run access preflight
2. Create dedicated project folder
3. Inspect source website
4. Map source structure
5. Observe desktop/mobile behavior
6. Extract permitted assets
7. Build
8. Run locally
9. Compare source vs implementation
10. Refine visible differences
11. Test responsive states
12. Run validation
13. Create Git repository
14. Push to GitHub when required
15. Produce final report

A successful build alone does not mean the task is complete.

## One Task = One Landing Page

Each Codex task/chat must work on only ONE landing page.

Multiple independent tasks may run concurrently in separate chats and separate folders.

Never modify sibling landing-page folders.

## Inspection

Before coding, inspect:

- page structure
- desktop layout
- mobile layout
- navigation
- fonts
- colours
- spacing
- images
- backgrounds
- icons
- buttons
- forms
- sliders/carousels
- animations
- sticky behavior
- hover states
- responsive behavior

Use browser inspection / Playwright when available.

Do not rely on a single screenshot when the live source is available.

## Visual Accuracy

Match:
- layout
- sizing
- spacing
- typography
- colours
- images
- backgrounds
- borders
- radius
- shadows
- icons
- buttons
- animation
- responsive behavior

Do not redesign unless instructed.

## Technology

For new cloned landing pages use the Website Cloner architecture.

Preferred:
- Next.js
- React
- TypeScript
- Tailwind CSS
- reusable components
- shadcn/ui where useful

## Browser Testing

Verify approximately:

Desktop: 1440px
Tablet: 768px
Mobile: 390px

Check:
- horizontal overflow
- overlap
- missing images
- broken navigation
- clipping
- responsive issues
- broken forms
- console errors

## Visual Comparison

Compare source and local implementation using matching viewport sizes.

Identify and fix meaningful differences before completion.

## Validation

Prefer:

npm run check

when available.

Otherwise run:
- npm run lint
- npm run typecheck
- npm run build

Do not hide failed checks.

## Security

Never expose:
- passwords
- API keys
- service tokens
- GitHub tokens
- database credentials
- environment secrets

Never commit .env secrets.

## Git & GitHub

Each landing-page project should use its own Git history unless instructed otherwise.

Before pushing:
- inspect git status
- remove temporary files
- confirm build passes
- use meaningful commits

Never force push.

After validation, create/push a PRIVATE GitHub repository when required.

Record:
- repository URL
- branch
- latest commit

## Deployment

Do NOT deploy unless explicitly requested.

Do not modify DNS, production domains, Cloudflare, production environment variables or production databases unless instructed.

## Notion

Do NOT automatically update Notion.

The user will manually copy the final project information into Notion.

## Completion Report

Return:

LANDING PAGE
Original URL:
Project name:

ACCESS PREFLIGHT
Local computer:
Browser:
GitHub:
Git:
Codex:
Website Cloner:
Model:

LOCAL PROJECT
Folder:
Framework:

GITHUB
Repository URL:
Visibility:
Branch:
Latest commit:

VALIDATION
Build:
Lint:
Typecheck:
Desktop:
Tablet:
Mobile:
Visual comparison:

IMPORTANT NOTES
Remaining differences:
Missing assets/content:
Unsupported behaviour:
Items requiring manual review:

DEPLOYMENT
Deployed: No unless explicitly requested.

NOTION
Automatically updated: No
Manual Notion update required: Yes
