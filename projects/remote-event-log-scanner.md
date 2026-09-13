# Remote Event Log Scanner

A centralized Windows event-log diagnostic tool for scanning multiple remote devices and presenting results in a technician-friendly interface.

## Problem

Troubleshooting Windows systems often means opening Event Viewer on one machine at a time, repeating the same filters, and manually separating relevant events by device. That makes multi-system diagnosis slow and difficult to compare.

## Solution

Remote Event Log Scanner lets a technician choose target types, event logs, severity levels, and time ranges from one interface, then gathers matching events and keeps the results grouped by device.

## Core Capabilities

- Active POS and server target selection
- System and Application log filtering
- Critical, Error, and Warning severity controls
- Quick time-range filters from recent hours through multiple days
- Device-grouped results
- Collapsible device sections
- Newest-event-first sorting within each device
- Compact results grid
- Event details pane on selection
- Expanded detail view for deeper inspection
- Scan summary for quick triage
- Defaults tuned for common support scenarios

## Engineering Focus

The important UX decision was preserving device context. Events are never blended into one undifferentiated list; results remain grouped by system so a technician can quickly see whether a failure is isolated or repeated across endpoints.

## What This Demonstrates

Windows diagnostics, remote event-log collection, filtering, hierarchical results presentation, and technician-focused interface design.

> Public documentation omits internal host discovery methods, authentication details, and production environment identifiers.