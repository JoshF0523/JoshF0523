# Configuration Editor & Deployment Tool

A remote configuration-management utility that locates a valid source system, launches the approved editor, and deploys the resulting configuration to selected qualifying endpoints.

## Problem

Configuration updates become error-prone when technicians must manually locate a good source file, verify that the required editor exists, make the change, and then copy the result to multiple systems one at a time.

## Solution

The utility automates source discovery, stages the configuration for editing with the approved editor, and then presents a clear lane-selection workflow for controlled deployment.

## Core Capabilities

- Automatic discovery of qualifying active endpoints
- Validation that both configuration and editor components are present
- First-valid-source selection
- Launch through the approved configuration editor
- Selected-target deployment workflow
- Clear separation between edit and deploy stages
- No unnecessary endpoint-protection changes
- Menusys-style multi-target selection experience
- Validation-driven source handling to reduce bad deployments

## Engineering Focus

The design separates **source discovery**, **editing**, and **deployment** into explicit phases. That keeps the operator in control while automating the repetitive infrastructure work around the change.

## What This Demonstrates

Configuration management, remote file deployment, source validation, multi-target workflow design, and integration with existing vendor tools.

> Public documentation excludes proprietary configuration contents, production paths, target-selection queries, and internal deployment details.