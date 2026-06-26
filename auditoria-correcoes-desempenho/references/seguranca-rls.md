# Seguranca, RLS e permissoes

Revise autenticacao e autorizacao separadamente. Estar logado nao significa ter permissao.

## Verificar
- RLS ativado em tabelas publicas.
- Policies de SELECT, INSERT, UPDATE e DELETE separadas.
- UPDATE e DELETE restritos a owner, admin ou papel correto.
- Tabelas globais protegidas contra edicao por usuarios comuns.
- Policies com `using true` ou `with check true` sem justificativa.
- Usuario podendo alterar o proprio role.
- Funcoes RPC, triggers, Edge Functions, Server Actions ou API routes burlando RLS.
- Validacao confiavel de admin.

## Achados criticos
Classifique como critico quando:
- Qualquer usuario autenticado pode editar tabela global.
- Usuario consegue ler dados privados de outro usuario.
- Usuario consegue alterar o proprio papel.
- UPDATE ou DELETE usa `using true`/`with check true` em recurso sensivel.
- Admin e validado apenas no frontend.

## Exemplo de policy de UPDATE restrita a admin
```sql
alter table public.places enable row level security;

drop policy if exists "authenticated users can update places" on public.places;

create policy "admins can update places"
on public.places
for update
to authenticated
using (
  exists (
    select 1
    from public.profiles p
    where p.id = auth.uid()
      and p.role = 'admin'
  )
)
with check (
  exists (
    select 1
    from public.profiles p
    where p.id = auth.uid()
      and p.role = 'admin'
  )
);
```

## Saida esperada
Para cada policy, informe: tabela, operacao, quem deveria acessar, quem acessa hoje, risco, correcao e prioridade.
