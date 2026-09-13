# Service Pack Upgrade Utility

A centralized deployment utility for coordinating software service-pack upgrades across POS systems and infrastructure servers while tracking preparation, installation, reboot, recovery, and protection-state restoration.

## The Problem

Service-pack rollouts across mixed device types can require different payloads, different eligibility checks, different launch methods, and different post-install behavior. Manually coordinating those steps across many systems increases the chance of skipping a prerequisite, losing track of a reboot, or leaving a system in the wrong protection state.

## The Solution

The Service Pack Upgrade Utility provides a single technician workflow for selecting a software version and service pack, discovering eligible targets, performing preflight checks, staging the correct payload, launching the upgrade, and monitoring each target through completion.

## Core Capabilities

- Separate discovery of POS systems and server systems
- Version and service-pack selection
- Payload management for multiple supported upgrade packages
- Target filtering and reachability checks
- Silent preflight validation before deployment
- Per-target upgrade-stage tracking
- Visible installer launch where operator visibility is required
- Reboot detection and return-online monitoring
- Automatic completion checks
- Protection-state awareness and restoration for POS systems
- Multi-target progress reporting
- Support for retaining upgrade payloads for follow-up or audit workflows

## Upgrade State Model

A target progresses through clear operational stages such as:

`STARTING → INSTALLER STARTED → INSTALLER RUNNING → WAITING FOR REBOOT → REBOOTING → BACK ONLINE → COMPLETE`

This makes a long-running deployment easier to understand than a simple success/failure message.

## Protection-State Handling

The utility records the pre-upgrade state of application protection on each POS target. Systems that require a temporary maintenance state are prepared before deployment and returned to their original protected state after the upgrade and reboot complete. Systems already in an acceptable maintenance state are preserved rather than unnecessarily changed.

## Engineering Focus

This project combines deployment orchestration, remote execution, state persistence, reboot monitoring, device-type-specific behavior, and rollback-minded preparation. The important engineering challenge is not merely starting an installer—it is knowing when the target is actually ready, when installation is still active, when it has rebooted, and when the environment has been restored correctly.

## Reliability & Guardrails

- Validate targets before copying upgrade files
- Block deployment when required preparation cannot be completed
- Keep per-target state rather than assuming the fleet is uniform
- Monitor through reboot instead of marking complete when the installer launches
- Restore only states the utility itself changed
- Preserve systems that were intentionally disabled or already in maintenance mode

## What This Demonstrates

Fleet deployment automation, remote process management, state machines, Windows administration, reboot-aware orchestration, multi-version package management, safety checks, and operational UI design.

> Public documentation intentionally omits company-specific payloads, internal system names, credentials, network topology, and proprietary upgrade commands.