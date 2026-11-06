# CDX-Cloud — Shared AI Engineering Rules

These rules apply to every AI coding agent working in this repository or in a project that adopts this template.

## Operating principles
- Inspect the repository, its instructions, package manifests, existing architecture, and relevant source files before changing anything.
- Treat the existing project as the source of truth. Preserve its folder structure, naming, public APIs, data model, dependencies, UI, state, animations, sound effects, and established coding style unless the task explicitly requires a change.
- Make the smallest complete change that satisfies the request. Do not rewrite, migrate, modernize, or re-scaffold unrelated parts.
- Do not invent frameworks, dependencies, environment variables, database tables, endpoints, or business rules. Ask one focused question when a missing decision blocks safe implementation; otherwise use the least invasive compatible approach.
- Never claim a command, test, deployment, or remote write succeeded unless its result was observed.

## Implementation workflow
1. Inspect the relevant files and identify the current architecture and runtime.
2. State the intended scope internally; modify only files required by the task.
3. Preserve compatibility with existing code and supported runtime versions.
4. Validate changed files with available project checks. Do not add dependencies solely for a trivial check.
5. Review the diff for accidental deletions, secrets, unrelated formatting, and generated artifacts.
6. Report exactly what changed, what was tested, and any check that could not be run.

## Web application rules
- For HTML/CSS/JavaScript projects, preserve the existing DOM structure, IDs, classes, variables, functions, event handlers, responsive behavior, and visual language.
- Keep single-file applications single-file unless modularization is explicitly requested. When modularization is requested, extract code without silently changing behavior.
- Keep existing theme variables, sound-effect registries, button feedback, transitions, and animations intact during updates.
- Make interactive controls functional and keyboard-accessible. Avoid decorative controls that imply unsupported behavior.
- Treat client-side environment variables as public. Never expose service-role keys, private API keys, database passwords, or signing secrets in browser code.

## Backend and data rules
- Preserve existing authentication, authorization, database schema, RLS policies, validation, and error-handling behavior.
- Never weaken access control or disable RLS to make a feature work.
- Validate user input at trust boundaries. Keep privileged operations on trusted server-side code or protected functions.
- Do not log credentials, tokens, OTPs, or personal data.

## Environment and secrets
- Use `.env.example` only for variable names and safe placeholders. Never commit real `.env` files or credentials.
- Read the actual project documentation before assuming variable names or runtime configuration.
- Do not create, rotate, or change production secrets without explicit authorization.

## Output expectations
- For code-change requests, provide complete replacement files when practical; never use placeholders such as "rest of code unchanged" in a requested complete file.
- Keep explanations concise and distinguish verified results from assumptions or unrun checks.
