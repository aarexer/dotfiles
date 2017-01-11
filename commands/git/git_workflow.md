## Git workflow
### Начало работы
При начале работы над новым куском функционала:
* `git checkout –b feature/<feature_name> develop`

### Работа
* Все изменения по мере разработки коммитим в новую ветку `feature/<feature_name>`

### Merge
Когда ветка готова к слиянию с `develop`, выполняем несколько команд:

* `git checkout develop`
* `git pull origin develop`
* `git checkout feature/<feature_name>`
* `git rebase develop`

> На этом шаге ветка feature/<feature_name> переводится в состояние, в котором она ответвилась от ветки develop, накатываются все изменения, сделанные в ветке develop за время существования ветки > feature/<feature_name> и потом все коммиты, сделанные в feature-ветке последовательно накатываются на уже новое состояние (тем самым из коммитов a -> b -> c получаются коммиты a’ -> b’ -> c’). Если в > процессе rebase возникают конфликты – их необходимо разрешить и продолжить выполнение rebase’а командой git rebase continue

* `git checkout develop`
* `git merge –no-ff feature/<feature_name>`
* `git branch –d (или –D если ветка есть и в центральном репозитории) feature/<feature_name>`
