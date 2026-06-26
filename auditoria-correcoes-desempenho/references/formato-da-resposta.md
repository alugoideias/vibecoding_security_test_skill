# Formato da resposta

Use uma resposta objetiva, com evidencia, impacto e correcao.

## Resumo executivo
- Principais riscos.
- Areas criticas.
- Impacto.
- Prioridade geral.

## Achados criticos
Para cada achado:
- Status: Confirmado, hipotese forte, risco potencial ou nao validado.
- Evidencia: arquivo, trecho, endpoint, rota, query ou policy.
- Impacto.
- Correcao recomendada.
- Prioridade.

## Secoes tecnicas
Use este formato:
- Problema encontrado:
- Evidencia:
- Impacto:
- Solucao:
- Arquivos afetados ou script SQL recomendado:
- Prioridade:

## Arquivos completos corrigidos
Quando o arquivo completo foi fornecido:
- Entregue o arquivo completo corrigido.
- Preserve partes nao alteradas.
- Nao use `...` para ocultar codigo importante.
- Explique antes as mudancas.
- Informe o caminho sugerido.

Quando nao houver contexto suficiente:
- Diga que a versao completa depende do restante do arquivo.
- Entregue patch ou bloco parcial marcado como parcial.

## Scripts SQL
- Entregue script completo.
- Use `if exists` e `if not exists` quando fizer sentido.
- Inclua comentarios.
- Alerta antes de comandos destrutivos.
- Recomende staging antes de producao.
