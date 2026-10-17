# Windows Application Template — Requirements

## 1. Purpose

Create a reusable GitHub template for customizing open-source
Windows applications with personal branding and minor modifications.

## 2. User Environment

- Primary device: Android phone.
- GitHub repository management: GitHub website or app.
- Coding assistance: Claude.
- Preferred build environment: GitHub Actions.
- Budget: Free tools and services wherever possible.
- Local Windows development: Optional, not required by default.

## 3. Customization Requirements

The template should support, where practical:

- Changing the application name.
- Replacing logos, icons, and branding assets.
- Changing package or product identifiers when necessary.
- Adjusting application colours, text, and interface elements.
- Making small feature modifications.
- Preserving existing functionality.

## 4. Technology Support

Do not assume all Windows applications use the same technology.

Potential technologies include:

- C# and .NET.
- C and C++.
- Python.
- Electron and JavaScript/TypeScript.
- Other open-source Windows application frameworks.

Each project must be assessed before selecting its build workflow.

## 5. GitHub Actions

Where supported, workflows should:

- Build the application using compatible cloud runners.
- Run available tests.
- Produce downloadable build artifacts.
- Provide clear error messages.
- Avoid committing generated secrets or credentials.
- Use pinned or controlled dependencies where practical.

Do not assume every project can be built for free or without
additional configuration.

## 6. Licensing and Security

- Review the original licence before modifying or redistributing code.
- Preserve required copyright notices and licence files.
- Identify third-party licence obligations.
- Never include passwords, access tokens, or private keys in source files.
- Do not disable security features merely to make a build succeed.

## 7. Working Method

- Plan before making significant changes.
- Explain important decisions.
- Make changes in manageable stages.
- Test changes where possible.
- Report completed work and unresolved issues.
- Request user approval before destructive or irreversible actions.

## 8. Handover Deliverables

Claude should prepare:

- README.md
- PROJECT_REQUIREMENTS.md
- DECISIONS.md
- CHANGELOG.md
- REVIEW.md
- handoff.md

Additional files and directories should be introduced only when needed.

## 9. Definition of Success

A user can create a new repository from the template, follow clear
instructions, configure a supported Windows application, build it
using an appropriate workflow, and download the resulting artifacts.
