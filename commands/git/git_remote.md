## Remote repositories
#### Посмотреть все удаленные репозитории
`git remote -v`

Выведет список удаленных репозиториев.

#### Добавление
`git remote add name_of_repo https://github.com/aarexer/myrepo.git`
Здесь name_of_repo - это имя-сокращение.

Пример:
`git remote add boss https://github.com/aarexer/myrepo.git`

Добавили репозиторий и привязали его к иени boss.

Теперь можем работать с удаленным репозиторием.

#### Получение изменений
`git fetch [имя удал. сервера]`

Данная команда связывается с указанным удалённым проектом и забирает все те данные проекта, которых у вас ещё нет, но не мерджит и не применяет их.

Для применения надо отдельно сделать merge:
`git merge name/branch`
Например:
`git merge boss/master`

Выполнение `git pull` делает fetch и merge.

#### Переименование и удаление
`git remote rename old_name new_name`
 Изменит имя-ссылку на удаленный репозиторий.

 `git remote rm name` - удалит ссылку на удаленный репозиторий.
