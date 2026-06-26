# Chaves, secrets e variaveis de ambiente

Secrets privados nunca devem chegar ao browser, bundle final, logs publicos ou historico Git.

## Verificar
- `service_role` ou equivalente no frontend.
- Secrets hardcoded em codigo, configuracao ou exemplos.
- Uso correto de anon key, public key ou client key.
- Variaveis publicas e privadas separadas.
- Prefixos publicos como `VITE_` e `NEXT_PUBLIC_` usados apenas para valores seguros para browser.
- `.env` versionado indevidamente.
- `.gitignore` cobrindo arquivos sensiveis.
- Tokens em logs, mensagens de erro e responses.
- Necessidade de auditoria no historico Git.

## Termos para procurar
- service_role
- SUPABASE_SERVICE_ROLE_KEY
- secret
- private_key
- api_secret
- token
- password
- anon
- supabaseUrl
- supabaseKey

## Comandos uteis
```bash
git grep "service_role"
git grep "SUPABASE_SERVICE_ROLE"
git log -S "service_role" --all
git log -S "SUPABASE_SERVICE_ROLE_KEY" --all
gitleaks detect --source . -v
```

## Regra critica
Se uma chave privada ja foi commitada, remover do codigo nao basta. Oriente rotacionar a chave no provedor e investigar impacto.

## Saida esperada
Indique arquivo, tipo de chave, risco, se chega ao frontend, correcao e prioridade.
