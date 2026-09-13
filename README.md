<p align="center">
  <img src="assets/portfolio-header.svg" width="100%" alt="Josh Floyd - Business Automation, Windows Systems, Practical Software">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-Desktop%20Automation-blue" alt="Python">
  <img src="https://img.shields.io/badge/Windows-Systems%20Engineering-0078D4" alt="Windows">
  <img src="https://img.shields.io/badge/PWA-Mobile%20First-purple" alt="PWA">
  <img src="https://img.shields.io/badge/Supabase-Backend-3ECF8E" alt="Supabase">
  <img src="https://img.shields.io/badge/Vercel-Deployment-black" alt="Vercel">
  <img src="https://img.shields.io/badge/Automation-Operations-success" alt="Automation">
</p>

## About Me

I build practical software that turns repetitive, technical, or error-prone workflows into **simple, repeatable tools with clear status, verification, and guardrails**.

My projects span household budgeting, warehouse inventory, Windows diagnostics, POS administration, remote deployment, firmware maintenance, configuration management, data mapping, and payment-device support.

A large part of my work focuses on a specific challenge: taking procedures that normally require a technician to perform many manual steps across multiple systems and turning them into a controlled workflow that is easier to run, easier to understand, and harder to perform incorrectly.

---

## Flagship Applications

### 💵 [Monthly Bill Calendar](projects/monthly-bill-calendar.md)
A mobile-first household budgeting application built around **which paycheck should pay each bill**, not simply when the bill is due.

`PWA` • `Supabase` • `Vercel` • `Multi-user Sync` • `Pay-cycle Logic`

### 📦 [QR Inventory Manager](projects/qr-inventory-manager.md)
A warehouse-focused inventory system combining printable QR labels, phone scanning, USB HID scanners, desktop support, and shared quantity updates.

`QR` • `Google Sheets` • `Google Apps Script` • `Windows` • `Scanner Hardware`

---

# Professional Work Portfolio

➡️ **[View the complete categorized Work Projects Portfolio](WORK_PROJECTS.md)**

## Diagnostics & Troubleshooting

| Project | Purpose | Engineering Focus |
|---|---|---|
| **[POS Scan Utility 1.0](projects/pos-scan-utility.md)** | Centralized multi-system POS health and diagnostic scanning | Remote administration • GUI • Health checks |
| **[Log Collector](projects/log-collector.md)** | Automated collection of current troubleshooting files into a clean archive | Remote files • Filtering • ZIP packaging |
| **[Remote Event Log Scanner](projects/remote-event-log-scanner.md)** | Multi-device Windows event-log analysis with grouped results and drill-down details | Event logs • Filtering • Diagnostics UX |

## Deployment, Upgrades & Configuration

| Project | Purpose | Engineering Focus |
|---|---|---|
| **[Service Pack Upgrade Utility](projects/service-pack-upgrade-utility.md)** | Coordinates multi-target upgrades through install, reboot, recovery, and completion | Deployment orchestration • State machines • Reboot monitoring |
| **[Healthy Benefits Upgrade Utility V1](projects/healthy-benefits-upgrade-utility.md)** | Guided V1 remote upgrade workflow with explicit lane selection and post-upgrade HB verification | Remote deployment • Status scanning • Verification |
| **[Menusys Management Tool](projects/menusys-management-tool.md)** | Centralized configuration and selected-target deployment management | Configuration • Deployment • Operator workflow |
| **[CFG Editor & Deployment Tool](projects/cfg-editor-deployment-tool.md)** | Source discovery, controlled configuration editing, and selected-lane deployment | Discovery • Configuration lifecycle • Validation |
| **[WinPOS Restart Utility](projects/winpos-restart-utility.md)** | Verified remote application restart with context-aware execution | Process lifecycle • Interactive sessions • Remote automation |

## Hardware & Payment-System Maintenance

| Project | Purpose | Engineering Focus |
|---|---|---|
| **[5916 Firmware Flash Utility](projects/5916-firmware-flash-utility.md)** | Scans, updates, and verifies display firmware across active systems | Firmware • Hardware integration • Verification-first automation |
| **[Pinpad Maintenance Utility](projects/pinpad-maintenance-utility.md)** | Local payment-device servicing, driver maintenance, profile deployment, and staged loading | Payment hardware • Drivers • State/timer management |
| **[Remote PINPAD Maintenance Utility](projects/remote-pinpad-maintenance.md)** | Coordinates complex remote payment-device maintenance and recovery | Payment hardware • State management • Process control |

## Data & Operational Automation

| Project | Purpose | Engineering Focus |
|---|---|---|
| **[Mapping Utility](projects/mapping-utility.md)** | Converts historical product data into compact department mapping ranges | CSV analysis • Classification • Range inference |
| **[QR Inventory Manager](projects/qr-inventory-manager.md)** | Fast warehouse quantity maintenance by QR or USB scanner | Inventory • QR • Shared data |

---

## How I Design Automation

My work repeatedly follows the same engineering principles:

**Discover before acting.** Determine which systems are online, eligible, or in the correct state before making changes.

**Verify transitions.** A command being launched is not the same as a task being completed. Important state changes are checked before the workflow moves forward.

**Preserve original state.** When a utility temporarily changes a system for maintenance, it tracks what it changed and restores only what it owns.

**Keep targets independent.** In multi-system operations, one failed device should not make the status of successful devices unclear.

**Use technician-friendly status.** Operator-facing tools should explain what is happening in plain language rather than exposing unnecessary command-line noise.

**Fail safely.** If preparation or verification fails, the tool should stop, isolate the affected target, or clearly identify what requires attention.

---

## Technology & Engineering Areas

### Desktop & Windows
`Python` • `C# / .NET` • `Windows Forms` • `Windows GUI Applications` • `PowerShell` • `Batch` • `Remote Administration` • `Process Management` • `Executable Packaging`

### Systems & Operations
`Deployment Automation` • `Configuration Management` • `Windows Event Logs` • `Remote Diagnostics` • `Reboot Monitoring` • `State Machines` • `Fleet Operations`

### Hardware & Integration
`Firmware Maintenance` • `Payment Peripherals` • `QR Scanners` • `USB HID Devices` • `POS Hardware Workflows`

### Web, Mobile & Data
`Progressive Web Apps` • `Supabase` • `Vercel` • `Google Sheets` • `Google Apps Script` • `CSV Processing` • `Mobile-first UX`

---

## Public Portfolio & Security

Some projects were created for specialized workplace environments. Public documentation intentionally omits credentials, internal infrastructure, production hostnames, private configuration values, proprietary payloads, sensitive maintenance commands, and employer-specific operational data.

The goal of this portfolio is to demonstrate the **engineering approach, workflow design, reliability logic, automation patterns, and user experience** without exposing production environments.

---

<p align="center">
  <b>Simple interfaces. Reliable automation. Real-world usefulness.</b>
</p>