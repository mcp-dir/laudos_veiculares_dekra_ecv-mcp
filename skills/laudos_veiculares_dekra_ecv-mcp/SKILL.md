---
name: laudos_veiculares_dekra_ecv-mcp
description: Skill da REST API do Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria) na MCP.AI: 1 endpoint em /api/laudos_veiculares_dekra_ecv. Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria) — REST API skill

Você tem acesso à **Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria)** REST API na MCP.AI.

> Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/laudos_veiculares_dekra_ecv
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/laudos_veiculares_dekra_ecv/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"login_usuario":"...","login_senha":"...","placa":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/laudos_veiculares_dekra_ecv/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `laudos_veiculares_dekra_ecv_consultar`

Laudos Veiculares DEKRA: ECV (Empresa Credenciada de Vistoria), consulta em fonte oficial. _(POST /api/laudos_veiculares_dekra_ecv/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `login_usuario` | string | Sim | Parâmetro de consulta "login_usuario". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `placa` | string | Sim | Parâmetro de consulta "placa". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_laudos_veiculares_dekra_ecv` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
