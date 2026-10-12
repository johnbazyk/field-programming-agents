# Agent Nightfall Field Operations

**Generic temporary on-site multi-agent programming kit for security systems integrators.**

A reusable pattern for spinning up specialized AI agents that help a technician program cameras, NVRs/VMS, and related IP devices on an isolated local network during a service call or install. Includes host computer management and a photo/documentation reporting workflow.

The kit runs on a dedicated multi-agent account. A **Field Supervisor** is the only interface the tech talks to. Specialists handle devices, VMS, credentials, documentation, and the Windows host itself under strict human approval.

---

## Why this kit

- Temporary by design.
- Cellular-only internet + device-subnet isolation.
- Plan → Approve → Execute → Verify.
- Generate-then-store credentials. Nothing left on the kit.
- ONVIF-first.
- Host computer tracked by a dedicated agent.
- Photo and completion report workflow via [Your Photo Documentation Tool].
- Built so other integrators can fork, adapt, and improve it.

## Quick Start

1. Create a dedicated multi-agent account.
2. Create the agents from the prompts in `agents/`.
3. Replace every `[placeholder]` with your VMS, brands, password manager, photo tool, and standards.
4. Configure the Windows host per `docs/windows-kit-setup.md`.
5. Run Phase 0 isolation checks before any real job.
6. On site, talk only to the Field Supervisor.

See `SPIN-UP.md` for the full process.

## Core Principles

- Cellular sole default route. Local interface reaches only the expected device subnet.
- Host firewall restricts local traffic.
- Generate credential → store in password manager immediately → then apply.
- Prefer structured APIs.
- Explicit scope locks and dry-run reports.

## Structure

```
agents/          Full system prompts
docs/            Isolation, Windows host, photo workflow
examples/        Company standards template
SPIN-UP.md       How to stand up the entire kit
```

## Contributing

Fork it, improve the prompts, add brand notes, tighten isolation, or share what worked. See `CONTRIBUTING.md`.

MIT — use it, adapt it, share improvements.

---

*The safety model (isolation + approvals + credential hygiene + host tracking) is the part that transfers to any company.*