---
description: Сведения о разработке расширений Microsoft Edge. Эти небольшие программы можно использовать для добавления новых функций в Microsoft EDGE или изменения существующих функций.
title: Расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
ms.technology: extensions
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: 4cc47ba9d927caf7457141f5c8c7eacbb9627b07
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571504"
---
# <span data-ttu-id="af855-105">Расширения Microsoft EDGE (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="af855-105">Microsoft Edge (EdgeHTML) extensions</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="af855-106">Расширения — это небольшие программы, которые можно использовать для добавления новых функций в Microsoft EDGE (EdgeHTML) или изменения существующих функций.</span><span class="sxs-lookup"><span data-stu-id="af855-106">Extensions are small programs that can be used to add new features to Microsoft Edge (EdgeHTML) or modify the existing functionality.</span></span> <span data-ttu-id="af855-107">Расширения предназначены для того, чтобы улучшить работу с повседневным просмотром пользователя, предоставив специализированные функциональность, важную для целевых аудиторий.</span><span class="sxs-lookup"><span data-stu-id="af855-107">Extensions are intended to improve a user’s day-to-day browsing experience by providing niche functionality that is important to targeted audiences.</span></span>

<span data-ttu-id="af855-108">Microsoft EDGE (EdgeHTML) поддерживает новую модель расширения на основе HTML, JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="af855-108">Microsoft Edge (EdgeHTML) supports a new HTML, JavaScript and CSS based extension model.</span></span> <span data-ttu-id="af855-109">Это новая модель, совместимая с хромом, которая означает, что существующие разработчики расширения Chrome смогут переносить свои расширения в Microsoft EDGE (EdgeHTML) с минимальными изменениями.</span><span class="sxs-lookup"><span data-stu-id="af855-109">This new model is Chrome-compatible which means that existing Chrome extension developers will be able to migrate their extensions to Microsoft Edge (EdgeHTML) with minimal changes.</span></span>

<span data-ttu-id="af855-110">Чтобы получить общие сведения о том, как создать расширение Microsoft EDGE (EdgeHTML) с начала разработки до публикации, ознакомьтесь с [руководством "Приступая к работе](./getting-started.md)".</span><span class="sxs-lookup"><span data-stu-id="af855-110">To get an overview of the end to end journey of creating a Microsoft Edge (EdgeHTML) extension from development to publishing, check out the [Getting started guide](./getting-started.md)!</span></span>


## <span data-ttu-id="af855-111">Популярные статьи</span><span class="sxs-lookup"><span data-stu-id="af855-111">Popular articles</span></span>

<table>
  <tr>
    <td><a href = "./api-support/extension-api-roadmap.md"><span data-ttu-id="af855-112">Схема расширения API</span><span class="sxs-lookup"><span data-stu-id="af855-112">Extension API roadmap</span></span></a></td>
    <td><span data-ttu-id="af855-113">Узнайте, какие API поддерживаются/в рамках разработки для Windows 10 Insider Preview и открытых сборок Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af855-113">Check out what APIs are supported/in development for Windows 10 Insider Preview and publicly released builds of Microsoft Edge.</span></span></td></p>
<p>  </tr>
  <tr>
    <td><a href = "./api-support/supported-apis.md"><span data-ttu-id="af855-114">Поддерживаемые API</span><span class="sxs-lookup"><span data-stu-id="af855-114">Supported APIs</span></span></a></td>
    <td><span data-ttu-id="af855-115">Получение сведений о поддерживаемых API-интерфейсах, включая известные проблемы и несовместимость с интерфейсом Chrome.</span><span class="sxs-lookup"><span data-stu-id="af855-115">Get info on our supported APIs including known issues and Chrome incompatibilities.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/creating-an-extension.md"><span data-ttu-id="af855-116">Создание расширения</span><span class="sxs-lookup"><span data-stu-id="af855-116">Creating an extension</span></span></a></td>
    <td><span data-ttu-id="af855-117">Не знакомы с развитием расширений по всему миру?</span><span class="sxs-lookup"><span data-stu-id="af855-117">New to the world of extension development?</span></span> <span data-ttu-id="af855-118">Ознакомьтесь с учебными курсами, чтобы быстро приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="af855-118">Try out some tutorials to get up to speed.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/packaging.md"><span data-ttu-id="af855-119">Упакован</span><span class="sxs-lookup"><span data-stu-id="af855-119">Packaging</span></span></a></td>
    <td><span data-ttu-id="af855-120">Сведения о том, как упаковать расширение после того, как вы&#39;завершили разработку.</span><span class="sxs-lookup"><span data-stu-id="af855-120">Learn how to package up your extension after you&#39;ve finished development.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/porting-chrome-extensions.md"><span data-ttu-id="af855-121">Перенос расширений хрома</span><span class="sxs-lookup"><span data-stu-id="af855-121">Porting Chrome extensions</span></span></a></td>
    <td><span data-ttu-id="af855-122">Создало расширение Chrome, которое вы&#39;d нравится для просмотра в Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="af855-122">Created a Chrome extension you&#39;d like to see on Microsoft Edge?</span></span> <span data-ttu-id="af855-123">Узнайте, как перенести его с помощью набора средств расширения Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af855-123">See how to port it with the Microsoft Edge Extension Toolkit.</span></span></td>

  </tr>
</table>
