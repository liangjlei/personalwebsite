# A Multi-Tenant Control Plane for Orchestrating Large Language Model Agents

**Jinglei Liang** · Systems Report, 2026

## Abstract
A control plane that turns a bare LLM-agent runtime into a team-ready platform:
multi-user, multi-model, and isolated per project/tenant, with the governance and
integrations needed for real internal delivery.

## Architecture
- **Control plane** (Hono + SQLite): users, API-key / OIDC auth, audit logging.
- **Unified streaming `invoke()`**: one API routing across four model families,
  with streaming responses.
- **Per-tenant assets**: skills, knowledge bases, and shared memory isolated by
  project.
- **Gateway bridge**: connects agent sessions to repository sync and webhooks for
  end-to-end workflows.

## Why it matters
Teams get consistent auth, auditing, and model routing without re-plumbing each
agent, and project data never leaks across tenants.

## Notes
Built atop an open-source agent runtime; the upstream project name, internal
hostnames, and organization identifiers are intentionally omitted.
