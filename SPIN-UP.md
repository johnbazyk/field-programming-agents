# Spin-Up Guide — Agent Nightfall Field Operations

Everything needed to stand up the full kit on a dedicated multi-agent account and configure the Windows field computer.

## Steps

1. Create or open the dedicated multi-agent account.
2. Create the agents using the prompts in `agents/`:
   - Field Supervisor
   - Device Programmer
   - VMS Programmer
   - Credentials Manager
   - Job Reporter ([Your Photo Documentation Tool])
   - Kit / Computer Manager
3. Configure the Windows 10 field computer per `docs/windows-kit-setup.md`.
4. Connect the account to your password manager, [Your Photo Documentation Tool], and ticketing system as required.
5. Fill in company standards in `examples/`.
6. Run Phase 0 isolation checks before any real job.
7. On site, the technician talks only to the Field Supervisor.

The Kit / Computer Manager tracks the host. The Job Reporter handles photo uploads and client report delivery after approval.

All high-stakes actions follow Plan → Approve → Execute → Verify.