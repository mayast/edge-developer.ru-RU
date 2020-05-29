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





# Открыть Microsoft Edge DevTools   



Существует множество способов открыть Microsoft Edge DevTools, так как разным пользователям нужен быстрый доступ к разным частям пользовательского интерфейса DevTools.  

## Открытие панели "элементы" для проверки модели DOM или CSS   

Если вы хотите проверить стили или атрибуты узла DOM, щелкните элемент правой кнопкой мыши и выберите команду **проверить**.  

> ##### Рис. 1  
> Параметр **проверки**  
> ![Параметр проверки][ImageInspectOption]  

Или нажмите клавиши `Control` + `Shift` + `C` \ (Windows \) или `Command` + `Option` + `C` \ (macOS \).  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Открытие панели консоли для просмотра сообщений, занесенных в журнал, или запуск JavaScript   

Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \), чтобы перейти прямо в панель **консоли** .  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Открытие последней открытой панели   

Нажмите клавиши `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  

## Открытие DevTools в главном меню Microsoft Edge  

Нажмите кнопку **Параметры и выберите другие \ (Alt + F \)** `...` , а затем — **Дополнительные инструменты**  >  **разработчика**.  

> ##### Рисунок 2  
> Открытие DevTools в главном меню Microsoft Edge  
> ![Открытие DevTools в главном меню Microsoft Edge][ImageOpenFromMain]  

## Автоматическое открытие DevTools на каждой новой вкладке   

Откройте Microsoft Edge из командной строки и передайте `--auto-open-devtools-for-tabs` флаг.  

Windows \ (CMD \):  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

Windows \ (PowerShell \):  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

MacOS  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/open) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
