figma-governance-spec.md v1.0

1. Purpose

This document defines the governance model used when creating, maintaining, reviewing, publishing, and handing off Figma assets.

The purpose is to:

* Maintain a single source of truth.
* Prevent file duplication and divergence.
* Protect internal design work from client visibility.
* Ensure development receives approved assets only.
* Standardize collaboration between UX, UI, Research, Product, and Development teams.
* Enable Codex to operate consistently across projects.

⸻

2. Governance Principles

Principle 01 — Single Source of Truth

Every component has exactly one master source.

Never create duplicate master components.

⸻

Principle 02 — Design Happens in Design Files

Design work must only occur inside Design Files.

Never create or modify designs in:

* Client Files
* Development Files

⸻

Principle 03 — Approval Before Handoff

Nothing moves to Client or Development before review.

⸻

Principle 04 — Published Components Are Controlled Assets

Published components are production assets.

Changes require governance.

⸻

Principle 05 — Branch First

When branching is available:

All design work starts in a branch.

Never work directly on Main.

⸻

3. Workspace Structure

Project

01 Research

02 UX

03 UI

04 Review

05 Client

06 Development

99 Archive

⸻

4. File Lifecycle

Design
↓
Review
↓
Client
↓
Development
↓
Released

Design

Purpose:

Exploration and creation.

Allowed:

✓ Create screens

✓ Create components

✓ Create variants

✓ Create patterns

✓ Create templates

Forbidden:

✗ Client review

✗ Development handoff

Review

Purpose:

Internal validation.

Allowed:

✓ Stakeholder review

✓ UX review

✓ UI review

✓ Accessibility review

Forbidden:

✗ New exploration

✗ New features

⸻

Client

Purpose:

Approved design presentation.

Allowed:

✓ Feedback

✓ Comments

✓ Validation

Forbidden:

✗ Design System Editing

✗ New Components

✗ Experiments

✗ Internal Notes

⸻

Development

Purpose:

Implementation source.

Allowed:

✓ Dev Mode

✓ Specifications

✓ Measurements

✓ Assets

Forbidden:

✗ Explorations

✗ Draft Work

✗ Research Notes

⸻

5. Branch Governance

Structure
Main
│
├── Feature
├── Feature
├── Feature

Rules

Never modify Main directly.

All changes start in a branch.

Every branch must:

* Have an owner
* Have a scope
* Have a review

Naming

feature/account-settings

feature/dashboard-redesign

feature/payment-flow

bugfix/table-density

experiment/ai-assistant

⸻

6. Branch Governance

Core Components

Examples:

Button
Input
Select
Checkbox
Radio

Rules:

Can affect every project.

Must be reviewed.

Advanced Components

Examples:

Table
Data Grid
Chart Container
Dashboard Widget

Rules:

May depend on Core Components.

Cannot modify Core Components.

Industry Components

Examples:

Account Card
Policy Card
Transaction Row

Rules:

Must extend the Core Library.

Must not fork Core Components.

⸻

7. Branch Governance

Created
↓
Reviewed
↓
Documented
↓
Accessibility Checked
↓
Published

Every component must pass:

✓ Auto Layout

✓ Variables

✓ Component Properties

✓ Variants

✓ Responsive Behavior

✓ Documentation

✓ Accessibility Notes

✓ Do / Don’t Examples

⸻

8. Client File Rules

Client Files must contain:

✓ Approved Screens

✓ Approved Flows

✓ Approved Components

✓ Approved Prototypes

Client Files must NOT contain:

✗ Drafts

✗ Explorations

✗ Design Tokens

✗ Component Playground

✗ Research Notes

✗ Internal Documentation

✗ Deprecated Screens

⸻

9. Development File Rules

Development Files must contain:

✓ Approved Screens

✓ Approved Components

✓ Documentation

✓ Assets

✓ Dev Mode References

Development Files must NOT contain:

✗ Experiments

✗ Draft Variants

✗ Research Notes

✗ Deprecated Components

✗ Hidden Design Work

⸻

10. Naming Standards

Components

Button/Primary/Default

Button/Secondary/Default

Input/Text/Default

Navigation/Side/Expanded

Patterns

Pattern/List

Pattern/Detail

Pattern/Reporting

Pattern/Onboarding

Templates

Template/Dashboard

Template/Form

Template/Analytics

Template/AI Workspace

⸻

11. Accessibility Governance

Every published component must:

✓ Support keyboard navigation

✓ Support visible focus states

✓ Meet WCAG AA contrast requirements

✓ Support screen readers when applicable

✓ Use semantic naming

⸻

12. Codex Governance Rules

Codex MUST:

* Read ai-design-library-spec.md first
* Read project-config.yaml second
* Read project-tokens.yaml third
* Read component-registry.yaml fourth
* Generate Foundations before Components
* Generate Core Components before Advanced Components
* Generate Advanced Components before Industry Components
* Generate Industry Components before Templates
* Use Auto Layout everywhere
* Use Variables everywhere
* Use Tokens everywhere
* Document every component
* Run self-audit before completion

Codex MUST NOT:

* Create duplicate components
* Create visual values without tokens
* Modify Client Files
* Modify Development Files
* Modify Main directly when Branching exists
* Publish undocumented components
* Publish inaccessible components

⸻

13. MStudio Workflow

Research
↓
UX
↓
UI
↓
Review
↓
Client
↓
Development
↓
Release

Additional Rules:

* Research outputs stay in Research files.
* UX outputs stay in UX files.
* UI outputs become the source for Review.
* Client receives approved outputs only.
* Development receives approved outputs only.
* Archive deprecated work instead of deleting it.

