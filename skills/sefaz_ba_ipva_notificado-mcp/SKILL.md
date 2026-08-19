---
name: sefaz_ba_ipva_notificado-mcp
description: Skill da REST API do SEFAZ BA: IPVA Notificado na MCP.AI: 1 endpoint em /api/sefaz_ba_ipva_notificado. SEFAZ BA: IPVA Notificado, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# SEFAZ BA: IPVA Notificado — REST API skill

Você tem acesso à **SEFAZ BA: IPVA Notificado** REST API na MCP.AI.

> SEFAZ BA: IPVA Notificado, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/sefaz_ba_ipva_notificado
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
curl -X POST https://api.mcp.ai/api/sefaz_ba_ipva_notificado/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/sefaz_ba_ipva_notificado/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `sefaz_ba_ipva_notificado_consultar`

SEFAZ BA: IPVA Notificado, consulta em fonte oficial. _(POST /api/sefaz_ba_ipva_notificado/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `renavam` | string | Não | Parâmetro de consulta "renavam". |
| `paf` | string | Não | Parâmetro de consulta "paf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_sefaz_ba_ipva_notificado` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
