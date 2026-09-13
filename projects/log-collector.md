# Log Collector

A technician-focused Windows utility for gathering diagnostic information from multiple remote systems and packaging it into a clean support archive.

## The Problem

Troubleshooting distributed Windows systems often means manually navigating to several machines, locating different log folders, filtering by date, copying files, and organizing the results before analysis can even begin.

## The Solution

Log Collector centralizes that work. The operator selects target systems and the utility gathers the required diagnostic material, applies age-based filtering where appropriate, and produces a single collection archive for review.

## Key Features

- Multi-system remote collection
- Graphical target selection
- Command-line support for scripted collection
- Recent-log filtering
- Collection of configuration, application, journal, and API-related diagnostics
- Clean per-device organization
- Automatic ZIP packaging
- Avoids creating empty device folders when nothing relevant is found
- Designed for repeatable technician workflows

## Engineering Focus

The project combines remote file access, filtering rules, error handling, consistent folder structure, and operator-friendly status reporting. The result is a much faster path from “something is wrong” to “the useful evidence is ready to inspect.”

## Technology

- Python
- Windows file/network automation
- GUI + command-line workflows
- ZIP/archive generation

## Status

Developed and refined through multiple working versions for real troubleshooting workflows.

> Public documentation intentionally omits private network paths, environment-specific host discovery logic, credentials, and proprietary log content.
