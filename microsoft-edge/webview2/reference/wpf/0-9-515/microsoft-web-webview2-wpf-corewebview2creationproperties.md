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
# <span data-ttu-id="76939-104">Класс Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="76939-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="76939-105">Пространство имен: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="76939-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="76939-106">Сборка: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="76939-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="76939-107">Этот класс является набором наиболее распространенных параметров, используемых для создания CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="76939-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="76939-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="76939-108">Summary</span></span>

 <span data-ttu-id="76939-109">Участников</span><span class="sxs-lookup"><span data-stu-id="76939-109">Members</span></span>                        | <span data-ttu-id="76939-110">Описания</span><span class="sxs-lookup"><span data-stu-id="76939-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="76939-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="76939-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="76939-112">Возвращает или задает значение, передаваемое в качестве параметра browserExecutableFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="76939-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="76939-113">Язык</span><span class="sxs-lookup"><span data-stu-id="76939-113">Language</span></span>](#language) | <span data-ttu-id="76939-114">Возвращает или задает значение, используемое для свойства Language параметра CoreWebView2EnvironmentOptions, передаваемого методу CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="76939-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="76939-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="76939-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="76939-116">Возвращает или задает значение, передаваемое в качестве параметра userDataFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="76939-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="76939-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="76939-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="76939-118">Создает новый экземпляр класса CoreWebView2CreationProperties с данными по умолчанию для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="76939-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="76939-119">Для ее основного назначения необходимо установить [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) для настройки среды, используемой [WebView2](microsoft-web-webview2-wpf-webview2.md) во время неявной инициализации.</span><span class="sxs-lookup"><span data-stu-id="76939-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="76939-120">Кроме того, это удобная служебная программа интеграции WPF, которая позволяет часто используемым параметрам среды быть свойствами зависимостей и создавать и использовать их в разметке.</span><span class="sxs-lookup"><span data-stu-id="76939-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="76939-121">Этот класс не предназначен для хранения всех возможных параметров настройки среды.</span><span class="sxs-lookup"><span data-stu-id="76939-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="76939-122">Если вам требуется полный контроль над средой, используемой элементом управления WebView2, необходимо явным образом инициализировать элемент управления, создав собственную среду с помощью CoreWebView2Environment. CreateAsync и передавая ее в [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*перед* тем, как установить для свойства [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) значение "что угодно".</span><span class="sxs-lookup"><span data-stu-id="76939-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="76939-123">Ознакомьтесь с документацией по классу [WebView2](microsoft-web-webview2-wpf-webview2.md) для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="76939-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="76939-124">Участников</span><span class="sxs-lookup"><span data-stu-id="76939-124">Members</span></span>

#### <span data-ttu-id="76939-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="76939-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="76939-126">Возвращает или задает значение, передаваемое в качестве параметра browserExecutableFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="76939-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="76939-127">общедоступная строка [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="76939-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="76939-128">Язык</span><span class="sxs-lookup"><span data-stu-id="76939-128">Language</span></span> 

<span data-ttu-id="76939-129">Возвращает или задает значение, используемое для свойства Language параметра CoreWebView2EnvironmentOptions, передаваемого методу CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="76939-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="76939-130">[язык](#language) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="76939-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="76939-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="76939-131">UserDataFolder</span></span> 

<span data-ttu-id="76939-132">Возвращает или задает значение, передаваемое в качестве параметра userDataFolder для CoreWebView2Environment. CreateAsync при создании среды с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="76939-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="76939-133">общедоступная строка [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="76939-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="76939-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="76939-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="76939-135">Создает новый экземпляр класса CoreWebView2CreationProperties с данными по умолчанию для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="76939-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="76939-136">общедоступная [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span><span class="sxs-lookup"><span data-stu-id="76939-136">public  [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

