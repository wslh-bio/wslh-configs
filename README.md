# wslh-configs
This repository stores WSLH-specific Nextflow profiles and configuration overlays used by workflows to standardize execution on WSLH systems.

## Purpose
- Centralize reusable Nextflow `profiles` for WSLH environments.
- Provide consistent defaults for compute resources, executors, and storage paths.
- Keep pipeline-specific overrides separate from upstream workflow code.

## How it is used
Pipelines include these configs at runtime using the `custom_config_base` parameter.

Example:
```
nextflow run <pipeline> --custom_config_base https://raw.githubusercontent.com/wslh-bio/wslh-configs/refs/heads/main -profile awsdev
```

## Conventions
- Add new WSLH profiles under a clearly named `profiles` section in the config file.
- Keep WSLH settings isolated from generic defaults.
- Document any required environment variables or paths alongside the profile.

## Repository layout
Add or update configs to support running pipelines using the WSLH environment. Keep config names descriptive and aligned with the pipelines that consume them.
