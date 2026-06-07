AI Design Library Generator
Generate scalable Figma Design Libraries using Codex.

Purpose

This repository provides a structured framework for generating production-ready Figma Design Libraries.

The system is based on:

* Atomic Design
* Design Tokens
* Reusable Components
* Industry Registries
* AI-Assisted Library Generation

How It Works

Codex follows this process:
1. Read README.md

2. Read ai-design-library-spec.md

3. Read project-config.yaml

4. Read project-tokens.yaml

5. Read component-registry.yaml

6. Read industry-priority.yaml

7. Load relevant industry registries

8. Generate Foundations

9. Generate Components

10. Generate Documentation

Repository Structure
design-library-system/

├─ README.md

├─ ai-design-library-spec.md
├─ design-md-template.md
├─ figma-governance-spec.md

├─ project-config.yaml
├─ project-tokens.yaml
├─ component-registry.yaml
├─ industry-priority.yaml

└─ registries/

Key Files
file:ai-design-library-spec.md   
purpose:Main generation rules

file:project-config.yaml         
purpose:Project configuration

file:project-tokens.yaml         
purpose:Token definitions

file:component-registry.yaml    
purpose:Component inventory

file:industry-priority.yaml      
purpose:Industry loading rules

file:design-md-template.md      
purpose:Page specification template

file:figma-governance-spec.md    
purpose:Figma workflow rules

Example Prompt
Read this repository.

Create a design library for:

Industry: Banking
Platform: Mobile App
Style: Corporate
Theme: Light

Generate Foundations first.
Ask before generating advanced components.

Supported Industries
Banking
Insurance
Fintech
Mobility
AI Platform

Core Principle
Generate less.
Reuse more.
Compose everything.

