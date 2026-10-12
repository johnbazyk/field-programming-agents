# Field Programming Agent Team — Generic Template

**Shareable template for security systems integrators**  
**Version:** 1.0  
**Purpose:** Spin up a small team of specialized AI agents (on a dedicated Grok Bot / SuperGrok account or similar multi-agent platform) for temporary on-site programming of cameras and IP systems.

This is a generic starting point. Replace the placeholders (marked `[like this]`) with your own brands, VMS, ticketing system, password rules, and standards. The core architecture, isolation model, and approval workflow stay the same.

See the full template content in this repository. Clone or fork to adapt for your company.

## Quick Start
1. Create a dedicated multi-agent account.
2. Create the five agents using the prompts in this README (or the agents/ folder once expanded).
3. Customize placeholders for your VMS, brands, password manager, and ticketing system.
4. Run isolation and bench tests before any real job.

## Core Principles
- Cellular-only internet + device-subnet isolation on the local interface.
- Plan (dry-run) → Approve → Execute → Verify for high-stakes writes.
- Generate credentials → store in password manager → then apply.
- Prefer structured APIs (ONVIF first).
- Field Supervisor is the single human interface.

Full detailed template, agent instructions, and adaptation notes are in the files of this repo.

---

*This repository provides a reusable multi-agent pattern for security integrators. Adapt freely.*
