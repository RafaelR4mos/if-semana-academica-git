# Semana Acadêmica – Git (Prática)

Repositório de prática para comandos básicos, branches, PRs, conflitos e merges.

## Como começar

```bash
git clone <URL-DO-SEU-REPO>
cd semana-academica-git
git checkout -b feature/<nome-feat>
```

> OBS: Se quiser testar uma branch com a pipeline de linting e pre-commit, deve executar o comando `npm install` para instalar as dependências do Node.

## Exercícios

### COMMIT BÁSICO e PR

1. Na sua branch, edite `src/index.html`, adicione seu nome na linha:

```html
<li>SEU NOME</li>
```

2. Adicione os itens em stage e faça um **commit semântico**. Use mensagens como `feat: add name`. Use o comando `git status` para garantir que seus itens foram adicionados com o `git add .`.

3. Faça o upload das suas alterações para o repositório remoto use a estrutura do comando:

```bash
git push origin <nome-da-sua-branch>
```

4. Abra um PR apontando para a branch `main` seguindo como base o arquivo de exemplo.

> OBSERVAÇÃO: Caso, você não esteja com a versão mais atualizada da branch `main` e outras pessoas tenham alterado a mesma linha no mesmo arquivo que você pode ser que você tenha um conflito. Você pode resolver o conflito na sua branch local e fazer um novo commit corrigindo isso.

## Alguns Padrões

### Padrões de Branches

- `feat/<nome-feat>` -> Nome de branch que representa a criação de uma nova funcionalidade
- `fix/<nome-fix>` -> Branch para correção de bugs ou problemas
- `docs/<nome-docs>` -> Branch para alterações na documentação
- `chore/<nome-chore>` -> Branch para tarefas de manutenção, atualizações de dependências, etc.
- `refactor/<nome-refactor>` -> Branch para refatoração de código sem alterar sua funcionalidade
- `test/<nome-test>` -> Branch para adição ou modificação de testes
- `style/<nome-style>` -> Branch para mudanças que não afetam o significado do código (formatação, espaços, etc.)
- `perf/<nome-perf>` -> Branch para mudanças de código que melhoram o desempenho

### Padrões de Commits

- Commits: Conventional Commits
  - `feat: ...` -> Adiciona nova funcionalidade
  - `fix: ...` -> Corrige um bug
  - `docs: ...` -> Alterações na documentação
  - `style: ...` -> Mudanças que não afetam o significado do código
  - `refactor: ...` -> Refatoração do código
  - `test: ...` -> Adição ou modificação de testes
  - `chore: ...` -> Atualizações de tarefas de build, configurações, etc.
  - `perf: ...` -> Melhorias de performance

## Dicas

- Evite commits diretamente na `main`: crie uma branch e abra PR.
- Use o template de PR para checklist e descrição.
- Caso tenha cometido algum erro de padrão no commit você pode usar o comando abaixo para desfazer:

```bash
git reset --soft HEAD~1
```

O commit é removido do histórico local, as alterações voltam para a staging area (você pode fazer um novo commit logo em seguida).cIdeal quando ainda não fez push.
