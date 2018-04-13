SOCKS proxy for Telegram in docker
==================================

Основано на https://hub.docker.com/r/vimagick/dante/

Как использовать:

* Отредактировать `DANTE_USERNANE` и `DANTE_PASSWORD` в `Dockerfile`
* По желанию отредактировать порт в `docker-compose.yml` (в `1080:1080` первый порт — это порт, под
  которым прокси будет выставлен на хост-машине)
* `docker-compose build`
* `docker-compose up -d`

Как сформировать ссылку для telegram:
`tg://socks?server=<host>&port=<port>&user=<username>&pass=<password>`

Особенности:

* Включена авторизация, пароль и логин задаются в `Dockerfile`.
* В `sockd.conf` доступ разрешён только к сетям Телеграма.



