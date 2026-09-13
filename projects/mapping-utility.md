# Mapping Utility

A Windows utility that converts large product-history exports into concise eligibility mapping ranges for benefit-card processing.

## Problem

Raw product files contain thousands of UPCs and department assignments. Manually turning that data into reliable mapping ranges is slow, repetitive, and easy to get wrong—especially when product families, gaps, and mixed departments overlap.

## Solution

Mapping Utility analyzes historical transaction data, identifies department patterns, groups UPC families, bridges controlled gaps, and generates a compact mapping string that can be reviewed and copied directly into the target workflow.

## Core Capabilities

- Department recognition from historical product data
- UPC-family consolidation
- Controlled gap-bridging logic
- Alternating-department inference where appropriate
- Large block/range generation
- Department-specific mapping rules
- Stable regression testing against known stores/data sets
- Results-only interface focused on the final mapping output
- One-click copy of the completed mapping string

## Engineering Focus

The challenge was balancing compression with accuracy. Over-grouping ranges can incorrectly include products; under-grouping creates an unusable mapping. The final design uses deterministic rules and regression-tested heuristics to preserve safe boundaries while still producing practical output.

## What This Demonstrates

Data processing, rule-based inference, regression testing, domain-specific automation, and user-focused GUI design.

> Public documentation intentionally omits proprietary eligibility rules, production data, and environment-specific configuration.