# FaithMeats Open WebUI Deployment

All-in-one laptop deployment config for Open WebUI at FaithMeats.

## What's Here

| File | Purpose |
|------|---------|
| `docker-compose.yml` | Main compose — trusted-header auth, loopback bind, 3 mcpo tool servers |
| `docker-compose.override.yml` | Local overrides |
| `docker-compose.oauth.yml.staged` | Staged OAuth config (not yet active) |
| `.gitignore` | Ignores .env, backups/, etc. |

## Tool Servers (mcpo bridges)

1. **Allura Memory** — governed org memory (`group_id=allura-faith-meats`)
2. **FaithClaw Chat** — FaithClaw agent (gate-enforced)
3. **Web & Notion Search** — read-only research tools (Tavily, Exa, Notion)

## Notes

- `.env` is NOT committed (contains secrets)
- After first boot, tool server config is managed in the DB via admin API/UI
- Cloudflare Tunnel: `chat.faithmeats.org` → localhost:8080

