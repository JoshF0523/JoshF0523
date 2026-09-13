# Healthy Benefits Upgrade Utility V1

A technician-focused remote multi-lane upgrade utility designed to make Healthy Benefits software deployment easier to run, easier to verify, and more consistent across qualifying POS systems.

## The Problem

Running the same application upgrade across multiple lanes can become repetitive and error-prone. A technician needs a clear way to choose the correct targets, launch the upgrade workflow consistently, confirm the deployment completed, and then verify Healthy Benefits status afterward.

## The Solution

Version 1 provides a straightforward guided workflow centered on target selection, upgrade execution, and post-upgrade verification. It keeps the operator in control of which lanes are changed and provides dedicated status-scan actions before or after maintenance.

## Core Capabilities

- Qualifying-lane discovery
- Multi-lane selection with no targets selected by default
- Visible technician-facing upgrade workflow
- Dedicated **Solidcore Status Scan** action
- Dedicated **HB Status Scan** action
- Post-upgrade prompt asking whether to run the HB Status Scan
- Short wait before the post-upgrade scan so services have time to settle
- Per-lane status and result visibility
- Consistent technician workflow across selected systems

## Workflow

A typical Version 1 maintenance session follows a simple sequence:

1. Discover the qualifying POS lanes.
2. Select the lanes that should receive the upgrade.
3. Run the upgrade workflow.
4. Review completion results.
5. When prompted, run the Healthy Benefits status scan.
6. Verify the selected lanes report the expected application status.

## Engineering Focus

The Version 1 design emphasizes **operator control and verification** rather than hiding the maintenance process. The technician explicitly chooses the deployment scope and has separate status-scan tools available to check the environment before or after the upgrade.

The post-upgrade verification step is important because successfully launching an installer does not by itself prove that the application is healthy afterward.

## What This Demonstrates

Remote software deployment, multi-target Windows automation, operator-controlled scope, post-maintenance verification, status scanning, technician-facing GUI design, and repeatable support workflows.

## Technology

`Python` • `Windows GUI` • `Remote Deployment` • `Status Scanning` • `Executable Packaging`

## Portfolio Version

This public portfolio intentionally showcases **Version 1 only**. Later experimental or expanded models are not included here.

> Public documentation intentionally excludes credentials, internal discovery queries, proprietary package names, private network details, and environment-specific maintenance commands.