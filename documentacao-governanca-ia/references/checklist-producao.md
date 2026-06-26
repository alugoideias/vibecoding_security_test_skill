# Checklist de producao

Use este checklist antes de publicar ou entregar.

## Produto e dominio
- [ ] Objetivo do produto documentado.
- [ ] Usuarios principais definidos.
- [ ] Entidades principais mapeadas.
- [ ] Casos de uso prioritarios descritos.
- [ ] Regras de negocio confirmadas.

## Arquitetura
- [ ] Responsabilidades separadas.
- [ ] UI nao concentra regra de negocio sensivel.
- [ ] Acesso a dados esta organizado.
- [ ] Padroes de pastas documentados.
- [ ] Hardcodes revisados.
- [ ] Duplicidades relevantes removidas ou registradas.

## Seguranca e dados
- [ ] Endpoints sensiveis exigem autenticacao.
- [ ] Endpoints sensiveis validam autorizacao.
- [ ] Usuario A nao acessa dados do usuario B.
- [ ] Admin e validado no backend/banco.
- [ ] Service role nao chega ao frontend.
- [ ] Env vars documentadas.

## Banco e performance
- [ ] Queries criticas mapeadas.
- [ ] Indices avaliados.
- [ ] Arrays/JSONB revisados para GIN quando necessario.
- [ ] Bundle inicial avaliado.
- [ ] Rotas raras carregam sob demanda.

## Testes e continuidade
- [ ] Testes unitarios para regras criticas.
- [ ] Testes e2e para fluxos principais.
- [ ] Testes de autorizacao.
- [ ] Registro de decisoes tecnicas atualizado.
- [ ] Proximo prompt recomendado documentado.
