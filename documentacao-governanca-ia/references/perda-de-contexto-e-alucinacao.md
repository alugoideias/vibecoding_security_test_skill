# Perda de contexto e alucinacao da IA

Revise sinais de codigo gerado sem contexto consistente.

## Sinais de perda de contexto
- Funcoes duplicadas com nomes parecidos.
- Regras contraditorias em arquivos diferentes.
- Componentes que resolvem o mesmo problema de formas diferentes.
- Imports inexistentes.
- Chamadas a funcoes que nao existem.
- Tabelas ou colunas citadas no codigo mas ausentes no banco.
- Comentarios que nao batem com a implementacao.
- Endpoints assumindo campos inexistentes.
- Validacoes inconsistentes entre frontend, backend e banco.

## Sinais de alucinacao tecnica
- Biblioteca usada com API inexistente.
- Metodo que nao existe na versao instalada.
- Configuracao invalida.
- SQL incompatível com PostgreSQL/Supabase.
- Policy que parece segura, mas nao valida owner, tenant ou role.
- Variavel de ambiente citada mas nunca definida.

## Como reduzir risco
- Manter mapa de dominio atualizado.
- Manter mapa de APIs e tabelas.
- Incluir versoes de bibliotecas quando relevante.
- Pedir que a IA cite arquivos e evidencias.
- Exigir testes ou comandos de verificacao.
- Criar checkpoints: "antes de implementar, confirme premissas".

## Saida esperada
Liste inconsistencias, arquivos afetados, risco, como validar e como corrigir.
