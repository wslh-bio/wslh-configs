# custom-configs
This repository stores WSLH-specific Nextflow profiles and configuration overlays used by workflows to standardize execution on WSLH systems.

## Purpose
- Centralize reusable Nextflow `profiles` for WSLH environments.
- Provide consistent defaults for compute resources, executors, and storage paths.
- Keep pipeline-specific overrides separate from upstream workflow code.

## How it is used
Pipelines include these configs at runtime and select a WSLH profile. Typical usage:

- Include this repository's config file(s) with `-c`.
- Select a WSLH profile with `-profile`.

Example:
nf-run <pipeline> -c /path/to/custom-configs/<config>.config -profile wslh

## Conventions
- Add new WSLH profiles under a clearly named `profiles` section in the config file.
- Keep WSLH settings isolated from generic defaults.
- Document any required environment variables or paths alongside the profile.

## Repository layout
Add or update files to match your WSLH setup. Keep config names descriptive and aligned with the pipelines that consume them.
