# MinecraftTest

A full Paper (Minecraft server) setup used to test hosting a Minecraft server on railway.com. The server is pre-configured and ready to launch, with the EULA accepted, a survival-world configuration, and two utility plugins installed. This was an experiment in cloud-deploying a Java-based Minecraft server.

## Tech Stack

- Java (Minecraft / Paper server, paperclip launcher)
- Paper 1.21.8 (Minecraft 1.21.8 server jar)
- Plugins: spark (performance profiler), bStats (metrics)
- Hosting: railway.com (per the README)

## Features / Contents

- `paper.jar` - Paper 1.21.8 server jar (paperclip launcher, ~50 MB)
- `eula.txt` - Minecraft EULA accepted (`eula=true`)
- `server.properties` - server configuration:
  - Survival gamemode, easy difficulty
  - 20 max players, view-distance 10, simulation-distance 10
  - `online-mode=false` (cracked/offline-mode compatible)
  - Standard port 25565, PvP enabled
- `plugins/spark/config.json` - spark profiler with background profiler enabled
- `plugins/bStats/config.yml` - bStats metrics enabled
- `plugins/.paper-remapped/` - Paper's generated remap files
- `README.md` - original note: "Testing Minecraft server hosting on railway.com"
- Git history: initial commit, then "setup complete"

## Getting Started

```bash
# Requires Java (Java 21 recommended for Paper 1.21.8)
java -Xms2G -Xmx2G -jar paper.jar nogui
```

The server binds to port 25565 by default and starts a survival world.

## Notes

Hosting experiment - the server config (`online-mode=false`, port 25565, easy difficulty) was tuned for quick testing on railway.com rather than production. spark and bStats are standard maintenance/monitoring plugins. Only two commits exist: the initial upload and a "setup complete" commit.
