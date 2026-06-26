# Documentacao tecnica minima

Crie documentacao que ajude a manter e auditar o projeto.

## Documentos recomendados
- Visao geral do produto.
- Modelo de dominio.
- Casos de uso.
- Mapa de tabelas.
- Mapa de APIs/endpoints.
- Mapa de permissoes.
- Mapa de variaveis de ambiente.
- Arquitetura de pastas.
- Padroes de codigo.
- Plano de testes.
- Checklist de producao.
- Registro de decisoes tecnicas.

## Mapa de APIs
Para cada endpoint:
- Metodo e rota.
- Quem chama.
- Dados de entrada.
- Dados retornados.
- Autenticacao.
- Autorizacao.
- Tabelas ou servicos usados.
- Erros esperados.
- Dados sensiveis envolvidos.

## Mapa de permissoes
Para cada recurso:
- Quem pode criar.
- Quem pode ler.
- Quem pode atualizar.
- Quem pode excluir.
- Onde a permissao e validada.

## Mapa de env vars
Para cada variavel:
- Nome.
- Publica ou privada.
- Onde e usada.
- Pode ir para o browser?
- Ambiente: dev, staging, producao.
