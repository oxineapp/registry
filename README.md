# Oxine app registry

What Oxine's app store (Settings → Apps) lists besides the apps built into Oxine.

- `approved.txt`: repos on the "From the community" shelf, one `creator/repo` per line. The repo also needs the `oxine-app` topic. The store shows each one by the name, tagline and icon in its `manifest.json`.
- `registry.json`: the Featured shelf ("Picked by the Oxine team"). Each entry has `repo` (`creator/repo`), `name`, and optionally `tagline` and `icon` (an SF Symbol name).

To list an app, open a pull request. The app's repo needs a GitHub release that Oxine can install: a `manifest.json` whose `id` is `creator.repo`, the binary it names under `run.arm64`, and `SHA256SUMS`. The manifest format is in [APPS_DESIGN.md](https://github.com/oxineapp/oxine/blob/master/APPS_DESIGN.md).
