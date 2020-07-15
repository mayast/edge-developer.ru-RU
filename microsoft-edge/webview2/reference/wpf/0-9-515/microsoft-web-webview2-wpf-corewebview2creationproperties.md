---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 72c85df7d2d58d74cf27e04eb7128fdfa14ca2d9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880257"
---
# Класс Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Пространство имен: Microsoft. Web. WebView2. WPF \
Сборка: Microsoft.Web.WebView2.Wpf.dll

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

Этот класс является набором наиболее распространенных параметров, используемых для создания CoreWebView2Environment.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[BrowserExecutableFolder](#browserexecutablefolder) | Возвращает или задает значение, передаваемое в качестве параметра browserExecutableFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.
[Язык](#language) | Возвращает или задает значение, используемое для свойства Language параметра CoreWebView2EnvironmentOptions, передаваемого методу CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.
[UserDataFolder](#userdatafolder) | Возвращает или задает значение, передаваемое в качестве параметра userDataFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.
[CoreWebView2CreationProperties](#corewebview2creationproperties) | Создает новый экземпляр класса CoreWebView2CreationProperties с данными по умолчанию для всех свойств.

Для ее основного назначения необходимо установить [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) для настройки среды, используемой [WebView2](microsoft-web-webview2-wpf-webview2.md) во время неявной инициализации. Кроме того, это удобная служебная программа интеграции WPF, которая позволяет часто используемым параметрам среды быть свойствами зависимостей и создавать и использовать их в разметке.

Этот класс не предназначен для хранения всех возможных параметров настройки среды. Если вам требуется полный контроль над средой, используемой элементом управления WebView2, необходимо явным образом инициализировать элемент управления, создав собственную среду с помощью CoreWebView2Environment. CreateAsync и передавая ее в [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*перед* тем, как установить для свойства [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) значение "что угодно". Ознакомьтесь с документацией по классу [WebView2](microsoft-web-webview2-wpf-webview2.md) для обзора инициализации.

## Участников

#### BrowserExecutableFolder 

Возвращает или задает значение, передаваемое в качестве параметра browserExecutableFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.

> общедоступная строка [BrowserExecutableFolder](#browserexecutablefolder)

#### Язык 

Возвращает или задает значение, используемое для свойства Language параметра CoreWebView2EnvironmentOptions, передаваемого методу CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.

> [язык](#language) общедоступной строки

#### UserDataFolder 

Возвращает или задает значение, передаваемое в качестве параметра userDataFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.

> общедоступная строка [UserDataFolder](#userdatafolder)

#### CoreWebView2CreationProperties 

Создает новый экземпляр класса CoreWebView2CreationProperties с данными по умолчанию для всех свойств.

> общедоступная [CoreWebView2CreationProperties](#corewebview2creationproperties)()

