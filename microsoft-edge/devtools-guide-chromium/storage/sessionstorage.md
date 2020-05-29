---
title: Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612083"
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





# Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools   

  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`sessionStorage`][MDNSessionStorage] пар "ключ-значение".  

## Просмотр ключей и значений sessionStorage   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Область **манифеста** отображается по умолчанию.  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifest]  

1.  Разверните меню **хранилище сеанса** .  
    
    > ##### Рисунок 2  
    > Меню « **хранилище сеанса** »  
    > ![Меню «хранилище сеанса»][ImageSessionStorageMenu]  

1.  Выберите домен, чтобы просмотреть пары "ключ-значение".  
    
    > ##### Рисунок3  
    > SessionStorage пары "ключ-значение"  
    > ![Пары "sessionStorage" "ключ-значение"][ImageSessionStorage]  

1.  Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.  
    
    > ##### Рисунок4  
    > Просмотр значения `x-sid` ключа  
    > ![Просмотр значения ключа x-SID][ImageSessionStorageViewer]  

## Создание новой пары "ключ-значение" для sessionStorage   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.  
    
    > ##### Рисунок 5  
    > Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.  
    > ![Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.][ImageSessionStorageCreate]  

## Изменение ключей и значений sessionStorage   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.  
    
    > ##### Рисунок6  
    > Редактирование `sessionStorage` ключа  
    > ![Редактирование ключа sessionStorage][ImageSessionStorageEdit]  

## Удаление пар ключ-значение sessionStorage   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Выберите пару "ключ-значение", которую вы хотите удалить.  DevTools выделит ее синей, чтобы показать, что она выбрана.  

1.  Нажмите клавишу `Delete` или выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .  

## Удаление всех пар ключ-значение sessionStorage для домена   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  

1.  Нажмите **Очистить все** ![ Очистить все ][ImageClearIcon] .  

## Взаимодействие с sessionStorage с помощью консоли   

Так как вы можете запустить JavaScript на **консоли**, и так как **консоль** имеет доступ к контекстам JavaScript на странице, можно взаимодействовать с `sessionStorage` ней из **консоли**.  

1.  Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если вы хотите получить доступ к `sessionStorage` парам "ключ-значение" домена, отличного от страницы, на которой вы являетесь.  
    
    > ##### Рисунок7  
    > Изменение контекста JavaScript **консоли**  
    > ![Изменение контекста JavaScript консоли][ImageJSContext]  

1.  Выполняйте `sessionStorage` выражения на консоли так же, как и в JavaScript.  
    
    > ##### Рисунок8  
    > Взаимодействие с `sessionStorage` **консолью**  
    > ![Взаимодействие с sessionStorage из консоли][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Рисунок 2: меню «хранилище сеанса»"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Рисунок 3: пары "ключ-значение" sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Рисунок 4: Просмотр значения ключа x-SID"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Рис. 5: пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение."  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Рисунок 6: Редактирование ключа sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Рис. 7: изменение контекста JavaScript консоли"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Рисунок 8: взаимодействие с sessionStorage из консоли"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
