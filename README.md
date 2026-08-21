# PNCP

### PNCP para Claude, ChatGPT e agentes de IA

Consulta de licitações e contratações públicas no Brasil (PNCP): busca de editais e pregões por palavra-chave, estado e modalidade, oportunidades com filtro de faixa de valor, detalhe da contratação com itens e preços, documentos do edital (link do PDF e texto), contratos, atas de registro de preços e planejamento anual. Hospedado pela plataforma, sem credenciais.

- 📊 **13 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `PNCP` e **URL** `https://api.mcp.ai/p_pncp`.

### Cursor

[➕ Instalar PNCP no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pncp&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wbmNwIn0=)

### VS Code (Copilot Chat)

[➕ Instalar PNCP no VS Code](vscode:mcp/install?name=pncp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pncp%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_pncp
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Liste os pregões eletrônicos publicados em SP na última semana
Busque editais de 'merenda escolar' abertos
Quem ganhou a licitação CNPJ X, ano 2025, sequencial 12?
```

---

## 13 ferramentas disponíveis

| Tool | Descrição |
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

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Pré-pago (carteira de créditos), paga por uso. Veja [docs/precos.md](docs/precos.md).

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: Fontes públicas de contratações governamentais (dados abertos), o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_pncp`.


---

## Suporte

- 📧 [pncp@mcp.ai](mailto:pncp@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/pncp-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_pncp` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
