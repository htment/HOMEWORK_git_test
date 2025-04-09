1. git clone git@github.com:netology-code/sys-pattern-homework.git
2. git init - инициализируем репозиторий
3. git config --global init.defaultBranch main
4. git branch --show  показать теущую ветку 
  git checkout -b  master создать новую ветку и переключиться на нее
5. git status  статус
6. git diff --staged показать изменения
7. git add README.md Перевел файл в состояние staged:
---еще раз смотрим изменения
8. git diff
   git diff --staged
9. git add .

10. git remote add origin git@github.com:htment/HOMEWORK_git_test.git подключаем удаленный репозиторий
11. git remote -v просмотр удаленных репозиториев
12. git push origin master пушим в ветку master

новая ветка
git checkout -b dev

. Создал в ветке dev файл test.sh с произвольным содержимым:
echo "#!/bin/bash" > test.sh
echo "echo 'Hello from dev.'" >> test.sh
chmod +x test.sh

несколько коммитов и пушей в ветку dev
git add test.sh
git commit -m "Add test.sh with greetings"
echo "echo 'Second line from dev.'" >> test.sh
git add test.sh
git commit -m "Update test.sh - add second line"
git push origin dev


git push --set-upstream origin dev в Git используется для отправки локальной ветки dev на 
git branch -d branchName — безопасное удаление: ветка будет если был merge
git branch -D branchName — принудительное удаление


git checkout -p test test.sh - один файл


git rebase -i <хеш_коммита_перед_тем_который_нужно_изменить>
 git rebase -i (интерактивный rebase):  Это самый распространённый и гибкий способ.  Он позволяет редактировать историю коммитов.
  Вы можете внести необходимые изменения в файлы, закоммитить их (возможно, с новым сообщением) и продолжить rebase командой git rebase --continue. 
  
Измените команду на reword, edit или squash:  В редакторе вы увидите список коммитов, которые будут затронуты rebase. Найдите коммит, который нужно изменить, и измените команду перед ним с pick на:

    * reword:  Позволяет изменить сообщение коммита.
    * edit: Позволяет изменить как сообщение коммита, так и сами файлы.  Это наиболее подходящий вариант, если нужно изменить содержимое коммита.
    * squash:  Объединяет этот коммит с предыдущим.

.  git revert более безопасен в этом отношении.  Если вы не уверены, лучше использовать git revert.

создать подреппозиторий
git submodule add git@github.com:netology-code/sdvps-materials.git sdvps-materials