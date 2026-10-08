# Landing Page Revamp

## Purpose and authorization
Migrate the supplied Notion accounts' landing pages into editable, faithful frontend code. When the user supplies a Notion account link for cloning, read it and proceed through inspection, implementation, verification, GitHub delivery, Cloudflare Pages staging deployment, and the authorized Notion updates. Do not require repeated confirmation for routine steps. A batch normally contains five accounts; the first pilot contains one account with multiple URLs. This file does not create a scheduled daily run.

## Account boundaries and destination
- One Notion account row = one account folder on this computer, one Codex chat, and one GitHub repository covering ALL populated landing-page URL fields.
- Reuse an existing folder for the account when its identity can be verified. Otherwise automatically create a lowercase, dash-separated account folder under this landing-page-revamp workspace; do not ask the user to create it or supply a path. Inspect the destination before writing and never overwrite an existing project. If a name collision belongs to another account, use a stable Notion UUID suffix. Record the absolute folder path and Notion page UUID in the account manifest so resumes reuse the same folder.
- Create a separate account chat when requested by the user, and give it the complete account scope and folder path. Do not create duplicate chats or repositories on resume.
- Use lowercase names with dashes. Preserve the stable Notion page UUID in the account manifest; do not identify accounts by display name alone.
- Same-origin pages share an app with source pathnames preserved. Different origins use isolated apps under apps/{origin-slug}/ in the same repository, with separate styles, assets, ports and run instructions.
- Keep language variants, thank-you pages, meaningful query/fragment states and reused sources in scope. Record redirects and original-to-local mappings. Never silently discard a URL or merge client deliveries.

## Standing approval for cloning
- Proceed automatically with all commands and routine decisions necessary for the requested account cloning: inspection, folder/template setup, dependency installation, asset preparation, implementation, local servers, checks, commits, repository creation, pushes, Cloudflare Pages staging project setup and deployment, and the specified Notion delivery-property updates. Do not ask for repeated approval or confirmation prompts for these authorized steps.
- Choose reasonable defaults within this scope and record them. GitHub owner and repository visibility are settled below; do not ask to confirm them again.
- These instructions express user authorization; they do not change the runtime approval policy or connector permission settings and cannot bypass an app approval dialog, access restriction or automatic review rejection. Report a genuine blocker accurately and continue independent authorized work.
- Request missing information only when it cannot be established from Notion, the account manifest or available access and is necessary to proceed correctly. Production activation and reviewer messages retain the separate scope boundaries below.

## Notion: preserve the exact source schema
- Fetch the supplied account page and inspect its actual properties and parent data-source schema before any mutation. Extract every populated URL field from Landing Page Link through Landing Page Link 12, using the exact field names returned by Notion. Follow pagination or fetch referenced content if necessary.
- Preserve the account's original properties, spelling, option values, and unrelated data. Do not invent or rename columns or status options.
- Expected delivery columns are GitHub Link, Staging Link and LP Revamp Status. Verify these exist and have compatible types before updating. If the actual schema differs, resolve the mapping with the user rather than guessing.
- Expected workflow: Not Started -> Cloned -> QC -> Automation -> Hosted -> Live. Do not add Cloning or Blocked options. Track work-in-progress and blockers locally.
- Only after complete route coverage, visual/interaction checks, passing production checks, verified GitHub delivery, and a verified Cloudflare Pages staging deployment: set GitHub Link to the account repository URL, Staging Link to the deployed staging URL, and LP Revamp Status to the existing Cloned option. Read all three properties back to verify success.
- Do not mark a partial or blocked account Cloned. Preserve TBC ownership and record exceptions explicitly.
- Do not notify or mention reviewers unless the user explicitly authorizes the notification. A status update does not authorize a message.

## Template and canonical clone workflow
Use the installed ai-website-cloner:clone-website skill:
`C:/Users/imana/.codex/plugins/cache/created-by-me-remote/ai-website-cloner/1.0.0/skills/clone-website/SKILL.md`.
Read it before preparing an account. Its bundled assets/template.zip is the pinned upstream starter. For an empty app directory, validate archive destinations and extract safely; never modify the plugin installation. For compatible existing applications, inspect and reuse them.

Read the extracted application's AGENTS.md, package.json, and .agents/skills/clone-website/SKILL.md, plus the installed skill's references/cloning-workflow.md and references/inspection-guide.md. Preserve upstream instructions and add account-specific instructions without replacing the canonical workflow. /clone-website is an agent convention, not a shell command.

Verify Node.js 24+ and npm. Preserve the lockfile, install fresh starters with npm ci, and record runtime versions and template revision. Read the relevant installed Next.js guides in node_modules/next/dist/docs/ before writing application code; do not assume remembered APIs apply. Validate the chosen hosting/build contract before relying on it. The template's Vercel default is not a production hosting decision.

## Implementation standards from the template
- Next.js App Router, React, strict TypeScript, shadcn/ui and Tailwind as supplied by the pinned template. Avoid unreviewed dependency upgrades.
- Named exports, PascalCase components, camelCase utilities, two-space indentation, mobile-first responsive layouts, no any.
- Match source copy, assets, fonts, colors, spacing, section order, motion and interactions. Make no unsolicited redesign changes.
- Build editable components; do not deliver screenshots, iframes or copied production bundles as the implementation.
- Store inspection briefs and route manifests in docs/research/, comparison evidence in docs/design-references/, scoped assets in public/sites/, and source-specific components in src/components/sites/ where the canonical workflow specifies them.
- Keep secrets, .env files, browser profiles and real lead data out of commits. Inspect and adapt irrelevant template deployment workflows before enabling them.

