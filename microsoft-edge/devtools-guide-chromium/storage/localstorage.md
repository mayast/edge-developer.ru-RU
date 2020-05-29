---
title: Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612013"
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





# Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools   



В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`localStorage`][MDNWindowsLocalStorage] пар "ключ-значение".  

## Просмотр ключей и значений localStorage   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Область **манифеста** отображается по умолчанию.  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifest]  

1.  Разверните меню **Локальное хранилище** .  
    
    > ##### Рисунок 2  
    > В меню " **Локальное хранилище** " отображаются два домена: `https://business.bing.com` и `https://www.bing.com`  
    > ![Меню «локальное хранилище»][ImageLocalStorageMenu]  

1.  Выберите домен, чтобы просмотреть пары "ключ-значение".  
    
    > ##### Рисунок3  
    > `localStorage`Пары "ключ-значение" для `https://www.bing.com` домена  
    > ![LocalStorage пары "ключ-значение" для https://www.bing.com домена][ImageLocalStorage]  

1.  Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.  
    
    > ##### Рисунок4  
    > Просмотр значения `eventLogQueue_Online` ключа  
    > ![Просмотр значения ключа eventLogQueue_Online][ImageLocalStorageViewer]  

## Создание новой `localStorage` пары "ключ-значение"   

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.  
    
    > ##### Рисунок 5  
    > Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.  
    > ![Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.][ImageLocalStorageCreate]  

## Изменение `localStorage` ключей и значений   

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.  
    
    > ##### Рисунок6  
    > Редактирование `localStorage` ключа  
    > ![Редактирование ключа localStorage][ImageLocalStorageEdit]  

## Удаление `localStorage` пар "ключ-значение"   

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Выберите пару "ключ-значение", которую вы хотите удалить.  DevTools выделит ее синей, чтобы показать, что она выбрана.  

1.  Нажмите клавишу `Delete` или выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .  

## Удаление всех `localStorage` пар "ключ-значение" для домена   

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  

1.  Нажмите **Очистить все** ![ Очистить все ][ImageClearIcon] .  

## Взаимодействие с `localStorage` консолью   

Так как вы можете запускать JavaScript на **консоли**, а так как у **консоли** есть доступ к контекстам JavaScript страницы, взаимодействие с `localStorage` **консолью**возможно.  

1.  Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если требуется получить доступ к `localStorage` парам "ключ-значение" домена, отличного от отображаемой страницы.  
    
    > ##### Рисунок7  
    > Изменение контекста JavaScript **консоли**  
    > ![Изменение контекста JavaScript консоли][ImageJSContext]  

1.  Выполняйте `localStorage` выражения на консоли так же, как и в JavaScript.  
    
    > ##### Рисунок8  
    > Взаимодействие с `localStorage` **консолью**  
    > ![Взаимодействие с localStorage из консоли][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Рисунок 2: меню "локальное хранилище""  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Рисунок 3: localStorage пары "ключ-значение" для https://www.bing.com домена"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Рисунок 4: Просмотр значения ключа eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Рис. 5: пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение."  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Рисунок 6: Редактирование ключа localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Рис. 7: изменение контекста JavaScript консоли"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Рисунок 8: взаимодействие с localStorage из консоли"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
