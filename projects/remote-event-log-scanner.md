# Remote Event Log Scanner

A centralized Windows event-log diagnostic utility for scanning multiple remote devices and presenting results in a technician-friendly interface without losing per-system context.

## The Problem

Traditional Windows troubleshooting often means opening Event Viewer one machine at a time, repeating the same filters, copying event details manually, and trying to compare results across systems afterward. That process is slow and makes it difficult to tell whether an issue is isolated to one device or repeated across the environment.

## The Solution

Remote Event Log Scanner gives the technician one interface for choosing target types, Windows logs, severity levels, and time windows. It gathers matching events remotely, groups them by device, and provides a compact result view with deeper event details available on demand.

## Core Capabilities

- Active POS and infrastructure-server target modes
- System and Application log selection
- Critical, Error, and Warning severity filtering
- Quick time windows ranging from recent hours through multiple days
- Device-grouped result presentation
- Collapsible device sections
- Newest-event-first ordering within each system
- Scan summary for fast triage
- Compact primary results grid
- Single-click event details pane
- Expanded detail view for deeper investigation
- Defaults optimized for common technician workflows

## Engineering Focus

The most important interface decision was **preserving device context**. Events are never merged into one undifferentiated timeline. A technician can see which system generated an event, collapse systems that are not relevant, and compare patterns across endpoints without losing ownership of the evidence.

The utility also separates filtering from inspection: broad controls quickly reduce the search space, while the details pane keeps long event messages out of the main grid until the technician actually needs them.

## Reliability & UX Design

- Keep every event tied to its originating device
- Sort consistently within each device group
- Distinguish target discovery from event retrieval failures
- Use sensible default filters for common support cases
- Avoid overloading the main grid with full message text
- Make deeper event content available without leaving the workflow

## What This Demonstrates

Windows Event Log integration, remote diagnostics, hierarchical data presentation, filtering systems, multi-target troubleshooting, UI information architecture, and technician-focused desktop design.

## Technology

`Python` • `Windows Event Logs` • `Remote Administration` • `Desktop GUI` • `Filtering & Grouped Results`

> Public documentation omits internal host-discovery methods, authentication details, network information, and production environment identifiers.