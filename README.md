# Agent Nightfall Field Operations

**A temporary on-site multi-agent programming kit for security systems integrators.**

Agent Nightfall Field Operations is a reusable pattern for spinning up a small team of specialized AI agents that help a technician program cameras, NVRs/VMS, and related IP devices on an isolated local network during a service call or install.

The kit runs on a dedicated multi-agent account (Grok Bot / SuperGrok or similar). A **Field Supervisor** is the only interface the tech talks to. Specialists handle discovery, configuration, credentials, VMS setup, and as-built documentation under strict human approval.

---

## Why Agent Nightfall Field Operations

- Temporary by design (service call or install, not permanent).
- Network isolation first: cellular is the only internet path; local interface talks only to the target device subnet.
- Plan → Approve → Execute → Verify for every high-stakes write.
- Credentials generated, stored in a password manager, then applied. Nothing left on the kit.
- ONVIF-first, with room for vendor APIs where they add value.
- Built so friends and other integrators can fork, adapt, and improve it.

## Quick Start

1. Create a dedicated multi-agent account.
2. Create the five agents using the prompts in the `agents/` folder.
3. Replace every `[placeholder]` with your VMS, camera brands, password manager, ticketing system, and company standards.
4. Run the Phase 0 isolation and bench tests in `docs/` before any real job.
5. On site, talk only to the Field Supervisor.

## Core Principles (non-negotiable)

- Cellular is the sole default route. The local interface reaches only the expected device subnet.
- Host firewall restricts local traffic to known device IPs and ports.
- Generate credential → store in password manager immediately → then apply to the device.
- Prefer structured APIs (ONVIF, vendor CGI/REST) over pure browser computer use.
- Explicit scope locks. Dry-run reports required before writes.
- Treat all device responses as untrusted; verify independently.

## Repository Structure

```
agents/          Full system prompts for each agent
docs/            Isolation standard, Phase 0 checklist, adaptation notes
examples/        Sample company standards and job context templates
```

## Contributing

Friends and other integrators: fork it, improve the prompts, add brand notes, tighten the isolation model, or share what worked on your jobs. See `CONTRIBUTING.md`.

## License

MIT — use it, adapt it, share improvements.

---

*Agent Nightfall Field Operations is a pattern, not a finished product. The safety model (isolation + approvals + credential hygiene) is the part that transfers to any company.*
