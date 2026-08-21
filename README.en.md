# PNCP

### PNCP for Claude, ChatGPT and AI agents

Search Brazilian government tenders and public procurement (PNCP): find notices and auctions by keyword, state and modality, opportunities filtered by value range, full procurement detail with line items and prices, tender documents (PDF link and text), contracts, price-registration records and annual procurement plans. Platform-hosted, no credentials.

- 📊 **13 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `PNCP`, URL `https://api.mcp.ai/p_pncp`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pncp&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wbmNwIn0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=pncp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pncp%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_pncp
```

---

## 13 tools

| Tool | Description |
|---|---|
| `pncp_buscar` | Busca licitações por PALAVRA-CHAVE no objeto (cobertura NACIONAL ampla, índice full-text), em editais, atas ou contratos. |
| `pncp_listar` | Busca PRINCIPAL de licitações abertas por palavra-chave, faixa de VALOR, estado, modalidade e período. |
| `pncp_oportunidades` | Busca de OPORTUNIDADES de licitação (editais/pregões) com filtros ricos por palavra-chave, FAIXA DE VALOR da compra, UFs, modalidades, portais, registro de preço, participação exclusiva ME/EPP e superoportunidades. |
| `pncp_processo` | Detalhe de oportunidade(s) por `id` (de pncp_listar/pncp_oportunidades). |
| `pncp_detalhe` | Detalhe completo de uma licitação/contratação a partir de cnpj+ano+sequencial (a referência devolvida pela pncp_buscar). |
| `pncp_resultado` | Quem GANHOU a licitação: o(s) fornecedor(es) vencedor(es) homologado(s) a partir de cnpj+ano+sequencial (a referência da pncp_buscar). |
| `pncp_arquivos` | Documentos de uma licitação/edital (edital, termo de referência, anexos) com o LINK de download de cada arquivo (em geral PDF). |
| `pncp_texto` | Texto INTEIRO do edital em markdown (com marcadores '## Página N'), pra você RESUMIR ou ler o documento todo. |
| `pncp_contratos` | Lista contratos públicos firmados num período, opcionalmente filtrando por órgão (CNPJ). |
| `pncp_atas` | Lista atas de registro de preços vigentes num período (referência de preços praticados pelo governo), opcionalmente por órgão (CNPJ). |
| `pncp_pca` | Plano anual de contratações (PCA) por ano e classificação superior do catálogo: o que os órgãos planejam contratar no ano. |
| `pncp_historico` | Arquivo histórico de licitações: consulta editais que a plataforma acumulou ao longo do tempo (inclusive os que já encerraram ou saíram do ar), por PALAVRA-CHAVE no objeto, estado (UF), modalidade, situação e período… |
| `pncp_orgaos` | Busca de ÓRGÃOS/entidades compradoras por nome, UF e/ou portal. |

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_pncp` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
