ï»¿# ê°Å¸Å½Â¬ VideosAvatar ê¢â¬â avatar falante INEMA com HeyGen

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Ecossistema para gerar vêÂ­deos de **avatar falante** no HeyGen a partir de um roteiro de texto (9:16, 720p, voz PT-BR) e **entregar o MP4 no bot do openpcbot** (Telegram).

**PêÂ¡gina de guia:** https://inematds.github.io/videosavatar/

## Os dois caminhos (mesma geraêÂ§êÂ£o, billing diferente)

| Caminho | Cofre que gasta | Auth | Skill do Claude Code |
|---|---|---|---|
| **API direta** (`POST /v3/videos`) | pool de **API** (pay-as-you-go) | API key | `heygen-cli` |
| **MCP remoto** (`mcp.heygen.com`) | crêÂ©ditos da **assinatura** (plano) | OAuth | `heygen-mcp` |

Os dois usam os mesmos IDs de avatar/voz e entregam no mesmo bot. Prefira a **assinatura** (crêÂ©ditos jêÂ¡ pagos no mêÂªs); deixe a API como reserva.

## Uso rêÂ¡pido (skill heygen-cli)

```bash
node ~/.claude/skills/heygen-cli/scripts/heygen.mjs --text "sua fala aqui"
node ~/.claude/skills/heygen-cli/scripts/heygen.mjs voices --lang pt   # vozes PT
node ~/.claude/skills/heygen-cli/scripts/heygen.mjs avatars            # seus perfis
```

Defaults: 9:16 êÂ· 720p êÂ· voz PT-BR êÂ· entrega no bot. SaêÂ­da em `~/projetos/output/heygen/<slug>/`.

## Assinatura (skill heygen-mcp)

```bash
claude mcp add --transport http heygen https://mcp.heygen.com/mcp/v1/
# depois: /mcp ê¢â â heygen ê¢â â Authenticate (login no navegador)
```

## ConfiguraêÂ§êÂ£o

Tudo vem do `.env` do openpcbot: `HEYGEN_API_KEY`, `HEYGEN_AVATAR_ID_NEI`, `HEYGEN_VOICE_ID_NEI`, `TELEGRAM_BOT_TOKEN`, `ALLOWED_CHAT_ID`. **Nenhuma credencial fica neste repo.**

---
INEMA.CLUB êÂ· https://inema.club

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>