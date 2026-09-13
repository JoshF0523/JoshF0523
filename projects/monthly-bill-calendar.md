# Monthly Bill Calendar

A mobile-first budgeting application built around **paychecks**, not just due dates.

## The Problem

Most bill calendars tell you *when* something is due. That still leaves the user deciding which paycheck should cover each bill, how much will be left afterward, and how to handle two people with different pay schedules.

## The Solution

Monthly Bill Calendar turns that planning into a repeatable system. Each person can have their own paycheck schedule, bill list, payment rules, and editable check amounts while sharing synchronized household data.

## Key Features

- Multi-person household support
- Independent bills and settings per person
- Recurring paycheck schedules
- Bill assignment by closest check or defined pay-cycle logic
- Editable paycheck amounts
- Payment-plan support across multiple checks
- Enable/disable controls for individual bills
- Future paycheck planning
- Recent paycheck history
- Shared synchronization between phones
- Installable Progressive Web App experience on Android and iPhone
- Mobile-first interface designed for quick weekly use

## Engineering Focus

The interesting part of this project is not simply storing bills. The application has to reason about **cash-flow timing**: which paycheck should fund which obligation, how future checks are generated, and how changes remain synchronized between multiple users.

## Technology

- Progressive Web App architecture
- Supabase backend and synchronization
- Vercel deployment
- Mobile-first web UI

## Status

Actively developed and used as a practical household planning tool.

> Public portfolio documentation intentionally excludes private financial data, account information, access credentials, and production configuration.
