# Como usar as Skills de Auditoria e Governanca

Este pacote contem duas Skills complementares.

## 1. auditoria-correcoes-desempenho
Use quando o objetivo for revisar codigo, banco, APIs, seguranca, performance e gerar correcoes copiaveis.

Exemplos de pedido:

```txt
Use /auditoria-correcoes-desempenho para revisar este projeto antes de producao.
Analise frontend, Supabase, RLS, endpoints, secrets, queries e testes.
Entregue achados criticos, scripts SQL e arquivos corrigidos quando houver contexto.
```

```txt
Use /auditoria-correcoes-desempenho para auditar estes arquivos.
Procure endpoints publicos, exposicao de dados, service_role, policies perigosas, bundle inflado e queries sem indice.
```

## 2. documentacao-governanca-ia
Use quando o objetivo for organizar o projeto para evolucao, documentar dominio, casos de uso, regras, responsabilidades e governanca com IA.

Exemplos de pedido:

```txt
Use /documentacao-governanca-ia para documentar este projeto.
Crie modelo de dominio, casos de uso, mapa de dados, mapa de APIs, mapa de permissoes e checklist de producao.
```

```txt
Use /documentacao-governanca-ia para revisar sinais de perda de contexto e alucinacao da IA neste projeto.
Procure duplicidades, hardcodes, regras contraditorias, funcoes inexistentes e lacunas de governanca.
```

## Fluxo recomendado

1. Primeiro use `documentacao-governanca-ia` para criar o mapa do projeto.
2. Depois use `auditoria-correcoes-desempenho` para auditar o codigo contra esse mapa.
3. Ao corrigir, atualize a documentacao com as decisoes tecnicas novas.
4. Quando a Skill falhar, ajuste a description se ela nao disparou ou ajuste as instrucoes se ela disparou, mas respondeu mal.

## Uso no Lovable

- Adicione cada pasta como uma Skill separada no workspace.
- Nao una as duas em uma unica Skill gigante.
- Use a barra `/` para chamar manualmente quando quiser garantir a Skill correta.
- Tambem deixe a description trabalhar: se o pedido estiver bem escrito, a Skill pode ser acionada automaticamente.
- Use arquivos de apoio como referencias carregadas sob demanda.
- Depois de editar uma Skill, comece uma nova conversa para garantir que a versao nova seja considerada.

## Uso no ChatGPT

Opcao A: Custom GPT
- Crie um GPT para auditoria tecnica e outro para documentacao/governanca.
- Cole o conteudo do `SKILL.md` nas Instructions do GPT correspondente.
- Envie os arquivos da pasta `references` como Knowledge.
- Teste no Preview com prompts reais.

Opcao B: conversa normal
- Anexe ou cole o `SKILL.md` e os arquivos de referencia relevantes.
- Peça explicitamente: "Use estas instrucoes como playbook para revisar meu projeto".
- Para tarefas recorrentes, prefira criar um GPT ou Skill dedicada quando sua conta/workspace permitir.

Opcao C: Skills nativas, quando disponiveis no seu workspace
- Suba cada pasta como uma Skill independente.
- Mantenha o nome curto, claro e sem sobreposicao.
- Atualize a description quando a Skill nao for acionada no momento certo.

## Boas praticas

- Skills nao substituem prompts. O prompt do dia ainda precisa dizer qual projeto, qual trecho e qual objetivo.
- Skills nao executam verificacoes sozinhas. Elas orientam o assistente a revisar, perguntar, analisar e corrigir.
- Skills muito grandes e sobrepostas tendem a atrapalhar. Prefira poucas, focadas e bem descritas.
- Atualize as Skills quando o projeto mudar.
- Mantenha Knowledge para fatos estaveis do projeto e Skills para workflows repetiveis.
