---
title: Справочник по API консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601756"
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





# Справочник по API консоли   

  

Используйте методы API консоли для записи сообщений на консоль из JavaScript.  В разделе Начало [работы с сообщениями журнала на консоли можно][DevtoolsConsoleLog] ознакомиться с интерактивным введением в раздел.  Ознакомьтесь со [справочными материалами API для консольных программ] [DevtoolConsoleUtilities] , если вы ищете удобные методы, такие как `debug()` или `monitorEvents()` доступные только на консоли.  

## затребованного  

```javascript
console.assert(expression, object)
```

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

При вычислении выводит на консоль [сообщение об ошибке](#error) `expression` `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### Рис. 1  
> Результат `console.assert()` примера  
> ![Результат примера Console. Assert ()][ImageAssert]  

## Сброс  

```javascript
console.clear()
```

Очищает консоль.  

```javascript
console.clear();  
```  

Если включен [протокол Preserve][DevtoolsConsoleReferenceLevel] , метод [clear](#clear) отключен.  

Дополнительные сведения: [Очистка консоли][DevtoolsConsoleReferenceClear]  

## счет  

```javascript
console.count([label])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Записывает количество вызовов метода [Count](#count) в той же строке и с тем же `label` .  Для сброса счетчика используйте метод [countReset](#countreset) .  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### Рисунок 2  
> Результат `console.count()` примера  
> ![Результат примера Console. Count ()][ImageCount]  

## countReset  

```javascript
console.countReset([label])
```  

Сбрасывает число.  

```javascript
console.countReset();
console.countReset('coffee');
```  

## отладка  

```javascript
console.debug(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Идентичен методу [log](#log) .  

```javascript
console.debug('debug');  
```  

> ##### Рисунок3  
> Результат `console.debug()` примера  
> ![Результат примера Console. Debug ()][ImageDebug]  

## dir  

```javascript
console.dir(object)
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Печатает представление JSON указанного объекта.  

```javascript
console.dir(document.head);
```  

> ##### Рисунок4  
> Результат `console.dir()` примера  
> ![Результат примера Console. dir ()][ImageDir]  

## dirxml  

```javascript
console.dirxml(node)
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Печатает XML-представление потомков `node` .  

```javascript
console.dirxml(document);
```  

> ##### Рисунок 5  
> Результат `console.dirxml()` примера  
> ![Результат примера Console. DirXML ()][ImageDirXml]  

## ошибка  

```javascript
console.error(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Error`  

Выводит на `object` консоль сообщение об ошибке, форматирует его как ошибку и включает трассировку стека.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### Рисунок6  
> Результат `console.error()` примера  
> ![Результат примера Console. Error ()][ImageError]  

## группа  

```javascript
console.group(label)
```  

Визуально группирует сообщения, пока не будет использован метод [groupEnd](#groupend) .  Используйте метод [groupCollapsed](#groupcollapsed) , чтобы свернуть группу при первом входе в систему на консоли.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### Рисунок7  
> Результат `console.group()` примера  
> ![Результат примера Console. Group ()][ImageGroup]  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

То же, что и в методе [log](#log) , за исключением того, что группа изначально свернута при входе в систему на консоли.  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Прекращение визуальной группировки сообщений.  Просмотрите метод [группировки](#group) .  

## "Сведения"  

```javascript
console.info(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Идентичен методу [log](#log) .  

```javascript
console.info('info');
```  

> ##### Рисунок8  
> Результат `console.info()` примера  
> ![Результат примера console.info ()][ImageInfo]  

## выходе  

```javascript
console.log(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Вывод на консоль сообщения.  

```javascript
console.log('log');
```  

> ##### Рисунок9  
> Результат `console.log()` примера  
> ![Результат примера Console. log ()][ImageLog]  

## таблич  

```javascript
console.table(array)
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Заносит в журнал массив объектов в виде таблицы.  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

> ##### Рисунок 10  
> Результат `console.table()` примера  
> ![Пример использования Console. Table ()][ImageTable]  

## time  

```javascript
console.time([label])
```  

Запуск нового таймера.  Используйте метод [timeEnd](#timeend) , чтобы остановить таймер и напечатать время, затраченное на консоль.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### Рисунок11  
> Результат `console.time()` примера  
> ![Результат примера Console. Time ()][ImageTime]  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Останавливает таймер.  Просмотрите метод [time (время](#time) ).  

## событий  

```javascript
console.trace()
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Выводит на консоль трассировку стека.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### Рисунок12  
> Результат `console.trace()` примера  
> ![Результат примера Console. Trace ()][ImageTrace]  

## оповещает  

```javascript
console.warn(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Warning`  

Вывод на консоль предупреждения.  

```javascript
console.warn('warn');
```  

> ##### Рисунок13  
> Результат `console.warn()` примера  
> ![Результат примера Console. warn ()][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Рисунок 1: результат примера Console. Assert ()"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Рисунок 2: результат примера Console. Count ()"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Рисунок 3: результат примера Console. Debug ()"  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Рисунок 4: результат примера Console. dir ()"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Рисунок 5: результат примера Console. DirXML ()"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Рисунок 6: результат примера Console. Error ()"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Рисунок 7: результат примера Console. Group ()"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Рисунок 8: результат примера console.info ()"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Рисунок 9: результат примера Console. log ()"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Рисунок 10: результат примера Console. Table ()"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Рисунок 11: результат примера Console. Time ()"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Рисунок 12: результат примера Console. Trace ()"  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Рисунок 13: результат примера Console. warn ()"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Удаление ссылки на консоль консоли"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Сохранение сообщений на странице с загрузкой на консоли"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтрация по уровню журнала — Справочник по консоли"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/api) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
