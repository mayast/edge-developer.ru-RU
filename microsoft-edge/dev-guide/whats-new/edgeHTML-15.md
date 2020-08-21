---
description: В этом руководстве представлен обзор функций и стандартов для разработчиков, включенных в Microsoft EdgeHTML 15.
title: Новые функции и API в EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.custom: seodec18
ms.openlocfilehash: 4febe4be1fce29207de7a57b61d96eae0a5c02ab
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941921"
---
# Новые возможности В EdgeHTML 15  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Ниже перечислены изменения, публикуемые в текущем выпуске платформы Microsoft Edge с [обновлением Windows 10 Creators Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) \(04.04.2017, сборка 15063\).  Обзор изменений общего браузера Microsoft Edge см. в статье "Новые возможности [Microsoft Edge в Windows 10 Creators Update".](https://blogs.windows.com/msedgedev/2017/04/11)  

Сведения о последующих сборках Windows Insider Preview см. в статье ["Новые возможности Microsoft EdgeHTML".](../whats-new.md)  

Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_15](./edgehtml-15.md)  

## Новые возможности  

### Настраиваемые свойства CSS  

Теперь В Microsoft Edge теперь поддерживаются пользовательские [свойства CSS CSS](https://drafts.csswg.org/css-variables)— .k.a CSS.  Переменные CSS позволяют создавать пользовательские свойства CSS, которые можно повторно использовать во всех таблицах стилей для уменьшения количества повторяющихся данных, например повторяющихся цветов.  Использование переменных CSS очень просто:  

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Эблемная дебет  

EdgeHTML 15 представляет спецификацию [API пересечения через API-интерфейс OBserver.](https://w3c.github.io/IntersectionObserver)  API пересечения окна сервера Observer Observer позволяет асинхронно относительно модулям запросов к положению и видимости элементов DOM относительно других элементов или глобального представления.  Это позволит избежать необходимости для пользовательского дорогостоящего кода путем создания метода, которые эффективнее уведомляют элементы в режиме просмотра.  

### JavaScript  

Оптимизация производительности учитывают удобство воспроизведения центра с пограничным модулем Chakra JavaScript.  В обновлении Windows 10 Creators Update камера сохраняет память, перекладывая функции и оптимизируя аргументы наушников и повышает производительность минифрованного кода.  

Кроме того, в браузере EdgeHTML 15 представлены следующие предварительные версии функций:  

#### Экспертные функции JavaScript  

Доступно с `about:flags`  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) \([демонстрация](https://webassembly.org/demo)\)  
*   [Общие память и атоминции](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

Более подробные сведения о том, как производить [работу JavaScript, WebAssembly и "Общий](https://blogs.windows.com/msedgedev/2017/04/20) доступ" в Microsoft Edge, чтобы получить дополнительные сведения.  

### API запроса оплаты  

[API запросов платежа теперь поддерживается,](https://w3.org/TR/payment-request) что упрощенная оформление заказа и оплаты в Интернете на компьютерах и телефонах с Windows 10.  Этот API позволяет Microsoft Edge выступать в качестве промежуточного метода между методами, потребителями и методами оплаты \(например, кредитные карты\), которые хранятся в облаке.  Дополнительные сведения об API запросов о платежесм см. в [упрощенном веб-платеже: знакомство с API](https://blogs.windows.com/msedgedev/2016/12/15) запросов о платежах и руководству по [созданию запросов](/microsoft-edge/dev-guide/device/payment-request-api) платежей по платформе.  

### TCP Fast Open (TFO)  
TCP — это функция, сокращающая количество круговых путей, необходимых для открытия соединения TCP, повышая производительность сети.  Дополнительные сведения см. в статье "Создание более раннего и безопасного веб-сайта" [с помощью TCP С ранним открытием TCP.](https://blogs.windows.com/msedgedev/2016/06/15)  Из-за различий в различных топологиях сети эта функция по умолчанию не включена в Microsoft Edge.  Чтобы включить ее, `about:flags` введите в адресную строку и установите **флажок "Включить поддержку TCP раннего доступа"** в разделе **"Сетевой доступ".**  

### Поддержка кодеков веб-кодеков веб-кодеков WebRTC и кодеков rTC  

EdgeHTML 15 поддерживает часть API WebRTC 1.0 для взаимодействия с приложениями, созданными в более ранних версиях API-браузера W3C WebRTC-PCI Circa 2015.  Дополнительные сведения см. в [справке WebRTC.](/previous-versions//mt806139(v=vs.85))  

Чтобы использовать преимущества наших более сложных функций для одноранговых и видеосвязи, мы рекомендуем [использовать API-музыку связи](https://ortc.org)в режиме реального времени.  API ORTC лучше подходит для ситуаций, когда вы хотите настроить голосовые и видеозвонки, а также напрямую контролировать отдельные транспортные, отправитель и объекты приемадления.  

Microsoft Edge поддерживает видео h.264/AVC и VP8 с ORTC и WebRTC 1.0, обеспечивает поддержку обоих типов кодеков: [abs-send-time,](https://webrtc.org/experiments/rtp-hdrext/abs-send-time) [hog-remb, glob-remb,](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03) [отзывы потери рисунков и стандартную среднюю фильтрацию](https://tools.ietf.org/html/rfc4585) [RTP.](https://tools.ietf.org/html/rfc4588)  

Дополнительные сведения см. в статье Общие сведения о [WebRTC 1.0](https://blogs.windows.com/msedgedev/2017/01/31)и взаимодействии в реальном времени в Microsoft Edge.  

### WebVR  

В Microsoft Edge теперь [поддерживается WebVR](https://immersive-web.github.io/webxr)— экспериментальный API, подключающий демонстрацию мониторинга Windows Mixed Reality и Microsoft Edge.  Это подключение позволяет работать с контентом VR на веб-сайте, то есть иммерсивные виртуальные возможности виртуальной оптимизации больше не ограничиваются классическими приложениями.  

Виртуальная реальность в Microsoft Edge оснащено Веб-GL, API JavaScript для отрисовки трехмерных и двухмерных графики.  Поддерживаются веб-приложения и приложения, созданные с помощью библиотек WebGL, например babylonJS.  После подключения WebVR отправляет визуальные элементы, соответствующие положению и датчику.  API WebVR также поддерживает спектры, благодаря расширению [для игры.](../dom/gamepad-api.md)  По умолчанию ЭтоA Включен, поэтому не тратить переключение.  

Дополнительные сведения [см. в справке API веб-браузера](/previous-versions//mt806281(v=vs.85)) [и API игры.](https://developer.mozilla.org/docs/Web/API/Gamepad_API)  

 > [!NOTE] 
 > Так как речь WebVR еще находится в разработке, реализация Microsoft Edge может измениться ниже строки ниже.  

## Обновленные компоненты  

### Политика безопасности содержимого (уровень 2)  

Сайты, уже использующие облачные службы Облака CSP 1, следует и дальше работать со службой поддержки Microsoft Edge для CSP 2, однако лучше всего переключать направляемые сценарии, которые нагрузят нагрузку на `frame-src` новую `child-src` прямую проверку вашего сайта.  \(в соглашении CSP 3, больше не будет применяться к рабочим `frame-src` файлам.\) Облачных служб облачных служб:  

:::row:::
   :::column span="1":::
      Новые практические важные  
   :::column-end:::
   :::column span="2":::
      `base-uri`, `child-src` `form-action` `frame-ancestors` и `plugin-types` .  Дополнительные [сведения см. в поддерживаемых веб-каналах](../security/content-security-policy.md) Майкрософт.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Поддержка работников  
   :::column-end:::
   :::column span="2":::
      Сценарии фона регулируются собственной политикой, отлично от политики загрузки документов.  Как и при использовании узлов ных документов, вы можете настроить облачную группу для работника в заголовке ответа.  Кроме того, новая возможность в функции облачных решений 2 также влияет на создание потоков. `allow-scripts` `allow-same-origin` `sandbox`  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Встроенные сценарии и стили  
   :::column-end:::
   :::column span="2":::
      С помощью встроенных сценариев и стилей можно использовать встроенные сценарии и блоки стилей, предоставляя нумерацию и хэш-код в качестве белого механизма.  Nonces — это случайные базовые значения, созданные на каждой странице, загружаемые как в политике CSP, так и в тегах сценариев на странице.  Когда страница динамического призагрузки, сервер создает его неоглавленное значение, вставляет его в NonceToken на страницу, и обязвивает ее в заголовок HTTP security Policy (HTTP).  Хэш-значения формируются статическими значениями: \(четырьмя, тока-тихифами\) из содержимого элемента или элемента, указанного в `<script>` `<style>` политике `script-src` `style-src` облачных процессов.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Отчеты об нарушении облачных оболочки  
   :::column-end:::
   :::column span="2":::
      Новое событие `SecurityPolicyViolationEvent` теперь достиглось нарушениями Упростить совершение облачных решений.  Старый механизм создания отчетов CSP по-прежнему `report-uri` поддерживается.  В отчеты о нарушении часто добавлено несколько новых полей, `effectiveDirective` включая \(нарушена нарушение\), `statusCode` \(программа HTTP response code\) `sourceFile` \(URL-адрес ресурса, находящегося в оперативной папке\) `lineNumber` `columnNumber` и.  
   :::column-end:::
:::row-end:::  

### Проверка подлинности в Интернете  

Поддержка Microsoft Edge для выделения [API веб-проверки подлинности с](../device/web-authentication.md) [помощью радиальной](https://www.microsoft.com/windows/comprehensive-security) силы Windows Hello обновлена следующими изменениями:  

*   Первонаправленная реализация API проверки подлинности по интернет-интерфейсу, впервые реализованного в [браузере Edge 14](https://blogs.windows.com/msedgedev/2016/08/04) \(windows 10 юбилейное обновление Windows 10, сборка 10240, 7.07.2016\) был передано через префикс \(интерфейс [MSCredentials\).](/previous-versions//mt697639(v=vs.85))  Хотя эти API доступны в среде EdgeHTML 15, теперь они теперь не предусмотрены в изолированных средах Инициаторов, которые определены более непрефиксированными, и скорее всего, будут продолжать изменяться, поэтому их можно продолжать изменять, как в составе стандартов реферализации. [recent snapshot](https://w3.org/TR/2016/WD-webauthn-20160928)  

*   Последняя реализация Microsoft Edge по умолчанию отключена и доставлена за флаг \(введите в адресной строке символ \(тип в адресной `about:flags` строке для включения функции\).  

*   В Microsoft Edge пока нет внешних учетных данных, таких как USB-ключи или Bluetooth устройства.  Текущий API ограничен только для внедренных учетных данных, хранящихся в TPM.  Программное обеспечение используется, если TPM недоступен на устройстве.  

*   В настоящее время вошедший в учетную запись пользователя Windows должен быть настроен для поддержки ПИН-кода и предпочтительно лица или отпечатков пальцами.  Это необходимо для проверки подлинности Windows проверки подлинности доступа к телевизору.  

*   Из [стандартных](https://w3.org/TR/webauthn/#extension-predef) расширений, описанных в скобке, Microsoft Edge поддерживает [только FIDO AppId](https://w3.org/TR/webauthn/#extension-appid) \( `webauthn_txAuthSimple` \).  

*  В `timeoutSeconds` настоящее время эта возможность не вычисляется  

### WebDriver  

EdgeHTML 15 предлагает удобное обновление WebDriver, включая поддержку запасной строки командной строки и новых конечных точках команд:  

| Метод | URI Template | Команда |  
|:--- |:---  |:--- |    
| POST | /session id}/alert/accept | [Принять оповещение](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert) |  
| POST | /session id}/ alert/dismiss | [Отклонить оповещение](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert) |  
| GET | /session id}/alert/text | [Получение оповещения](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text) |  
| POST | /session id}/alert/text | [Отправка оповещения](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text) |  
| POST | /session id}/execute/async | [Запуск сценария ASync](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script) |  
| POST | /session id}/execute/sync | [Сценарий](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script) |  
| GET | /session id}/window | [Получить маркер окна](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle) |  
| GET | /session/{session id}/window/handles | [Получение маркеров окон](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles) |  

Дополнительные сведения и состояние других функций WebDriver см. в [веб-диспетчере веб-диспетчера.](../../webdriver.md)  

## Новый API в Microsoft EdgeHTML 15  

Ниже приведен полный список новых aPI в Microsoft EdgeHTML 15.  Они указаны в `[interface name].[api name]` формате.  

<iframe height='582' scrolling='no' title='Новый API EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. статью "Перо <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> нового EdgeHTML15" </a> для приложений @MicrosoftEdgeDocumentation Microsoft Edge <a href='http://codepen.io/MicrosoftEdgeDocumentation'> </a> (@MicrosoftEdgeDocumentation) на <a href='http://codepen.io'> коде </a> кода.</iframe>  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 12/ Windows сборка 10240 (07.07.2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Windows сборка 10586 (11.11.2015)](./edgehtml-13.md)  

[EdgeHTML 14/ Windows сборка 14393 (8.08.2016)](./edgehtml-14.md)  
