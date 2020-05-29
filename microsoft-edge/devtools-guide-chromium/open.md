---
title: Открыть Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601889"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# <span data-ttu-id="ea099-103">Открыть Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ea099-103">Open Microsoft Edge DevTools</span></span>   



<span data-ttu-id="ea099-104">Существует множество способов открыть Microsoft Edge DevTools, так как разным пользователям нужен быстрый доступ к разным частям пользовательского интерфейса DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea099-104">There are many ways to open Microsoft Edge DevTools, because different users want fast access to different parts of the DevTools UI.</span></span>  

## <span data-ttu-id="ea099-105">Открытие панели "элементы" для проверки модели DOM или CSS</span><span class="sxs-lookup"><span data-stu-id="ea099-105">Open the Elements panel to inspect the DOM or CSS</span></span>   

<span data-ttu-id="ea099-106">Если вы хотите проверить стили или атрибуты узла DOM, щелкните элемент правой кнопкой мыши и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="ea099-106">When you want to inspect the styles or attributes of a DOM node, right-click the element and select **Inspect**.</span></span>  

> ##### <span data-ttu-id="ea099-107">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="ea099-107">Figure 1</span></span>  
> <span data-ttu-id="ea099-108">Параметр **проверки**</span><span class="sxs-lookup"><span data-stu-id="ea099-108">The **Inspect** option</span></span>  
> ![Параметр проверки][ImageInspectOption]  

<span data-ttu-id="ea099-110">Или нажмите клавиши `Control` + `Shift` + `C` \ (Windows \) или `Command` + `Option` + `C` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="ea099-110">Or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Option`+`C` \(macOS\).</span></span>  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <span data-ttu-id="ea099-111">Открытие панели консоли для просмотра сообщений, занесенных в журнал, или запуск JavaScript</span><span class="sxs-lookup"><span data-stu-id="ea099-111">Open the Console panel to view logged messages or run JavaScript</span></span>   

<span data-ttu-id="ea099-112">Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \), чтобы перейти прямо в панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="ea099-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to jump straight into the **Console** panel.</span></span>  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## <span data-ttu-id="ea099-113">Открытие последней открытой панели</span><span class="sxs-lookup"><span data-stu-id="ea099-113">Open the last panel you had open</span></span>   

<span data-ttu-id="ea099-114">Нажмите клавиши `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="ea099-114">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  

## <span data-ttu-id="ea099-115">Открытие DevTools в главном меню Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ea099-115">Open DevTools from the Microsoft Edge main menu</span></span>  

<span data-ttu-id="ea099-116">Нажмите кнопку **Параметры и выберите другие \ (Alt + F \)** `...` , а затем — **Дополнительные инструменты**  >  **разработчика**.</span><span class="sxs-lookup"><span data-stu-id="ea099-116">Click **Settings and more \(Alt+F\)** `...` and then select **More Tools** > **Developer Tools**.</span></span>  

> ##### <span data-ttu-id="ea099-117">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="ea099-117">Figure 2</span></span>  
> <span data-ttu-id="ea099-118">Открытие DevTools в главном меню Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ea099-118">Opening DevTools from the Microsoft Edge main menu</span></span>  
> ![Открытие DevTools в главном меню Microsoft Edge][ImageOpenFromMain]  

## <span data-ttu-id="ea099-120">Автоматическое открытие DevTools на каждой новой вкладке</span><span class="sxs-lookup"><span data-stu-id="ea099-120">Auto-open DevTools on every new tab</span></span>   

<span data-ttu-id="ea099-121">Откройте Microsoft Edge из командной строки и передайте `--auto-open-devtools-for-tabs` флаг.</span><span class="sxs-lookup"><span data-stu-id="ea099-121">Open Microsoft Edge from the command line and pass the `--auto-open-devtools-for-tabs` flag.</span></span>  

<span data-ttu-id="ea099-122">Windows \ (CMD \):</span><span class="sxs-lookup"><span data-stu-id="ea099-122">Windows \(CMD\):</span></span>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

<span data-ttu-id="ea099-123">Windows \ (PowerShell \):</span><span class="sxs-lookup"><span data-stu-id="ea099-123">Windows \(PowerShell\):</span></span>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

<span data-ttu-id="ea099-124">MacOS</span><span class="sxs-lookup"><span data-stu-id="ea099-124">macOS:</span></span>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Рисунок 1: параметр "Проверка""  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Рисунок 2: открытие DevTools в главном меню Microsoft Edge"  

<!-- links -->  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> <span data-ttu-id="ea099-127">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ea099-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ea099-128">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/open) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ea099-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/open) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ea099-130">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ea099-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
