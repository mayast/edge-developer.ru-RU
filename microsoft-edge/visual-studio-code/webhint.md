---
description: Использование подсказки в коде Visual Studio
title: расширение ссылки и кода
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, код для VS, код Visual Studio, ссылка "веб-подсказка"
ms.openlocfilehash: ec218fab8cbfb8181a0416c8e0eadc0e00412529
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695861"
---
# Расширение ссылки и кода  

Используйте веб- [подсказку][WebhintMain], настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта.  Она проверяет ваш код на предмет рекомендаций и распространенных ошибок. Этот проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation][OpenjsFoundation].  Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана: расширение кода и ссылки на него":::
   Снимок экрана: расширение кода и ссылки на него  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS][VisualstudioMarketplaceWebhint].  Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели " **проблемы** ".  

## Конфигурация  

Это расширение использует JSON-файл [конфигурации по умолчанию][GithubWebhintioIndexjson] , который активирует подсказки и синтаксические анализаторы для HTML, CSS, шаблонов системы \ (JSX/Целевая, угловая и т. д.), JavaScript/TypeScript и т. д.  

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

Если вы хотите, чтобы дополнительные элементы управления подсказками и парсеры были активированы, создайте локальный `.hintrc` файл для настройки веб-подсказки.  Чтобы получить справку по выводу из конкретных подсказок, ознакомьтесь с [руководством пользователя по этой подсказке][WebhintDocsUserguideConfiguringSummary].  

## Связь с командой "Подсказка"  

Отправьте отзыв, выполнив [архивацию проблем][GithubWebhintioIssuesNew] в [репозитории GitHub][GithubWebhintio]веб контрольных подсказок.  

Чтобы присвоить это расширение, ознакомьтесь с руководством по соавтору для ссылки на ссылку [и расширение кода][GithubWebhintioExtensionVscodeContributing].  

## См. также  

*   [Специальные возможности][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint VS Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Специальные возможности | Документы Microsoft"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Код Visual Studio | Документы Microsoft"  

[GithubWebhintio]: https://github.com/webhintio/hint "Подсказка | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Всплывающая подсказка | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index. JSON-webhintio/подсказка | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Новые проблемы — webhintio/подсказка | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "Подсказка | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Настройка подсказки | Документация по подсказкам"  
[WebhintMain]:  https://webhint.io "Подсказка"  
