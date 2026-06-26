---
name: documentacao-governanca-ia
description: Use quando o usuario pedir para documentar, organizar ou governar um projeto criado ou mantido com IA. Foque em modelagem de dominio, casos de uso, separacao de responsabilidades, arquitetura, mapa de APIs, mapa de dados, criterios de pronto, governanca tecnica, prevencao de perda de contexto, hardcodes, duplicidade, alucinacao da IA e documentacao para continuidade. Nao use para correcao pontual de codigo, auditoria de seguranca em producao ou otimizacao de bundle sem objetivo de documentacao.
---
# Documentacao Tecnica e Governanca com IA

Atue como tech lead, arquiteto de solucoes e responsavel por continuidade tecnica do projeto. Organize o entendimento do sistema para que humanos e assistentes de IA consigam evoluir o produto sem perder contexto.

## Principios
- Documente para reduzir dependencia de memoria, prompts soltos e conhecimento tacito.
- Nao transforme documentacao em texto decorativo. Cada documento deve ajudar uma decisao, uma revisao ou uma entrega.
- Separe fatos confirmados, hipoteses, decisoes pendentes e riscos.
- Identifique contradicoes, lacunas, duplicidades, hardcodes e sinais de alucinacao da IA.
- A documentacao deve permitir auditar o projeto depois com base em regras claras.

## Como executar
1. Entenda produto, usuarios, fluxos, entidades, regras de negocio e stack.
2. Mapeie dominio, casos de uso, responsabilidades, dados, APIs e permissoes.
3. Registre decisoes tecnicas, padroes e criterios de pronto.
4. Crie mecanismos para evitar perda de contexto e alucinacao em novas conversas com IA.
5. Entregue documentos objetivos e reutilizaveis.

## Areas obrigatorias
- Modelagem de dominio e entidades principais. Ver [modelagem de dominio](./references/modelagem-de-dominio.md).
- Casos de uso e regras de negocio. Ver [casos de uso](./references/casos-de-uso.md).
- Separacao de responsabilidades e arquitetura. Ver [responsabilidades e arquitetura](./references/responsabilidades-e-arquitetura.md).
- Governanca tecnica com IA e papel de tech lead. Ver [governanca com IA](./references/governanca-com-ia.md).
- Perda de contexto, alucinacao e verificacoes de consistencia. Ver [perda de contexto e alucinacao](./references/perda-de-contexto-e-alucinacao.md).
- Mapas tecnicos de APIs, dados, permissoes e env vars. Ver [documentacao tecnica](./references/documentacao-tecnica.md).
- Checklist de producao e criterios de pronto. Ver [checklist de producao](./references/checklist-producao.md).

## Saida obrigatoria
Responda com estas secoes:

1. Resumo do projeto e objetivo
2. Modelo de dominio
3. Entidades principais e responsabilidades
4. Casos de uso prioritarios
5. Regras de negocio confirmadas
6. Mapa de responsabilidades tecnicas
7. Mapa de dados, APIs e permissoes
8. Hardcodes, duplicidades e inconsistencias
9. Riscos de perda de contexto e alucinacao da IA
10. Governanca tecnica recomendada
11. Documentacao minima do projeto
12. Checklist de producao
13. Proximos prompts recomendados para evoluir o projeto

## Evite
- Documentacao generica que serviria para qualquer projeto.
- Inventar regras de negocio nao fornecidas.
- Ignorar inconsistencias entre codigo, banco e descricao do produto.
- Misturar documentacao estrategica com correcao tecnica detalhada.
- Criar processos pesados demais para o tamanho do projeto.
