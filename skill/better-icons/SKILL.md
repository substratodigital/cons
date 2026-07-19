---
name: better-icons
description: Diretrizes de busca e manipulação de ícones via `better-icons` (by better-auth) usando o repositório global do Iconify.
---

# Better Icons

Você gerencia a busca, adição e ingestão de ícones no projeto através do utilitário `better-icons`. Este pacote consulta a API do Iconify e possibilita adicionar imediatamente qualquer ícone ao código ou arquivo SVG.

## Identificação de Ícones (Icon ID)
Sempre busque ícones no formato `<prefix>:<name>`. 
**Exemplos populares:** 
- `lucide:home`
- `mdi:arrow-right`
- `heroicons:check`
- Coleções comuns: `lucide`, `mdi`, `heroicons`, `tabler`, `ph`, `solar`.

## Como Buscar e Consumir via CLI

1. **Buscar ícones:**
   Utilize o comando de search para encontrar opções quando o usuário pedir um ícone para uma dada situação.
   ```bash
   # Buscar no geral
   better-icons search "query" --limit 10
   
   # Buscar e já salvar em um diretório /icons
   better-icons search "check" -d ./icons
   ```

2. **Obter código do Ícone (Output em tela ou arquivo)**
   Quando quiser obter apenas o SVG na interface:
   ```bash
   better-icons get lucide:home > icon.svg
   
   # Em cores customizadas (ex: formato dark mode)
   better-icons get mdi:home --color '#333' --size 24 --json
   ```

## Boas Práticas
- Evite criar ou chutar SGVs gerados por IA. Sempre use o `better-icons` se a biblioteca existir. Funciona perfeitamente com todas as bibliotecas padrão do ecossistema front-end (React, Vue, etc).
- Utilize a paleta de cores CSS (`currentColor`) quando quiser exportar arquivos vinculados à folha de estilo principal do framework como Tailwind (`text-primary`, `fill-current`... ) usando a opção `--color`.
- Caso exista um Servidor MCP do Better Icons habilitado neste workspace, você também pode usar as tools `search_icons`, `get_icon`, `sync_icon` via MCP na sua interface para lidar diretamente com os componentes em React/Svelte/Vue.
