# QR Inventory Manager

A warehouse-focused inventory system designed for fast quantity updates with phones and USB scanners.

## The Problem

Traditional inventory software can be too heavy for a simple warehouse workflow where the main need is to identify an item and adjust its current quantity quickly.

## The Solution

The QR Inventory Manager uses printable QR labels and a shared inventory source so an employee can scan an item, review its current quantity, and make a simple `+1` or `-1` adjustment.

## Key Features

- QR-code labels for inventory items
- Phone-based scanning workflow
- Zebra USB scanner support through keyboard/HID mode
- Simple `+1` and `-1` quantity controls
- Shared inventory updates through Google Sheets
- Windows desktop utility support
- Phone-first workflow for warehouse use
- Dedicated “scan next item” flow
- Label layout designed with practical printing spacing
- Item filtering to exclude retired/invalid inventory rows

## Engineering Focus

The main design goal is speed and simplicity. The tool avoids POS-style complexity and focuses only on the warehouse actions that matter: identify the item, show the current quantity, adjust it, and move to the next scan.

## Integration

- Google Sheets as a shared inventory data source
- Google Apps Script web workflow for mobile access
- Windows desktop utility for keyboard/HID scanners
- QR-code generation and printing

## Status

Developed as a practical warehouse inventory tool with both mobile and Windows scanning workflows.

> Public documentation omits production sheet identifiers, access configuration, internal deployment URLs, and private inventory data.
