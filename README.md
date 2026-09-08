# OPS-AGENT — instaladores

Repo **público solo de binarios**. El código es privado (`lte-nexus/ops-station-agent`).

## Cómo se versiona

**Un tag = una versión del agent.** Dentro de ese Release van los tres instaladores (no hay `v0.1.1-linux` ni tags por SO).

| Tag | Linux | Windows | macOS (demo) |
|-----|--------|---------|----------------|
| `v0.1.1` | `ops-agent-linux.tar.gz` | `ops-agent.exe` | `ops-agent` |
| `v0.1.2` | los tres otra vez | | |

El portal (RRHH → Estaciones) apunta a **una** versión. Al publicar `v0.1.2` se cambian las tres URLs juntas.

Cómo sale un Release: tag `v*` en el repo privado → CI arma Linux + Windows + macOS → este repo.

Baja desde [Releases](https://github.com/lte-nexus/ops-agent-releases/releases) o desde el portal. No abras PRs de código aquí.
