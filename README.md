# Aprendendo Git :squid:

#### Sumário de Comandos:

- [git init](#git-init)
- [git add](#git-add[)
- [git rm](#git-rm)
- [git commit](#git-commit)
- [git status](#git-status)

<hr>

## Ciclo de vida de um repositório git

#### Durante o desenvolvimento os arquivos dentro de um repositório git  passam por um ciclo de vide que tem os seguintes status:

- [Untracked](#untracked)
- [Unmodified](#unmodified)
- [Modified](#modified)
- [Staged](#staged)



É possível verificar o status dos arquivos do repositório através do comando [git status](#git-status)

### Untracked

Todos os arquivos inicialmente estarão neste estágio, aqui é onde os arquivos são adicionados ao ambiente do repositório mais anida não estão sendo monitorados pelo git, para fazer isso será necessário adicioná-los usando o **[gid add](#git-add)**.

Após adicioná-lo ele vai direto para o status [Staged](#staged)

### Unmodified

Neste estágio estarão os arquivos que já foram "commitados" e ainda não sofreram nenhuma alteração. Quando um arquivo neste estágio sofrer alguma alteração eles irão para o estágio [modified](#modified).

### Modified

Quando um arquivo sofre uma alteração ele passa para este estágio, 

### Staged

Os arquivos neste estágio estão prontos para serem armazenados atravez do comando [git commit](#git-commit). Após as alterações terem sido armazenadas pelo commit os arquivos que foram "commitados" vão para o estágio [unmodified](#unmodified).

# git init

```bash
git init #inicia um repositório git na pasta atual.
```

# git add

```bash
git add * #adiciona todos os arquivos ao rastreamento do git para que ele gerencie suas mudanças e armazená-las em commits.
```

```bash
git add <arquivo> #adiciona o <arquivo> ao rastreamento do git para que ele gerencie suas mudanças e armazená-las em commits.
```

# git rm

```bash
git rm <arquivo> #remove o <arquivo> do rastreamento do git para deixar de gerenciar mudancas e incluir em commits.
```

# git restore

```bash
git restore --staged <arquivo> #
```

# git commit

```bash
git commit -m "Comentário do commit" #cria um commit 'salvando' o status do projeto. -m > especifica a mensagem, uma breve descrição das modificações.

git commit -a -m "Comentário do commit" # -a > adiciona todos os arquivos ao commit.
```

# git status

```bash
git status #mostra o status do repositório se existe algum arquivo que não está sendo rastreado, arquivos modificados, deletados, mostra de maneira geral o status de todo o repositório.
```





# Fluxo de trabalho git

- git init - iniciar o repositório.
- git add < arquivo > / * - adiciona o < arquivo > específico ou * todos os arquivos a área de Staged(pronto para fazer o commit)