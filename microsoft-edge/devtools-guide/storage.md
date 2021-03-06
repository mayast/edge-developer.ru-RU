---
description: Проверка веб-хранилища, IndexedDB, файлов cookie и кэша запросов и ответов с помощью панели хранилища
title: DevTools — хранилище
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, веб-хранилище, локальное хранилище, хранилище сеанса, IndexedDB, файлы cookie, сотрудник службы, кэш
ms.custom: seodec18
ms.openlocfilehash: 8de6e1f90f86fa09b116646918c6be1d8cfb0a72
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571722"
---
# Хранилище

С помощью панели " **хранилище** " можно проверять различные данные, хранящиеся на локальном компьютере, и управлять ими, в том числе:

 - Пары ключей и значений в [веб-хранилище](#local-and-session-storage-managers) (*Локальное* и хранилище *сеансов* )
 - Структурированные данные с [индексированной базой](#indexeddb-manager) данных
 - [Файлы cookie](#cookies-list) для домена
 - [Кэш](#cache-manager) (пары запросов и ответов) для отладки рабочего процесса службы

Разверните любую из этих категорий и щелкните дочерний элемент, чтобы открыть вкладку "Диспетчер ресурсов".

## Локальные и Диспетчеры хранилища сеанса

С помощью *локального диспетчера хранилища* и *диспетчера хранилища сеанса* просмотрите веб-хранилище для своей страницы и управляйте им. 

Папки " **Локальное хранилище** " и " **хранилище сеанса** " в [*средстве выбора ресурсов*](./debugger.md#resource-picker) панели хранилища выводят список источников для страницы. При выборе одной из этих рамок открывается редактируемая таблица текущих пар ключ-значение, заданных с помощью [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) или [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), соответственно (и/или непосредственно из [списка хранилищ](#storage-list)DevTools).

![Диспетчер DevTools cookies](./media/storage_web_storage.png)

На вкладках *Локальное хранилище* и *хранилище сеансов* можно выполнить указанные ниже действия.

 - **Refresh** ( `Ctrl+F5` ) [список хранилищ](#cookies-list) для просмотра текущего набора пар "ключ-значение" для данного домена. (Список не обновляется автоматически при обновлении сценария.)
 - **Имитация ограничения размера хранилища** для веб-хранилища Microsoft Edge. У каждого домена и дочернего домена есть своя область хранения, но есть Объединенные ограничения.
    - **Дочерние домены:** до 5 МБ свободного места
    - **Домены:** до 10 МБ свободного места
    - **Общее количество для всех доменов:** до 50 МБ свободного места

   Хранилище сеанса очищается, как только вкладка последнего браузера, ссылающаяся на ее источник, будет закрыта. Записи локального хранилища остаются неопределенными до тех пор, пока они не будут очищены с помощью страницы вручную или пользователем:

   **Параметры**  >  **Очистка данных браузера**  >  **Файлы cookie и сохраненные данные веб-сайтов**

![Очистка обзора данных на панели "параметры Microsoft Edge"](./media/settings_clear_browsing_data.png)

### Список хранилищ

В таблице *список хранилищ* можно выполнить указанные ниже действия.

 - **Проверьте и отсортируйте** пары "ключ-значение", щелкнув любое имя столбца в таблице.
 - **Измените** *ключ* и *значение* существующего элемента, щелкнув ячейку.
 - **Удалить** ( `Del` ). в контекстном меню щелкните правой кнопкой мыши пункт *удалить элемент*.
 - **Добавьте** новую пару ключ/значение, щелкнув пустую строку в нижней части таблицы.


### Горячие

| Действие              | Появивше      |
|:--------------------|:--------------|
| Обновить             | `Ctrl` + `F5` |
| Удалить элемент         | `Del`         |
| Копирование выделенных элементов | `Ctrl` + `C`  |
| Выделить все          | `Ctrl` + `A`  |


## Менеджер IndexedDB

С помощью вкладки **IndexedDB** можно проверять структурированные данные, хранящиеся на клиентском компьютере, и управлять ими. В частности, вы можете проверить или отсортировать и обновить хранилища объектов и индексы, а также удалить отдельные записи ключа.

> [!TIP]
> Вы можете использовать нашу демонстрацию [микшера звука](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) для тестирования *IndexedDB Manager* в Microsoft Edge DevTools.

Чтобы удалить все данные IndexedDB, сохраненные для текущего пользователя в Microsoft EDGE, используйте меню " *Параметры* Microsoft Edge".

**...** >  **Параметры**  >  **Очистка данных браузера**  >  **Файлы cookie и сохраненные данные веб-сайтов**

Папка **IndexedDB** в [*средстве выбора ресурсов*](./debugger.md#resource-picker) отладчика отображает список источников происхождения из ресурсов, загруженных страницей. Любые базы данных IndexedDB (IDB) будут указаны в исходном виде, а также их хранилища объектов. 

![Менеджер DevTools IndexedDB](./media/storage_indexeddb.png)

### Панель инструментов IndexedDB

На панели инструментов *IndexedDB* вы можете:

 - **Refresh** ( `Ctrl+F5` ) для просмотра текущих записей в хранилище объектов или индексе базы данных. После внесения изменений в базу данных руководитель IndexedDB не будет автоматически обновляться.

### Список записей в хранилище объектов

Из *хранилища объектов* или таблицы *индексов* можно выполнить указанные ниже действия.

 - Для **проверки и сортировки** пар "ключ-значение" щелкните любое имя столбца в таблице.
 - **Refresh** ( `Ctrl+F5` )
 - **Удалить элемент** ( `Del` ), чтобы удалить выбранный элемент из хранилища объектов или предметного указателя. Вы также можете сделать это с помощью [контекстного меню](#context-menu) правой кнопкой мыши, а затем *удалить элемент*.
 - **Копировать выделенные элементы** ( `Ctrl+C` ), чтобы скопировать выделенный элемент в буфер обмена. Вы также можете сделать это с помощью [контекстного меню](#context-menu) правой кнопкой мыши и *выбрать команду Копировать выбранный элемент*.
 - **Выберите все** ( `Ctrl+A` ), чтобы выбрать все записи в хранилище объектов или предметном указателе. Вы также можете сделать это в [контекстном меню](#context-menu) правой кнопкой мыши и *выбрать пункт Все*.

Столбцы в *хранилище объектов* или таблице *индексов* можно сортировать:

Столбец | Описание
:------------ | :-------------
Раздел | Имя пары "ключ-значение" (то же, что и *первичный ключ*) при итерации по хранилищу объектов; Имя ключа индекса (Текущая клавиша курсора) при итерации по индексу.
Первичный ключ | Имя пары "ключ-значение" (Дополнительные сведения о [ключах](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)IDB см *MDN в веб-документах* .)
Значение | Значение пары "ключ-значение"

Узнайте больше о [концепциях и использовании](https://developer.mozilla.org/docs/Web/API/IndexedDB_API) *MDN в веб-документах* для IndexedDB.

### Контекстное меню

В дополнение к [панели инструментов *IndexedDB* ](#indexeddb-toolbar)можно также управлять данными в хранилищах объектов или индексами в **контекстном меню** и/или с помощью сочетаний [клавиш](#shortcuts).

### Горячие

Действие | Появивше
:------------ | :-------------
Обновить | `Ctrl` + `F5`
Удаление пары "ключ-значение" | `Del`
Копирование выделенных элементов | `Ctrl` + `C`
Выделить все | `Ctrl` + `A`

## Диспетчер cookie-файлов

Используйте *Диспетчер файлов cookie* для проверки и управления файлами cookie для данного домена. 

В папке **cookies** в [*средстве выбора ресурсов*](./debugger.md#resource-picker) отладчика отображается список происхождения из ресурсов, загруженных страницей. При выборе одного из этих фреймов открывается таблица, представляющая текущие файлы cookie, заданные заголовком [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) или сценарием с помощью [файла Document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).

![Диспетчер DevTools cookies](./media/storage_cookies.png)

На панели инструментов вкладки " *cookie* " можно выполнять следующие действия:

 - **Обновите** ( `Ctrl+F5` ) [список cookies](#cookies-list) , чтобы просмотреть текущий набор cookie-файлов для данного домена. (Список не обновляется автоматически).
 - **Удалите все файлы cookie** ( `Ctrl+Shift+Del` ) (сеанс и постоянный) для пути к текущей странице.
 - **Удалите все cookie-файлы сеанса** ( `Ctrl+Del` ) для пути к текущей странице.

Для полного удаления *списка cookie*-файлов вам может потребоваться **удалить все cookie-файлы для домена** на панели инструментов " [**сеть**](./network.md#toolbar) ".

### Список cookie-файлов

В таблице *cookie List* можно выполнить указанные ниже действия.

 - **Проанализировать и отсортировать** файлы cookie, щелкнув любое имя столбца в таблице.
 - **Измените** *имя* и *значение* существующего файла cookie, щелкнув ячейку.
 - **Удалить** ( `Del` ) файл cookie из [контекстного меню](#context-menu) правой кнопкой мыши *удалить файл cookie*.
 - **Добавьте** новый файл cookie сеанса для указанного *домена или пути* , щелкнув пустую строку в нижней части таблицы. Это работает только для cookie-файлов сеансов. постоянные файлы cookie (с определенными датами истечения срока действия) должны быть установлены с традиционными методами. Значения *домена* и *пути* автоматически заполняются в соответствии с расположением страницы.

Столбцы в *списке cookie-файлов* доступны для сортировки:

Столбец | Описание
:------------ | :-------------
Name | Имя cookie-файла
Значение | Значение cookie-файла
Домен | Имя узла cookie-файла (может быть пустым)
Путь | URL-путь для файла cookie (может быть пустым)
Срок действия истекает | Максимальное время существования cookie в качестве метки времени HTTP-даты. Если `Expires` значение не `Max-Age` задано, запись считается файлом cookie *сеанса* .
Только HTTP | Указывает, был ли для файла cookie задана `HttpOnly` директива, указывающая на то, что он недоступен из JavaScript
Защита | Указывает, был ли в качестве файла cookie указана `Secure` директива, указывающая на то, что она будет отправлена на сервер из запроса с помощью SSL и протокола HTTPS.

Дополнительные сведения о свойствах файлов cookie вы увидите в разделе **MDN Web doc** [Set-cookies](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) .

### Контекстное меню

Помимо вкладки *cookies* , вы [toolbar](#cookies-manager)также можете управлять файлами cookie с помощью **контекстного меню** и (или) сочетаний [клавиш](#shortcuts).

### Горячие

| Действие                     | Появивше                 |
|:---------------------------|:-------------------------|
| Обновить                    | `Ctrl` + `F5`            |
| Удаление файла cookie              | `Del`                    |
| Удаление всех файлов cookie         | `Ctrl` + `Shift` + `Del` |
| Удаление всех файлов cookie сеанса | `Ctrl` + `Del`           |
| Копирование выделенных элементов        | `Ctrl` + `C`             |
| Выделить все                 | `Ctrl` + `A`             |

### Диспетчер кэша

При нажатии на определенную запись кэша откроется диспетчер **кэша** рабочих процессов служб, в котором можно проверить и при необходимости удалить записи кэша (пары ключ-значение для*запроса* и *ответа* ).

![Диспетчер кэша](./media/storage_cache.png)

### Горячие

#### Диспетчер кэша

| Действие              | Появивше      |
|:--------------------|:--------------|
| Обновить             | `Ctrl` + `F5` |
| Удалить элемент         | `Del`         |
| Копирование выделенных элементов | `Ctrl` + `C`  |
| Выделить все          | `Ctrl` + `A`  |
