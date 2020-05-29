---
ms.assetid: e56172c0-b635-4c02-8e0c-56bf8cb4c164
description: Узнайте, как приступить к работе с веб-дисководом, а также с помощью протокола связи, позволяющего программам и сценариям управлять поведением браузера.
title: EdgeHTML
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, веб-дисковод, Selenium, тестирование
ms.openlocfilehash: 0a6ef78103852234a6b52dfe88e60273cc3bd3d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572866"
---
# EdgeHTML
API веб- [накопителей](https://www.w3.org/TR/webdriver/) W3C — это платформа и независимый от языка интерфейс и протокол проводной связи, позволяющая программам и сценариям управлять поведением браузера.

С помощью этого устройства разработчики могут создавать автоматические тесты, имитирующие взаимодействие с пользователем. Это отличается от модульных тестов JavaScript, поскольку веб-дисковод имеет доступ к функциональным возможностям и сведениям, которые JavaScript запускается в браузере, и может более точно имитировать события пользователей и события на уровне операционной системы. Кроме того, веб-дисковод также может управлять тестированием между несколькими окнами, вкладками и страницами в одном тестовом сеансе.

Чтобы приступить к работе с веб-диском Microsoft EDGE (EdgeHTML), воспользуйтесь приведенными ниже сведениями.

Реализация веб [-дисковода](https://www.w3.org/TR/webdriver/) Microsoft EDGE (EdgeHTML) поддерживает спецификацию и [протоколы](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol) HTTP для обратной совместимости с существующими тестами.

## Начало работы с веб-дисководом для Microsoft EDGE (EdgeHTML)
* Установка Windows 10.
* Скачайте соответствующий сервер [Microsoft](https://developer.microsoft.com/microsoft-edge/tools/webdriver/) для сборки Windows и Microsoft EDGE (EdgeHTML).
* Скачайте выбранную вами языковую привязку веб дисков. [Все привязки языков Selenium поддерживают Microsoft EDGE (EdgeHTML)](https://docs.seleniumhq.org/download/).

> [!NOTE]
> Вы можете найти справку, вопросы о проблемах и запросы функций файла на [веб-сайте Microsoft EDGE (EdgeHTML), которые & поддерживать](https://developer.microsoft.com/microsoft-edge/support/).


## Использование устройства
Чтобы приступить к работе с веб-диском в Microsoft EDGE (EdgeHTML), ознакомьтесь с приведенными ниже примерами.

* [Пример кода C \n](https://gist.github.com/InstyleVII/baf25274c55e891076d5#file-webdriver-cs) для открытия окна браузера, навигации по Bing.com и поиска "веб-дисковода" (GitHub).

## Флаги командной строки сервера для серверного устройства
Список флагов командной строки для сервера.

| Имя    | Описание                                                                                                      | Доступная версия |
|:--------|:-----------------------------------------------------------------------------------------------------------------|:------------------|
| размещать    | IP-адрес узла для использования на сервере для работы с ним (по умолчанию: localhost)                                                     | 14393             |
| порт    | Порт, используемый для сервера-накопителя (по умолчанию: 17556)                                                            | 14393             |
| пакет | ApplicationUserModelId (AUMID) для приложения, которое должно запускаться сервером-дисководом.                        | 14393             |
| подробный | Получено запросов на вывод и ответов, отправленных сервером.                                             | 14393             |
| silent  | Ничего не выводит                                                                                                  | 15063             |
| version | Выводит версию MicrosoftWebDriver. exe                                                                    | 17763             |
| PNG     | Использовать протокол HTTP-накопителя W3C (параметр по умолчанию)                                                                      | 17763             |
| jwp     | Использовать протокол для связи JSON                                                                                           | 17763             |
| проём | Очищает временные данные и разделы реестра, заданные сервером--пакетом. Другие параметры игнорируются | 17763             |

## Для устройства для провода W3C
Поддержка для каждой команды спецификации веб- [накопителя W3C](https://www.w3.org/TR/webdriver/).

### Возможности
| Возможность                       | Раздел                       | Состояние                   | Доступная версия |
|:---------------------------------|:--------------------------|:-------------------------|:------------------|
| Имя браузера                     | "browserName"             | Поддерживается                | 17763             |
| Версия браузера                  | "browserVersion"          | Поддерживается                | 17763             |
| Название платформы                    | "platformName"            | Поддерживается                | 17763             |
| Получение сертификатов незащищенного TLS | "acceptInsecureCerts"     | Не &nbsp; поддерживается       | Н/Д               |
| Стратегия загрузки страниц               | "pageLoadStrategy"        | Поддерживается                | 17763             |
| Настройка прокси-сервера              | посредник                   | Не &nbsp; поддерживается       | Н/Д               |
| Размеры окна и положение  | "setWindowRect"           | Поддерживается                | 17763             |
| Настройка таймаутов сеанса   | времени ожидания                | Поддерживается                | 17763             |
| Неуправляемая реакция на запрос        | "unhandledPromptBehavior" | &nbsp;Поддерживается частично | 17763             |
| InPrivate                        | "MS: InPrivate"            | Поддерживается                | 17763             |
| Пути расширения                  | "MS: extensionPaths"       | Поддерживается                | 17763             |
| Начальная страница                       | "MS: startPage"            | Поддерживается                | 17763             |

### Стратегии локаторов
| Стратегия локатора                                                        | Состояние    | Доступная версия |
|:------------------------------------------------------------------------|:----------|:------------------|
| [Селекторы CSS](https://www.w3.org/TR/webdriver/#css-selectors)         | Поддерживается | 17763             |
| [Текст ссылки](https://www.w3.org/TR/webdriver/#link-text)                 | Поддерживается | 17763             |
| [Текст частичной ссылки](https://www.w3.org/TR/webdriver/#partial-link-text) | Поддерживается | 17763             |
| [Имя тега](https://www.w3.org/TR/webdriver/#tag-name)                   | Поддерживается | 17763             |
| [Выражения](https://www.w3.org/TR/webdriver/#xpath)                         | Поддерживается | 17763             |

### Команды
| Метод HTTP | Шаблон URI                                                   | Команда                                                                                   | Состояние             | Доступная версия |
|:------------|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------|:-------------------|:----------------  |
| POST        | /session                                                       | [Новый сеанс](https://www.w3.org/TR/webdriver/#new-session)                               | Поддерживается          | 17763             |
| DELETE      | /Session/{Session ID}                                          | [Удаление сеанса](https://www.w3.org/TR/webdriver/#delete-session)                         | Поддерживается          | 17763             |
| GET         | /STA                                                        | [Состояние](https://www.w3.org/TR/webdriver/#status)                                         | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Timeouts                                 | [Получение таймаутов](https://www.w3.org/TR/webdriver/#get-timeouts)                             | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Timeouts                                 | [Установка таймаутов](https://www.w3.org/TR/webdriver/#set-timeouts)                             | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/URL                                      | [Перейдите к разделу](https://www.w3.org/TR/webdriver/#navigate-to)                               | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/URL                                      | [Получить текущий URL-адрес](https://www.w3.org/TR/webdriver/#get-current-url)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Back                                     | [Back](https://www.w3.org/TR/webdriver/#back)                                             | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Forward                                  | [Forward](https://www.w3.org/TR/webdriver/#forward)                                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Refresh                                  | [Обновить](https://www.w3.org/TR/webdriver/#refresh)                                       | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Title                                    | [Получить заголовок](https://www.w3.org/TR/webdriver/#get-title)                                   | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Window                                   | [Получение маркера окна](https://www.w3.org/TR/webdriver/#get-window-handle)                   | Поддерживается          | 17763             |
| DELETE      | /Session/{Session ID}/Window                                   | [Закрыть окно](https://www.w3.org/TR/webdriver/#close-window)                             | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Window                                   | [Переключиться на окно](https://www.w3.org/TR/webdriver/#switch-to-window)                     | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Window/Handles                           | [Получение дескрипторов окон](https://www.w3.org/TR/webdriver/#get-window-handles)                 | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Frame                                    | [Перейти к рамке](https://www.w3.org/TR/webdriver/#switch-to-frame)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Frame/Parent                             | [Переключение на родительский фрейм](https://www.w3.org/TR/webdriver/#switch-to-parent-frame)         | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Window/Rect                              | [Получить прямоугольник окна](https://www.w3.org/TR/webdriver/#get-window-rect)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Window/Rect                              | [Установка прямоугольной области окна](https://www.w3.org/TR/webdriver/#set-window-rect)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Window/Maximize                          | [Развернуть окно](https://www.w3.org/TR/webdriver/#maximize-window)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Window/Minimize                          | [Окно свертывания](https://www.w3.org/TR/webdriver/#minimize-window)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Window/Fullscreen                        | [Полноэкранное окно](https://www.w3.org/TR/webdriver/#fullscreen-window)                   | Не &nbsp; поддерживается | Н/Д               |
| GET         | /Session/{Session ID}/element/Active                           | [Получить активный элемент](https://www.w3.org/TR/webdriver/#get-active-element)                 | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/element                                  | [Найти элемент](https://www.w3.org/TR/webdriver/#find-element)                             | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Elements                                 | [Поиск элементов](https://www.w3.org/TR/webdriver/#find-elements)                           | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/element/{element ID}/element             | [Найти элемент из элемента](https://www.w3.org/TR/webdriver/#find-element-from-element)   | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/element/{element ID}/Elements            | [Поиск элементов из элемента](https://www.w3.org/TR/webdriver/#find-elements-from-element) | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/Selected            | [Выбран элемент](https://www.w3.org/TR/webdriver/#is-element-selected)               | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/attribute/{name}    | [Получить атрибут элемента](https://www.w3.org/TR/webdriver/#get-element-attribute)           | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/Property/{Name}     | [Получение свойства элемента](https://www.w3.org/TR/webdriver/#get-element-property)             | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/CSS/{Property имя} | [Получение значения CSS для элемента](https://www.w3.org/TR/webdriver/#get-element-css-value)           | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/Text                | [Получение текста элемента](https://www.w3.org/TR/webdriver/#get-element-text)                     | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/Name                | [Получить имя тега элемента](https://www.w3.org/TR/webdriver/#get-element-tag-name)             | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/Rect                | [Получение элемента Rect](https://www.w3.org/TR/webdriver/#get-element-rect)                     | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/element/{element ID}/Enabled             | [Элемент включен](https://www.w3.org/TR/webdriver/#is-element-enabled)                 | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/element/{element ID}/Click               | [Щелчок элемента](https://www.w3.org/TR/webdriver/#element-click)                           | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/element/{element ID}/Clear               | [Очистка элемента](https://www.w3.org/TR/webdriver/#element-clear)                           | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/element/{element ID}/sendKeys            | [Клавиши для отправки элементов](https://www.w3.org/TR/webdriver/#element-send-keys)                   | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Source                                   | [Получение исходного кода страницы](https://www.w3.org/TR/webdriver/#get-page-source)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Execute/Sync                             | [Выполнение сценария](https://www.w3.org/TR/webdriver/#execute-script)                         | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Execute/Async                            | [Выполнение сценария Async](https://www.w3.org/TR/webdriver/#execute-async-script)             | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/cookie                                   | [Получение всех файлов cookie](https://www.w3.org/TR/webdriver/#get-all-cookies)                       | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/cookie/{Name}                            | [Получение именованного файла cookie](https://www.w3.org/TR/webdriver/#get-named-cookie)                     | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/cookie                                   | [Добавление файла cookie](https://www.w3.org/TR/webdriver/#add-cookie)                                 | Поддерживается          | 17763             |
| DELETE      | /Session/{Session ID}/cookie/{Name}                            | [Удаление файла cookie](https://www.w3.org/TR/webdriver/#delete-cookie)                           | Поддерживается          | 17763             |
| DELETE      | /Session/{Session ID}/cookie                                   | [Удаление всех файлов cookie](https://www.w3.org/TR/webdriver/#delete-all-cookies)                 | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Actions                                  | [Выполнение действий](https://www.w3.org/TR/webdriver/#perform-actions)                       | Поддерживается          | 17763             |
| DELETE      | /Session/{Session ID}/Actions                                  | [Действия при выпуске](https://www.w3.org/TR/webdriver/#release-actions)                       | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Alert/dismiss                            | [Закрыть оповещение](https://www.w3.org/TR/webdriver/#dismiss-alert)                           | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Alert/Accept                             | [Уведомление о принятии](https://www.w3.org/TR/webdriver/#accept-alert)                             | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/Alert/Text                               | [Получение текста оповещения](https://www.w3.org/TR/webdriver/#get-alert-text)                         | Поддерживается          | 17763             |
| POST        | /Session/{Session ID}/Alert/Text                               | [Отправка текста оповещения](https://www.w3.org/TR/webdriver/#send-alert-text)                       | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/screenshot                               | [Сделать снимок экрана](https://www.w3.org/TR/webdriver/#take-screenshot)                       | Поддерживается          | 17763             |
| GET         | /Session/{Session ID}/screenshot/{element ID}                  | [Снимок экрана: создать элемент](https://www.w3.org/TR/webdriver/#take-element-screenshot)       | Поддерживается          | 17763             |

## Протокол для проводной связи JSON
Поддержка по протоколу для каждой команды для [протокола связи JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol).

### Команды
| Метод HTTP | Путь                                                                                                                                                         | Состояние             | Доступная версия |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------|
| GET         | [/STA](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)                                                                               | Поддерживается          | 10240             |
| POST        | [/session](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#session-1)                                                                           | Поддерживается          | 10240             |
| GET         | [/sessions](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessions)                                                                           | Поддерживается          | 10240             |
| GET         | [/session/: sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Поддерживается          | 10240             |
| DELETE      | [/session/: sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Timeouts](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeouts)                                        | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Timeouts/async_script](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsasync_script)               | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Timeouts/implicit_wait](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsimplicit_wait)             | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/window_handle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handle)                              | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/window_handles](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handles)                            | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/URL-адрес](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/URL-адрес](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Forward](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidforward)                                          | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Back](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidback)                                                | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Refresh](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidrefresh)                                          | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Execute](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute)                                          | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/execute_async](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute_async)                              | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/снимок экрана](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidscreenshot)                                    | Поддерживается          | 10240             |
| GET         | [/session/: sessionId/IME/available_engines](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeavailable_engines)               | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/: sessionId/IME/active_engine](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactive_engine)                       | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/: sessionId/IME/активировал (-а)](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivated)                               | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/IME/отключить](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimedeactivate)                             | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/IME/Activate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivate)                                 | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Frame](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframe)                                              | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/Frame/Parent](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframeparent)                                 | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Поддерживается          | 10586             |
| DELETE      | [/session/: sessionId/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/Window/: windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Window/: windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/Window/: windowHandle/position (место)](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Window/: windowHandle/position (место)](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Window/: windowHandle/Maximize](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlemaximize) | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Поддерживается          | 10240             |
| DELETE      | [/session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Поддерживается          | 10586             |
| DELETE      | [/session/: sessionId/cookie/: Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookiename)                                  | Поддерживается          | 10240             |
| GET         | [/session/: sessionId/Source (источник)](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsource)                                            | Поддерживается          | 10586             |
| GET         | [/session/: sessionId}/Title](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtitle)                                             | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/элемент](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelement)                                          | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/элементы](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelements)                                        | Поддерживается          | 10586             |
| POST        | [/session/: ИД сеанса/элемента/активен](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementactive)                             | Поддерживается          | 10586             |
| GET         | [/session/: ИД сеанса/элемента/: ID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementid)                                    | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: ИД сеанса/элемента/: ID/элемент](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelement)                     | Поддерживается          | 10586             |
| POST        | [/session/: ИД сеанса/элемента/: ID/элементы](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelements)                   | Поддерживается          | 10586             |
| POST        | [/session/: ИД сеанса/элемента/: ID/щелчок](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclick)                         | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Element/: ID/Submit](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsubmit)                       | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/Text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidtext)                           | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/Element/: ID/value](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidvalue)                         | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/ключи](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidkeys)                                                | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidname)                           | Поддерживается          | 10240             |
| POST        | [/session/: ИД сеанса/элемента/: ID/Clear](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclear)                         | Поддерживается          | 10240             |
| GET         | [/session/: ИД сеанса/элемента/: ID/Selected](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidselected)                   | Поддерживается          | 10240             |
| GET         | [/session/: sessionId/Element/: ID/включено](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidenabled)                     | Поддерживается          | 10240             |
| GET         | [/session/: sessionId/Element/: ID/Attribute/: Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidattribute/:name)     | Поддерживается          | 10240             |
| GET         | [/session/: sessionId/Element/: ID/Equals/: other](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidequals/:other)         | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/отображено](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementiddisplayed)                 | Поддерживается          | 10240             |
| GET         | [/session/: sessionId/Element/: ID/Location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation)                   | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/location_in_view](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation_in_view)   | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsize)                           | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/CSS/:p ropertyName](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidcss/:propertyName) | Поддерживается          | 10240             |
| GET         | [/session/: ИД сеанса/ориентации](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: ИД сеанса/ориентации](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/: sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/accept_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidaccept_alert)                                | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/dismiss_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddismiss_alert)                              | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/MoveTo](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidmoveto)                                            | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/щелчок](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidclick)                                              | Поддерживается          | 10240             |
| POST        | [/session/: sessionId/buttondown](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttondown)                                    | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/BUTTONUP](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttonup)                                        | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddoubleclick)                                  | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/Touch/щелчок](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchclick)                                   | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Touch/стрелка вниз](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdown)                                     | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Touch/up](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchup)                                         | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Touch/Move](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchmove)                                     | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: ИД сеанса/сенсорная (прокрутка)](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll)                                 | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: ИД сеанса/сенсорная (прокрутка)](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll-1)                               | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Touch/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdoubleclick)                       | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: sessionId/Touch/longclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchlongclick)                           | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: ИД сеанса, сенсорный ввод и жест](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick)                                   | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/: ИД сеанса, сенсорный ввод и жест](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick-1)                                 | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/: sessionId/Location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/Location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Поддерживается          | 10586             |
| DELETE      | [/session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Поддерживается          | 10586             |
| DELETE      | [/session/: sessionId/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/local_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagesize)                     | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Поддерживается          | 10586             |
| POST        | [/session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Поддерживается          | 10586             |
| DELETE      | [/session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Поддерживается          | 10586             |
| DELETE      | [/session/: sessionId/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/session_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagesize)                 | Поддерживается          | 10586             |
| GET         | [/session/: sessionId/log](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlog)                                                  | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/: sessionId/log/типы](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlogtypes)                                       | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/: sessionId/application_cache/Status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidapplication_cachestatus)         | Поддерживается          | 10586             |  
