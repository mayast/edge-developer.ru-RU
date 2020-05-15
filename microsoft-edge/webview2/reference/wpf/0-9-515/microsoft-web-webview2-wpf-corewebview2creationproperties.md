---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d2c3b3ee179dec217418241031142549d170e440
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654611"
---
# Класс Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Пространство имен: Microsoft. Web. WebView2. WPF \
Сборка: Microsoft. Web. WebView2. WPF. dll

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

