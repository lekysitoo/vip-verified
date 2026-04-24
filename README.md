## GitHub Data Store (HaxBall Desktop)

Estructura base para sync desde `localhost:5483` usando GitHub Contents API.

### Carpetas

- `users/` -> un JSON por usuario (`{discord_id}.json`)
- `teams/` -> un JSON por equipo (`{team_id}.json`)
- `indexes/` -> índices compartidos
- `state/` -> estado global (meta/settings/stores)

### Archivos requeridos iniciales

- `indexes/nick_to_discord.json`
- `indexes/team_members.json`
- `state/meta.json`
- `state/pro_settings.json`
- `state/friends_store.json`
- `state/teams_meta.json`

### Variables `.env` en tu app

- `GITHUB_TOKEN` (PAT con permiso `contents: write`)
- `GITHUB_OWNER`
- `GITHUB_REPO`
- `GITHUB_BRANCH` (default: `main`)
- `GITHUB_BASE_PATH` (default: `haxball-data`)

Si `GITHUB_BASE_PATH=haxball-data`, la app lee/escribe en esta carpeta.
