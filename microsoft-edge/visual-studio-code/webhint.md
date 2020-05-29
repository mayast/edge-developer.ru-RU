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
# <span data-ttu-id="e4d27-104">расширение ссылки и кода</span><span class="sxs-lookup"><span data-stu-id="e4d27-104">webhint VS Code extension</span></span>

<span data-ttu-id="e4d27-105">Используйте веб- [подсказку](https://webhint.io), настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта.</span><span class="sxs-lookup"><span data-stu-id="e4d27-105">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="e4d27-106">Она проверяет ваш код на предмет рекомендаций и распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="e4d27-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="e4d27-107">Этот проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="e4d27-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="e4d27-108">Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.</span><span class="sxs-lookup"><span data-stu-id="e4d27-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Снимок экрана: расширение кода и ссылки на него](./media/webhint-extension.png)

<span data-ttu-id="e4d27-110">Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="e4d27-110">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="e4d27-111">Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели "проблемы".</span><span class="sxs-lookup"><span data-stu-id="e4d27-111">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

## <span data-ttu-id="e4d27-112">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="e4d27-112">Configuration</span></span>

<span data-ttu-id="e4d27-113">Это расширение использует JSON-файл [конфигурации по умолчанию](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) , который активирует подсказки и парсеры для HTML, CSS, шаблонов систем (JSX/целевой, радиальной и т. д.), JavaScript, TypeScript и т. д.</span><span class="sxs-lookup"><span data-stu-id="e4d27-113">This extension uses a [default configuration](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) json file that activates hints and parsers for HTML, CSS, templating systems (JSX/TSX, Angular, and so on), JavaScript/TypeScript, and more.</span></span>

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

<span data-ttu-id="e4d27-114">Если вы хотите, чтобы дополнительные элементы управления подсказками и парсеры были активированы, создайте локальный `.hintrc` файл для настройки веб-подсказки.</span><span class="sxs-lookup"><span data-stu-id="e4d27-114">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span> <span data-ttu-id="e4d27-115">Инструкции по выводу результатов из конкретных подсказок можно найти в [руководстве пользователя по этой подсказке](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span><span class="sxs-lookup"><span data-stu-id="e4d27-115">For help with output from specific hints, see the [webhint user guide](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span></span>

## <span data-ttu-id="e4d27-116">Отзыв</span><span class="sxs-lookup"><span data-stu-id="e4d27-116">Feedback</span></span>

<span data-ttu-id="e4d27-117">Отправьте нам отзыв, выполнив [архивацию по вопросу](https://github.com/webhintio/hint/issues/new) в [репозитории GitHub](https://github.com/webhintio/hint).</span><span class="sxs-lookup"><span data-stu-id="e4d27-117">Send us your feedback by [filing an issue](https://github.com/webhintio/hint/issues/new) on the [webhint GitHub repo](https://github.com/webhintio/hint).</span></span> 

<span data-ttu-id="e4d27-118">Чтобы присвоить это расширение, ознакомьтесь со статьей [руководство по расширению ссылки и расширений кода](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="e4d27-118">To contribute to the extension, please read the [webhint VS Code extension contribution guide](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span></span>

## <span data-ttu-id="e4d27-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e4d27-119">See also</span></span>
  - [<span data-ttu-id="e4d27-120">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="e4d27-120">Accessibility</span></span>](/microsoft-edge/accessibility)
  - [<span data-ttu-id="e4d27-121">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e4d27-121">Visual Studio Code</span></span>](/microsoft-edge/visual-studio-code/)
