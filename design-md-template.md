design-md-template
1. Metadata
page:
  name:
  type:
  product:
  platform:
  industry:

2. Metadata
Provide a high-level overview of platform performance,
operational health, AI agent activity,
cost efficiency, and business impact.

3. User Types
users:
  - Administrator
  - Operator
  - Analyst
  - Executive

4. Primary Goals
  goals:
  - Monitor platform health
  - Review agent performance
  - Identify anomalies
  - Take action quickly

5. Success Metrics
success_metrics:
  - Time to insight
  - Task completion rate
  - Error recovery rate
  - Engagement frequency

6. Layout Structure
layout:

  header:
    required: true

  sidebar:
    required: true

  content:
    layout: grid

  footer:
    required: false

7. Information Architecture
sections:

  - Overview KPIs

  - Trends

  - Alerts

  - AI Insights

  - Recent Activity

8. Component Mapping
components:

  kpis:
    organism: metric_card

  trends:
    organism: chart_container

  alerts:
    organism: alert

  activity:
    organism: activity_feed

9. States
states:

  loading:
    required: true

  empty:
    required: true

  success:
    required: true

  error:
    required: true

10. Responsive Behavior
responsive:

  desktop:
    columns: 12

  tablet:
    columns: 8

  mobile:
    columns: 4
  
11. Accessibility
accessibility:

  wcag: AA

  keyboard_navigation: true

  screen_reader: true

  visible_focus: true

12. Content Rules
content:

  tone:
    professional

  avoid:
    - jargon
    - ambiguity

  readability:
    medium

13. AI Rules
ai_rules:

  use_registry_components_only: true

  use_design_tokens_only: true

  do_not_create_custom_patterns: true

  do_not_skip_states: true

  generate_documentation: true

14. Codex Instructions
When generating this page:

1. Read ai-design-library-spec.md
2. Read figma-governance-spec.md
3. Read project-config.yaml
4. Read project-tokens.yaml
5. Read component-registry.yaml
6. Use existing registry items first
7. Generate layout
8. Generate states
9. Generate documentation
10. Run self-audit

