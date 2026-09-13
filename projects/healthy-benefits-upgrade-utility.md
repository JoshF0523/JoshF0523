# Healthy Benefits Upgrade Utility

A remote multi-lane upgrade utility that standardizes software deployment while preserving each target system's pre-existing protection state.

## Problem

Upgrading software across many POS lanes is risky when each lane may be in a different system-protection state. A reliable tool has to prepare only the lanes that need preparation, run the upgrade visibly and interactively, verify completion, and restore only the settings it changed.

## Solution

The utility discovers qualifying lanes, records each lane's starting state, performs state-aware preparation when required, runs the upgrade, verifies progress, and returns only the lanes it changed back to their original protected state.

## Core Capabilities

- Multi-lane selection with no targets preselected
- Read-only system-protection status scans
- State-aware upgrade preparation
- Preservation of systems already disabled or already in maintenance/update mode
- Verified transition before deployment begins
- Controlled upgrade launch and monitoring
- Post-upgrade verification
- Automatic return to protected mode only when the utility made the original change
- Separate health/status scan functions
- Package-management workflow for updating embedded deployment payloads

## Engineering Focus

The most important design principle is state preservation. The utility does not assume every endpoint starts the same way and does not blindly force a common end state. Instead, it records the initial state, changes only what is necessary, and restores only what it changed.

## What This Demonstrates

Remote deployment, state-machine design, transactional rollback thinking, endpoint protection integration, package management, and technician-centered UI design.

> Public documentation intentionally excludes credentials, internal commands, proprietary package names, network topology, and production configuration.