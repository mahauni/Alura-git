Para começar um repositorio em sua maquina:
git init



Para visualizar os arquivos com mais detalhes:
git status



Para adicionar os arquivos:
git add .   -> todos os arquivos
ou 
git add ./path_to_file
ou para adicionar todos os arquivos no folder colocado
git add ./folder/*



Para commitar no git
git commit -m "Sua mensagem descritiva por favor"



Para visualizar mais informações sobre os commits:
git log

mostra os commits em uma linha (menos informaçoes)

git log --oneline

mostra os commits com maior detalhes

git log -p

formate os logs com
git log --pretty="format:%H

Para ver as tags to --pretty
https://devhints.io/git-log-format

site para ver mais detalhes no git log:
https://devhints.io/git-log


Para ignorar arquivos com o
.gitignore


Para iniciar um repositorio remoto para apenas controlar versões
git init --bare


para adicionar o repositorio remoto em seu repositorio main
git remote add servidor-local ./path_to_the_repo
                              [Pode ser qualquer endereço valido para o git]

listar os repositorios remotos conhecidos no repositorio atual
git remote

listar com mais informações
git remote -v


Para clonar 
git clone [Endereço que voce colocou no endereço do repositorio remoto] [nome da pasta que voce quer onde clone]


enviar todas as alteraçoes para o repositorio remoto
git push [do repositori em que voce esta] [para o repositorio remote que voce quer enviar]


Pega as mudanças do repositorio
git pull [repositorio onde voce esta] [branch de onde o repositorio esta os arquivos]

rename the remote of your current repo
git remote rename origin local