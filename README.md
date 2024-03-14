# GitTutorial
Repositório para guardar algumas configs e comandos git para possível estudos necessários no futuro.

Comandos importantes Git:
-git c "nome do commit" : add todos os arquivos alterados e ja commita.
-git commit --amend : commita no ultimo commit ja feito.

Config github para facilitar merge, commits e adicionar pretty no git log:
-git config --global core.editor code
-git config --global --edit

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




suposicao:
Preciso criar uma kan para testar algo que talvez seja util para codigo e caso seja
passar essas alteracoes para outra branch.
-Exemplo:
	*branch principal : develop
	*branch atual : KAN-21
	*branch nova " testBranch

&fluxo :
1-git pull origin KAN-21
2-git checkout develop
3-git pull origin develop
4-git checkout -b "testBranch"
5-git add .( adicione os arquivos separadamente caso precise de mais de um commit
6-git commit -m "nome do commit"
7-git checkout KAN-21
8-git merge testBranch
9-git push origin KAN-21
