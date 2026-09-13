# Pinpad Maintenance Utility

A local Windows payment-device servicing application that guides technicians through parameter setup, device inspection, driver maintenance, configuration/profile deployment, staged software loading, reboot operations, and status verification.

## The Problem

Local pinpad maintenance can require many tightly ordered steps. The technician must identify the correct device family and lane parameters, use the proper communication settings, select the right operation, wait through device-controlled loading stages, interpret progress correctly, and avoid rebooting the PC unless an installation actually succeeded.

When those steps are performed manually, the process is slower and more vulnerable to configuration mistakes or incomplete maintenance.

## The Solution

Pinpad Maintenance Utility provides a structured local workflow where the technician first establishes the lane/device parameters and then performs only the maintenance actions appropriate to that setup.

The application separates **parameter selection** from **operations**, making the current device context visible before the technician begins a change.

## Core Capabilities

- Device information and status inspection
- Required lane-parameter setup before maintenance actions are enabled
- Device reboot controls
- Driver installation and replacement workflows
- Driver verification before Windows restart
- Device-profile/configuration deployment
- Support for multiple approved payment-device profiles
- Full and quick-load workflows
- Multi-stage device loading with visible progress
- Device-downloader installation
- Per-stage readiness timers
- Clear completion and failure status
- Light and dark interface modes for technician use

## Device Loading Workflow

Long-running loads are presented as explicit stages rather than one opaque operation. The utility tracks transfer progress separately from fixed device-readiness timing so a completed file transfer does not incorrectly imply that the device is immediately ready for the next stage.

Quick-load workflows can skip stages that are not required while preserving the same completion and timing rules for the remaining stages.

## Driver Maintenance

The driver workflow is designed to be verification-first:

1. Detect and remove an existing supported driver when necessary.
2. Install the approved driver for the current Windows architecture and selected communication port.
3. Verify that the expected driver is registered successfully.
4. Schedule a Windows restart only after successful installation and verification.

A failed uninstall, install, or verification does **not** trigger an automatic reboot.

## Protection-State Awareness

The utility checks whether the local system is in an appropriate maintenance state before preparing its embedded service payload. If application protection would block the maintenance package, the technician receives a clear instruction rather than a generic extraction or access-denied error.

The tool does not silently change protection state during startup; that decision remains explicit to the technician.

## Engineering Focus

This project combines local hardware integration, parameter validation, staged device operations, timer/state coordination, software-driver maintenance, verification logic, and operator safety.

A key design principle is that **progress, completion, and readiness are different states**. The interface reflects those differences rather than reporting success too early.

## Reliability & Guardrails

- Require complete device parameters before unlocking maintenance operations
- Verify driver installation before allowing restart behavior
- Never manufacture a successful load merely because a timer expired
- Keep file-transfer completion separate from device-readiness timing
- Preserve clear stage-by-stage status during long operations
- Block startup early when system protection would prevent maintenance files from loading
- Keep advanced actions explicit and technician-driven

## What This Demonstrates

Payment-peripheral maintenance, Windows driver management, hardware communication setup, staged workflow orchestration, state-machine design, timer coordination, embedded payload management, validation-first automation, and technician-focused GUI design.

## Technology

`C# / .NET` • `Windows Forms` • `Payment Device Maintenance` • `Driver Installation` • `Embedded Payloads` • `State & Timer Management`

> Public documentation intentionally omits maintenance credentials, vendor payloads, device certificates, proprietary profiles, protected system commands, and production-specific configuration values.