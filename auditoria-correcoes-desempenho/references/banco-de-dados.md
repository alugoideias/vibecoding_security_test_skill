# Banco de dados, queries e indices

Revise consultas pensando no crescimento da base, nao apenas no volume atual.

## Verificar
- Queries criticas de feed, matching, busca, perfil, dashboard, login, listagens e admin.
- Filtros, joins, ordenacoes e foreign keys sem indice adequado.
- Busca em arrays, JSONB ou texto sem indice apropriado.
- Arrays de preferencias de usuario sem indice GIN quando usados em matching.
- Select amplo retornando colunas desnecessarias.
- Queries em loop no frontend ou backend.
- Falta de paginacao, limit e ordenacao estavel.
- Policies RLS que tornam queries lentas.

## Indices recomendaveis
- B-tree para colunas usadas em igualdade, range, joins e ordenacao.
- GIN para arrays, JSONB e busca textual quando a query pesquisa dentro da estrutura.

## Exemplo GIN
```sql
create index if not exists nome_tabela_coluna_gin_idx
on public.nome_tabela
using gin (nome_coluna);
```

## Exemplo EXPLAIN
```sql
explain analyze
select *
from public.nome_tabela
where preferencias && array['cinema', 'tecnologia'];
```

## Sinais de alerta
- Seq Scan em tabela grande.
- Muitas linhas removidas por filtro.
- Custo alto em query frequente.
- Ordenacao cara sem indice.
- Nested loop inesperado em grande volume.

## Saida esperada
Para cada query relevante, informe problema, evidencia, impacto, correcao, script SQL recomendado e prioridade.
