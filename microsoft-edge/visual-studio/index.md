---
description: Microsoft EDGE (Chromium) и Visual Studio
title: Visual Studio
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, VS, Visual Studio, отладчик
ms.openlocfilehash: 27f4b7d4dc85e3cd5ba49497dec2d4658166794b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572788"
---
# Visual Studio

[Visual Studio](https://visualstudio.microsoft.com/vs/) — это интегрированная среда разработки (IDE), которую можно использовать для редактирования, отладки, построения и публикации веб-приложений. Это мощная функциональная программа, которую можно использовать для различных аспектов разработки веб-приложений. В Visual Studio и более поздних версиях стандартных редакторов и отладчика, которые предоставляют большинство IDEs, для упрощения процесса разработки используются компиляторы, средства завершения кода, графические конструкторы и многие другие функции. Заголовку на [эту страницу](https://visualstudio.microsoft.com/downloads/) , чтобы скачать Visual Studio, если вы еще не используете ее.

В настоящее время Visual Studio 2019 поддерживает отладку JavaScript в Microsoft Edge для ASP\.NET платформы и ASP\.NET основных приложений. Воспользуйтесь приведенными ниже инструкциями, чтобы отладить Microsoft Edge из Visual Studio.

## Запуск Microsoft Edge
Visual Studio создает базовое приложение ASP\.NET и ASP\.NET, запускает веб-сервер, запускает Microsoft EDGE и подключает весь отладчик Visual Studio нажатием одной кнопки. Это позволяет отлаживать JavaScript, работающий в Microsoft EDGE, прямо из интегрированной среды разработки.

### Создание нового веб-приложения ASP.NET

Откройте Visual Studio 2019 и выберите **создать новый проект**. На следующем экране выберите **базовое веб-приложение ASP\.NET** и нажмите кнопку **Далее**.

> ##### Рис. 1  
> Создание нового веб-приложения ASP.NET для ![ создания базового веб-приложения ASP.NET](./media/create-new-project.png)  

Укажите **имя проекта** для нового проекта и нажмите кнопку **создать**. В этом примере в качестве шаблона, в котором показано, как интегрировать метод **реагируют. js** с основным приложением ASP.NET, выберите команду **создать**.

### Запуск Microsoft Edge из Visual Studio

После создания проекта откройте приложение **ClientApp/src/компоненты/Counter. js**. Теперь назовите Visual Studio для отладки JavaScript, выбрав раскрывающийся список рядом с кнопкой " **воспроизвести** зеленый" и **IIS Express**. 

> ##### Рисунок 2  
> Раскрывающийся список рядом с кнопкой « **воспроизвести** зеленый» и **IIS Express** 
> ![ рядом с кнопкой «воспроизвести зеленый» и IIS Express](./media/vs-dropdown.png)  

Нажмите кнопку **Отладка скриптов** и выберите пункт **включена**.

> ##### Рисунок3  
> Включение отладки сценариев в Visual Studio ![ включить отладку сценариев в Visual Studio](./media/enable-script-debugging.png)  

В том же раскрывающемся меню выберите пункт **веб-браузер** и щелкните канал предварительного просмотра Microsoft EDGE, на который вы хотите запустить Visual Studio: Microsoft Edge Канарские, dev или Beta. Если вы еще не сделали этого, перейдите на [эту страницу](https://www.microsoftedgeinsider.com/download) , чтобы установить каналы предварительной версии Microsoft Edge.

> ##### Рисунок4  
> Выберите канал предварительной версии Microsoft EDGE, который вы хотите запустить в Visual Studio, и ![ выберите канал предварительной версии Microsoft EDGE, который вы хотите запустить в Visual Studio.](./media/set-web-browser.png)  

> [!NOTE]
> Если вы выбрали Microsoft EDGE (EdgeHTML), Visual Studio запустит ее вместо Microsoft EDGE (Chromium). [Установите каналы предварительной версии Microsoft Edge](https://www.microsoftedgeinsider.com/download) и выберите их или убедитесь, что версия Microsoft EDGE, установленная на вашем компьютере, — Microsoft EDGE (Chromium), а не Microsoft EDGE (EdgeHTML).

Теперь, когда Visual Studio настроено правильно, нажмите зеленую кнопку **воспроизведения** . Visual Studio будет создавать приложение, запускать веб-сервер, запускать Microsoft EDGE и переходить к `https://localhost:44362/` любому порту, указанному в **launchSettings. JSON**.

> ##### Рисунок 5  
> Microsoft EDGE, запущенный из Visual Studio ![ Microsoft EDGE, запущенный из Visual Studio](./media/edge-launch.png)  

### Отладка JavaScript, выполняемая в Microsoft Edge

Вернитесь в Visual Studio. В разделе **Counter. js**установите точку останова в строке 13, щелкнув внутреннее поле рядом с этой строкой.

> ##### Рисунок6
> Установка точки останова в Visual Studio с помощью переплета рядом с строкой 13 в разделе **Counter. js** 
> ![ Установка точки останова в Visual Studio путем нажатия переплета рядом с строкой 13 в поле counter. js](./media/set-breakpoint.png)  

Теперь переключитесь обратно на экземпляр Microsoft EDGE, на котором запущен Visual Studio. Щелкните **Счетчик** в NavMenu в левой части страницы. Теперь нажмите кнопку **увеличить**.

> ##### Рисунок7
> Страница счетчика в веб-приложении ASP.NET Core ![](./media/edge-counter.png)  

Отладчик JavaScript в Visual Studio будет заключаться в точке останова, заданной в **Counter. js**. Visual Studio теперь приостанавливает выполнение JavaScript, запущенное в Microsoft EDGE, и вы можете пошагово прокручивать сценарий по строкам.

> ##### Рисунок8
> Visual Studio приостанавливает JavaScript, работающий в Microsoft EDGE, в ![ Visual Studio приостанавливает JavaScript, работающий в Microsoft Edge](./media/hit-breakpoint.png)  

Этот пример является незначительным демонстрацией функциональных возможностей, доступных в Visual Studio. Узнайте больше о том, что можно сделать в Visual Studio 2019, прочитав [документацию](https://docs.microsoft.com/visualstudio/windows/?view=vs-2019).

## Присоединиться к Microsoft Edge
В предыдущем рабочем процессе Visual Studio запускает Microsoft Edge. С помощью этого рабочего процесса вы сможете присоединить отладчик Visual Studio к уже запущенному экземпляру Microsoft Edge. 

Прежде всего убедитесь, что у вас нет запущенных экземпляров Microsoft Edge. Теперь в терминале выполните следующую команду:

```console
start msedge –remote-debugging-port=9222
```

В Visual Studio откройте меню **Отладка** и выберите команду **присоединиться к процессу** или нажмите клавишу `Ctrl`  +  `Alt`  +  `P` .

> ##### Рисунок9
> Выбор пункта " **присоединиться к процессу** " в Visual Studio с помощью ![ команды * * присоединиться к процессу * * в Visual Studio](./media/attach-to-process.png)  

В диалоговом окне **присоединиться к процессу** настройте **тип подключения** на HTTP **-протокол WebSocket (без проверки подлинности)**. В текстовом поле **подключить конечный объект** введите `http://localhost:9222/` и нажмите клавишу `Enter` . В диалоговом окне " **присоединиться к процессу** " должен отобразиться список открытых вкладок, указанных в Microsoft Edge.

> ##### Рисунок 10
> Настройка диалогового окна " **присоединиться к процессу** " в Visual Studio ![ Настройка диалогового окна "присоединиться к процессу" в Visual Studio](./media/attach-to-process-dialog.png)  

Нажмите кнопку **выбрать...** и проверьте **JavaScript (Microsoft Edge – Chromium)**. Вы можете добавить вкладки, перейти к новым вкладкам и закрыть вкладки и увидеть изменения, которые отображаются в диалоговом окне " **присоединиться к процессу** ", нажав кнопку " **Обновить** ". Выберите вкладку, которую вы хотите отладить, и нажмите кнопку **прикрепить**.

Отладчик Visual Studio теперь присоединен к Microsoft Edge! Вы можете приостановить выполнение JavaScript, установить точки останова и просмотреть `console.log()` инструкции прямо в окне вывода отладочных данных в Visual Studio.

## Отзыв
Мы рады узнать больше о том, как работать с JavaScript в Visual Studio! Отправьте нам отзыв, щелкнув значок **обратной связи** в Visual Studio или выбрав [@VisualStudio и @EdgeDevTools](https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools).

> ##### Рисунок11
> Значок **обратной связи** в Visual Studio ![ , значок обратной связи в Visual Studio](./media/feedback-icon.png)  
