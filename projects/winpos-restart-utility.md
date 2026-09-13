# WinPOS Restart Utility

A lightweight remote-support utility for restarting POS application processes across active lanes with verification and operator-safe behavior.

## Problem

Restarting POS software across multiple lanes can require repeated remote sessions, manual process checks, and inconsistent timing. A reliable restart also needs to confirm that the application actually stopped before starting it again.

## Solution

The utility discovers active POS lanes, stops the application cleanly, confirms the process is no longer running, waits through a short stabilization period, and then restarts the application using a workflow designed to work both interactively and through remote-support tooling.

## Core Capabilities

- Active-lane discovery
- Verified application shutdown
- Controlled delay before restart
- Remote and local execution modes
- Interactive-session launch handling
- Hidden/silent behavior for remote-support execution
- Visible operator feedback for manual execution
- Per-lane status reporting

## Engineering Focus

The key challenge was not simply issuing stop/start commands; it was making the restart reliable across remote execution contexts where session visibility and process ownership differ from a normal desktop launch.

## What This Demonstrates

Windows process control, remote execution, session-aware automation, defensive verification, and small-tool UX design.

> Public documentation excludes internal host discovery details, deployment paths, credentials, and production environment information.