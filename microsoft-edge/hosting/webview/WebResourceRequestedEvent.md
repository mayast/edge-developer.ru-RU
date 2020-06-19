---
description: Событие, которое возникает при выполнении HTTP-запроса.
title: Объект WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751984"
---
# Объект WebResourceRequestedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Событие, которое возникает при выполнении HTTP-запроса.  

## Свойства  

### аргументы  

Сведения о запросе ресурсов.  Это элемент [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).  

Это свойство доступно только для чтения.  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### Значение свойства  

Type (тип): **ANY**  
