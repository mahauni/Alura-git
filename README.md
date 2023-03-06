GIT
===

### Para começar um repositorio em sua maquina:
```bash
$ git init
```

### Para visualizar os arquivos com mais detalhes:
```bash
$ git status
```



### Para adicionar os arquivos:
```bash
adicionar todos os arquivos:
$ git add .

adicionar um arquivo:
$ git add ./path_to_file

adicionar todos os arquivos no folder colocado:
$ git add ./folder/*
```


### Para commitar no git:
```bash
% git commit -m "Sua mensagem descritiva por favor"
```


### Para visualizar mais informações sobre os commits:
```bash
$ git log

mostra os commits em uma linha (menos informaçoes):
$ git log --oneline

mostre os commits com maior detalhes:
$ git log -p

mostre as linhas de desenvolvimento do repo:
$ git log --graph

formate os logs com:
$git log --pretty="format:%H
```

#### Para ver as tags to --pretty:
https://devhints.io/git-log-format

#### site para ver mais detalhes do git log:
https://devhints.io/git-log

<br>
Ignore arquivos com o .gitignore
<br>
<br>

### Para iniciar um repositorio remoto na sua maquina para apenas controlar versões:
```bash
$ git init --bare
```


### Para adicionar o repositorio remoto em seu repositorio main:
```bash
Pode ser qualquer endereço valido para o git:
$ git remote add servidor-local ./path_to_the_repo

listar os repositorios remotos conhecidos no repositorio atual:
$ git remote

listar com mais informações:
$ git remote -v
```

### Para clonar:
```bash
git clone [endereço que voce colocou no endereço do repositorio remoto] [nome da pasta que voce quer onde clone]

enviar todas as alteraçoes para o repositorio remoto:
git push [do repositori em que voce esta] [para o repositorio remote que voce quer enviar]


Pega as mudanças do repositorio:
git pull [repositorio onde voce esta] [branch de onde o repositorio esta os arquivos]

rename the remote of your current repo:
git remote rename origin local
```

Para visualizar as branchs

git branch

Para criar uma nova branch:

git branch [nome da branch]


Para mudar para uma branch
git checkout [nome da branch]

Criar uma branch e mudar diretamente para ela:
git checkout -b [nome da branch]

Para visualizar com maiores detalhes como fuciona as branchs:
https://git-school-github.io/visualizing-git/


Para unificar sua branch de desenvolvimento com a master e criando um unico commit (merge commit) para demonstrar essa ação:
git merge [nome da branch de desenvolvimento]


Para voce unificar a branch mantendo os commits da branch de desenvolvimento na master:
git rebase [nome da branch de desenvolvimento]


Para desfazer de alterações no git:

Não foi ainda git add
git checkout -- [nome do arquivo]

Quando foi git add:
git reset HEAD [nome do arquivo]

Quando foi git commit:
git revert [hash do commit]


Salvar modificações de forma temporaria onde não utilize commits e gere um log:

git stash

Para mostrar suas stash:
git stash list

Para recuperar a stash
git stash apply [numero da stash]
e a stash continuaria existindo. Então para limpar a stash
git stash drop [numero da stash]

recupera a stash a remove a stash junto
git stash pop


Visualizar um codigo que ja foi pushed no repositorio remoto:

git checkout [hash do push que foi efetuado na repo remota]

todos os commits feitos aqui serão descartados ao voltar para a master.
Porém se voce fizer uma branch nesse push. Voce podera modificar e manter as atualizações de seus commits (Ex: como que aconteceu com o vim e neovim)


Ver a diferença entre dois commits feitos

git diff [hash do commit antigo]..[hash do commit mais novo]

Ver as alterações feitas e não commitadas (não foi usado git add)
git diff


Gerar uma versão release (Gerar um marco):

git tag -a [nome da tag (ex. v0.1.0)] -m "mensagem ao adicionar a tag"

Mostrar todas as tags disponiveis:
git tag

Para colocar a tag no repositorio remoto
git push origin [tag ex: v0.1.0]

após ser feita a marcação, não é possivel mais modificala. Após esse momento por exemplo, se a versão 0.1 foi released, todos os commits serão apenas para a versão proxima 0.2 nesse exemplo.