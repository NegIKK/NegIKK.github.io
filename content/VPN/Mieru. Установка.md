---
publish: true
created: 2026-08-27 19:42
modified: 2026-09-02T10:47:16.121Z
tags:
  - впн
---

```cardlink
url: https://github.com/enfein/mieru/blob/main/docs/server-install.md
title: "mieru/docs/server-install.md at main · enfein/mieru"
description: "mieru is a socks5 / HTTP / HTTPS proxy to bypass censorship. 見える是一款 socks5 / HTTP / HTTPS 网络代理翻墙工具。 - enfein/mieru"
host: github.com
favicon: https://github.githubassets.com/favicons/favicon.svg
image: https://opengraph.githubassets.com/e3ecc3721ebf2f797ee8d7adc872624093bba9249f66f40fccd834d6a53c525a/enfein/mieru
```

# Настройка сервера

Вставляем команду и соглашаемся с кстановкой "Mita"
![[Заметки/files/Pasted image 20260827194433.png]]

Подтверждаем, что хотим сконфигурировать сервер
![[Заметки/files/Pasted image 20260827194520.png]]

Жмем enter. Все равно всегда сидим из под рута
![[Заметки/files/Pasted image 20260827194745.png]]

Выбираем что хотим, мне нравится ставить имя и пароль самостоятельно
![[Заметки/files/Pasted image 20260827194758.png]]

Оставляем TCP по умолчанию
![[Заметки/files/Pasted image 20260827195037.png]]

Я выставляю диапазон портов. Не забудь их открыть в фаерволе
![[Заметки/files/Pasted image 20260827195053.png]]

Применяем наши настройки
![[Заметки/files/Pasted image 20260827195109.png]]

Видим, что сервер запустился. После всех настроек можно проверить работоспособность через `systemctl status mita`
![[Заметки/files/Pasted image 20260827195919.png]]

# Настройка клиента

Настраиваем файл, который получит клиент, чтобы зайти на сервер

Соглашаемся с генерацией конфигурации для клиента
![[Заметки/files/Pasted image 20260827195944.png]]

Далее все прокликиваем на стандартных настройках
![[Заметки/files/Pasted image 20260827200008.png]]

Пример конфигурации в формате json
![[Заметки/files/Pasted image 20260827200208.png]]

## Коротко о подключении

Фактически сервер выдает инфу о том как подключится к нашему серверу, но на себе я не смог проверить где эти файлы бы работали. У яблочников работает только через добавление сервера через файл. Но только в формате yaml

То же самое но в формате yaml

```
proxies:
  - name: server1
    type: mieru
    server: 1.11.111.111
    port-range: 9000-9010
    transport: TCP
    udp: false
    username: 123
    password: 456
    multiplexing: MULTIPLEXING_HIGH
```

Он нам не генерит файл сам. Так что тупо создаем текстовый документ, вписываем свои значения в шаблон выше, меняем расширение файла на yaml и кидаем яблочному.

На ПК и Андроиде просто нужно знать логин, пароль, IP адрес, порты. Все что в шаблоне выше. Только вводить надо в графы программ
