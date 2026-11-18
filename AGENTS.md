# Altyn Knowledge Base — Agent Instructions

## Purpose
This repository is the shared knowledge base of the Altyn ecosystem.

It is used by:
- Human developers
- Hermes AI agent
- Other AI agents and automated tools
- Obsidian

## Core Rules

1. Read relevant documentation before making technical recommendations.
2. Treat documented facts as the primary source of project knowledge.
3. Never invent project architecture, API endpoints or implementation details.
4. Distinguish confirmed facts, assumptions and proposals.
5. Keep documentation in Markdown.
6. Preserve existing information when updating documents.
7. Never delete documentation without explicit permission.
8. Update documentation when significant project decisions change.
9. Use relative Markdown links between documents.
10. Keep documents understandable to both humans and AI agents.

## Documentation Format

Use YAML frontmatter where appropriate.

Example:

---
title: Document title
status: active
updated: YYYY-MM-DD
tags:
  - altyn
---

## Security

NEVER commit:
- Private keys
- Seed phrases
- Passwords
- API secrets
- Access tokens
- Private user information

## Agent Workflow

Before working:
1. Read README.md.
2. Read relevant project documentation.
3. Check current tasks and decisions.
4. Identify missing or contradictory information.

After working:
1. Document confirmed changes.
2. Update related documents.
3. Record important architectural decisions.
4. Do not commit or push without authorization.

## Knowledge Quality

Prefer:
- Facts over assumptions
- Sources over speculation
- Current information over outdated notes
- Small focused documents over huge files
