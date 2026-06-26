# Testes tecnicos

O objetivo e evitar que correcoes quebrem fluxo critico ou autorizacao.

## Testes unitarios
Criar para:
- Regras de negocio criticas.
- Validacoes de input.
- Funcoes de permissao.
- Transformacoes de dados.
- Calculos e matching.

## Testes de integracao
Criar para:
- Services que acessam banco ou APIs.
- Endpoints com autenticacao.
- Queries e filtros importantes.
- RPCs e Edge Functions.

## Testes e2e
Criar para:
- Login e cadastro.
- Criacao e edicao de perfil.
- Fluxo principal do produto.
- Area admin.
- Permissao negada.
- Estados de erro, loading e vazio.

## Testes de seguranca obrigatorios
- Usuario A nao acessa dados do usuario B.
- Usuario comum nao chama endpoint de admin.
- Usuario sem login nao acessa dados privados.
- UPDATE e DELETE respeitam owner, tenant ou role.
- Endpoint nao retorna campos sensiveis desnecessarios.

## Saida esperada
Para cada teste sugerido, informe objetivo, tipo, fluxo, cenario e criterio de sucesso.
