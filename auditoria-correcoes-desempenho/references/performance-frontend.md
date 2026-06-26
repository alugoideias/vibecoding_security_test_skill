# Performance de frontend

Revise o carregamento inicial e o custo de JavaScript antes de qualquer otimizacao visual.

## Verificar
- Bundle inicial inflado.
- Paginas carregadas no primeiro acesso sem necessidade.
- Admin, termos, configuracoes, dashboard e telas raras entrando junto com a tela inicial.
- Falta de lazy loading por rota.
- Falta de code splitting.
- Vendors misturados com codigo de aplicacao.
- Bibliotecas grandes importadas de forma global.
- Componentes pesados carregados antes de serem usados.
- Falta de estado de loading para rotas lazy.
- Cache incorreto para assets versionados.

## Evidencias a buscar
- Arquivos de rotas com imports diretos de todas as paginas.
- Configuracao Vite, Webpack ou Next.js sem analise de chunks.
- Build analyzer mostrando vendor ou pagina rara no chunk inicial.
- Imports como biblioteca inteira quando so uma funcao e usada.

## Correcoes comuns
- Usar lazy loading por rota.
- Separar paginas em chunks proprios.
- Separar vendors por estabilidade: react, supabase, ui, charts.
- Substituir bibliotecas grandes ou carregar sob demanda.
- Configurar cache longo para assets com hash e no-cache para HTML.

## Metricas
- Tamanho do bundle inicial.
- Numero de chunks.
- LCP, INP e CLS.
- Tempo ate interacao.
- Tempo de carregamento da primeira rota.
