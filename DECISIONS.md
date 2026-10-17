# Project Decisions

This document records the agreed design decisions for the
Windows Application Customization Template.

## D001 — Primary Purpose

The repository is a reusable template for customizing existing
open-source Windows applications.

It is not intended to implement a new Windows application from scratch.

## D002 — Primary User Device

The user primarily manages projects from an Android phone.

Instructions and workflows must minimize the need for local development
tools and manual source-code editing.

## D003 — Preferred Build Environment

GitHub Actions is the preferred build environment.

Each application must use a workflow compatible with its technology,
dependencies, licence, and build requirements.

## D004 — Cost

Prefer free and open-source tools.

Do not introduce paid services, subscriptions, or APIs without
explaining the cost and obtaining user approval.

## D005 — Customization

Prioritize the following changes:

1. Application name.
2. Application logo and icons.
3. Publisher and product information.
4. Colours and interface text.
5. Minor feature adjustments.

Larger changes require separate planning.

## D006 — Preserve Original Functionality

Do not replace the original application architecture unnecessarily.

Prefer small, documented changes that preserve existing functionality.

## D007 — Licensing

Before importing or modifying an application, review its licence
and relevant third-party licences.

Do not remove required copyright notices or licence information.

## D008 — Security

Never commit credentials, private keys, passwords, or API secrets.

Do not weaken security controls merely to make a build succeed.

## D009 — User Approval

Ask the user before destructive changes, major architectural changes,
external publication, or actions with significant consequences.

Routine, reversible tasks may proceed within the approved requirements.

## D010 — Testing

Use the tests and validation procedures appropriate to each application.

Report which tests ran, which passed, and which could not be performed.

A successful build does not automatically mean the application
works correctly.

## D011 — Technology Flexibility

Do not assume all Windows applications use the same technology.

Select build workflows based on the actual source code.

## D012 — Documentation

Keep instructions concise, practical, and suitable for a user
working primarily from an Android phone.

Record significant changes and unresolved issues.
