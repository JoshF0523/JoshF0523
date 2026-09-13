# Work Projects Portfolio

This section documents the operational software, Windows utilities, deployment tools, diagnostic systems, and hardware-maintenance workflows I have designed and built.

The common theme across these projects is **turning multi-step technical procedures into repeatable, technician-friendly workflows with clear validation and guardrails**.

> Public documentation is intentionally sanitized. Credentials, proprietary company data, internal network details, production hostnames, vendor payloads, private configuration values, and sensitive maintenance commands are not published.

---

## Diagnostics & Troubleshooting

### [POS Scan Utility 1.0](projects/pos-scan-utility.md)
A centralized GUI for multi-system POS health checks and diagnostic scanning. Designed to replace repetitive per-lane troubleshooting with a consistent operator workflow.

**Engineering areas:** remote administration, system health checks, GUI design, status normalization, technician UX.

### [Log Collector](projects/log-collector.md)
Collects the most useful configuration, application, journal, integration, and recent troubleshooting logs from selected remote systems into a clean diagnostic archive.

**Engineering areas:** remote file collection, time-window filtering, archive generation, GUI/CLI interoperability, support workflows.

### [Remote Event Log Scanner](projects/remote-event-log-scanner.md)
Searches Windows event logs across multiple devices using target, log, severity, and time filters while keeping results clearly separated by system.

**Engineering areas:** Windows event logs, remote querying, grouped result presentation, filtering, drill-down diagnostics.

---

## Deployment & Upgrade Automation

### [Service Pack Upgrade Utility](projects/service-pack-upgrade-utility.md)
Coordinates multi-target software upgrades across POS and server systems, including preflight checks, payload selection, installer monitoring, reboot detection, recovery, and post-upgrade restoration.

**Engineering areas:** fleet deployment, state machines, reboot-aware monitoring, remote process execution, package management, safety checks.

### [Healthy Benefits Upgrade Utility V1](projects/healthy-benefits-upgrade-utility.md)
A guided Version 1 multi-lane upgrade tool with explicit target selection, dedicated status scans, and post-upgrade Healthy Benefits verification.

**Engineering areas:** remote deployment, status scanning, post-maintenance verification, technician-facing workflow design.

### [Menusys Management Tool](projects/menusys-management-tool.md)
Centralizes controlled configuration and deployment actions across selected systems from one operator interface.

**Engineering areas:** target selection, remote deployment, configuration management, validation, GUI workflow design.

### [CFG Editor & Deployment Tool](projects/cfg-editor-deployment-tool.md)
Locates a valid source configuration environment, launches the correct editor workflow, and deploys the completed configuration only to selected eligible systems.

**Engineering areas:** source discovery, configuration lifecycle management, selected-target deployment, validation-first automation.

### [WinPOS Restart Utility](projects/winpos-restart-utility.md)
A remote-aware application restart workflow that discovers active systems, verifies shutdown, waits for a controlled interval, and restarts the application in the appropriate user context.

**Engineering areas:** Windows process lifecycle, interactive sessions, remote execution, context-aware behavior, lightweight automation.

---

## Hardware & Payment-System Maintenance

### [5916 Firmware Flash Utility](projects/5916-firmware-flash-utility.md)
Scans firmware state across active systems, identifies current versus outdated devices, coordinates firmware maintenance, handles vendor-tool display requirements, and verifies the completed write before offering shutdown actions.

**Engineering areas:** firmware integration, hardware state detection, vendor tool orchestration, verification-first workflows, fault isolation.

### [Pinpad Maintenance Utility](projects/pinpad-maintenance-utility.md)
A local payment-device servicing application for parameter setup, device inspection, driver maintenance, profile deployment, staged loading, reboot operations, and verification.

**Engineering areas:** payment hardware, Windows driver management, staged device loading, parameter validation, readiness-state tracking.

### [Remote PINPAD Maintenance Utility](projects/remote-pinpad-maintenance.md)
Coordinates a dependency-heavy remote payment-device maintenance workflow involving application state, maintenance mode, device loading, validation, and controlled completion.

**Engineering areas:** payment hardware, remote process control, state management, multi-step maintenance, recovery safeguards.

---

## Data, Mapping & Warehouse Operations

### [Mapping Utility](projects/mapping-utility.md)
Analyzes historical item data and produces compact product/department mapping ranges using department recognition, range inference, gap bridging, and UPC-family consolidation.

**Engineering areas:** data analysis, classification logic, range generation, CSV processing, business-rule automation.

### [QR Inventory Manager](projects/qr-inventory-manager.md)
A warehouse-focused QR inventory system supporting phone scanning, USB HID scanners, shared quantity updates, and simple `+1 / -1` adjustments.

**Engineering areas:** QR workflows, Google Sheets integration, desktop/mobile interoperability, scanner hardware, warehouse UX.

---

## Engineering Patterns Across the Portfolio

These projects repeatedly use the same engineering principles:

- **Discover before acting** — determine which systems are actually eligible or reachable.
- **Validate every transition** — do not assume a command succeeded because it was launched.
- **Preserve original state** — only restore or modify system state when the utility intentionally changed it.
- **Separate targets** — one failed system should not make the status of every other target ambiguous.
- **Use plain-language status** — technicians should not need to interpret raw command output to understand progress.
- **Design around the real workflow** — automate repetitive technical steps while keeping meaningful operator decisions visible.
- **Fail safely** — stop or isolate a target when required preparation or verification fails.

---

## Technology Areas

`Python` • `C# / .NET` • `Windows Forms` • `Windows Automation` • `PowerShell` • `Batch` • `Remote Administration` • `Desktop GUI` • `Executable Packaging` • `Windows Event Logs` • `Hardware/Firmware Integration` • `Payment Device Maintenance` • `QR Systems` • `Google Sheets` • `CSV/Data Processing` • `Deployment Orchestration` • `State Management`

---

### Portfolio Scope

The pages in this repository describe architecture, workflows, engineering decisions, and operator experience. Production source code for specialized workplace systems is not published where doing so could expose proprietary implementation details or operational security information.