# exercicio01



Passo 1 - Definição de usuário e e-mail:
Comandos: git config --global user.name "Jean Paulo Leandro" e git config --global user.email "jean.leandro@aluno.faculdadeimpacta.com.br"

@Jeanpleandro ➜ /workspaces/codespaces-blank $ git config --global user.name "Jean Paulo Leandro"
@Jeanpleandro ➜ /workspaces/codespaces-blank $ git config --global user.email "jean.leandro@aluno.faculdadeimpacta.com.br"

Passo 2 - Criação do diretório exercicio01.
Comando: mkdir exercicio01

@Jeanpleandro ➜ /workspaces/codespaces-blank $ mkdir exercicio01
@Jeanpleandro ➜ /workspaces/codespaces-blank $ cd exercicio01/

Passo 3 - Criação do subdiretório .git, acesso ao subdiretório e listar os arquivos do subdiretório .git
Comandos git init, cd .git e ls -l
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 $ git init
Initialized empty Git repository in /workspaces/codespaces-blank/exercicio01/.git/
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ cd .git
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01/.git (main) $ ls -l
total 32
-rw-rw-rw-  1 codespace codespace   21 Aug  5 15:21 HEAD
drwxrwxrwx+ 2 codespace codespace 4096 Aug  5 15:21 branches
-rw-rw-rw-  1 codespace codespace   92 Aug  5 15:21 config
-rw-rw-rw-  1 codespace codespace   73 Aug  5 15:21 description
drwxrwxrwx+ 2 codespace codespace 4096 Aug  5 15:21 hooks
drwxrwxrwx+ 2 codespace codespace 4096 Aug  5 15:21 info
drwxrwxrwx+ 4 codespace codespace 4096 Aug  5 15:21 objects
drwxrwxrwx+ 4 codespace codespace 4096 Aug  5 15:21 refs

Passo 4 - Verificar o status.
Comando: git status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

Passo 5 - Criação do arquivo README.md
Comando vi README.md

@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ vi README.md

Passo 6 - Verificar o status.
Comando: git status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

Passo 7 - Adicionar o arquivo README.md no modo stage e verificar o status.
Comandos git add . e git status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add .
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

Passo 8 - Commit do arquivo README.md
Comando git commit -m "git README.md"
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "git README.md"
[main (root-commit) 3e5dbd6] git README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
 
EXERCÍCIO – Básico sobre staging / commit:

a) No working dir, executar o comando: echo 01 > arquivo.txt
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 01 > arquivo.txt

b) Adicionar o arquivo no staging e conferir o status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt 
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arquivo.txt

c) Commitar o arquivo do staging com a descrição "git add example - arquivo.txt“
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "git add example - arquivo.txt"
[main a08be3d] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

d) Sobrescrever o conteúdo do arquivo.txt: echo 02 > arquivo.txt
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 02 > arquivo.txt

e) Verificar o diffing no arquivo
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

f) Adicionar novamente o arquivo no staging e conferir o status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt 
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

g) Verificar o diffing no arquivo
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff

h) Sobrescrever o conteúdo do arquivo.txt: echo 03 > arquivo.txt
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 03 > arquivo.txt

i) Verificar o diffing no arquivo
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

j) Fazer o restore do arquivo da área de staging e verificar o status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git restore arquivo.txt
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

k) Realizar o commit do arquivo e verificar o log
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt 
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "Atualizacao do arquivo.txt"
[main 7004486] Atualizacao do arquivo.txt
 1 file changed, 1 insertion(+), 1 deletion(-)
 
l) Adicionar um arquivo gitignore com o seguinte conteúdo: *.txt
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ vi .gitignore

m) Criar um arquivo novo.txt e verificar o status
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ touch novo.txt
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add .
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "add o arquivo .gitignore"
[main f3edeb3] add o arquivo .gitignore
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
nothing to commit, working tree clean
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ 
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ 
@Jeanpleandro ➜ /workspaces/codespaces-blank/exercicio01 (main) $ 
