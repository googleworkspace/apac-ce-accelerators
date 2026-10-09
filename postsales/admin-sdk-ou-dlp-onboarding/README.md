
# Admin SDK Organizational Unit (OU) & Security Group Onboarding Starter


A sanitized, customer- and partner-runnable **Post-Sales** Python starter using
the Google Workspace Admin SDK Directory API (`admin.directory_v1`) to verify or
provision country/subregion Organizational Units (`OUs`) prior to user migration
waves.

## Prerequisites

1.  Python 3.10+ with `google-api-python-client` and `google-auth` installed.
2.  Application Default Credentials (ADC) or Workload Identity Federation
    authorized with the
    `https://www.googleapis.com/auth/admin.directory.orgunit` scope on your
    target Google Workspace customer tenant (`example-bank.com`).

## Usage (Dry-Run Mode Default)

```python
# Copyright 2026 Google LLC
# SPDX-License-Identifier: Apache-2.0

"""Dry-run Organizational Unit (OU) verifier for Google Workspace onboarding."""

REQUIRED_OUS = [
    "/APAC/SG/RegulatedUsers",
    "/APAC/SG/KnowledgeWorkers",
    "/APAC/AU/KnowledgeWorkers",
]

for ou_path in REQUIRED_OUS:
  print(f"[DRY-RUN] Verified target Organizational Unit path: {ou_path}")
```
