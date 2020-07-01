---
title: Открыть Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 06e547d2d413535a6f14d829d30dc4d7b11ac92b
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844007"
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

Каждая из указанных ниже задач позволяет проверить стили и атрибуты узла DOM.

*   Наведите указатель мыши на элемент, откройте контекстное меню, а затем выберите команду **проверить**.  
*   Нажмите клавиши `Control` + `Shift` + `C` \ (Windows \) или `Command` + `Option` + `C` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-right-click-inspect.msft.png" alt-text="Параметр * * Проверка * *" lightbox="./media/bing-right-click-inspect.msft.png":::
   Параметр **проверки**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Открытие панели консоли  

Каждая из указанных ниже задач позволяет открывать область [консоли][DevToolsConsoleIndex] для просмотра сообщений, занесенных в журнал, или запуска JavaScript.  

*   Чтобы открыть область [консоли][DevToolsConsoleIndex] , выполните указанные ниже действия.  
    
    1.  [Откройте DevTools](#open-microsoft-edge-devtools).  
    1.  Выберите область [консоли][DevToolsConsoleIndex] .  

*   Чтобы перейти прямо в область [консоли][DevToolsConsoleIndex] , нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Открытие предыдущей панели  

Чтобы перейти к предыдущей открытой панели, нажмите клавиши `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  

## Открыть Microsoft Edge DevTools  

Каждая из указанных ниже задач позволяет открыть DevTools.  

*   Чтобы открыть Microsoft Edge DevTools, выполните указанные ниже действия.  
    
    1.  Щелкните `...` значок \ ( **Параметры и** значок "Дополнительно").  
    1.  Нажмите кнопку **другие инструменты**.  
    1.  Выберите **Инструменты разработчика**.  
    
*   Чтобы открыть Microsoft Edge DevTools, нажмите клавиши `F12` или `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Открытие DevTools в главном меню Microsoft Edge" lightbox="./media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Открытие DevTools в главном меню Microsoft Edge  
:::image-end:::  

## Автоматическое открытие DevTools на каждой новой вкладке  

Чтобы автоматически открыть DevTools на каждой новой вкладке, откройте Microsoft Edge из командной строки и передайте `--auto-open-devtools-for-tabs` флаг.  

#### [CMD (Windows)](#tab/cmd-windows/)  

<a id="selenium-tools-install"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-windows/)  

<a id="selenium-tools-install"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [Bash (macOS)](#tab/bash-macos/)  

<a id="selenium-tools-install"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

* * *  

<!-- links -->  

[DevToolsConsoleIndex]: ./console/index.md "Обзор консоли | Документы Microsoft"  
[DevtoolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools — документы Майкрософт"  

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
