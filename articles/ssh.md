## What is it?
ssh - это протокол безопасного доступа к удаленным системам.

С этого помощью протокола мы можем:
* login - осуществлять доступ к системам
* Обмениваться файлами через scp
* Монтировать удаленные ФС
* Туннелировать сетевые порты

Клиент-серверный протокол. 
Должна быть серверная часть и клиентская.

Клиенты:

* Mac OS: temrinal, iterm2
* Win: Putty, Xshell, CyGwin, Git-bash
* Linux: terminal

При каждом коннекте - fingerprint, т.е генерация ключа, который уникально идентифицирует данный сервер.

А далее уже вводим логин/пароль.

Но это не самая лучшая идея, так как лучше польщоваться ключами:

Есть два ключа:
* Public key - хранится на сервере в открытом виде(.pub)
* Private key - хранится зашифрованным у пользователя(.ppk)

Публичный ключ можно представить как замок, доступный всем. Без ключа(приватного ключа) этот замок не представляет ценности.
Информация шифруется публичным ключом, но без приватного ключа мы не сможем расшифровать эту информацию. 

Причем, даже тот, кто шифрует информацию ее не расшифрует без приватного ключа.

Также и в обратную сторону.

Преимущества:
* Сложно взломать
* Хэш пароля не хранится на серврере
* Публичный ключ проще передавать
* Пользователь может иметь несколько ключей

Ключи хранятся в `.ssh`. Права на папку лучше ставить только для пользователя, т.е `chmod 700 .ssh`
Далее в `authorized_keys` копируем наш ключ(публичный).

После чего - на файл `authorized_keys` выставляем права `chmod 600 authorized_keys`

Для генерации:
* В Unix используем утилиту ssh-keygen
* В Windows с офф сайта Putty скачиваем key generator.

После генерации сохраняем ключи.
Можно также для дополнительной защиты задать фразу-пароль.

