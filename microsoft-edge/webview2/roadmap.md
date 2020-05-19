---
description: Узнайте о том, что дальше в WebView2
title: План для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: bc55c5a731ab6cba8f9be15208029aad0ad5357a
ms.sourcegitcommit: a75e062b71831ea850c85287a8d7d7ce3b55ec84
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659746"
---
# <span data-ttu-id="060a3-104">WebView2ная схема Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="060a3-104">Microsoft Edge WebView2 Roadmap</span></span>

##### <span data-ttu-id="060a3-105">Последнее обновление: Май 2020</span><span class="sxs-lookup"><span data-stu-id="060a3-105">Last Updated: May 2020</span></span>

<span data-ttu-id="060a3-106">Элемент управления WebView2 позволяет разработчикам внедрять веб-технологии в собственные приложения.</span><span class="sxs-lookup"><span data-stu-id="060a3-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span> <span data-ttu-id="060a3-107">В этом документе представлен перспективный план для WebView2.</span><span class="sxs-lookup"><span data-stu-id="060a3-107">This document outlines the prospective roadmap for WebView2.</span></span> 

> [!NOTE]
> <span data-ttu-id="060a3-108">WebView2 находится в активном состоянии, и план продолжит развиваться в соответствии с изменениями рынка и отзывами пользователей, поэтому обратите внимание на то, что описанные здесь планы не являются исчерпывающими и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="060a3-108">WebView2 is under active development and the roadmap will continue to evolve based on market changes and customer feedback, so please note that the plans outlined here aren't exhaustive and are subject to change.</span></span> 

<span data-ttu-id="060a3-109">Если у вас возникли проблемы или вопросы о планах, оставьте отзыв в [репозитории обратной связи](https://github.com/MicrosoftEdge/WebViewFeedback).</span><span class="sxs-lookup"><span data-stu-id="060a3-109">If you have concerns or questions about the Roadmap, please leave feedback in the [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback).</span></span>

<span data-ttu-id="060a3-110">У группы WebView2 есть несколько основных усилий.</span><span class="sxs-lookup"><span data-stu-id="060a3-110">The WebView2 team has a few major efforts underway:</span></span>

1.  <span data-ttu-id="060a3-111">Установщик среды выполнения WebView2 (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="060a3-111">WebView2 Runtime Installer (Q4 2020)</span></span>
2.  <span data-ttu-id="060a3-112">Фиксированная версия (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="060a3-112">Fixed Version (Q4 2020)</span></span>
3.  <span data-ttu-id="060a3-113">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="060a3-113">General Availability</span></span> 
    *   <span data-ttu-id="060a3-114">Win32 C/C++ (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="060a3-114">Win32 C/C++ (Q4 2020)</span></span>
    *   <span data-ttu-id="060a3-115">.NET (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="060a3-115">.NET (Q4 2020)</span></span>
    *   [<span data-ttu-id="060a3-116">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="060a3-116">WinUI 3.0</span></span>](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## <span data-ttu-id="060a3-117">Установщик & среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="060a3-117">WebView2 Runtime & Installer</span></span>

<span data-ttu-id="060a3-118">Модель распространения WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) позволит вам назначать или устанавливать среду выполнения WebView2 на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="060a3-118">WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) distribution model will allow you to target or chain install the WebView2 Runtime onto your user's machine.</span></span> <span data-ttu-id="060a3-119">Предварительная версия среды выполнения WebView2 и установщика должна быть доступна Q3 2020 и Дж в Q4 2020.</span><span class="sxs-lookup"><span data-stu-id="060a3-119">A preview of the WebView2 Runtime and installer is expected to be available Q3 2020 and GA in Q4 2020.</span></span>

## <span data-ttu-id="060a3-120">Фиксированная версия</span><span class="sxs-lookup"><span data-stu-id="060a3-120">Fixed Version</span></span>

<span data-ttu-id="060a3-121">С помощью [фиксированной](./concepts/distribution.md#roadmap) модели распределения WebView2 можно упаковать двоичные файлы Microsoft EDGE в собственное приложение.</span><span class="sxs-lookup"><span data-stu-id="060a3-121">WebView2 [Fixed](./concepts/distribution.md#roadmap) distribution model allows you to package the Microsoft Edge binaries inside your native application.</span></span> <span data-ttu-id="060a3-122">Инженерные задачи в настоящее время в предварительной версии не запланировались до конца Q3 2020 и Дж 4 квартала 2020.</span><span class="sxs-lookup"><span data-stu-id="060a3-122">Engineering work is currently under way with a preview anticipated to be ready towards the end of  Q3 2020 and GA Q4 2020.</span></span>

## <span data-ttu-id="060a3-123">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="060a3-123">General Availability</span></span> 

### <span data-ttu-id="060a3-124">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="060a3-124">Win32 C/C++</span></span>

<span data-ttu-id="060a3-125">Пакет SDK для Win32 C/C++ должен быть в 4 квартале 2020 вскоре после среды выполнения WebView2 и установщика GA.</span><span class="sxs-lookup"><span data-stu-id="060a3-125">The Win32 C/C++ SDK is expected to GA in Q4 2020, shortly after the WebView2 Runtime and installer GA.</span></span>

### <span data-ttu-id="060a3-126">.NET</span><span class="sxs-lookup"><span data-stu-id="060a3-126">.NET</span></span>

<span data-ttu-id="060a3-127">.NET SDK упаковывает пакет SDK C/C++ для Win32.</span><span class="sxs-lookup"><span data-stu-id="060a3-127">The .NET SDK wraps the Win32 C/C++ SDK.</span></span> <span data-ttu-id="060a3-128">Предполагается, что пакет .NET SDK вскоре скоро будет после того, как Win32 C/C++ GA в 4 квартале 2020.</span><span class="sxs-lookup"><span data-stu-id="060a3-128">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>

### <span data-ttu-id="060a3-129">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="060a3-129">WinUI 3.0</span></span>

<span data-ttu-id="060a3-130">Вы можете перенести WebView2 в приложения UWP с помощью [Win UI 3,0](/uwp/toolkits/winui3/), в настоящее время в Alpha.</span><span class="sxs-lookup"><span data-stu-id="060a3-130">You can bring WebView2 to UWP applications through [Win UI 3.0](/uwp/toolkits/winui3/), currently in alpha.</span></span> <span data-ttu-id="060a3-131">Извлеките [схему библиотеки пользовательского интерфейса Windows](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) , чтобы поддерживать актуальность.</span><span class="sxs-lookup"><span data-stu-id="060a3-131">Checkout the [Windows UI Library Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) to keep up to date.</span></span>  
