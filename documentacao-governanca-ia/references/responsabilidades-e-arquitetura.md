# Responsabilidades e arquitetura

Separe UI, regras de negocio, validacao, autorizacao, acesso a dados e integracoes.

## Verificar
- Componentes fazendo query, validacao, permissao e renderizacao juntos.
- Chamadas diretas ao Supabase ou API espalhadas por paginas.
- Regras de negocio repetidas em varios lugares.
- Hooks com responsabilidades demais.
- Services ausentes ou confusos.
- Backend misturando autenticacao, autorizacao, validacao e execucao sem clareza.
- Tipos, schemas e contratos duplicados.

## Mapa sugerido
- UI: renderiza e coleta interacao.
- Hooks/controllers: coordenam estado da tela.
- Use cases/services: executam regra de negocio.
- Repositories/clients: acessam banco ou API.
- Policies/backend: validam autorizacao real.
- Schemas: validam input e output.

## Saida esperada
- Mapa de camadas.
- Responsabilidade de cada pasta ou modulo.
- Pontos de acoplamento.
- Regras duplicadas.
- Recomposicao recomendada sem reescrever tudo.
