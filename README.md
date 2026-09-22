# cf-oci-mirror-action

[![Download and Mirror packages from anaconda](https://github.com/channel-mirrors/mirrormirror/actions/workflows/cron.yml/badge.svg)](https://github.com/channel-mirrors/mirrormirror/actions/workflows/cron.yml)

This action mirrors conda-forge and bioconda diligently.

The workflows use Pixi with `pixi.toml` and `pixi.lock` (Linux CI and Apple Silicon Macs).
Check the environment locally with `pixi run --locked conda-oci mirror --help`.
Update dependencies, including the mirror's Git revision, with `pixi update`.

Note: the action needs a working GHA_PAT for authentication. This PAT currently has to be a _classic_ PAT with (only) the `write:packages` scope.