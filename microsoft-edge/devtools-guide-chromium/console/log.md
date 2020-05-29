---
title: Начало работы с сообщениями журнала на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601735"
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
   limitations under the License.  -->





# <span data-ttu-id="3ea6a-103">Начало работы с сообщениями журнала на консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="3ea6a-104">В этом интерактивном учебнике показано, как записывать и фильтровать сообщения на консоли [Microsoft Edge DevTools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

> ##### <span data-ttu-id="3ea6a-105">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="3ea6a-105">Figure 1</span></span>  
> <span data-ttu-id="3ea6a-106">Сообщения на консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-106">Messages in the Console</span></span>  
> ![Сообщения на консоли][ImageLogExample]  

<span data-ttu-id="3ea6a-108">Этот учебник предназначен для выполнения в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="3ea6a-109">Предполагается, что вы знакомы с основами веб-разработки, например с помощью JavaScript для добавления интерактивности на страницу.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="3ea6a-110">Настройка ролика и DevTools</span><span class="sxs-lookup"><span data-stu-id="3ea6a-110">Set up the demo and DevTools</span></span>   

<span data-ttu-id="3ea6a-111">Этот учебник разработан таким образом, чтобы вы могли открыть демонстрацию и попробовать все рабочие процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="3ea6a-112">После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="3ea6a-113">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры журнала консоли** , чтобы открыть ее на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-113">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="3ea6a-114">Примеры журнала консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  <span data-ttu-id="3ea6a-115">Чтобы открыть DevTools, сосредоточьте демонстрацию и нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3ea6a-115">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="3ea6a-116">По умолчанию DevTools открывается справа от демонстрации.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-116">By default DevTools opens to the right of the demo.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-117">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="3ea6a-117">Figure 2</span></span>  
    > <span data-ttu-id="3ea6a-118">DevTools открывается справа от демонстрации</span><span class="sxs-lookup"><span data-stu-id="3ea6a-118">DevTools opens to the right of the demo</span></span>  
    > <span data-ttu-id="3ea6a-119">! [DevTools открывается справа от демонстрации] [ImageDevToolsRight]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-119">![DevTools opens to the right of the demo][ImageDevToolsRight]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="3ea6a-120">[Закрепите DevTools в нижней части окна или открепите его в отдельном окне][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="3ea6a-120">[Dock DevTools to the bottom of the window or undock it into a separate window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-121">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="3ea6a-121">Figure 3</span></span>  
    > <span data-ttu-id="3ea6a-122">DevTools закреплено в нижней части демонстрации</span><span class="sxs-lookup"><span data-stu-id="3ea6a-122">DevTools docked to the bottom of the demo</span></span>  
    > <span data-ttu-id="3ea6a-123">! [DevTools закреплена в нижней части демонстрации] [ImageDevToolsBottom]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-123">![DevTools docked to the bottom of the demo][ImageDevToolsBottom]</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-124">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="3ea6a-124">Figure 4</span></span>  
    > <span data-ttu-id="3ea6a-125">Браузер в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="3ea6a-125">Browser in a separate window</span></span>  
    > <span data-ttu-id="3ea6a-126">! [Браузер в отдельном окне] [ImageDevToolsSeparateBrowse]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-126">![Browser in a separate window][ImageDevToolsSeparateBrowse]</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-127">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="3ea6a-127">Figure 5</span></span>  
    > <span data-ttu-id="3ea6a-128">DevTools отсоединяется в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="3ea6a-128">DevTools undocked in a separate window</span></span>  
    > <span data-ttu-id="3ea6a-129">! [DevTools открепляются в отдельном окне] [ImageDevToolsSeparateDevTools]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-129">![DevTools undocked in a separate window][ImageDevToolsSeparateDevTools]</span></span>  
    
## <span data-ttu-id="3ea6a-130">Просмотр сообщений, записанных из JavaScript</span><span class="sxs-lookup"><span data-stu-id="3ea6a-130">View messages logged from JavaScript</span></span>   

