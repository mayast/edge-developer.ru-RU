---
description: Добавивсь в мир пользователей Windows 10, выполнив распространение PWA в Microsoft Store
title: Прогрессивные веб-приложения в Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, EDGE, Windows, Microsoft Store, индекс Bing PWA
ms.openlocfilehash: a4491f19b89e8b0f6fa511f146744499e2074f22
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572828"
---
# Прогрессивные веб-приложения в Microsoft Store

Когда вы публикуете прогрессивное веб-приложение (PWA) в [Microsoft Store](https://developer.microsoft.com/store), потенциальная аудитория приложения расширяется до всего 700 000 000 активных ежемесячных пользователей практически в Windows 10. 

PWAs в Microsoft Store, вы получите ряд преимуществ.

- **Обнаружение** приложений в магазине Microsoft Store осуществляется с помощью различных категорий, проверенных коллекций и фильтров поиска, обеспечивая простой просмотр и прием покупок для потенциальных пользователей вашего приложения. Вы также можете [усовершенствовать свой список в магазине](/windows/uwp/publish/app-screenshots-and-images) с помощью снимков экрана, главный Имиджевый баннер изображения и видеоконференций!

- **Надежность** — клиенты Windows знают, что они могут доверять своим покупкам и загрузкам из Microsoft Store, так как они соответствуют требованиям строгого [качества и безопасности](/legal/windows/agreements/store-policies)Microsoft.

- **Простая установка** — Microsoft Store обеспечивает единообразное и понятное взаимодействие между [всеми приложениями для Windows 10](https://www.microsoft.com/store/apps/windows?icid=CNavAppsWindowsApps), позволяя всем пользователям устанавливать веб-приложения PWA независимо от того, где он находится на техническом комфорте.

- **Бизнес-аналитика** — [информационная панель центра разработки для Windows](/windows/uwp/publish/using-the-windows-dev-center-dashboard) для Microsoft Store содержит [подробную](/windows/uwp/publish/analytics) информацию о том, сколько пользователей Windows достигают о том, как они используют этот PWA и что им нужно сказать. Вы также можете находить метрики и данные телеметрии на работоспособности приложения, об использовании рекламы и т. д.

Существует два способа получить PWA в Microsoft Store.

1. Вы можете [отправить ее вручную](#submitting-your-pwa-manually)или

2. Если веб-сайт PWA отвечает [определенным условиям](#criteria-for-automatic-submission), он может [автоматически индексироваться](#automatic-pwa-importing-with-bing) с помощью агента Bing. (Вы также можете [отказаться](#opting-out-of-automatic-microsoft-store-import) от автоматической отправки.)

Независимо от способа отправки после того, как ваш PWA будет принят в Microsoft Store, вы получите доступ ко всем описанным выше возможностям.

## Отправка PWA вручную

Для распространения приложения и продвижения его в Microsoft Store необходимо отправить его в виде пакета приложения для Windows (*appx* -файл).  Для веб-приложений, размещенных на сервере, например PWAs, этот пакет просто включает метаданные приложения и начальные значки экрана (и ни один из собственно кода приложения). Таким образом, вы можете установить и запустить веб-приложение на начальном экране вместе с другими [приложениями для Windows 10](/windows/uwp/get-started/whats-a-uwp) , запустив в упрощенном коде оболочки приложения (*WWAHost. exe* ) независимо от окна браузера Microsoft Edge.  

> [!IMPORTANT]
> Обработчик приложений EdgeHTML используется оберткой веб-платформы WWAHost, что может привести к различиям совместимости для PWA на базе Microsoft EDGE (Chromium).  Перед отправкой приложения в магазин Microsoft Edge убедитесь в том, что вы пройдете полное тестирование вашего приложения, так как в этом случае уже не будет обновлена новая версия веб-сайта в качестве обработчика EdgeHTML.  

Вот как это сделать.

### Предварительные условия

- **Существующий PWA**. Вот как можно [преобразовать веб-приложение в PWA,](./get-started.md) если оно еще не существует. 
- **Инструмент для создания пакетов Windows APPX для PWAs**. Вот как можно [создать и запустить PWA в Windows](./windows-features.md) с помощью Visual Studio. Вы также можете использовать [конструктор PWA](https://www.pwabuilder.com/) для создания пакета Windows.
- [**Учетная запись разработчика приложений Microsoft Store**](/windows/uwp/publish/opening-a-developer-account). В зависимости от выбранного типа и местоположения учетной записи, а для регистрации требуется действительная [учетная запись Майкрософт](https://account.microsoft.com/), это может быть [единовременно](/windows/uwp/publish/account-types-locations-and-fees) .


### Отправка сообщений в магазине с помощью *Visual Studio* 

Выполните эти действия, чтобы [создать файл для отправки пакета приложения](/windows/uwp/packaging/packaging-uwp-apps#create-an-app-package-upload-file) для PWA в Visual Studio. Общие сведения об этом процессе смотрите в разделе [*Упаковка приложения UWP с помощью Visual Studio*](/windows/uwp/packaging/packaging-uwp-apps) .

Инструкции также помогут вам запустить [**Комплект сертификации приложений для Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit) , чтобы протестировать приложение на соответствие требованиям Microsoft Store. Это необязательно, но настоятельно рекомендуется.

### Отправка в магазине через *центр разработки для Windows*

Ниже показано, как использовать *конструктор PWA* для создания пакета приложения для отправки в центр разработки для Windows.

1. Создание приложения для Windows 10. Вот как можно запустить [PWA как приложение для Windows с помощью Visual Studio](./windows-features.md). Вы также можете использовать [конструктор PWA](https://www.pwabuilder.com/) для создания приложения для Windows 10.

2. Зарезервируйте имя приложения для Microsoft Store, войдя на [информационную панель центра разработки для Windows](https://developer.microsoft.com/dashboard/windows/overview) , указав данные своей учетной записи, и выполните действия, чтобы [создать приложение, сохранив его имя](/windows/uwp/publish/create-your-app-by-reserving-a-name). Каждое зарезервированное имя должно быть уникальным в Microsoft Store.

3. Когда вы отправляете пакеты приложения, значения *DisplayName*, *Name*, *Publisher*и *PublisherDisplayName* в файле *. appxmanifest* должны соответствовать значениям, назначенным вашему приложению на информационной панели центра разработки для Windows при резервировании имени. 

    Войдите в [информационную панель центра разработки для Windows](https://developer.microsoft.com/dashboard/windows/overview)и найдите значения удостоверения приложения в разделе **App management**  >  **удостоверение приложения**для управления приложениями:

    ![Информационная панель центра разработки для Windows, параметры удостоверения приложения](./media/dashboard-app-identity.png)

    Затем найдите `appxmanifest.xml` файл и замените указанные ниже значения, назначенные на информационной панели центра разработки для Windows.

    - **<имя удостоверения = "** *пакет/удостоверение/имя*
    - **<Identity Publisher = "** *пакет/идентификация/издатель*
    - **<DisplayName** **>** *Имя, зарезервированное для вашего приложения* 
    - **<PublisherDisplayName** **>** *Package/Properties/PublisherDisplayName***</PublisherDisplayName>**

4. Теперь вы готовы к компиляции всех ресурсов PWA в один `.appx` файл, который можно отправить в Microsoft Store. В командной строке перейдите в каталог вашего веб-манифеста и создайте пакет Windows 10 (указанный ниже, а также необязательное ведение журнала отладки):

    ```
    pwabuilder package -p windows10 -l debug
    ```

    Appx-файл будет создан в следующем расположении: `PWA\Store packages\windows10\package\windows.appx` .

5. Перед тем как приступить к отправке приложения для submisison в Microsoft Store, рекомендуется протестировать приложение на соответствие политикам Microsoft Store. Это можно сделать, загрузив [**Комплект сертификации приложений для Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit), запустив его, а затем выбрав *appx* -файл приложения для тестирования. После завершения всех тестов вы получите отчет об областях для устранения.

6. Загрузите пакет и завершите отправку, войдя на [панель мониторинга центра разработки для Windows](https://developer.microsoft.com/dashboard/windows/overview) и разворачивая **отправку**  >  **Submisison 1** . Следуйте указаниям контрольного списка, чтобы завершить [Описание требуемого магазина](/windows/uwp/publish/app-submissions) и [отправить пакет приложения](/windows/uwp/publish/upload-app-packages).

Дополнительные сведения о всех возможностях и службах, доступных разработчикам приложений Microsoft Store, можно найти в разделе [*Публикация приложений для Windows*](https://developer.microsoft.com/store/publish-apps) в [центре разработки для Windows](https://developer.microsoft.com/windows).

## Автоматическое импорт PWA с помощью Bing

Точно так же, как [Манифест веб-приложения](https://developer.mozilla.org/docs/Web/Manifest) PWA — это сигнал для поддержки платформ, которые ваше приложение не поддерживает, и готово к представлению как полностью интегрированных приложений, оно также является подсказкой веб-агента Bing, которую вы хотите учитывать для автоматического включения в Microsoft Store. 

Если веб-сайт PWA отвечает указанным ниже требованиям, служба индексирования Bing автоматически обновит версию PWA в формате [*appx*](#submitting-your-pwa-manually) , требуемом для установки в Windows 10, и собирать страницу продукта магазина приложения на основе метаданных в манифесте веб-приложения. После того как вы выйдете из PWA, вы сможете дополнительно настроить страницу магазина и получить доступ к аналитикам пользователей и другим средствам управления приложениями с помощью информационной панели центра разработки для Windows.

### Условия для автоматической отправки

Чтобы автоматически упаковываться и передаваться в список для Microsoft Store, для вашего PWA потребуется:

- [X] непустой файл манифеста веб-приложения по крайней мере:

  - Имя
  - Описание
  - Значок приложения по крайней мере 512 x 512 пикселей

- [X] уникальная Базовая логика (незначительная модификация кода из [стандартного шаблона приложения](https://en.wikipedia.org/wiki/Boilerplate_code) )

- [X] для обслуживания через безопасное соединение (HTTPS)

- [X] (-а) сценарии обслуживания рабочих процессов

- [X] не нарушают никаких законов или [политик Microsoft Store](/legal/windows/agreements/store-policies).

Мы не будем получать все приложения, которые удовлетворяют этим критериям, но будут включать их в наши вопросы для кандидатов, так как мы постепенно развернут нашу программу.

### Выход из автоматического импорта Microsoft Store

PWA может отказаться от автоматического импорта в Microsoft Store с помощью файла, `robots.txt` содержащего следующие файлы:

```
User-agent: bingbot
Disallow: /manifest.json
```

Это направлено на то, что программа-обходчик Bing (Bingbot) проигнорирует файл веб-манифеста для целей индексирования PWA. Это не повлияет на ранжирование поиска на сайте в процессе регулярного [веб-индексирования](https://www.bing.com/webmaster/help/help-center-661b2d18)Bing.
