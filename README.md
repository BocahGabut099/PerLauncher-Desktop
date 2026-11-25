# PerLauncher

PerLauncher is a Windows-first Minecraft Java launcher based on the Prism Launcher codebase.

## Desktop features retained from the launcher engine

- Multiple isolated instances and Minecraft version management.
- Java runtime detection plus per-instance Java and RAM settings.
- Fabric, Forge, NeoForge and Quilt installation.
- Modrinth modpack discovery/import and supported mod/resource workflows.
- CurseForge integration when a PerLauncher-owned API key is configured.
- Worlds, resource packs, shader packs, screenshots, logs and instance export/import.
- Native Microsoft/Xbox/Minecraft authentication when a PerLauncher Client ID is configured.
- Offline username accounts for offline-mode servers and local testing.

## Build

Pushing to `develop` or a `perlauncher/**` branch starts the Windows MSVC x64 Release workflow. Open **Actions → Build → Run workflow** to start it manually. The workflow uploads a standard ZIP, a portable ZIP and a Windows installer.

## GitHub Actions secrets

Add these under **Settings → Secrets and variables → Actions**:

- `PERLAUNCHER_MSA_CLIENT_ID` — optional Microsoft Entra application Client ID. Without it, Microsoft sign-in is intentionally hidden.
- `PERLAUNCHER_CURSEFORGE_API_KEY` — optional API key issued to PerLauncher. Without it, CurseForge discovery is disabled; Modrinth remains available.

Do not commit OAuth client secrets or API keys.

## Authentication status

- Microsoft: native Microsoft/Xbox/Minecraft flow, provided PerLauncher configures its own Client ID.
- Offline: local profile for offline-mode servers and testing; it does not grant paid Minecraft entitlements or access to online-mode servers.
- Ely.by: Android currently uses the PerLauncher Cloudflare OAuth ticket flow. Desktop Ely.by is not included in this patch; it needs its own account type, refresh flow and Authlib Injector launch integration before it can be called working.

## Upstream compatibility

Minecraft metadata and legacy Forge library endpoints remain on Prism-compatible services to preserve version and mod-loader compatibility until PerLauncher operates its own mirrors.

## License and attribution

PerLauncher is distributed under GPL-3.0-only and derives from Prism Launcher, with retained PolyMC and MultiMC attribution. PerLauncher is a separate project and is not endorsed by Prism Launcher.