<span data-ttu-id="3ea6a-131">Большинство сообщений, которые вы видите на консоли, поступают от веб-разработчиков, которые написали JavaScript страницы.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-131">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="3ea6a-132">Цель этого раздела — рассказать вам о различных типах сообщений, которые вы, вероятно, видите на консоли, и объясните, как можно вести журнал для каждого типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-132">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="3ea6a-133">Нажмите кнопку " **сведения о журнале** " в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-133">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="3ea6a-134">Получает запись в журнал консоли.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-134">gets logged to the Console.</span></span>
    
    > ##### <span data-ttu-id="3ea6a-135">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="3ea6a-135">Figure 6</span></span>  
    > <span data-ttu-id="3ea6a-136">Консоль после нажатия кнопки " **сведения о журнале** "</span><span class="sxs-lookup"><span data-stu-id="3ea6a-136">The Console after clicking **Log Info**</span></span>  
    > <span data-ttu-id="3ea6a-137">! [Консоль после нажатия кнопки "сведения о журнале"] [ImageLogInfo]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-137">![The Console after clicking Log Info][ImageLogInfo]</span></span>  
    
1.  <span data-ttu-id="3ea6a-138">Рядом с `Hello, Console!` сообщением в консоли щелкните **log. js: 2**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-138">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="3ea6a-139">Откроется панель источники, в которой выделена строка кода, которая привела к тому, что сообщение будет записано на консоль.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-139">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="3ea6a-140">Сообщение было занесено в журнал при выполнении кода JavaScript на странице `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-140">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    > ##### <span data-ttu-id="3ea6a-141">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="3ea6a-141">Figure 7</span></span>  
    > <span data-ttu-id="3ea6a-142">DevTools открывает панель "источники" после того, как вы щелкните **log. js: 2**</span><span class="sxs-lookup"><span data-stu-id="3ea6a-142">DevTools opens the Sources panel after you click **log.js:2**</span></span>  
    > <span data-ttu-id="3ea6a-143">! [DevTools открывает панель «источники» после того, как вы щелкните log. js: 2] [ImageSourceLog]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-143">![DevTools opens the Sources panel after you click log.js:2][ImageSourceLog]</span></span>  
    
1.  <span data-ttu-id="3ea6a-144">Вернитесь на консоль с помощью одного из следующих рабочих процессов:</span><span class="sxs-lookup"><span data-stu-id="3ea6a-144">Navigate back to the Console using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="3ea6a-145">Откройте вкладку **консоль** .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-145">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="3ea6a-146">Нажимайте клавиши `Control` + `[` \ (Windows \) или `Command` + `[` \ (macOS \) до тех пор, пока не будет фокус на панели консоли.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-146">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="3ea6a-147">[Откройте меню команд][DevToolsCommandMenu], начните вводить текст `Console` , выберите команду **Показать панель консоли** , а затем нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-147">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="3ea6a-148">Нажмите кнопку **предупреждение журнала** в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-148">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="3ea6a-149">Получает запись в журнал консоли.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-149">gets logged to the Console.</span></span>  <span data-ttu-id="3ea6a-150">Сообщения, которые форматируются таким образом, представляют собой предупреждения.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-150">Messages formatted like this are warnings.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-151">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="3ea6a-151">Figure 8</span></span>  
    > <span data-ttu-id="3ea6a-152">Консоль после нажатия кнопки " **Журнал** "</span><span class="sxs-lookup"><span data-stu-id="3ea6a-152">The Console after clicking **Log Warning**</span></span>  
    > <span data-ttu-id="3ea6a-153">! [Консоль после нажатия кнопки Log Warning] [ImageConsoleLogWarning]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-153">![The Console after clicking Log Warning][ImageConsoleLogWarning]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="3ea6a-154">Если вы хотите просмотреть код, который привел к тому, что сообщение записалось определенным образом, нажмите на сценарий \ (например, `log.js:12` \), чтобы просмотреть код, который привел к форматированию сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-154">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="3ea6a-155">Щелкните значок **развернуть расширение** ![ ][ImageExpandIcon] перед `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-155">Click the **Expand** ![Expand][ImageExpandIcon] icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="3ea6a-156">DevTools показывает [трассировку стека][WikiStackTrace] , ведущая к вызову.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-156">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-157">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="3ea6a-157">Figure 9</span></span>  
    > <span data-ttu-id="3ea6a-158">Трассировка стека</span><span class="sxs-lookup"><span data-stu-id="3ea6a-158">A stack trace</span></span>  
    > <span data-ttu-id="3ea6a-159">! [Трассировка стека] [ImageStackTrace]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-159">![A stack trace][ImageStackTrace]</span></span>  
    
    <span data-ttu-id="3ea6a-160">Трассировка стека указывает на то, что вызвана функция с именем `logWarning` , которая, в свою очередь, вызывает функцию с именем `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-160">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="3ea6a-161">Другими словами, вызов, который произошел первым, находится в нижней части трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-161">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="3ea6a-162">Вы можете регистрировать трассировку стека в любое время, вызывая `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-162">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="3ea6a-163">Нажмите " **журнал ошибок**".</span><span class="sxs-lookup"><span data-stu-id="3ea6a-163">Click **Log Error**.</span></span>  <span data-ttu-id="3ea6a-164">Регистрируется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="3ea6a-164">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### <span data-ttu-id="3ea6a-165">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="3ea6a-165">Figure 10</span></span>  
    > <span data-ttu-id="3ea6a-166">Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="3ea6a-166">An error message</span></span>  
    > <span data-ttu-id="3ea6a-167">! [Сообщение об ошибке] [ImageLogError]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-167">![An error message][ImageLogError]</span></span>  
    
1.  <span data-ttu-id="3ea6a-168">Нажмите кнопку **таблица журнала**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-168">Click **Log Table**.</span></span>  <span data-ttu-id="3ea6a-169">Таблица, посвященная знаменитым исполнителям, записывается на консоль.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-169">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3ea6a-170">`birthday`Столбец заполняется только для одной строки.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-170">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="3ea6a-171">Проверьте код, чтобы узнать, почему это так.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-171">Check the code to figure out why that is.</span></span>
    
    > ##### <span data-ttu-id="3ea6a-172">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="3ea6a-172">Figure 11</span></span>  
    > <span data-ttu-id="3ea6a-173">Таблица в консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-173">A table in the Console</span></span>  
    > <span data-ttu-id="3ea6a-174">! [Таблица на консоли] [ImageConsoleTable]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-174">![A table in the Console][ImageConsoleTable]</span></span>  
    
1.  <span data-ttu-id="3ea6a-175">Нажмите кнопку **Группа журналов**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-175">Click **Log Group**.</span></span>  <span data-ttu-id="3ea6a-176">Названия четырех знаменитых turtlesных, преступных, группируются под `Adolescent Irradiated Espionage Tortoises` меткой.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-176">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-177">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="3ea6a-177">Figure 12</span></span>  
    > <span data-ttu-id="3ea6a-178">Группа сообщений на консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-178">A group of messages in the Console</span></span>  
    > <span data-ttu-id="3ea6a-179">! [Группа сообщений на консоли] [ImageConsoleLogGroup]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-179">![A group of messages in the Console][ImageConsoleLogGroup]</span></span>  
    
1.  <span data-ttu-id="3ea6a-180">Выберите пункт **Журнал настраиваемого**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-180">Click **Log Custom**.</span></span>  <span data-ttu-id="3ea6a-181">Сообщение с красной рамкой и синим фоном записываются в консоль.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-181">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-182">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="3ea6a-182">Figure 13</span></span>  
    > <span data-ttu-id="3ea6a-183">Сообщение с настраиваемым форматированием в консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-183">A message with custom formatting in the Console</span></span>  
    > <span data-ttu-id="3ea6a-184">! [Сообщение с настраиваемым форматированием в консоли] [ImageConsoleLogCustomFormatting]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-184">![A message with custom formatting in the Console][ImageConsoleLogCustomFormatting]</span></span>  
    
<span data-ttu-id="3ea6a-185">Основная идея здесь заключается в том, что если вы хотите записывать сообщения на консоль из JavaScript, используйте один из этих `console` методов.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-185">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="3ea6a-186">Каждый метод форматирует сообщения по-разному.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-186">Each method formats messages differently.</span></span>  

<span data-ttu-id="3ea6a-187">В этом разделе есть еще больше методов, чем было показано ниже.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-187">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="3ea6a-188">В этом учебнике показано, как ознакомиться с другими методами.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-188">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="3ea6a-189">Просмотр сообщений, записанных браузером</span><span class="sxs-lookup"><span data-stu-id="3ea6a-189">View messages logged by the browser</span></span>   

<span data-ttu-id="3ea6a-190">Браузер также регистрирует сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-190">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="3ea6a-191">Обычно это происходит при возникновении проблемы со страницей.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-191">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="3ea6a-192">Нажмите кнопку **причина 404**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-192">Click **Cause 404**.</span></span>  <span data-ttu-id="3ea6a-193">Браузер регистрирует `404` ошибку сети из-за того, что JavaScript пытается получить несуществующий файл.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-193">The browser logs a `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-194">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="3ea6a-194">Figure 14</span></span>  
    > <span data-ttu-id="3ea6a-195">Ошибка 404 в консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-195">A 404 error in the Console</span></span>  
    > <span data-ttu-id="3ea6a-196">! [Ошибка 404 в консоли] [ImageConsoleLogError]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-196">![A 404 error in the Console][ImageConsoleLogError]</span></span>  
    
1.  <span data-ttu-id="3ea6a-197">Нажмите кнопку **Причина ошибки**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-197">Click **Cause Error**.</span></span>  <span data-ttu-id="3ea6a-198">Браузер регистрирует неперехваченные записи, `TypeError` так как JavaScript пытается обновить несуществующий узел DOM.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-198">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-199">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="3ea6a-199">Figure 15</span></span>  
    > <span data-ttu-id="3ea6a-200">TypeError на консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-200">A TypeError in the Console</span></span>  
    > <span data-ttu-id="3ea6a-201">! [TypeError на консоли] [ImageConsoleLogTypeError]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-201">![A TypeError in the Console][ImageConsoleLogTypeError]</span></span>  
    
1.  <span data-ttu-id="3ea6a-202">Щелкните раскрывающийся список **уровни журнала** и включите параметр **подробный** , если он отключен.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-202">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="3ea6a-203">Подробнее о фильтрации можно узнать в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-203">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="3ea6a-204">Это необходимо сделать, чтобы убедиться в том, что следующее сообщение отображается в журнале.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-204">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-205">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="3ea6a-205">Figure 16</span></span>  
    > <span data-ttu-id="3ea6a-206">Включение **подробного** уровня ведения журнала</span><span class="sxs-lookup"><span data-stu-id="3ea6a-206">Enabling the **Verbose** log level</span></span>  
    > <span data-ttu-id="3ea6a-207">! [Включение подробного уровня ведения журнала] [ImageVerboseLogLevel]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-207">![Enabling the Verbose log level][ImageVerboseLogLevel]</span></span>  
    
1.  <span data-ttu-id="3ea6a-208">Нажмите кнопку **вызвать нарушение**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-208">Click **Cause Violation**.</span></span>  <span data-ttu-id="3ea6a-209">Страница перестает отвечать на запросы в течение нескольких секунд, а затем браузер заносит сообщение `[Violation] 'click' handler took 3000ms` на консоль.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-209">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="3ea6a-210">Точная длительность может отличаться.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-210">The exact duration may vary.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-211">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="3ea6a-211">Figure 17</span></span>  
    > <span data-ttu-id="3ea6a-212">Нарушение в консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-212">A violation in the Console</span></span>  
    > <span data-ttu-id="3ea6a-213">! [Нарушение в консоли] [ImageConsoleLogViolation]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-213">![A violation in the Console][ImageConsoleLogViolation]</span></span>  
    
## <span data-ttu-id="3ea6a-214">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="3ea6a-214">Filter messages</span></span>   

<span data-ttu-id="3ea6a-215">На некоторых страницах вы видите консоль с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-215">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="3ea6a-216">DevTools предоставляет множество различных способов фильтрации сообщений, которые не связаны с задачей.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-216">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="3ea6a-217">Фильтрация по уровню ведения журнала</span><span class="sxs-lookup"><span data-stu-id="3ea6a-217">Filter by log level</span></span>   

<span data-ttu-id="3ea6a-218">Каждому `console` методу назначается уровень серьезности: `Verbose` , `Info` , `Warning` или `Error` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-218">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="3ea6a-219">Например, `console.log()` `Info` сообщение на уровне, в то время как `console.error()` сообщение на `Error` уровне.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-219">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="3ea6a-220">Щелкните раскрывающийся список **уровни журнала** и отключите **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-220">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="3ea6a-221">Уровень отключается, если рядом с ним больше нет метки.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-221">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="3ea6a-222">`Error`Сообщения на уровне пропадают.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-222">The `Error`-level messages disappear.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-223">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="3ea6a-223">Figure 18</span></span>  
    > <span data-ttu-id="3ea6a-224">Отключение `Error` сообщений уровня на консоли</span><span class="sxs-lookup"><span data-stu-id="3ea6a-224">Disabling `Error`-level messages in the Console</span></span>  
    > <span data-ttu-id="3ea6a-225">! [Отключение сообщений уровня ошибки на консоли] [ImageConsoleDisablingLogError]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-225">![Disabling Error-level messages in the Console][ImageConsoleDisablingLogError]</span></span>  
    
1.  <span data-ttu-id="3ea6a-226">Снова щелкните в раскрывающемся списке **уровни журнала** и повторно включите **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-226">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="3ea6a-227">`Error`Снова появятся сообщения уровня.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-227">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="3ea6a-228">Фильтрация по тексту</span><span class="sxs-lookup"><span data-stu-id="3ea6a-228">Filter by text</span></span>   

<span data-ttu-id="3ea6a-229">Если вы хотите только просматривать сообщения, содержащие точную строку, введите эту строку в текстовом поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-229">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="3ea6a-230">Введите `Dave` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-230">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="3ea6a-231">Все сообщения, в которых не указана строка `Dave` , скрыты.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-231">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="3ea6a-232">Кроме того, вы можете увидеть `Adolescent Irradiated Espionage Tortoises` метку.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-232">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="3ea6a-233">Это ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-233">That is a bug.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-234">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="3ea6a-234">Figure 19</span></span>  
    > <span data-ttu-id="3ea6a-235">Фильтрация сообщений, которые не включают</span><span class="sxs-lookup"><span data-stu-id="3ea6a-235">Filtering out any message that does not include</span></span> `Dave`  
    > <span data-ttu-id="3ea6a-236">! [Фильтрация сообщений, которые не включают Дэйв] [ImageLogTextFiltering]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-236">![Filtering out any message that does not include Dave][ImageLogTextFiltering]</span></span>  
    
1.  <span data-ttu-id="3ea6a-237">`Dave`"Удалить" из текстового поля " **Фильтр** ".</span><span class="sxs-lookup"><span data-stu-id="3ea6a-237">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="3ea6a-238">Все сообщения снова появятся.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-238">All the messages reappear.</span></span>  

### <span data-ttu-id="3ea6a-239">Фильтрация по регулярному выражению</span><span class="sxs-lookup"><span data-stu-id="3ea6a-239">Filter by regular expression</span></span>   

<span data-ttu-id="3ea6a-240">Если вы хотите отобразить все сообщения, которые содержат шаблон текста, а не определенную строку, используйте [регулярное выражение][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="3ea6a-240">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="3ea6a-241">Введите `/^[AH]/` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-241">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="3ea6a-242">Введите этот шаблон в [Regex][|::ref1::|Main] , чтобы узнать, что он делает.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-242">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-243">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="3ea6a-243">Figure 20</span></span>  
    > <span data-ttu-id="3ea6a-244">Фильтрация сообщений, не соответствующих шаблону</span><span class="sxs-lookup"><span data-stu-id="3ea6a-244">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    > <span data-ttu-id="3ea6a-245">! [Фильтрация сообщений, не соответствующих шаблону] [ImageLogRegExFiltering]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-245">![Filtering out any message that does not match a pattern][ImageLogRegExFiltering]</span></span>  
    
1.  <span data-ttu-id="3ea6a-246">`/^[AH]/`"Удалить" из текстового поля " **Фильтр** ".</span><span class="sxs-lookup"><span data-stu-id="3ea6a-246">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="3ea6a-247">Все сообщения будут снова видны.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-247">All messages are visible again.</span></span>  

### <span data-ttu-id="3ea6a-248">Фильтрация по источнику сообщения</span><span class="sxs-lookup"><span data-stu-id="3ea6a-248">Filter by message source</span></span>   

<span data-ttu-id="3ea6a-249">Если вы хотите только просматривать сообщения, поступившие с определенного URL-адреса, используйте **боковую панель**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-249">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="3ea6a-250">Нажмите кнопку **Показать боковую панель консоли** ![ , чтобы показать боковую панель консоли ][ImageShowConsoleSidebarIcon] .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-250">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon].</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-251">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="3ea6a-251">Figure 21</span></span>  
    > <span data-ttu-id="3ea6a-252">Боковая панель</span><span class="sxs-lookup"><span data-stu-id="3ea6a-252">The Sidebar</span></span>  
    > <span data-ttu-id="3ea6a-253">! [Боковая панель] [ImageConsoleSidebar]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-253">![The Sidebar][ImageConsoleSidebar]</span></span>  
    
1.  <span data-ttu-id="3ea6a-254">Щелкните значок **развернуть** развернутый ![ ][ImageExpandIcon] рядом с количеством сообщений.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-254">Click the **Expand** ![Expand][ImageExpandIcon] icon next to the number of messages.</span></span>  <span data-ttu-id="3ea6a-255">На [рисунке 21](#figure-21)количество сообщений обозначается **13 сообщениями**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-255">In [Figure 21](#figure-21), the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="3ea6a-256">На **боковой панели** отображается список URL-адресов, которые привели к тому, что сообщения записываются в журнал.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-256">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="3ea6a-257">Например, это `log.js` связано с 11 сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-257">For example, `log.js` caused 11 messages.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-258">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="3ea6a-258">Figure 22</span></span>  
    > <span data-ttu-id="3ea6a-259">Просмотр источника сообщений на боковой панели</span><span class="sxs-lookup"><span data-stu-id="3ea6a-259">Viewing the source of messages in the Sidebar</span></span>  
    > <span data-ttu-id="3ea6a-260">! [Просмотр источника сообщений на боковой панели] [ImageConsoleSidebarLogSource]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-260">![Viewing the source of messages in the Sidebar][ImageConsoleSidebarLogSource]</span></span>  
    
### <span data-ttu-id="3ea6a-261">Фильтрация по пользовательским сообщениям</span><span class="sxs-lookup"><span data-stu-id="3ea6a-261">Filter by user messages</span></span>   

<span data-ttu-id="3ea6a-262">Более того, после того, как вы щелкните **сведения журнала**, сценарий вызывается `console.log('Hello, Console!')` для записи сообщения на консоль.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-262">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="3ea6a-263">Сообщения, которые регистрируются из сценария JavaScript вроде этого, называются **сообщениями пользователей**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-263">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="3ea6a-264">В отличие от того, когда вы щелкните **Причина ошибки 404**, браузер записал `Error` сообщение о том, что запрошенный ресурс не найден.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-264">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="3ea6a-265">Такие сообщения считаются **сообщениями браузера**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-265">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="3ea6a-266">Используйте **боковую панель** , чтобы отфильтровать сообщения браузера и показать только сообщения пользователей.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-266">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="3ea6a-267">Выберите **9 пользовательских сообщений**.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-267">Click **9 User Messages**.</span></span>  <span data-ttu-id="3ea6a-268">Сообщения браузера скрыты.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-268">The browser messages are hidden.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-269">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="3ea6a-269">Figure 23</span></span>  
    > <span data-ttu-id="3ea6a-270">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="3ea6a-270">Filtering out browser messages</span></span>  
    > <span data-ttu-id="3ea6a-271">! [Фильтрация сообщений браузера] [ImageConsoleLogBrowserFiltering]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-271">![Filtering out browser messages][ImageConsoleLogBrowserFiltering]</span></span>  
    
1.  <span data-ttu-id="3ea6a-272">Щелкните **13 сообщений** , чтобы снова Показать все сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-272">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="3ea6a-273">Использование консоли рядом с любой другой панелью</span><span class="sxs-lookup"><span data-stu-id="3ea6a-273">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="3ea6a-274">Что делать, если стили редактируются, но вам нужно быстро проверить журнал консоли на что-то?</span><span class="sxs-lookup"><span data-stu-id="3ea6a-274">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="3ea6a-275">Используйте денежный ящик.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-275">Use the Drawer.</span></span>  

1.  <span data-ttu-id="3ea6a-276">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-276">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3ea6a-277">Нажмите клавишу `Escape` .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-277">Press `Escape`.</span></span>  <span data-ttu-id="3ea6a-278">Откроется вкладка "консоль" для **ящика** .</span><span class="sxs-lookup"><span data-stu-id="3ea6a-278">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="3ea6a-279">У него есть все функции панели консоли, которые использовались в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="3ea6a-279">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="3ea6a-280">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="3ea6a-280">Figure 24</span></span>  
    > <span data-ttu-id="3ea6a-281">Вкладка «консоль» в ящике</span><span class="sxs-lookup"><span data-stu-id="3ea6a-281">The Console tab in the Drawer</span></span>  
    > <span data-ttu-id="3ea6a-282">! [Вкладка "консоль" в ящике] [ImageDrawerConsole]</span><span class="sxs-lookup"><span data-stu-id="3ea6a-282">![The Console tab in the Drawer][ImageDrawerConsole]</span></span>  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Рисунок 1: сообщения на консоли"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-example-Devtools-right-Console.MSFT.png "Рисунок 2: DevTools откроется справа от демо"  
[ImageDevToolsBottom]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-example-Devtools-Bottom-Console.MSFT.png "Рисунок 3: DevTools закреплены в нижней части демона"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-example-Devtools-separate-Console-Browse.MSFT.png "Рисунок 4: браузер в отдельном окне"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-example-Devtools-separate-Console-Devtools.MSFT.png "Рисунок 5: DevTools открепляются в отдельном окне"  
[ImageLogInfo]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-info.MSFT.png "Рисунок 6: консоль после нажатия кнопки" сведения о журнале ""  
[ImageSourceLog]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Sources-logjs.MSFT.png "Рисунок 7: DevTools открывает панель" источники "после того, как вы щелкните log. js: 2  
[ImageConsoleLogWarning]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-Warning.MSFT.png "Рисунок 8: консоль после нажатия кнопки" log warning "  
[ImageStackTrace]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-Warning-Expanded.MSFT.png "Рисунок 9: трассировка стека"  
[ImageLogError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-Error.MSFT.png "Рисунок 10: сообщение об ошибке"  
[ImageConsoleTable]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-Table.MSFT.png "Рисунок 11: таблица на консоли"  
[ImageConsoleLogGroup]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-Group.MSFT.png "Рисунок 12: группа сообщений на консоли"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-log-Custom.MSFT.png "Рисунок 13: сообщение с настраиваемым форматированием в консоли"  
[ImageConsoleLogError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Cause-404.MSFT.png "Рисунок 14: ошибка 404 в консоли"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Cause-Error.MSFT.png "Рисунок 15: TypeError на консоли"  
[ImageVerboseLogLevel]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Cause-error-log-Levels.MSFT.png "Рисунок 16: включение подробного уровня ведения журнала"  
[ImageConsoleLogViolation]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Cause-Violation.MSFT.png "Рисунок 17: нарушение в консоли"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Cause-Violation-log-Levels.MSFT.png "Рисунок 18: отключение сообщений уровня ошибки на консоли"  
[ImageLogTextFiltering]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-ALL-messages-Text-Filter.MSFT.png "рис. 19", чтобы отфильтровать все сообщения, не содержащие Дэйв "  
[ImageLogRegExFiltering]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-ALL-messages-Regex-Filter.MSFT.png "Рисунок 20: Фильтрация любого сообщения, не соответствующего шаблону"  
[ImageConsoleSidebar]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-ALL-messages.MSFT.png "Рисунок 21: Боковая панель"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-Expanded-ALL-messages.MSFT.png "рис. 22: Просмотр источника сообщений на боковой панели"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-User-messages.MSFT.png "Рисунок 23: Фильтрация сообщений браузера"  
[ImageDrawerConsole]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Elements-drawer-Console-sidebar-ALL-messages.MSFT.png "Рисунок 24: вкладка" консоль "в ящике"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft Edge \ (Chromium \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Справочник по консоли"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с сообщениями в журнале | Цепь"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "Регулярное выражение"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедии"  


> [!NOTE]
> <span data-ttu-id="3ea6a-316">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3ea6a-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3ea6a-317">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/log) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3ea6a-317">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3ea6a-319">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3ea6a-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
