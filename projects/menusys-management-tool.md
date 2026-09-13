# Menusys Management Tool

A centralized Windows management utility for controlled configuration and deployment workflows across selected remote systems.

## The Problem

Configuration changes and file deployments become repetitive and risky when each endpoint must be handled independently. Technicians need a way to identify eligible systems, make the deployment scope explicit, stage approved content, and confirm what happened on every target.

## The Solution

The Menusys Management Tool provides one operator interface for discovering systems, selecting exactly which devices should be changed, staging source content, deploying it, and reviewing per-target results.

## Core Capabilities

- Centralized target discovery
- Explicit multi-select deployment scope
- Controlled source/staging workflow
- Selected-target file/configuration deployment
- Per-target progress reporting
- Clear success and failure outcomes
- Technician-oriented Windows GUI
- Reusable deployment pattern later applied to related utilities
- Operator-controlled target selection rather than automatic broad rollout

## Engineering Focus

The main design principle is **safe repeatability**. Source selection and target selection are kept separate so the operator can verify both before making a change. The tool also treats each remote system independently so a failure on one target does not obscure successful deployments elsewhere.

The project became a reference pattern for several later administration tools because it established a reliable structure for discovery, staging, selection, deployment, and result reporting.

## Reliability & Guardrails

- Discover and validate targets before deployment
- Require explicit target selection
- Separate the source artifact from destination scope
- Report results individually for each system
- Avoid assuming all systems share the same availability or state
- Keep operational feedback visible throughout the deployment

## What This Demonstrates

Configuration management, remote deployment, multi-target Windows automation, technician-facing GUI design, scope control, reusable workflow architecture, and error isolation.

## Technology

`Python` • `Windows GUI` • `Remote File Deployment` • `Configuration Management` • `Executable Packaging`

> Public documentation intentionally omits proprietary file names, internal system-discovery logic, credentials, production paths, and private configuration data.