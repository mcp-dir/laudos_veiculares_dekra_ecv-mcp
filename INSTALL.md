# Instalação rápida

Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_laudos_veiculares_dekra_ecv`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria)` / `https://api.mcp.ai/p_laudos_veiculares_dekra_ecv`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "laudos_veiculares_dekra_ecv": { "type": "http", "url": "https://api.mcp.ai/p_laudos_veiculares_dekra_ecv" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=laudos_veiculares_dekra_ecv&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9sYXVkb3NfdmVpY3VsYXJlc19kZWtyYV9lY3YifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "laudos_veiculares_dekra_ecv": { "url": "https://api.mcp.ai/p_laudos_veiculares_dekra_ecv" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=laudos_veiculares_dekra_ecv&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_laudos_veiculares_dekra_ecv%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "laudos_veiculares_dekra_ecv": { "type": "http", "url": "https://api.mcp.ai/p_laudos_veiculares_dekra_ecv" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_laudos_veiculares_dekra_ecv
```

Dúvidas? [laudos_veiculares_dekra_ecv@mcp.ai](mailto:laudos_veiculares_dekra_ecv@mcp.ai)
