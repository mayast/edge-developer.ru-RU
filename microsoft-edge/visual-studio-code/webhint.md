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
# <span data-ttu-id="0a0fa-104">Расширение ссылки и кода</span><span class="sxs-lookup"><span data-stu-id="0a0fa-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="0a0fa-105">Используйте веб- [подсказку][WebhintMain], настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта.</span><span class="sxs-lookup"><span data-stu-id="0a0fa-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="0a0fa-106">Она проверяет ваш код на предмет рекомендаций и распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="0a0fa-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="0a0fa-107">Этот проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="0a0fa-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="0a0fa-108">Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.</span><span class="sxs-lookup"><span data-stu-id="0a0fa-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана: расширение кода и ссылки на него":::
   <span data-ttu-id="0a0fa-110">Снимок экрана: расширение кода и ссылки на него</span><span class="sxs-lookup"><span data-stu-id="0a0fa-110">Screenshot of webhint VS Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="0a0fa-111">Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="0a0fa-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="0a0fa-112">Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели " **проблемы** ".</span><span class="sxs-lookup"><span data-stu-id="0a0fa-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <span data-ttu-id="0a0fa-113">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="0a0fa-113">Configuration</span></span>  

<span data-ttu-id="0a0fa-114">Это расширение использует JSON-файл [конфигурации по умолчанию][GithubWebhintioIndexjson] , который активирует подсказки и синтаксические анализаторы для HTML, CSS, шаблонов системы \ (JSX/Целевая, угловая и т. д.), JavaScript/TypeScript и т. д.</span><span class="sxs-lookup"><span data-stu-id="0a0fa-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="0a0fa-115">Если вы хотите, чтобы дополнительные элементы управления подсказками и парсеры были активированы, создайте локальный `.hintrc` файл для настройки веб-подсказки.</span><span class="sxs-lookup"><span data-stu-id="0a0fa-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="0a0fa-116">Чтобы получить справку по выводу из конкретных подсказок, ознакомьтесь с [руководством пользователя по этой подсказке][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="0a0fa-116">For help with output from specific hints, see [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <span data-ttu-id="0a0fa-117">Связь с командой "Подсказка"</span><span class="sxs-lookup"><span data-stu-id="0a0fa-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="0a0fa-118">Отправьте отзыв, выполнив [архивацию проблем][GithubWebhintioIssuesNew] в [репозитории GitHub][GithubWebhintio]веб контрольных подсказок.</span><span class="sxs-lookup"><span data-stu-id="0a0fa-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="0a0fa-119">Чтобы присвоить это расширение, ознакомьтесь с руководством по соавтору для ссылки на ссылку [и расширение кода][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="0a0fa-119">To contribute to the extension, see [webhint VS Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <span data-ttu-id="0a0fa-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0a0fa-120">See also</span></span>  

*   [<span data-ttu-id="0a0fa-121">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="0a0fa-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="0a0fa-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0a0fa-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

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
