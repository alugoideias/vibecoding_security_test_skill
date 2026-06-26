# Endpoints, APIs e exposicao de dados

Parta do principio de que qualquer pessoa pode chamar a API diretamente, sem passar pela interface.

## Verificar
- Endpoints publicos sem autenticacao.
- Endpoints que retornam dados sensiveis sem autorizacao.
- Nome, e-mail, telefone, endereco, documentos, localizacao ou dados de pagamento em respostas publicas.
- Listagens retornando dados de todos os usuarios sem filtro por owner, tenant, role ou permissao.
- Endpoints de admin protegidos apenas por UI.
- Alteracao manual de id em URL ou payload acessando recurso de outro usuario.
- APIs, RPCs, Edge Functions, Server Actions e API routes sem validacao.
- Buckets publicos indevidos.
- Arquivos privados acessiveis por URL direta.
- Falta de rate limit em rotas sensiveis.
- Logs ou erros expondo dados internos.

## Testes mentais obrigatorios
- Usuario A acessa dados do usuario B.
- Usuario comum chama endpoint de admin.
- Pessoa sem login chama endpoint de listagem.
- Ids sao alterados manualmente.
- Arquivos privados sao baixados por URL direta.
- Payload tenta fazer update ou delete indevido.

## Achados criticos
Classifique como critico quando:
- Dados pessoais aparecem sem autenticacao.
- Dados de todos os usuarios retornam em endpoint publico.
- Usuario comum acessa dados privados de outro usuario.
- Rota protegida apenas no frontend permite acesso direto ao backend.
- Endpoint de admin aceita usuario comum.

## Frase obrigatoria para riscos reais
"Este e um problema critico de seguranca. O fato de a aplicacao funcionar nao significa que ela esteja segura. A correcao precisa ser feita no backend, no banco de dados ou nas policies, nao apenas na interface."

## Saida esperada
Para cada endpoint ou recurso: metodo, dados retornados, exige autenticacao, valida autorizacao, quem deveria acessar, quem acessa hoje, risco, correcao e prioridade.
