# AI Design Library Specification (ai-design-library-spec.md)

## 1. Purpose

This repository exists to help Codex generate scalable, reusable, production-ready Figma Design Libraries.

The goal is not to generate screens.

The goal is to generate a high-quality design system that can be used across multiple projects.

Codex must prioritize:

- Reusability
- Consistency
- Scalability
- Accessibility
- Maintainability

---

## 2. Core Philosophy

This repository follows Atomic Design.

Hierarchy:

text Foundations → Atoms → Molecules → Organisms → Patterns → Templates 

Codex MUST follow this hierarchy.

Components must never skip levels.

---

## 3. Generation Strategy

Generation mode:

text Core First 

Codex MUST:

1. Generate Foundations
2. Generate Atoms
3. Generate Molecules
4. Generate Organisms
5. Generate Patterns
6. Generate Templates

Codex MUST NOT start from Templates.

Codex MUST NOT generate the entire library at once.

---

## 4. Discovery Mode

Default:

yaml discovery_mode: true 

When discovery mode is enabled:

Codex must ask questions before generating advanced components.

Questions may include:

- Industry
- Product type
- Platform
- Theme
- Density
- Accessibility target
- Visual style

When discovery mode is disabled:

Codex may continue using existing configuration files.

---

## 5. Project Configuration

Codex MUST read:

text project-config.yaml 

before generating anything.

Project configuration overrides default behavior.

---

## 6. Token System

Codex MUST read:

text project-tokens.yaml 

before generating components.

All visual decisions must be based on tokens.

Hardcoded values should be avoided whenever possible.

---

## 7. Color System

The provided primary color should be treated as:

text 500 

Codex must generate:

text 50 100 200 300 400 500 600 700 800 900 950 

for:

- Primary
- Secondary
- Neutral
- Success
- Warning
- Error
- Info

Naming:

text sys-color-primary-500 

---

## 8. Typography System

Input:

text Font Family 

Codex generates:

text Display Heading Title Body Label Caption 

Typography scale must be editable.

Codex should not lock typography decisions.

---

## 9. Layout System

Grid standards:

Desktop → 12 Columns

Tablet → 8 Columns

Mobile → 4 Columns

Admin Dashboard → Sidebar Layout

Responsive behavior is required.

---

## 10. Density System

Supported densities:

text Compact Comfortable Spacious 

All major components should support density variants.

---

## 11. Component Rules

Every component MUST:

✓ Use Auto Layout

✓ Use Variables

✓ Use Component Properties

✓ Use Nested Components

✓ Support Responsive Resizing

✓ Include Variants

✓ Include States

✓ Include Documentation

✓ Include Usage Notes

✓ Include Accessibility Notes

✓ Include Do / Don't Examples

✓ Include Token References

---

## 12. Variant Structure

Standard variant dimensions:

text Type Size State Theme Density Icon Layout Platform 

Use only necessary dimensions.

Avoid unnecessary complexity.

---

## 13. Accessibility

Target:

text WCAG AA 

Requirements:

- Visible focus states
- Accessible contrast
- Keyboard support
- Screen reader compatibility
- Minimum touch target
- Disabled states must not rely on color only

---

## 14. Supported Platforms

Supported platforms:

- Desktop
- Responsive Web
- Mobile
- Tablet
- Admin Dashboard

Platform-specific variants are allowed.

---

## 15. AI Components

The library supports AI-native experiences.

Examples:

- AI Assistant Panel
- Prompt Input
- Suggestion Chips
- Confidence Score
- Source Citation Card
- Human Review Status
- Agent Card
- Tool Call Log
- Automation Status

These components are optional unless requested.

---

## 16. Industry Registries

Before generating industry-specific components:

Codex MUST read:

text industry-priority.yaml 

Then load only relevant industry registries.

Do not load unrelated industries.

---

## 17. Governance

Design flow:

text Design ↓ Review ↓ Client ↓ Development 

Codex must respect governance rules defined in:

text figma-governance-spec.md 

---

## 18. Library Structure

Recommended Figma Pages:

text 00 Cover  01 Foundations  02 Atoms  03 Molecules  04 Organisms  05 Patterns  06 Templates  07 AI Components  08 Documentation  09 Playground 

---

## 19. Generation Priorities

Priority order:

text 1 Foundations  2 Core Inputs  3 Buttons & Actions  4 Navigation  5 Feedback  6 Data Display  7 Overlays  8 Forms  9 Tables  10 Dashboard Components  11 Mobile Patterns  12 AI Components 

---

## 20. Final Rule

Codex should always optimize for:

- Simplicity
- Reusability
- Scalability

When uncertain:

Prefer fewer components with stronger composition.

Do not generate complexity unless there is a clear requirement.