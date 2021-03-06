# Боевой Информационный Сервер (БИЦ)
## на Ruby 2.4.0 и Rails 5

Требует:

* Ruby 2.4.0
* Rails 5
* PostgreSQL версии 9 и выше

Пользователя для базы данных надо создать самостоятельно, см. команду `createuser` в PostgreSQL.

В `config/database.yml.sample` лежит сэмпл настройки к базе данных. Надо его скопировать в `config/database.yml` и написать в имя/пароль/имя базы то что у вас

`db/crebas.pgsql` создаёт таблицы в базе. Запускать надо на голой существующей базе.

Скрипт `db/recreate_db.sh` создаёт новую базу (имя базы параметром скрипта, пароль задан как `имя_gfhjkm`), и запускает `crebas.pgsql` внутри. Подходит для in-house серверочка.

Штатно обычно это всё работало на Linux Debian последних версий, Ruby/Rails ставятся с помощью RVM (https://rvm.io), под сервер Apache 2 собирается Passenger (https://www.phusionpassenger.com/library/)

Под Windows не пытался запустить никогда.

Пароль администратора на старте 'admin', меняйте.

## Образ системы с работающим сервером БИЦ

Файл OVA для импорта в систему виртуализации VirtualBox (https://www.virtualbox.org) выложен на Яндекс.Диск: https://yadi.sk/d/SABV-nOC3KRF6z

## Импорт персонажей из JoinRpg

Теперь БИЦ умеет импортировать персонажей из JoinRpg (http://joinrpg.ru). Для этого администратор должен зайти на страницу _Импорт персонажей из JoinRpg_, ввести там ссылку на персонажей, выглядящую как `http://joinrpg.ru/ID/characters/activetoken?Token=HERECOMESTHETOKEN` и нажать кнопку _Импортировать_.
