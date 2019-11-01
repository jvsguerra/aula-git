# Git e GitHub

Guia prático para iniciantes.

# SCENES

- [x] Você deseja criar pontos na história da produção do seu projeto
```bash
$ git init
$ git add <file>
$ git commit -m "<message>"
```

- [x] Você deseja verificar mudanças feitas no seu projeto
```bash
$ git log
commit 6a84ed64ffbb1252a49d7928e5f27f250bc6d9ef (HEAD -> master)
Author: jvsguerra <jvsguerra@gmail.com>
Date:   Fri Nov 1 17:31:17 2019 -0300

    added landing page

$ git show <id>
    updated landing page

diff --git a/landingpage.html b/landingpage.html
index e69de29..5f12980 100644
--- a/landingpage.html
+++ b/landingpage.html
@@ -0,0 +1,2 @@
+landing page alteração
+
```

- [x] Você começa uma nova funcionalidade no seu projeto, sem estragar o que já foi feito.
```bash
$ git branch <name>
$ git checkout <name>
Switched to branch '<name>'

$ git branch
* <name>
  master
```

- [x] Você adiciona as novas funcionalidades ao seu projeto em produção
```bash
$ git checkout master
$ git merge <name>
Updating 1578097..dac38ea
Fast-forward
 cart.html | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 cart.html
```

- [x] Você quer deletar a branch da nova funcionalidade, depois de aplicar em seu projeto.
```bash
$ git branch -D <name>
Deleted branch <name> (was dac38ea).
```

- [x] Você quer colocar seu projeto na nuvem.
```bash
$ git remote add origin https://github.com/jvsguerra/aula-git.git
$ git remote -v
origin  https://github.com/jvsguerra/aula-git.git (fetch)
origin  https://github.com/jvsguerra/aula-git.git (push)

$ git push -u origin master

$ git config credential.helper store // Salva credenciais do GitHub
```

- [x] Você vai pegar um projeto já iniciado, para trabalhar com o time
```bash
$ git clone https://github.com/maykbrito/instagram-profile-header.git
$ cd instagram-profile-header/
```

- [x] Você precisa resolver um conflito.
```bash

```

- [x] Antes de enviar a resolução, precisamos atualizar o projeto local.
```bash
$ git pull
```

- [x] Você precisa voltar um arquivo para um determinado momento da linha do tempo.
```bash
$ git log
$ git status
$ git checkout <id> -- <file>
```

- [x] Você precisa recuperar algo deletado.
```bash
$ git log
$ git status
$ git checkout <id> -- <file>
```

* `git init` // inicia a linha do tempo
* `git add` // adiciona ou atualiza mudanças para irem para a linha do tempoo
* `git commit` // adiciona um ponto na linha do tempo
* `git log` // visualiza os pontos na linha do tempo / commit
* `git status` // informa o estado das alterações do nosso projeto
* `git show` // apresenta determinado ponto na história
* `git branch` // gerenciar novas linhas do tempo
* `git checkout` // manipula as linhas do tempo
* `git merge` // unir linhas do tempo
* `git push` // envia alterações locais para o repositório remoto
* `git clone` // clonar um projeto / repositório
* `git pull` // puxa do repositório remoto