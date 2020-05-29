---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Сведения о том, как перенести расширение Chrome на Microsoft Edge с помощью набора средств расширения Microsoft Edge.
title: Перенос расширений хрома
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: 38bf1324c2e7e6f7754912177ce0e53d6c15a276
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571505"
---
# <span data-ttu-id="6dda4-104">Перенос расширения с Chrome на Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6dda4-104">Porting an extension from Chrome to Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="6dda4-105">Перенос расширения с Chrome на Microsoft Edge осуществляется очень просто с помощью [набора средств расширения Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="6dda4-105">Porting an extension from Chrome to Microsoft Edge is made easy with the help of the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span> <span data-ttu-id="6dda4-106">Это средство разработчика преобразует распакованное расширение Chrome в неупакованное расширение Microsoft Edge с помощью API моста и использование все ошибки в `manifest.json` файле.</span><span class="sxs-lookup"><span data-stu-id="6dda4-106">This developer tool converts an unpacked Chrome extension to an unpacked Microsoft Edge extension by bridging APIs and surfacing any errors in your `manifest.json` file.</span></span>


### <span data-ttu-id="6dda4-107">Мосты API</span><span class="sxs-lookup"><span data-stu-id="6dda4-107">API bridges</span></span>
<span data-ttu-id="6dda4-108">Для обеспечения возможности эффективного переноса API Chrome на поддерживаемые API Microsoft EDGE в папке расширения добавляются два сценария.</span><span class="sxs-lookup"><span data-stu-id="6dda4-108">In order to allow for seamless porting of Chrome APIs to supported Microsoft Edge APIs, two scripts are added to your extension's folder.</span></span> <span data-ttu-id="6dda4-109">Эти сценарии API моста (если это необходимо), поэтому вам не придется беспокоиться о том, как изменить какой-либо код, специфичный для Chrome, в фоновом сценарии или скриптах содержимого.</span><span class="sxs-lookup"><span data-stu-id="6dda4-109">These scripts bridge APIs (polyfiling where necessary), meaning you won't have to worry about changing any Chrome specific code in your background script or content scripts.</span></span>

<span data-ttu-id="6dda4-110">После преобразования вы увидите, что они включены в файл манифеста расширения с помощью `"-ms-preload"` ключа:</span><span class="sxs-lookup"><span data-stu-id="6dda4-110">After conversion, you will see them included in the manifest file of your extension with the `"-ms-preload"` key:</span></span>

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## <span data-ttu-id="6dda4-111">Использование набора средств расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6dda4-111">Using the Microsoft Edge Extension Toolkit</span></span>

<span data-ttu-id="6dda4-112">Ниже приведены инструкции по преобразованию расширения Chrome для работы в Microsoft EDGE в ознакомительной версии Windows 10 годовщина.</span><span class="sxs-lookup"><span data-stu-id="6dda4-112">The following instructions detail how to convert your Chrome extension to run on Microsoft Edge in the Windows 10 Anniversary Update edition:</span></span>

1. <span data-ttu-id="6dda4-113">Установите [набор средств расширения Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="6dda4-113">Install the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span>
2. <span data-ttu-id="6dda4-114">Сделайте копию папки расширения Chrome для безопасного хранения.</span><span class="sxs-lookup"><span data-stu-id="6dda4-114">Make a copy of your Chrome extension's folder for safe keeping.</span></span> <span data-ttu-id="6dda4-115">В процессе преобразования код будет перезаписан.</span><span class="sxs-lookup"><span data-stu-id="6dda4-115">The conversion process will overwrite the code.</span></span> 
3. <span data-ttu-id="6dda4-116">Запустите набор средств расширения Microsoft EDGE и загрузите копию расширения.</span><span class="sxs-lookup"><span data-stu-id="6dda4-116">Run the Microsoft Edge Extension Toolkit and load the copy of your extension.</span></span>  
 ![Кнопка "загрузить расширение"](./../media/save-folder.png)
4. <span data-ttu-id="6dda4-118">Исправьте все ошибки, обнаруженные в текстовом редакторе инструмента.</span><span class="sxs-lookup"><span data-stu-id="6dda4-118">Correct all the errors that are reported within the tool's text editor.</span></span> <span data-ttu-id="6dda4-119">Нажмите кнопку "повторно проверить", чтобы проверить наличие ошибок после внесения исправлений.</span><span class="sxs-lookup"><span data-stu-id="6dda4-119">Select "Re-validate" to check for errors after making corrections.</span></span>  
 ![расширение — набор средств поиска ошибок](./../media/extension-toolkit.png)
5. <span data-ttu-id="6dda4-121">Нажмите кнопку "сохранить файлы".</span><span class="sxs-lookup"><span data-stu-id="6dda4-121">Select "Save files".</span></span>

<span data-ttu-id="6dda4-122">Теперь вы можете выйти из набора инструментов и загрузить расширение в Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="6dda4-122">You can now exit out of the toolkit and load your extension in Microsoft Edge!</span></span> 

<span data-ttu-id="6dda4-123">Поиск известных проблем с платформой осуществляется с помощью средства [отслеживания проблем EdgeHTML](http://issues.microsoftedge.com).</span><span class="sxs-lookup"><span data-stu-id="6dda4-123">You can search for known platform issues with the [EdgeHTML issue tracker](http://issues.microsoftedge.com).</span></span> <span data-ttu-id="6dda4-124">Если вы считаете, что нашли что-нибудь новое, [откройте вопрос](https://developer.microsoft.com/microsoft-edge/platform/issues/new/).</span><span class="sxs-lookup"><span data-stu-id="6dda4-124">If you think you've found something new, [open an issue](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span></span>
