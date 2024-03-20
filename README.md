# GitTutorial

Este repositório é destinado a guardar algumas configurações e comandos do Git para possíveis estudos futuros.

## Comandos Importantes do Git:

- `git c "nome do commit"`: Adiciona todos os arquivos alterados e faz o commit.
- `git commit --amend`: Faz um commit no último commit já feito.

## Configurações do GitHub para Facilitar Merges, Commits e Adicionar Estilo ao Git Log:

```bash
git config --global core.editor code
git config --global --edit
```

-Cole esse codigo : 

[core]
	editor = code
[user]
	email = email do github
	name = usuario do github
[push]
	followTags = true
[core]
	editor = code --wait
[alias]
	s = !git status -status
	c = !git add --all && git commit -m
	l = !git log --pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
##Suposição:
Suponha que seja necessário criar uma branch para testar algo que talvez seja útil para o código e, caso seja confirmado, passar essas alterações para outra branch.

Exemplo de Fluxo:
1. `git pull origin KAN-21`
2. `git checkout develop`
3. `git pull origin develop`
4. `git checkout -b "testBranch"`
5. `git add . (adicione os arquivos separadamente caso precise de mais de um commit)`
6. `git commit -m "nome do commit"`
7. `git checkout KAN-21`
8. `git merge testBranch`
9. `git push origin KAN-21`
