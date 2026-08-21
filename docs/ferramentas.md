# Ferramentas

PNCP expõe 13 ferramentas (todas somente leitura).

### 1. `pncp_buscar`
**Input**: `termo` (opcional), `termos` (opcional), `tipo` (opcional), `ordenacao` (opcional), `status` (opcional), `pagina` (opcional), `tam_pagina` (opcional)

Busca licitações por PALAVRA-CHAVE no objeto (cobertura NACIONAL ampla, índice full-text), em editais, atas ou contratos.

### 2. `pncp_listar`
**Input**: `termos` (opcional), `data_inicial` (opcional), `data_final` (opcional), `modalidade` (opcional), `apenas_abertas` (opcional), `uf` (opcional), `municipio` (opcional), `cnpj` (opcional), `valor_min` (opcional), `valor_max` (opcional), `ordenacao` (opcional), `tamanho_pagina` (opcional), `pagina` (opcional), `incluir_valor` (opcional), `expandir` (opcional)

Busca PRINCIPAL de licitações abertas por palavra-chave, faixa de VALOR, estado, modalidade e período.

### 3. `pncp_oportunidades`
**Input**: `termos` (opcional), `termo` (opcional), `excluir` (opcional), `data_inicial` (opcional), `data_final` (opcional), `tipo_periodo` (opcional), `valor_min` (opcional), `valor_max` (opcional), `ufs` (opcional), `modalidades` (opcional), `portais` (opcional), `superoportunidades` (opcional), `participacao_exclusiva` (opcional), `excluir_registro_preco` (opcional), `somente_sigilosos` (opcional), `itens_desertos` (opcional), `tipo_item` (opcional), `pesquisa_ampla` (opcional), `expandir` (opcional), `pagina` (opcional)

Busca de OPORTUNIDADES de licitação (editais/pregões) com filtros ricos por palavra-chave, FAIXA DE VALOR da compra, UFs, modalidades, portais, registro de preço, participação exclusiva ME/EPP e superoportunidades.

### 4. `pncp_processo`
**Input**: `id` (opcional), `ids` (opcional)

Detalhe de oportunidade(s) por `id` (de pncp_listar/pncp_oportunidades).

### 5. `pncp_detalhe`
**Input**: `cnpj`, `ano`, `sequencial`, `itens` (opcional), `resultado` (opcional)

Detalhe completo de uma licitação/contratação a partir de cnpj+ano+sequencial (a referência devolvida pela pncp_buscar).

### 6. `pncp_resultado`
**Input**: `cnpj`, `ano`, `sequencial`, `numero_item` (opcional)

Quem GANHOU a licitação: o(s) fornecedor(es) vencedor(es) homologado(s) a partir de cnpj+ano+sequencial (a referência da pncp_buscar).

### 7. `pncp_arquivos`
**Input**: `cnpj`, `ano`, `sequencial`

Documentos de uma licitação/edital (edital, termo de referência, anexos) com o LINK de download de cada arquivo (em geral PDF).

### 8. `pncp_texto`
**Input**: `cnpj`, `ano`, `sequencial`, `documento` (opcional), `de_pagina` (opcional), `ate_pagina` (opcional)

Texto INTEIRO do edital em markdown (com marcadores '## Página N'), pra você RESUMIR ou ler o documento todo.

### 9. `pncp_contratos`
**Input**: `data_inicial`, `data_final`, `cnpj_orgao` (opcional), `pagina` (opcional), `tamanho_pagina` (opcional)

Lista contratos públicos firmados num período, opcionalmente filtrando por órgão (CNPJ).

### 10. `pncp_atas`
**Input**: `data_inicial`, `data_final`, `cnpj` (opcional), `pagina` (opcional), `tamanho_pagina` (opcional)

Lista atas de registro de preços vigentes num período (referência de preços praticados pelo governo), opcionalmente por órgão (CNPJ).

### 11. `pncp_pca`
**Input**: `ano_pca`, `codigo_classificacao_superior`, `pagina` (opcional), `tamanho_pagina` (opcional)

Plano anual de contratações (PCA) por ano e classificação superior do catálogo: o que os órgãos planejam contratar no ano.

### 12. `pncp_historico`
**Input**: `termo` (opcional), `uf` (opcional), `modalidade` (opcional), `situacao` (opcional), `valor_min` (opcional), `valor_max` (opcional), `desde` (opcional), `ate` (opcional), `pagina` (opcional), `tam_pagina` (opcional)

Arquivo histórico de licitações: consulta editais que a plataforma acumulou ao longo do tempo (inclusive os que já encerraram ou saíram do ar), por PALAVRA-CHAVE no objeto, estado (UF), modalidade, situação e período…

### 13. `pncp_orgaos`
**Input**: `termo` (opcional), `termos` (opcional), `uf` (opcional), `portais` (opcional), `antecipagov` (opcional), `pagina` (opcional)

Busca de ÓRGÃOS/entidades compradoras por nome, UF e/ou portal.

## Prompts de exemplo

```
Liste os pregões eletrônicos publicados em SP na última semana
Busque editais de 'merenda escolar' abertos
Quem ganhou a licitação CNPJ X, ano 2025, sequencial 12?
```
