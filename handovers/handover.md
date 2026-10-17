# HANDOVER TO CLAUDE
# Windows Application Customization Template

## 1. Your Role

Act as a senior software engineer, Windows application build
engineer, and GitHub Actions specialist.

Your task is to inspect this repository and implement a reusable,
secure, well-documented GitHub template for customizing existing
open-source Windows applications.

Do not merely describe what should be done. Implement the project,
create the necessary files, test your work, and report the results.

## 2. Project Objective

The user wants to take suitable open-source Windows applications
and create customized versions with:

- A new application name.
- Their own logo and icons.
- Custom publisher and product information.
- Adjustments to colours, text, and interface appearance.
- Minor feature modifications where necessary.
- Downloadable Windows application builds.

The original application's core functionality should be preserved
unless the user explicitly approves a change.

The result must be reusable for future application projects.

## 3. User Environment and Constraints

- Primary device: Android phone.
- Repository management: GitHub website or mobile app.
- Coding assistance: Claude.
- Preferred build environment: GitHub Actions.
- Budget: Prefer free tools and services.
- Local Windows development: Avoid requiring it unless necessary.
- File transfer: Prefer ZIP-based handovers and GitHub uploads.
- The user may not have advanced programming knowledge.

Provide simple, step-by-step instructions suitable for mobile use.

Do not assume the user can install Android Studio or other large
development environments.

Do not require paid APIs, subscriptions, or external services
without explaining the cost and obtaining approval.

## 4. First Inspect the Existing Repository

Before creating or changing files:

1. Inspect the complete repository structure.
2. Read README.md.
3. Read DECISIONS.md.
4. Read CHANGELOG.md.
5. Read REVIEW.md.
6. Read handovers/PROJECT_REQUIREMENTS.md.
7. Read this handover.
8. Identify missing documentation and conflicting instructions.
9. Produce a concise implementation plan.

Preserve existing work unless there is a documented reason to change it.

Do not restart the project or replace existing files unnecessarily.

## 5. Important Technical Reality

Windows applications use different programming languages, build
systems, dependency managers, and packaging formats.

There is no single build command or workflow that works for every
Windows application.

The template must therefore separate:

A. Common project configuration and documentation.

B. Application-specific source code and modifications.

C. Technology-specific build and packaging procedures.

D. GitHub Actions workflows.

Never claim universal compatibility without testing it.

## 6. Required Template Features

### 6.1 Application Configuration

Design a clear configuration system for supported applications.

Where the original application permits these changes, configuration
should cover:

- Application name.
- Internal product name.
- Publisher name.
- Version.
- Logo and icon locations.
- Package identifier, where applicable.
- Product description.
- Website and support information.
- Application-specific customization options.

Document which fields can be configured automatically and which
require manual source-code changes.

Do not promise that changing a configuration file will automatically
rename every application.

### 6.2 Branding Assets

Provide a documented location for:

- Application logos.
- Windows executable icons.
- Installer icons.
- Splash screen assets, where supported.
- Other branding resources.

Explain supported image formats, dimensions, and conversion
requirements.

Preserve the original assets until replacements have been tested.

### 6.3 Source Application Integration

Provide a clear procedure for importing an existing open-source
Windows application.

The procedure must explain:

1. How to identify the original source repository.
2. How to check the software licence.
3. How to obtain the source code.
4. How to identify the technology and build system.
5. How to identify branding resources.
6. How to configure the application.
7. How to apply and document changes.
8. How to build and test the result.

Avoid destructive replacement of the template's own configuration.

Do not automatically merge unrelated source repositories without
an explicit, documented procedure.

### 6.4 Technology-Specific Build Support

Assess the feasibility of supporting these technologies:

- C# and .NET.
- C and C++.
- Python.
- Electron.
- JavaScript and TypeScript desktop applications.
- Other Windows-compatible frameworks when required.

Prioritize a practical initial implementation rather than attempting
to implement every technology at once.

For each supported technology, document:

- Required source files.
- Build tools.
- Dependencies.
- Build commands.
- Packaging procedure.
- Expected output.
- Known limitations.

Implement only workflows that can be justified by the repository
structure and tested appropriately.

Do not create workflows that claim to support a technology but
cannot actually build an application using it.

### 6.5 GitHub Actions

Use GitHub Actions for cloud builds where supported.

Provide an appropriate workflow structure that can:

- Validate project configuration.
- Check required files.
- Install or configure required build tools.
- Restore dependencies.
- Run available tests.
- Build the Windows application.
- Package the result where supported.
- Upload successful build outputs as downloadable artifacts.
- Report failures clearly.

Prefer Windows runners for builds requiring a Windows environment.

Use appropriate workflow permissions, dependency controls, and
timeouts.

Do not expose secrets in logs or generated artifacts.

Do not automatically publish releases or distribute applications
externally without user approval.

### 6.6 Build Artifacts

Explain how to download build outputs from GitHub Actions using
an Android phone.

Distinguish between:

- Executable files.
- Portable application packages.
- Installers.
- MSIX packages.
- Other framework-specific outputs.

