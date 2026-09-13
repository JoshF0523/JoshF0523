# Menusys Management Tool

A centralized Windows management utility for controlled configuration and deployment workflows across selected remote systems.

## The Problem

Configuration changes and file deployments across multiple endpoints can become repetitive and error-prone when each machine must be handled separately.

## The Solution

The Menusys Management Tool gives the operator one place to discover eligible systems, choose specific targets, stage approved content, deploy it, and review the outcome.

## Key Features

- Centralized target discovery
- Multi-select deployment workflow
- Controlled source/staging process
- Per-target progress and result reporting
- GUI designed around technician workflows
- Reusable deployment pattern for related administration tools
- Guardrails that keep the operator in control of which systems are changed

## Engineering Focus

The project is centered on safe repeatability: separate source selection from target selection, make the deployment scope explicit, and provide clear feedback for each remote system.

## Technology

- Python
- Windows GUI development
- Remote file deployment
- Configuration-management workflows
- Executable packaging

## Status

Developed as a proven management pattern and used as a reference design for later remote deployment utilities.

> Public documentation intentionally omits proprietary file names, internal system-discovery logic, credentials, private paths, and production configuration data.
