# GameMinder AMP Templates

CubeCoders AMP application templates for GameMinder hosted tables.

## GameMinder Foundry

Foundry Virtual Tabletop, set up to be run by GameMinder through its AMP proxy. It is based on the Foundry VTT template in [CubeCoders/AMPTemplates](https://github.com/CubeCoders/AMPTemplates).

Differences from the upstream template:

- Foundry's `routePrefix`, `hostname`, `proxySSL` and `proxyPort` are AMP settings, mapped into `data/Config/options.json`.
- The table refuses to start until `data/Config/admin.txt` exists, so a table never runs without an admin password.
- The GameMinder Foundry module is installed into `data/Data/modules/gameminder` on every update.
- Foundry runs with `--noipdiscovery` and bounded logs (`--logsize=1m --maxlogs=7`).
- Sleep mode is off. Linux only.

You bring your own Foundry license.

## Using it in AMP

In the AMP panel, open Configuration, then Instance Deployment, add `IanTWright/gameminder-amp-templates` to the configuration repositories, and fetch the latest templates. "GameMinder Foundry" then appears in the application list when creating an instance.
