# ðŸŽ¬ VideosAvatar â€” avatar falante INEMA com HeyGen

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Ecossistema para gerar vÃ­deos de **avatar falante** no HeyGen a partir de um roteiro de texto (9:16, 720p, voz PT-BR) e **entregar o MP4 no bot do openpcbot** (Telegram).

**PÃ¡gina de guia:** https://inematds.github.io/videosavatar/

## Os dois caminhos (mesma geraÃ§Ã£o, billing diferente)

| Caminho | Cofre que gasta | Auth | Skill do Claude Code |
|---|---|---|---|
| **API direta** (`POST /v3/videos`) | pool de **API** (pay-as-you-go) | API key | `heygen-cli` |
| **MCP remoto** (`mcp.heygen.com`) | crÃ©ditos da **assinatura** (plano) | OAuth | `heygen-mcp` |

Os dois usam os mesmos IDs de avatar/voz e entregam no mesmo bot. Prefira a **assinatura** (crÃ©ditos jÃ¡ pagos no mÃªs); deixe a API como reserva.

## Uso rÃ¡pido (skill heygen-cli)

```bash
node ~/.claude/skills/heygen-cli/scripts/heygen.mjs --text "sua fala aqui"
node ~/.claude/skills/heygen-cli/scripts/heygen.mjs voices --lang pt   # vozes PT
node ~/.claude/skills/heygen-cli/scripts/heygen.mjs avatars            # seus perfis
```

Defaults: 9:16 Â· 720p Â· voz PT-BR Â· entrega no bot. SaÃ­da em `~/projetos/output/heygen/<slug>/`.

## Assinatura (skill heygen-mcp)

```bash
claude mcp add --transport http heygen https://mcp.heygen.com/mcp/v1/
# depois: /mcp â†’ heygen â†’ Authenticate (login no navegador)
```

## ConfiguraÃ§Ã£o

Tudo vem do `.env` do openpcbot: `HEYGEN_API_KEY`, `HEYGEN_AVATAR_ID_NEI`, `HEYGEN_VOICE_ID_NEI`, `TELEGRAM_BOT_TOKEN`, `ALLOWED_CHAT_ID`. **Nenhuma credencial fica neste repo.**

---
INEMA.CLUB Â· https://inema.club

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>