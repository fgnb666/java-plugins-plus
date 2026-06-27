# EssentialsX Multiplatform

This repository builds separate EssentialsX entry jars for multiple Minecraft server platforms:

- Paper / Bukkit-compatible servers
- Fabric servers
- BungeeCord proxies
- Velocity proxies

Vanilla Minecraft servers do not load plugins directly. Use the Fabric jar with a Fabric server, or run a plugin-capable server/proxy such as Paper, BungeeCord, or Velocity.

## Project Layout

```text
common/    Shared platform-neutral service code
paper/     Paper plugin entry and plugin.yml
fabric/    Fabric mod entry and fabric.mod.json
bungee/    BungeeCord plugin entry and bungee.yml
velocity/  Velocity plugin entry with annotation metadata
```

## Build

```bash
mvn clean package
```

The platform jars are produced under each module's `target/` directory:

- `paper/target/EssentialsX-Paper-*.jar`
- `fabric/target/EssentialsX-Fabric-*.jar`
- `bungee/target/EssentialsX-BungeeCord-*.jar`
- `velocity/target/EssentialsX-Velocity-*.jar`

GitHub Actions also collects them into the release as fixed filenames:

- `EssentialsX-Paper-1.21.11.jar`
- `EssentialsX-Fabric-1.21.11.jar`
- `EssentialsX-BungeeCord-1.21.11.jar`
- `EssentialsX-Velocity-1.21.11.jar`

- [AppService.java](common/src/main/java/com/example/essentialsx/common/AppService.java)
