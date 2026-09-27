# ArcKit for Claude

The Claude Code marketplace for [ArcKit](https://arckit.org), the Enterprise Architecture Governance Harness: slash commands, agents, skills and hooks that turn architecture governance into a systematic, template-driven process.

## Install

```text
/plugin marketplace add tractorjuice/arckit-claude
/plugin install arckit@arckit-claude
```

Then add any overlays you need, for example `/plugin install arckit-uae@arckit-claude`. Every overlay needs the `arckit` core plugin.

## Plugins

Each plugin lives in its own folder under `plugins/`, with its own README:

- [`plugins/arckit`](plugins/arckit): the core plugin
- Jurisdiction overlays: [`uae`](plugins/uae), [`fr`](plugins/fr), [`nl`](plugins/nl), [`ca`](plugins/ca), [`eu`](plugins/eu), [`at`](plugins/at), [`au`](plugins/au), [`au/energy`](plugins/au/energy), [`us`](plugins/us)
- Sector overlays: [`uk/finance`](plugins/uk/finance), [`uk/nhs`](plugins/uk/nhs), [`uk/gcloud`](plugins/uk/gcloud) (proprietary, see its LICENSE)
- Method overlays: [`togaf/adm`](plugins/togaf/adm), [`oaa`](plugins/oaa), [`agent/architecture`](plugins/agent/architecture)
- Tooling: [`repo`](plugins/repo), [`fde`](plugins/fde)

## Data and privacy

ArcKit collects no usage data. What each plugin sends, and when, is in its README; the core plugin's is in [`plugins/arckit/README.md`](plugins/arckit/README.md#data-and-privacy). Privacy policy: <https://arckit.org/privacy.html>.

## Source

This repository is generated from [tractorjuice/arc-kit](https://github.com/tractorjuice/arc-kit) at each release. Open issues and pull requests there.
