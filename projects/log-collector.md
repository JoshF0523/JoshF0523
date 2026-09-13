# Log Collector

A technician-focused Windows diagnostic utility that gathers the evidence needed for troubleshooting from multiple remote systems and packages it into one clean support archive.

## The Problem

Distributed POS environments generate useful diagnostic information in many different locations: application logs, configuration files, transaction journals, integration logs, API logs, and date-based diagnostic folders. Gathering that information manually requires a technician to connect to each system, locate multiple paths, determine which files are recent enough to matter, copy them, and organize the results before troubleshooting can even begin.

## The Solution

Log Collector turns that preparation work into a repeatable collection workflow. The technician selects one or more systems—or launches the collector through a scripted command—and the utility gathers the required files, applies age filters to time-based logs, keeps data separated by device, and creates a single archive for review.

## Core Capabilities

- Multi-system remote diagnostic collection
- Graphical lane/target selection
- Command-line operation for scripted or remote-support workflows
- Collection of application configuration and primary application logs
- Date-window filtering for high-volume journal and analysis data
- Integration/API log collection
- Clean per-device folder organization
- Automatic ZIP packaging
- Consistent output location for predictable technician use
- Avoids empty device folders when no relevant files are found
- Supports both interactive and remote-launch usage patterns

## Engineering Focus

The key engineering challenge is **collecting enough information to be useful without creating a noisy, oversized archive**. Different log types require different handling: some files should always be included, while high-volume folders need date filtering so the technician receives the most relevant evidence rather than an entire historical dataset.

The utility also has to tolerate partial failures. One unavailable target or missing log folder should not invalidate successful collections from other systems.

## Reliability & Workflow Design

- Keep every target independent
- Continue collecting useful data when optional sources are missing
- Apply clear time-window rules to date-sensitive logs
- Produce predictable folder structure for faster analysis
- Package only meaningful content
- Support technician-driven GUI use and automated command-line execution from the same tool

## What This Demonstrates

Remote Windows file access, multi-target orchestration, time-based filtering, resilient error handling, archive generation, GUI/CLI interoperability, and support-oriented workflow design.

## Technology

`Python` • `Windows Automation` • `Remote File Access` • `ZIP Packaging` • `GUI + CLI`

> Public documentation intentionally omits internal network paths, production host discovery, credentials, proprietary log contents, and company-specific configuration data.