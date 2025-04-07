# Домашнее задание к занятию "`Название занятия`" - `Фамилия и имя студента`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

1. Зарегистрировал аккаунт на GitHub.
2. Создал новый публичный репозиторий с названием HOMEWORK_git_test и инициализировал его с файлом README.md.
3. Склонировал репозиторий, используя https протокол:

```git clone https://github.com/git@github.com:htment/HOMEWORK_git_test.git```
4. Перешел в каталог с клоном репозитория:
```cd GIT_TEST```
5. Произвел первоначальную настройку Git:
```
git config --global user.name 
git config --global user.email
 ```
6. Выполнил команду git status и запомнил результат:

```git status```

Результат: On branch master; nothing to commit, working tree clean (или аналогичное).
7. Отредактировал файл README.md, добавив текст.
8. Повторно выполнил git status:

```git status```

Результат: Теперь файл README.md находится в состоянии Modified.

9. Посмотрел изменения в файле README.md:
```git diff```

10. Перевел файл в состояние staged:

```git add README.md```

11. Ещё раз выполнил команды:

```
git diff
git diff --staged
```

12. Сделал коммит:

```
git commit -m 'First commit'
```

13. Сделал пуш:

```
git push origin master
```

Ссылка на коммит: [First commit](https://github.com/htment/HOMEWORK_git_test/tree/7809500bb05012e02133feb61845c0b7750fbeee)



---

### Задание 2
1. Создал файл .gitignore:

```touch .gitignore```

Проверил его статус:
```git status```

Результат: файл .gitignore находится в состоянии Untracked.

2. Добавил файл .gitignore в следующий коммит:

```git add .gitignore```

3. Написал правила в .gitignore, чтобы игнорировать файлы .pyc и все файлы в директории cache:


```
*.pyc
cache/

```

4. Сделал коммит:

```git commit -m 'Add .gitignore file'```

5. Сделал пуш:

```git push origin master```

Ссылка на коммит: 

[Add .gitignore file](https://github.com/htment/HOMEWORK_git_test/tree/10c93856e58a965c8deea7a1e16269ac178489ee)





---

### Задание 3

`Приведите ответ в свободной форме........`

1. Создал новую ветку dev и переключился на неё:
```
git checkout -b dev
```
2. Создал в ветке dev файл test.sh с произвольным содержимым:
```

echo "#!/bin/bash" > test.sh
echo "echo 'Hello from dev.'" >> test.sh
chmod +x test.sh
```
3. Сделал несколько коммитов и пушей в ветку dev:
```
git add test.sh
git commit -m "Add test.sh with greetings"
echo "echo 'Second line from dev.'" >> test.sh
git add test.sh
git commit -m "Update test.sh - add second line"
git push origin dev
```
4. Переключился на основную ветку:
```
git checkout master
```
5. Добавил файл main.sh в основной ветке с произвольным содержимым, сделал коммит и пуш:
```
echo "#!/bin/bash" > main.sh
echo "echo 'Hello from main branch.'" >> main.sh
chmod +x main.sh
git add main.sh
git commit -m "Add main.sh with greetings from main"
git push origin master
```
6. Сделал мердж ветки dev в основную:
```
git merge dev -m "Merge dev into master"
```
7. Сделал пуш в основной ветке:
```
git push origin master
```
8. Ветку dev не удалял, она осталась для дальнейшей работы.

Ссылка на граф коммитов:
[Граф коммитов](https://github.com/htment/HOMEWORK_git_test/network)




### Задание 4

Задание 4*(дополнительное)
1. Создал ветку conflict и переключился на неё:
```
git checkout -b conflict
```
2. Внес изменения в файл test.sh:
```
echo "echo 'Conflict line from conflict branch.'" >> test.sh
git add test.sh
git commit -m "Update test.sh in conflict branch"
git push origin conflict
```
3. Переключился на основную ветку:
```
git checkout master
```
4. Изменил ту же самую строчку в файле test.sh:
```
echo "echo 'Conflict line from master branch.'" >> test.sh
git add test.sh
git commit -m "Update test.sh in master branch"
git push origin master
```
5. Сделал мердж ветки conflict в основную и решил конфликт:
```
git merge conflict
```
В случае конфликта откроется редактор для разрешения конфликта. Сохраните изменения, чтобы оставить код из ветки conflict.

6. Сделал пуш:
```
git push origin master
```
Ссылка на граф коммитов:
[Граф коммитов](https://github.com/htment/HOMEWORK_git_test/network)



