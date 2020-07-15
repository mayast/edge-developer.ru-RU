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
# <span data-ttu-id="47630-104">Класс Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="47630-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="47630-105">Пространство имен: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="47630-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="47630-106">Сборка: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="47630-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="47630-107">Этот класс является набором наиболее распространенных параметров, используемых для создания CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="47630-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="47630-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="47630-108">Summary</span></span>

 <span data-ttu-id="47630-109">Участников</span><span class="sxs-lookup"><span data-stu-id="47630-109">Members</span></span>                        | <span data-ttu-id="47630-110">Описания</span><span class="sxs-lookup"><span data-stu-id="47630-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47630-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="47630-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="47630-112">Возвращает или задает значение, передаваемое в качестве параметра browserExecutableFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="47630-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="47630-113">Язык</span><span class="sxs-lookup"><span data-stu-id="47630-113">Language</span></span>](#language) | <span data-ttu-id="47630-114">Возвращает или задает значение, используемое для свойства Language параметра CoreWebView2EnvironmentOptions, передаваемого методу CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="47630-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="47630-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="47630-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="47630-116">Возвращает или задает значение, передаваемое в качестве параметра userDataFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="47630-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="47630-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="47630-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="47630-118">Создает новый экземпляр класса CoreWebView2CreationProperties с данными по умолчанию для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="47630-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="47630-119">Для ее основного назначения необходимо установить [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) для настройки среды, используемой [WebView2](microsoft-web-webview2-wpf-webview2.md) во время неявной инициализации.</span><span class="sxs-lookup"><span data-stu-id="47630-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="47630-120">Кроме того, это удобная служебная программа интеграции WPF, которая позволяет часто используемым параметрам среды быть свойствами зависимостей и создавать и использовать их в разметке.</span><span class="sxs-lookup"><span data-stu-id="47630-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="47630-121">Этот класс не предназначен для хранения всех возможных параметров настройки среды.</span><span class="sxs-lookup"><span data-stu-id="47630-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="47630-122">Если вам требуется полный контроль над средой, используемой элементом управления WebView2, необходимо явным образом инициализировать элемент управления, создав собственную среду с помощью CoreWebView2Environment. CreateAsync и передавая ее в [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*перед* тем, как установить для свойства [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) значение "что угодно".</span><span class="sxs-lookup"><span data-stu-id="47630-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="47630-123">Ознакомьтесь с документацией по классу [WebView2](microsoft-web-webview2-wpf-webview2.md) для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="47630-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="47630-124">Участников</span><span class="sxs-lookup"><span data-stu-id="47630-124">Members</span></span>

#### <span data-ttu-id="47630-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="47630-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="47630-126">Возвращает или задает значение, передаваемое в качестве параметра browserExecutableFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="47630-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="47630-127">общедоступная строка [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="47630-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="47630-128">Язык</span><span class="sxs-lookup"><span data-stu-id="47630-128">Language</span></span> 

<span data-ttu-id="47630-129">Возвращает или задает значение, используемое для свойства Language параметра CoreWebView2EnvironmentOptions, передаваемого методу CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="47630-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="47630-130">[язык](#language) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="47630-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="47630-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="47630-131">UserDataFolder</span></span> 

<span data-ttu-id="47630-132">Возвращает или задает значение, передаваемое в качестве параметра userDataFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="47630-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="47630-133">общедоступная строка [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="47630-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="47630-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="47630-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="47630-135">Создает новый экземпляр класса CoreWebView2CreationProperties с данными по умолчанию для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="47630-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="47630-136">общедоступная [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span><span class="sxs-lookup"><span data-stu-id="47630-136">public  [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

