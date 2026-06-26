# Modelagem de dominio

Modele o projeto a partir do problema de negocio, nao a partir das telas.

## Verificar
- Entidades principais.
- Relacionamentos entre entidades.
- Regras que pertencem a cada entidade.
- Estados possiveis e transicoes.
- Campos genericos demais, como `type`, `status` ou `data`, sem regra clara.
- Tabelas que nao refletem bem o dominio.
- Conceitos duplicados com nomes diferentes.
- Regras de negocio espalhadas em componentes.

## Saida esperada
Para cada entidade:
- Nome.
- Responsabilidade.
- Campos principais.
- Relacionamentos.
- Regras de negocio.
- Quem pode criar, ler, atualizar e excluir.
- Duvidas ou decisoes pendentes.

## Sinais de problema
- Uma tela sabe regras demais.
- Um componente decide permissao.
- A mesma entidade aparece com nomes diferentes.
- O banco permite estados que o produto nao deveria permitir.
