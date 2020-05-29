---
title: Новые возможности EdgeHTML 18
description: Это руководство содержит общие сведения о функциях и стандартах разработчика, включенных в Microsoft Edge.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/06/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, Devtools
ms.custom: RS5
ms.openlocfilehash: b9285be7169f197a687e9f754a20cf67bbde160d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570907"
---
# Руководство для разработчиков Microsoft Edge

> [!TIP]
> Мы [собрались](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) с другими браузерами и веб-сообществом в [MDN веб-документы](https://developer.mozilla.org/) в качестве наиболее удобного места для полезной и несмещенной документации, независимой от браузера, для текущих и новых веб-технологий, основанных на стандартах. Сведения о поддержке API EdgeHTML можно найти непосредственно на каждой странице [библиотеки веб-ссылок MDN](https://developer.mozilla.org/docs/Web). Посетите [состояние платформы](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) Microsoft Edge для получения последних возможностей, поддерживаемых в Microsoft Edge. 


## Новые возможности EdgeHTML 18

EdgeHTML 18 содержит следующие новые и обновленные функции, которые поставляются в текущем выпуске платформы Microsoft EDGE, согласно [обновлению Windows 10 октябрь 2018](/windows/uwp/whats-new/windows-10-build-17763) (10/2018, сборка 17763). Изменения в конкретных сборках [Insider](https://insider.windows.com/) Preview для Windows можно найти в [журнале изменений Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) и [о новых](./dev-guide/whats-new.md)возможностях EdgeHTML.

Ниже приведен список постоянных [https://aka.ms/devguide_edgehtml_18](https://aka.ms/devguide_edgehtml_18) изменений.

## Новые и обновленные функции

### Политики автозапуска

Благодаря обновлению 2018 для Windows 10 октября Microsoft Edge предоставляет пользователям возможность персонализировать настройки браузера на веб-сайтах, которые заменяют звуковые файлы, чтобы свести к минимуму количество отвлекающих на веб-сайте и экономить пропускную способность. Пользователи могут настраивать поведение мультимедиа как для глобальных, так и для отдельных элементов управления автозапуска. Кроме того, Microsoft EDGE автоматически запрещает Автозапуск мультимедиа в закладках на фоне.

Ознакомьтесь с руководством по [политикам автозапуска](./dev-guide/browser-features/autoplay-policies.md) , чтобы получить подробные сведения и рекомендации по обеспечению удобного взаимодействия с мультимедиа, размещенными на вашем сайте.

### Улучшения Chakra

EdgeHTML 18 включает обновления механизма JavaScript Chakra для поддержки новых возможностей и функций WASM в дополнение к улучшениям производительности и совместимости. Подробные сведения [ChakraCore в заметках о Выпуске 1,11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) .

### Обновления CSS

Мы сделали еще более подробное развитие реализации [масок CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) (за флагом *включения маскировки CSS* ) с помощью дополнительной поддержки [маскированных](https://developer.mozilla.org/docs/Web/CSS/mask-composite), [маскирующих](https://developer.mozilla.org/docs/Web/CSS/mask-position)масок и [масок-повторения](https://developer.mozilla.org/docs/Web/CSS/mask-repeat). В целях обеспечения совместимости сайтов Microsoft EDGE также поддерживает следующие функции *-WebKit-* -WebKit-Mask,-WebKit-Mask-WebKit,-WebKit-Mask-Image,-WebKit-Mask-Position-x,, Mask и Mask-,-WebKit-маски и размера-WebKit-Mask.

Кроме того, в Microsoft Edge предусмотрена поддержка [перетекания](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap
) и частичной поддержки [поведения перекрутки](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) ( `auto` и `contain` значений).


### Средства разработчика

Последнее обновление Microsoft Edge DevTools позволяет получить ряд специальных возможностей в пользовательском интерфейсе и, в частности, новые специальные панели для рабочих процессов и хранения, средства поиска файлов исходного кода в отладчике и новые домены протоколов пограничного DevTools для отладки стиля и макета и API консоли.

[DevTools в новейшем обновлении Windows 10 (EdgeHTML 18)](./devtools-guide/whats-new.md) есть все необходимые данные.

### Прослушивание отзыва

Мы будем рады вашим отзывам и реализовали поддержку нескольких запрошенных API-интерфейсов в EdgeHTML 18, в том числе [`DataTransfer.setDragImage()`](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) метод, используемый для задания настраиваемого изображения при перетаскивании и перетаскивании, а также [`secureConnectionStart`](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart) свойство API производительности ресурсов, которое можно использовать для возврата метки времени непосредственно перед тем, как браузер начнет процесс подтверждения, чтобы защитить текущее подключение. 

Кроме того, никто не должен перечислять коллекцию Attributes, поэтому мы добавили поддержку для [`Element.getAttributeNames`](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) возврата имен атрибутов элемента в виде массива строк, а также [`Element.toggleAttribute`](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) для переключения логического атрибута (удаления, если он присутствует и добавляется в противном случае).

### Прогрессивные веб-приложения

#### Фоновый сценарий времени существования

Приложения JavaScript для Windows 10 (веб-приложения, работающие в процессе *WWAHost. exe* ) теперь поддерживают дополнительный фоновый сценарий для приложения, который начинается перед активацией и запуском каких-либо представлений в течение процесса. Благодаря этому вы можете отслеживать и изменять навигацию, отслеживать состояние во всех переходах, отслеживать ошибки навигации и выполнять код перед активацией представлений. 

При указании [`StartPage`](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) в [манифесте приложения](/uwp/schemas/appxpackage/appx-package-manifest)каждый из представлений приложения (Windows) представляется сценарию в виде экземпляров нового [`WebUIView`](/uwp/api/windows.ui.webui.webuiview) класса, обеспечивая такие же события, свойства и методы, как общие (Win32) [WebView](/uwp/api/windows.web.ui.iwebviewcontrol). Ваш сценарий может прослушивать [`NewWebUIViewCreated`](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) событие, чтобы перехватить управление навигацией для нового представления.

```JavaScript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```

 Любая активация приложения с помощью фонового сценария `StartPage` будет основываться на самом сценарии для навигации.

#### Масштабирование текста

В Windows 10 октября с обновлением 2018 для улучшенной поддержки специальных возможностей, [*а также PWAs*](https://review.docs.microsoft.com/windows/uwp/design/input/text-scaling?branch=master#user-experience) установленной в Windows (в дополнение UWP и большинстве классических приложений) теперь поддерживается автоматическое включение этой функции. Для элементов управления PWAs и WebView текстовый масштаб работает таким же образом, как и масштабирование. Если пользователь изменяет масштаб масштабирования текста и масштаб DPI, результатом является произведение двух.

 Руководство по проектированию можно найти в статье [масштабирование текста](/windows/uwp/design/input/text-scaling) в *центре разработки для Windows*.

### Обновления служебных сотрудников 

Чтобы обновить сведения о сотрудниках служб и о том, как они работают, ознакомьтесь со статьей [API рабочих процессов служб]( https://developer.mozilla.org/docs/Web/API/Service_Worker_API) , написанными нашими партнерами, по адресу MDN.  В EdgeHTML 18 существовало несколько обновлений Microsoft EDGE, поддерживающих сотрудников служб. `fetchEvent`Позволяет сотруднику службы использовать [`preloadResponse`]( https://developer.mozilla.org/docs/Web/API/FetchEvent) для резервирования ответа, а также [`resultingClientId`]( https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) для возврата идентификатора клиента, управляемого текущим сотрудником службы.  
[`NavigationPreloadManager`]( https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager)Интерфейс предоставляет методы для управления предварительной загрузкой ресурсов, позволяя параллельно создавать запросы во время загрузки рабочего процесса, избегая задержки. Ознакомьтесь со всеми [поддерживаемыми свойствами API](#new-apis-in-edgehtml-18) для списка методов и свойств предварительной версии рабочих процессов для служб. 

### Проверка подлинности веб-сайта

Microsoft EDGE теперь включает [в себя поддержку непрефиксов для нового API проверки подлинности веб-](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge/) сервера (процесс [WebAuthN](https://w3c.github.io/webauthn/)). Веб-проверка подлинности предоставляет открытое, масштабируемое и функциональное решение для упрощения проверки подлинности, обеспечивая более эффективное и безопасный интерфейс, заменив пароли более надежными учетными данными, связанными с оборудованием. Реализация в Microsoft EDGE позволяет использовать [Windows Hello](https://www.microsoft.com/windows/windows-hello) , в дополнение к внешним средствам [проверки](https://fidoalliance.org) подлинности, таким как FIDO2 ключи безопасности или Fido U2F, для безопасной проверки подлинности на веб-сайтах.

Для получения дополнительных сведений заголовков в блоге, посвященном [веб-проверке подлинности в Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).

### WebDriver

Веб-диск теперь является [компонентом Windows по запросу](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (недостающий), что упрощает тестирование тестирования в Microsoft EDGE и получение нужной версии для вашего устройства. Вам больше не нужно составлять соответствие сборки и ветви или изменения вручную при установке веб-диска, так [как он будет](https://www.w3.org/TR/webdriver) автоматически обновляться в соответствии с новыми обновлениями для Windows 10. 

Чтобы установить веб-диск, включите режим разработчика или установите его в автономном режиме, перейдя в настройки > приложения > приложения & функции > управлять дополнительными функциями. Дополнительные сведения можно найти в описании [веб-накопителя на сайте блога Windows](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).

### Свойства веб-уведомлений
Теперь для веб-уведомлений поддерживаются четыре новых свойства [`actions`](https://developer.mozilla.org/docs/Web/API/notification/actions) : [`badge`](https://developer.mozilla.org/docs/Web/API/notification/badge) , [`image`](https://developer.mozilla.org/docs/Web/API/notification/image) и и `maxActions` улучшаются возможности создания уведомлений на веб-сайте, совместимых с существующими системами уведомлений, в то время как оставшиеся независимые от платформы.

### WebView

#### Обслуживание сотрудников
Теперь в дополнение к браузерам Microsoft EDGE и приложениям для JavaScript для Windows 10 поддерживаются [сотрудники служб](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) в элементе управления WebView. Все разновидности рабочих процессов Microsoft Edge WebView ([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)), поддерживающих обслуживание, тем не менее, имейте в виду, что [API push-уведомлений](https://developer.mozilla.org/docs/Web/API/Push_API) пока не доступен для версий UWP и Win32.

архитектуры приложений для архитектуры x64 требуются *нейтральные* (любые ЦП) или *64-разрядные* пакеты, так как работники служб не поддерживаются в процессах WOW64. (Для экономии места на диске версия WoW необходимых DLL не включена в Windows.)

#### Обновления для WebView Win32

В приложениях EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) для Windows Desktop (Win32) было добавлено несколько новых функций, включая возможность вставки сценария при загрузке страницы перед выполнением других сценариев на странице ( [`AddInitializeScript`](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript) ) и сведения о том, когда конкретный WebViewControl получает или теряет фокус ( [`GotFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [`LostFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus) ).

Кроме того, теперь вы можете создать новый WebViewControl как открытое окно [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) . [`NewWindowRequested`](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested)Событие по-прежнему уведомляет приложение при выполнении сценария в окне WebViewControl Calls. Open as всегда, но с EdgeHTML 18 с его помощью можно [`NewWindowRequestedEventArgs`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) получить РБП ( [`GetDeferral`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral) ), чтобы установить новый WebViewControl () в [`NewWindow`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow) качестве целевого объекта для окна. открыть:

```C#
WebViewControlProcess wvProc;
WebViewControl webView;

void OnWebViewControlNewWindowRequested(WebViewControl sender, WebViewControlNewWindowRequestedEventArgs args)
{

    if (args.Uri.Domain == "mydomain.com")
    {
        using deferral = args.GetDeferral();
        args.NewWindow = await wvProc.CreateWebViewControlAsync(
            parentWindow, targetWebViewBounds);
        deferral.Complete();
    }
    else
    {
        // Prevent WebView from launching in the default browser.
        args.Handled = true;
    }
}

String htmlContent = "<html><script>window.open('http://mydomain.com')</script><body></body></html>";

webView.NavigateToString(htmlContent);

```

Наконец, опытные пользователи могут заметить, что apppearance *веб-браузера для настольных приложений* (ранее именуемый *Win32WebViewHost*), внутреннее Системное приложение, представляющее Win32 WebView, в следующих местах:
- В *центре уведомлений Windows 10*. Источник этих уведомлений должен быть понятен как из WebView, размещенного в приложении Win32.
- В пользовательском интерфейсе параметров доступа к устройству (*Параметры->конфиденциальность->Камера/расположение/микрофона*). Отключение любого из этих параметров запрещает доступ из всех представлений, размещенных в приложениях Win32.

![Настройка доступа к устройствам в классическом приложении Web App Viewer](./dev-guide/media/desktop-app-web-viewer.png)


## Устаревшие возможности

### Фильтр XSS теперь устарел

Благодаря EdgeHTML 18 вы пройдете фильтр XSS в Microsoft Edge. Наши клиенты по-прежнему защищены благодаря современным стандартам, как [Политика безопасности контента (CSP)](https://developer.mozilla.org/docs/Web/HTTP/CSP), которые предоставляют более эффективные, производительные и безопасные механизмы для защиты от атак путем внедрения контента, благодаря высокой совместимости в современных браузерах.

## Новые API-интерфейсы в EdgeHTML 18

Полный список новых API-интерфейсов в EdgeHTML 18 Вы также изучите. Они указаны в формате [имя интерфейса]. [имя API].

> [!NOTE] 
> Несмотря на то что в DOM используются следующие API-интерфейсы, поведение некоторых из них по-прежнему может быть на стадии разработки и скрыто за экспериментальным флагом. Для официального приложения Word о поддержке функций вы можете обратиться к [Microsoft Edge Platform Status](https://developer.microsoft.com/microsoft-edge/platform/status/) .

<iframe height='580' scrolling='no' title='Новые API-интерфейсы в EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь с <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> новыми API для EdgeHTML 18 на </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) в <a href='https://codepen.io'> CodePen </a> .</iframe>

## Предыдущие выпуски EdgeHTML

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

[EdgeHTML 16/Windows Build 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)

[EdgeHTML 17/Windows Build 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)