Do not promise an installer when the build produces only an executable.

### 6.7 ZIP-Based Workflow

Design a practical ZIP-based workflow where it improves mobile use.

The user should be able to prepare source files, configuration,
branding assets, or approved changes as a ZIP archive.

Before implementing automated ZIP extraction:

- Define the accepted directory structure.
- Reject path traversal and unsafe archive entries.
- Reject symbolic links unless explicitly required and safely handled.
- Prevent overwriting protected workflow and configuration files.
- Define duplicate-file handling.
- Validate file types and archive contents.
- Report rejected files clearly.

Do not implement a ZIP upload mechanism merely for convenience
if a safer and simpler method is more appropriate.

Document any manual steps the user must perform.

### 6.8 Documentation

Maintain concise, accurate documentation.

The project should explain:

- What the template does.
- What it does not do.
- How to create a new repository from the template.
- How to configure branding.
- How to import source code.
- How to choose a supported build workflow.
- How to run builds.
- How to download artifacts.
- How to troubleshoot failures.
- How to review licences.
- How to maintain customized application versions.

## 7. Licensing and Copyright

Before implementing a real application customization, inspect its licence.

The template must instruct users to:

- Preserve required copyright notices.
- Preserve licence files.
- Comply with redistribution conditions.
- Review third-party dependency licences.
- Check trademark restrictions.
- Avoid implying official affiliation with the original publisher.

Do not assume that open-source software can always be redistributed
under a different name or logo without restrictions.

Do not remove notices required by the original licence.

## 8. Security

Apply secure defaults.

Requirements:

- Never commit passwords, API keys, or private tokens.
- Avoid unnecessary workflow permissions.
- Pin or control dependencies where practical.
- Avoid executing untrusted scripts.
- Validate archive extraction.
- Do not use pull-request code with privileged secrets.
- Avoid unsafe shell interpolation.
- Do not download or execute unverified binaries.
- Do not disable security controls to make builds succeed.

Document unresolved security concerns.

## 9. Testing Requirements

Create tests appropriate to the implemented features.

Where applicable, test:

- Configuration validation.
- Missing required files.
- Invalid configuration values.
- Branding asset validation.
- ZIP archive validation.
- Workflow configuration.
- Build output generation.

Use a testable sample or fixture only when necessary.

Do not include an unrelated complete application simply to
demonstrate the template.

Clearly distinguish between:

- Tests that passed.
- Tests that failed.
- Tests that were not run.
- Tests requiring a real application.

A successful YAML validation is not proof that a Windows application
builds successfully.

A successful compilation is not proof that the application works.

## 10. Required Repository Documentation

Create or update the following files:

- README.md
- PROJECT_REQUIREMENTS.md
- DECISIONS.md
- CHANGELOG.md
- REVIEW.md
- handoff.md

Preserve the existing handovers/PROJECT_REQUIREMENTS.md file.

Avoid unnecessary duplication between the root documentation and
the handovers folder.

Create any additional documentation or folders that are genuinely
needed.

Update CHANGELOG.md with the actual changes made.

Update REVIEW.md with real test results.

Update handoff.md with the final project status and instructions
for continuing the work.

## 11. Implementation Rules

Work in manageable stages.

First inspect the repository and prepare the implementation plan.

Then implement the common configuration, documentation, validation,
and initial build workflow.

Do not implement speculative features that cannot be tested.

Prefer maintainable, straightforward solutions over unnecessary
complexity.

Avoid adding dependencies without a clear reason.

Do not delete existing user files.

Do not make unsupported claims about compatibility or security.

If an important decision cannot be made safely, explain the
alternatives and ask the user.

## 12. GitHub Delivery

The user manages projects primarily from an Android phone.

Where possible, prepare changes in a form that can be uploaded
through GitHub or delivered as a ZIP archive.

If working through a local or cloud development environment:

1. Inspect the existing repository.
2. Implement the planned changes.
3. Run available tests.
4. Review the resulting file structure.
5. Prepare a ZIP containing the required project files if requested.
6. Exclude secrets, caches, temporary files, and unnecessary build output.
7. Provide concise upload instructions.

Do not claim to have committed files to GitHub unless that action
actually occurred.

## 13. Final Report

When implementation is complete, report:

1. What was implemented.
2. The final directory structure.
3. Files created or changed.
4. Supported technologies and their limitations.
5. Tests performed and their results.
6. Whether any real Windows application was successfully built.
7. How to create a new repository from the template.
8. How to customize an application's name and logo.
9. How to run GitHub Actions.
10. How to download build artifacts from Android.
11. Known limitations and outstanding work.
12. The recommended next step.

Use one of these final statuses:

- READY FOR TESTING
- READY FOR USE WITH DOCUMENTED LIMITATIONS
- NEEDS FIXES
- BLOCKED

Never report READY FOR USE merely because files were created.

## 14. Start Here

Inspect the repository and report the implementation plan first.

After the plan is established, proceed with the implementation
within the approved requirements.

The immediate objective is a practical, reusable Windows
application customization template—not a claim that every
open-source Windows application can be customized automatically.
