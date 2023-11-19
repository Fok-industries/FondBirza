Работа с фондовой биржей в рамках программной инженерии
artur@fok:~/Документы/GIT$ git init
подсказка: Using 'master' as the name for the initial branch. This default branch name
подсказка: is subject to change. To configure the initial branch name to use in all
подсказка: of your new repositories, which will suppress this warning, call:
подсказка: 
подсказка: 	git config --global init.defaultBranch <name>
подсказка: 
подсказка: Names commonly chosen instead of 'master' are 'main', 'trunk' and
подсказка: 'development'. The just-created branch can be renamed via this command:
подсказка: 
подсказка: 	git branch -m <name>
Инициализирован пустой репозиторий Git в /home/artur/Документы/GIT/.git/
artur@fok:~/Документы/GIT$ git add BIRZHA
warning: добавление встроенного git репозитория: BIRZHA/FondBirza
подсказка: You've added another git repository inside your current repository.
подсказка: Clones of the outer repository will not contain the contents of
подсказка: the embedded repository and will not know how to obtain it.
подсказка: If you meant to add a submodule, use:
подсказка: 
подсказка: 	git submodule add <url> BIRZHA/FondBirza
подсказка: 
подсказка: If you added this path by mistake, you can remove it from the
подсказка: index with:
подсказка: 
подсказка: 	git rm --cached BIRZHA/FondBirza
подсказка: 
подсказка: See "git help submodule" for more information.
artur@fok:~/Документы/GIT$ git commit -m "first"
[master (корневой коммит) 19b4a18] first
 1 file changed, 1 insertion(+)
 create mode 160000 BIRZHA/FondBirza
artur@fok:~/Документы/GIT$ git branch
* master
artur@fok:~/Документы/GIT$ git checkout -b
error: switch `b' requires a value
artur@fok:~/Документы/GIT$ git checkout -b slave
Переключились на новую ветку «slave»
artur@fok:~/Документы/GIT$ git branch
  master
* slave
artur@fok:~/Документы/GIT$ git checkout master
Переключились на ветку «master»
artur@fok:~/Документы/GIT$ git checkout -b develop
Переключились на новую ветку «develop»
artur@fok:~/Документы/GIT$ git checkout -b feature
Переключились на новую ветку «feature»
artur@fok:~/Документы/GIT$ git branch
  develop
* feature
  master
  slave
artur@fok:~/Документы/GIT$ git log
commit 19b4a18a2d71f988418466712fbe9d06e3cf9d84 (HEAD -> feature, slave, master, develop)
Author: FOK <arturfockin.2000@yandex.ru>
Date:   Mon Nov 20 02:08:09 2023 +0300

    first
artur@fok:~/Документы/GIT$ git add .
artur@fok:~/Документы/GIT$ git commit -m "second"
[feature 5b4ea87] second
 1 file changed, 1 insertion(+)
 create mode 100644 BIRZHA/BROKER/README.md
artur@fok:~/Документы/GIT$ git log
commit 5b4ea87a79b9bc1b17586b10fdb6c6dac8c15730 (HEAD -> feature)
Author: FOK <arturfockin.2000@yandex.ru>
Date:   Mon Nov 20 02:20:48 2023 +0300

    second

commit 19b4a18a2d71f988418466712fbe9d06e3cf9d84 (slave, master, develop)
Author: FOK <arturfockin.2000@yandex.ru>
Date:   Mon Nov 20 02:08:09 2023 +0300

    first
artur@fok:~/Документы/GIT$ git reset --hard 19b4a18a2d71f988418466712fbe9d06e3cf9d84
Указатель HEAD сейчас на коммите 19b4a18 first
artur@fok:~/Документы/GIT$ git log
commit 19b4a18a2d71f988418466712fbe9d06e3cf9d84 (HEAD -> feature, slave, master, develop)
Author: FOK <arturfockin.2000@yandex.ru>
Date:   Mon Nov 20 02:08:09 2023 +0300

    first
artur@fok:~/Документы/GIT$ git log --graph
* commit 19b4a18a2d71f988418466712fbe9d06e3cf9d84 (HEAD -> feature, slave, master, develop)
  Author: FOK <arturfockin.2000@yandex.ru>
  Date:   Mon Nov 20 02:08:09 2023 +0300
  
      first
artur@fok:~/Документы/GIT$ 