## Cloning phase boundaries
Forms use mock/stub submissions, validation and local success/thank-you flows. Do not send real leads, emails, WhatsApp messages, purchases or production CRM requests. Rewrite in-scope navigation to local routes and document external destinations.

Cloudflare Pages staging deployment is authorized immediately after cloning verification and GitHub delivery, before QC. Production activation, production automation and custom-domain changes follow QC and their applicable authorization. Later requirements include Cloudflare Turnstile, form-based lead capture, customer confirmation email, CLID/UTM tracking, GTM and PostHog; TwentyCRM is deferred. Do not install production credentials during cloning.

## Verification and GitHub delivery
- Inspect every source route in a real browser at desktop and mobile widths before building. Capture complete pages and relevant alternate states.
- Compare every local route with its source at matching widths, scroll positions and states; include an intermediate breakpoint where layout changes. Check assets, responsive wrapping, overflow, navigation, controls, motion and keyboard/focus behavior.
- Run npm run check for every app (lint, typecheck, production build), then browser smoke-test direct entry, refresh, runtime errors, assets and mocked form flows. Save evidence and record precise remaining gaps. Never claim pixel-perfect fidelity without comparison evidence.
- README must include install/run/build commands, pinned versions, app/port map, every source-to-local route, evidence location, mocked integrations and known gaps.
- GitHub destination is always locust08. Create one new private repository per account for this cloning delivery without additional confirmation. This replaces the earlier CRM08 destination. Verify access to locust08; never substitute another owner if access fails.
- If the account already has an older repository, leave it intact and create a new repository for this delivery. Use the account's existing Notion ID property in the name: landing-page-{account-slug}-{notion-id}. Inspect the actual ID property, including its prefix if it is a Notion unique ID. Sanitize the value for GitHub and record the exact original ID and resulting name. If no account ID property is populated, use the stable Notion page UUID as the fallback; never invent a numeric ID.
- Before creating a repository, inspect the manifest, existing remotes, Notion GitHub Link and the destination name. Reuse a repository already verified as belonging to this same cloning delivery on resume; do not create another new repository on every attempt. If a name belongs to an unrelated or older delivery, append the stable Notion UUID and, only if still necessary, a recorded numeric suffix. Preserve the selected name in the manifest.
- Do not delete, force-push or overwrite an older repository. Preserve its URL in the local manifest before replacing the Notion GitHub Link after successful delivery. Prepare the new remote without losing existing remote references.
- Keep the delivery repository's existing branch policy; use main for a new repository. Record the tested branch and full SHA. Verify remote SHA matches the tested local SHA before marking Cloned.
- On uncertain writes, read back before retrying. Resume the missing checkpoint instead of duplicating repositories or tracker updates.

## Cloudflare Pages staging deployment
- After completing cloning checks and pushing the tested commit to the account GitHub repository, automatically deploy that commit to Cloudflare Pages for staging. Continue through deployment and the Notion update without requesting routine confirmation.
- Inspect available Cloudflare access and existing account manifests and Pages projects before creating anything. Reuse a project verified as belonging to this same account delivery on resume. Never overwrite an unrelated project or change an existing production site. Record the Cloudflare account, project name, deployment ID, deployed full SHA and staging URL in the account manifest.
- Validate the app's Cloudflare Pages build and hosting contract before deployment. Keep deployment configuration and run instructions in the account repository; commit, push and recheck any required implementation or configuration changes before deploying the resulting tested SHA. Do not assume the template's Vercel configuration is suitable for Pages.
- Preserve all source routes and isolated origins in staging. When an account contains multiple apps, deploy each app and record every app-to-staging URL mapping. Populate the single Notion Staging Link with a verified account staging entry URL that gives reviewers access to every app; do not silently publish or link only one app.
- Keep forms and integrations mocked in staging. Do not activate real lead submission, email, messaging, purchases, production CRM integrations or custom domains as part of this step. Keep credentials out of commits.
- Wait for deployment success, verify the deployed commit matches the tested GitHub SHA, and browser smoke-test every deployed route, direct entry, refresh, assets, runtime errors, responsive layout, navigation and mocked form/thank-you flows. Save deployment evidence and precise remaining gaps with the account's existing verification records.
- Only after all required staging apps and routes pass verification, automatically write the verified deployed staging entry URL to the exact existing Notion Staging Link property together with the delivery properties specified above, then read them back. A staging deployment does not advance the workflow to Hosted or Live; the account remains Cloned and ready for QC.
- If Cloudflare access, the hosting contract, deployment, route verification or the Notion schema blocks completion, preserve existing delivery-property values and record the blocker locally. Do not claim staging completion or mark the account Cloned. On resume, inspect existing deployments and Notion values before retrying; continue from the missing checkpoint without duplicating projects or deployments unnecessarily.

## Completion report
Report the account, folder, covered source URLs and local routes, repository and tested commit, Cloudflare Pages project and verified staging URL(s), deployed commit, checks and evidence, known gaps/blockers, and read-back verification of GitHub Link, Staging Link and LP Revamp Status. Cloned means ready for QC, not production launch. Keep unresolved decisions visible without counting them as successful delivery.
