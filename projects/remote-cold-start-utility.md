# Remote Cold Start Utility

A remote POS maintenance utility designed to coordinate a controlled application restart and initiate a predefined safe cold-start workflow without requiring a technician to stand at each lane.

## Problem

Some recovery procedures require more than simply restarting the POS application. The application must close, restart in an interactive user session, enter a maintenance menu during startup, and choose the correct recovery option. Performing that manually across multiple lanes is slow and difficult to standardize.

## Solution

The utility centralizes lane discovery and orchestrates the restart sequence while checking for process state, remote-worker handshakes, and successful transitions before reporting completion.

## Core Capabilities

- Active-lane discovery and filtering
- Verified POS application shutdown
- Interactive-session restart handling
- Startup-time maintenance workflow coordination
- Per-lane progress and error reporting
- Handshake-based validation of remote workers
- Guardrails to avoid reporting success before the required state is reached

## Engineering Focus

This project exposed the difficulties of automating applications whose maintenance options depend on interactive keyboard input during a narrow startup window. The design evolved around stronger handshakes, process verification, and state-aware reporting rather than assuming that a launched command completed successfully.

## What This Demonstrates

Remote Windows automation, timing-sensitive workflows, process lifecycle management, interactive-session challenges, and iterative troubleshooting.

> Public documentation intentionally omits proprietary menu sequences, internal discovery queries, credentials, and environment-specific commands.