---
name: clone-website
description: Use when the user wants to clone, replicate, rebuild, or reverse-engineer one or more website URLs into a Next.js application, or set up the ai-website-cloner template.
---

# AI Website Cloner

Use the bundled JCodesMore template and its detailed cloning workflow. This plugin supplies instructions and project files; the host coding agent performs the work using browser automation and terminal/file tools.

## Inputs and prerequisites

- Obtain the target URL or URLs from the request. If missing, ask for them; setup-only requests can finish without a URL.
- Choose a project destination from the user's instructions or the current workspace. Ask only if the destination is ambiguous or there is an existing-route conflict.
- Require Node.js 24+, npm, terminal/file access, and browser automation. Detect available browser capabilities and use their documented APIs and applicable host skills. A plain web search cannot replace browser inspection. If these capabilities are unavailable, report the missing prerequisite without pretending generation succeeded.

## Prepare the application

1. Resolve [assets/template.zip](assets/template.zip) relative to this installed skill directory, never relative to the current working directory. It contains the complete pinned upstream starter, including its original agent instructions and cloning skill.
2. For a new application, extract the archive into the chosen empty directory. Validate archive member destinations remain inside that directory. Never overwrite an existing project, unpack into this plugin's installation, or edit bundled files in place.
3. For an existing compatible Next.js project, inspect its instructions and routes and use it directly; do not replace it with the starter.
4. Read the application's `AGENTS.md` and `package.json`. Verify `node --version`, install with `npm ci` in a fresh starter, and run `npm run check`. If setup fails, diagnose and report the actual error before continuing.
5. Read the local Next.js documentation as directed by the application's agent instructions before implementing application code.

## Clone and verify

Read [references/cloning-workflow.md](references/cloning-workflow.md) and [references/inspection-guide.md](references/inspection-guide.md) before inspecting or building. Follow their route isolation, asset extraction, exact component specifications, responsive behavior, incremental builds, and visual QA steps.

If the host permits parallel agents and worktrees, use the upstream dispatch workflow. Otherwise implement the same documented component specs sequentially and report that execution mode. Host and user constraints take priority.

Use authorized target content; do not bypass access controls. Reproduce frontend interactions with demo data unless backend integration was explicitly requested. Keep credentials out of source and research artifacts.

Run `npm run check`, then compare source and local pages at matching desktop and mobile sizes and exercise their interactions. Report output paths, route mapping, check results, and remaining fidelity gaps. Never claim pixel-perfect completion without comparison evidence. Start a local preview when requested or useful; publish only when authorized.
