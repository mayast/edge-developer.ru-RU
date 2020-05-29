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
# Перенос расширения с Chrome на Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Перенос расширения с Chrome на Microsoft Edge осуществляется очень просто с помощью [набора средств расширения Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb). Это средство разработчика преобразует распакованное расширение Chrome в неупакованное расширение Microsoft Edge с помощью API моста и использование все ошибки в `manifest.json` файле.


### Мосты API
Для обеспечения возможности эффективного переноса API Chrome на поддерживаемые API Microsoft EDGE в папке расширения добавляются два сценария. Эти сценарии API моста (если это необходимо), поэтому вам не придется беспокоиться о том, как изменить какой-либо код, специфичный для Chrome, в фоновом сценарии или скриптах содержимого.

После преобразования вы увидите, что они включены в файл манифеста расширения с помощью `"-ms-preload"` ключа:

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## Использование набора средств расширения Microsoft Edge

Ниже приведены инструкции по преобразованию расширения Chrome для работы в Microsoft EDGE в ознакомительной версии Windows 10 годовщина.

1. Установите [набор средств расширения Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).
2. Сделайте копию папки расширения Chrome для безопасного хранения. В процессе преобразования код будет перезаписан. 
3. Запустите набор средств расширения Microsoft EDGE и загрузите копию расширения.  
 ![Кнопка "загрузить расширение"](./../media/save-folder.png)
4. Исправьте все ошибки, обнаруженные в текстовом редакторе инструмента. Нажмите кнопку "повторно проверить", чтобы проверить наличие ошибок после внесения исправлений.  
 ![расширение — набор средств поиска ошибок](./../media/extension-toolkit.png)
5. Нажмите кнопку "сохранить файлы".

Теперь вы можете выйти из набора инструментов и загрузить расширение в Microsoft Edge! 

Поиск известных проблем с платформой осуществляется с помощью средства [отслеживания проблем EdgeHTML](http://issues.microsoftedge.com). Если вы считаете, что нашли что-нибудь новое, [откройте вопрос](https://developer.microsoft.com/microsoft-edge/platform/issues/new/).
