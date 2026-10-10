# Architecture

## Modular core

The platform is organised around independent domain modules for accounts, website records, scan execution, findings, reporting, monitoring, commerce and integrations. Modules share a small set of stable data contracts instead of writing directly into one another's presentation logic.

## Connector boundary

Platform-specific authentication and API behaviour stays inside connector adapters. The core receives normalised website and scan data, so reporting does not need to know whether information originated from WordPress, Shopify, Webflow, Wix or another supported integration.

## Analysis pipeline

Scan requests are validated and queued, individual analysers produce structured findings, and a normalisation layer assigns categories, severity and actionable guidance. The same findings can then power the web dashboard, PDF output, archives and monitoring.

## Presentation layer

The WordPress theme and customer screens consume platform services rather than duplicating scan logic. Responsive layouts are tested across desktop, tablet and mobile breakpoints.

## Deployment

Changes are assembled as versioned plugin and theme packages, validated in an isolated environment and transferred to production only after review. Backups, dependency checks and post-deployment verification are part of material releases.

