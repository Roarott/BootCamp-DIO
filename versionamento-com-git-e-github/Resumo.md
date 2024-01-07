# Versionamento de Código com Git e GitHub

Listagem comentada e resumida de códigos vistos no curso de Versionamento de Código com Git e GitHub promovido pela [Digital Innovation One](https://dio.me)

## 💻 Criação e Clonagem de Repositórios

```
git clone <URL> <folder-name>
# Clona <URL> a em <folder-name>

git clone <URL> --branch <branch-name> --single-branch <folder-name>
# Clona apenas <branch-name> a uma pasta <folder-name>

mkdir Directory-Name
# Cria um diretório

git init
# Cria um repositório local num diretório

git remote add <remote-repository-name> <URL>
# Conecta um repositório remoto <URL> ao repositório local

git remote -v
# Lista os repositórios remotos associados ao repositório local
```

## 🗳 Salvamento e Envio de Repositórios Locais aos Repositórios Remotos

```
git commit -m"<commit-message>"
# Salva o repositório local

git status
# Exibe o status da working tree

git log
# Exibe o histórico de commits do repositório

git add <file-name>
# Adiciona o <file-name> ao próximo commit
```

## ↩ Restauração de Repositórios Locais

```
rm -rf <folder-name>
# Deleta recursiva e forçadamente o <folder-name>
OBS.: É possível deletar o .git, assim restaurando o estado de repositório para um diretório

git reset --<mode> <commit-hash>
# <mode> == soft : Restaura o repositório ao estado de logo antes do primeiro commit após o <commit-hash>
# <mode> == mixed : Restaura o repositório ao estado de logo antes do primeiro commit após o <commit-hash> e todos os arquivos modificados e adicionados retornam a forma de não rastreados
# <mode> == hard : Deleta todas as alterações e adições de todos os commits posteriores ao <commit-hash>

git commit --amend -m"<mensagem-alterada>"
# Muda a mensagem do último commit para <mensagem-alterada>

git reflog
# Histórico ainda mais detalhado das alterações feitas nos commits do repositório
```

## 🔄 Enviando e Baixando Alterações com o Repositório Remoto

```
git push -u <remote-repository-name> <branch-name>
# Envia todas as alterações da <branch-name> para o <remote-repository-name>

git pull
# Baixa todas as alterações do repositório remoto para o repositório local
```

## 👷‍♂️ Trabalhando com Branches : Criando, Mesclando, Deletando e Tratando Conflitos

```
git branch -v
# Lista as branches do repositório e as commits associadas

git branch -d <branch-name>
# Deleta a branch com o nome <branch-name>

git checkout -b <branch-name>
# Cria uma branch com o nome <branch-name>

git merge <branch-name>
# Mescla a branch atual com a <branch-name>

git fetch <remote-repository-name> <branch-name>
# Baixa os arquivos de <branch-name> localizada em <remote-repository-name> sem mesclar os arquivos com o repositório local

git diff <local-branch-name> <remote-repository-branch>
# Exibe a diferença entre os arquivos de <local-branch-name> e os arquivos de <remote-repository-branch>

git stash
# Arquiva todas as modificações feitas

git stash <mode>
# <mode> == pop : Restaura as modificações feitas e as remove da lista stash
# <mode> == apply : Restaura as modificações feitas e as mantém na lista stash
```