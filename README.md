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