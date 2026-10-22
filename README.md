# OPS-AGENT — instaladores

Repo **público solo de binarios**. El código es privado (`lte-nexus/ops-station-agent`).

## Cómo se versiona

**Un tag = una versión del agent.** Dentro de ese Release van los tres instaladores (no hay `v0.1.1-linux` ni tags por SO).

| Tag | Linux | Windows | macOS (demo) |
|-----|--------|---------|----------------|
| `v0.1.1` | `ops-agent-linux.tar.gz` | `ops-agent.exe` | `ops-agent` |
| `v0.1.2` | los tres otra vez | | |
| `v0.1.3` | los tres otra vez | | |
| `v0.1.4` | Linux y macOS (arm64) con `trace follow` / `trace off`. Windows sigue el de v0.1.3 | | |

El portal (RRHH → Estaciones) apunta a **una** versión. Al publicar `v0.1.4` se cambian las tres URLs juntas.

El mismo `ops-agent-linux.tar.gz` trae el agente de cada PC (`scripts/install-desk.sh`). No hay un cuarto archivo. En el portal se baja desde la tarjeta **Agente de cada PC**, con el código de esa tarjeta (no el del servidor).

En Estaciones, **Última publicada** es el Release más nuevo de este repo. El botón del portal puede seguir apuntando a un tag anterior. Un tag anterior a `install-desk.sh` (el pin v0.1.7) no instala el agente de cada PC ni el actualizador de sala. Para instalar, usa el tag que dice la tarjeta.

Cómo sale un Release: tag `v*` en el repo privado → CI arma Linux + Windows + macOS → este repo.

Baja desde [Releases](https://github.com/lte-nexus/ops-agent-releases/releases) o desde el portal. No abras PRs de código aquí.
