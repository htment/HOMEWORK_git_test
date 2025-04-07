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