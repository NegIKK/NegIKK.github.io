---
publish: true
created: 2026-08-27 20:25
modified: 2026-08-27T20:49:50.625Z
tags:
  - впн
---

# Настройка на ПК

```embed
title: "GitHub - qr243vbi/nekobox: NyameBox, The Original NekoBox Rebranded, the cross-platform Qt proxy utility, empowered by sing-box and thrift"
image: "https://opengraph.githubassets.com/155a6d7860cfb0149817064f174a96feea407dc4c5ba685f502f104b72dd9daf/qr243vbi/nekobox"
description: "NyameBox, The Original NekoBox Rebranded, the cross-platform Qt proxy utility, empowered by sing-box and thrift - qr243vbi/nekobox"
url: "https://github.com/qr243vbi/NekoBox"
favicon: ""
aspectRatio: "50"
```

Качаем в releases, справа, последнюю версию. В большинстве случаев нужная нам версия - windows64. Устанавливаем или распаковываем папку из архива. Запускаем

## Подключение

Нажимаем Профили - Новый профиль
![[Заметки/files/Pasted image 20260827203749.png]]

Вбиваем параметры, которые нам должен дать владелец сервера
![[Заметки/files/Pasted image 20260827203924.png]]
Подробнее про параметры:

- Мультиплескирование - то, насколько сильно будет делиться трафик. Насколько я понимаю чем оно больше, тем сложнее отследить и тем сильнее дробятся данные. Но тем больше нагрузка. В рамках современного ПК думаю мало важно
- Если дали диапазон портов, то он указывается через дефис 9000-9010. Важно, чтоб графа порт все равно была заполнена. например первым из списка 9000

## Настройка портов для подключения других программ

Жмем Настройки - Основные настройки
![[Заметки/files/Pasted image 20260827203949.png]]

Ставим прослушиваемый порт. Любой, которым привыкли пользоваться. Ставим тип прокси mixed
![[Заметки/files/Pasted image 20260827203955.png]]

# Настройка на Android

```embed
title: "GitHub - ExclaveNetwork/Exclave: Proxy client"
image: "https://opengraph.githubassets.com/f9763e03d511f43bca596ca9982fae63b33134e7643e2aeee7a2177027b02b89/ExclaveNetwork/Exclave"
description: "Proxy client. Contribute to ExclaveNetwork/Exclave development by creating an account on GitHub."
url: "https://github.com/ExclaveNetwork/Exclave"
favicon: ""
aspectRatio: "50"
```

Устанавливаем Exclave. Качается по аналогии с инструкцией для ПК

## Подключение

Жмем плюсик - Ручные настройки - Mieru. Вбиваем параметры отправленные вам владельцем сервера. Все аналогично параметрам в версии для ПК. Если каких-то параметров вам не отравили, значит оставляем их по умолчанию.

![[Заметки/files/Pasted image 20260827204921.png|324]]![[Заметки/files/Pasted image 20260827204946.png|345]]

Не забываем настроить раздельное проксирование для приложений. Это ОЧЕНЬ ВАЖНО!

![[Заметки/files/Pasted image 20260827205352.png|334]]![[Заметки/files/Pasted image 20260827205407.png|334]]
