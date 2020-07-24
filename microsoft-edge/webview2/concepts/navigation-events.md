---
description: Навигация
title: Навигация
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895580"
---
# События навигации  

Нормальная последовательность событий навигации:,,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` и затем `NavigationCompleted` .  Следующие события описывают состояние WebView2 во время каждой навигации.  

| Sequence | Имя события | Сведения |  
|:--- |:--- |:--- |  
| 1,1 | `NavigationStarting`  |  WebView2 запускает навигацию и навигацию, что приводит к выполнению сетевого запроса.  Ведущее приложение может запретить запрос во время события.  |  
| 2 | `SourceChanged`  |  Источник изменений WebView2 меняется на новый URL-адрес.  Это событие может быть вызвано навигацией, которая не является причиной сетевого запроса, например Навигация по фрагменту.  |  
| Трехконтактный | `HistoryChanged`  |  История обновлений WebView2 в результате навигации.  |  
| четырехпроцессорном | `ContentLoading`  |  WebView загружает содержимое для новой страницы.  |  
| 5 | `NavigationCompleted`  |  WebView2 завершает загрузку содержимого на новой странице.  |  

Отслеживайте `navigations` каждый новый документ с помощью идентификатора навигации \ ( `NavigationId` \).  `NavigationId`WebView меняется каждый раз при успешном переходе на новый документ.

:::image type="complex" source="../media/navigation-graph.png" alt-text="События навигации Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   События навигации Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> Предыдущий рисунок представляет события навигации с тем же `NavigationId` свойством для соответствующего события arg.  

 `Navigations` события с разными экземплярами `NavigationId` события могут перекрываться.  Например, при запуске навигации необходимо дождаться связанного `NavigationStarting` события.  Если затем вы запустите другую навигацию, вы увидите `NavigationStarting` событие для первого перехода, за которым следует событие `NavigationStarting` для первой навигации, затем событие, `NavigationCompleted` а затем все остальные события навигации для второй навигации.  
 
 В случае ошибок может возникнуть или не быть `ContentLoading` событием в зависимости от того, продолжает ли переход страница ошибки.  
 
 В случае переадресации HTTP `NavigationStarting` в строке есть несколько событий, в которых для последующего события `IsRedirect` задано свойство, но оно остается прежним `NavigationId` .  
 
 Тот же документ `navigations` , например переход к фрагменту, не приводит к `NavigationStarting` событию, и его нельзя увеличить `NavigationId` .  

Для контроля и отмены `navigations` внутри подкадров в WebView используйте `FrameNavigationStarting` события and, `FrameNavigationCompleted` которые действуют так же, как эквивалентные события, не связанные с кадрами.  

<!-- links -->  
