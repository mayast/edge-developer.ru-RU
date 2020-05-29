---
description: Использование подсказки в коде Visual Studio
title: расширение ссылки и кода
author: hxlnt
ms.author: raweil
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, код для VS, код Visual Studio, ссылка "веб-подсказка"
ms.openlocfilehash: d3102bf4d8d4a8bba9225d8d3f68432197f775ac
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572790"
---
# расширение ссылки и кода

Используйте веб- [подсказку](https://webhint.io), настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта. Она проверяет ваш код на предмет рекомендаций и распространенных ошибок. Этот проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation](https://openjsf.org/). Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.

![Снимок экрана: расширение кода и ссылки на него](./media/webhint-extension.png)

Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели "проблемы".

## Конфигурация

Это расширение использует JSON-файл [конфигурации по умолчанию](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) , который активирует подсказки и парсеры для HTML, CSS, шаблонов систем (JSX/целевой, радиальной и т. д.), JavaScript, TypeScript и т. д.

```json
{
    "connector": "local",
    "extends": [
        "accessibility",
        "progressive-web-apps"
    ],
    "formatters": [
        "html",
        "summary"
    ],
    "hints": [
        "apple-touch-icons",
        "button-type",
        "compat-api/css",
        "compat-api/html",
        "create-element-svg",
        "css-prefix-order",
        "disown-opener",
        "highest-available-document-mode",
        "manifest-exists",
        "meta-charset-utf-8",
        "meta-viewport",
        "no-bom",
        "no-protocol-relative-urls",
        "scoped-svg-styles",
        "sri",
        "typescript-config/consistent-casing",
        "typescript-config/import-helpers",
        "typescript-config/is-valid",
        "typescript-config/no-comments",
        "typescript-config/strict",
        "typescript-config/target"
    ],
    "hintsTimeout": 10000,
    "parsers": [
        "babel-config",
        "css",
        "html",
        "javascript",
        "jsx",
        "less",
        "sass",
        "typescript",
        "typescript-config",
        "webpack-config"
    ]
}
```

Если вы хотите, чтобы дополнительные элементы управления подсказками и парсеры были активированы, создайте локальный `.hintrc` файл для настройки веб-подсказки. Инструкции по выводу результатов из конкретных подсказок можно найти в [руководстве пользователя по этой подсказке](https://webhint.io/docs/user-guide/configuring-webhint/summary/).

## Отзыв

Отправьте нам отзыв, выполнив [архивацию по вопросу](https://github.com/webhintio/hint/issues/new) в [репозитории GitHub](https://github.com/webhintio/hint). 

Чтобы присвоить это расширение, ознакомьтесь со статьей [руководство по расширению ссылки и расширений кода](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).

## См. также
  - [Специальные возможности](/microsoft-edge/accessibility)
  - [Visual Studio Code](/microsoft-edge/visual-studio-code/)
