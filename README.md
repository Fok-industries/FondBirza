Работа с фондовой биржей в рамках программной инженерии
artur@fok:~/Документы/GIT$ git init

Инициализирован пустой репозиторий Git в /home/artur/Документы/GIT/.git/
artur@fok:~/Документы/GIT$ git add BIRZHA

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
