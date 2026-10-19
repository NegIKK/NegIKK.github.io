---
pin: false
date: 2026-01-19 17:06
tags:
  - blender/python
Parent:
  - "[[Blender. Python]]"
---

Копируем папку с настройками блендера и называем другим именем. У меня это 5.0 dev

![[Заметки/files/Pasted image 20260119175452.png]]

Путь к настройкам:

`%AppData%\Blender Foundation\Blender\`

Создаем ярлык и в поле "Объект" Перед путем к exe файлу вписываем следующее:

```python
C:\Windows\System32\cmd.exe /C "set BLENDER_USER_RESOURCES={PATH_TO_PREFERENCES}&& start"
```

Вместо `{PATH_TO_PREFERENCES}` вписываем свой путь до настроек блендера. Важно не делать лишних пробелов после и до пути, иначе будет ошибка.

Как должно выглядеть в итоге. Мой пример:

```python
C:\Windows\System32\cmd.exe /C "set BLENDER_USER_RESOURCES=C:\Users\KeniGG\AppData\Roaming\Blender Foundation\Blender\5.0 dev&& start "D:\01_Programs\01_Work\blender-5.0.1-windows-x64\blender.exe
```

Чтобы VS Code запускала нужную нам среду, нужно в ее настройках добавить следующее:

```json
    "terminal.integrated.env.windows": {
        "BLENDER_USER_RESOURCES": "{PATH_TO_PREFERENCES}"
    },
```

Вместо `{PATH_TO_PREFERENCES}`, аналогично, вписываем свой путь до настроек блендера.

Чтобы открыть настройки VS Code -> `Ctrl+Shift+P` - вписать `Open User Settings`

![[Заметки/files/Pasted image 20260119180309.png]]

Так выглядят настройки у меня:

```json
{
    "blender.executables": [
        {
            "name": "5.0",
            "path": "D:\\01_Programs\\01_Work\\blender-5.0.1-windows-x64\\blender.exe",
            "isDefault": true
        },
    ],

    "terminal.integrated.env.windows": {
        "BLENDER_USER_RESOURCES": "C:\\Users\\KeniGG\\AppData\\Roaming\\Blender Foundation\\Blender\\5.0 dev"
    },
    

	//Другие настройки, не относятся к блендеру
    "editor.fontSize": 17,
    "editor.tabCompletion": "on",
    "editor.suggest.snippetsPreventQuickSuggestions": false,
    "editor.suggestSelection": "first",
    "csharp.suppressDotnetRestoreNotification": true,
    "dotnet.server.useOmnisharp": false,
    "workbench.colorTheme": "Catppuccin Macchiato",
    "workbench.iconTheme": "Catppuccin Frappé Icons",
    "security.workspace.trust.untrustedFiles": "open",
    "window.menuBarVisibility": "compact",
    "vscode-kanata.localKeysVariant": "deflocalkeys-winiov2",

}
```
