---
title: Доступ к локальным серверам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: daa96b604d5ad48a9de49dd24dc38eab79de9c9b
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898216"
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





# <span data-ttu-id="8905b-103">Доступ к локальным серверам</span><span class="sxs-lookup"><span data-stu-id="8905b-103">Access Local Servers</span></span>   




<span data-ttu-id="8905b-104">Размещение сайта на веб-сервере разработчика, а затем доступ к содержимому с устройства Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-104">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="8905b-105">С помощью USB-кабеля и Microsoft Edge DevTools, запустите сайт с компьютера для разработки и просмотрите сайт на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-105">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="8905b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8905b-106">Summary</span></span>  

*   <span data-ttu-id="8905b-107">Переадресация портов позволяет просматривать контент, размещенный на вашем компьютере, на котором работает веб-сервер, на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-107">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="8905b-108">Если веб-сервер использует настраиваемый домен, настройте на устройстве с Android доступ к контенту в этом домене с помощью собственного сопоставления доменов.</span><span class="sxs-lookup"><span data-stu-id="8905b-108">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="8905b-109">Настройка переадресации портов</span><span class="sxs-lookup"><span data-stu-id="8905b-109">Set up port forwarding</span></span>   

<span data-ttu-id="8905b-110">Переадресация портов позволяет устройству Android получать доступ к содержимому, размещенному на веб-сервере, работающем на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="8905b-110">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="8905b-111">Переадресация порта работает путем создания прослушивающего порта TCP на устройстве с Android, которое сопоставляется с портом TCP на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="8905b-111">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="8905b-112">Трафик между портами проходит через USB-соединение между устройством с Android и компьютером для разработки, поэтому подключение не зависит от конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="8905b-112">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="8905b-113">Чтобы включить перенаправление портов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8905b-113">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="8905b-114">Настройка [удаленной отладки][RemoteDebuggingGettingStarted] между компьютером разработчика и устройством с Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-114">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="8905b-115">Когда вы закончите работу, вы увидите устройство с Android в левом меню диалогового окна **Проверка устройств** и индикатор состояния **подключен** .</span><span class="sxs-lookup"><span data-stu-id="8905b-115">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="8905b-116">В диалоговом окне **Проверка устройств** в DevTools включите **переадресацию порта**.</span><span class="sxs-lookup"><span data-stu-id="8905b-116">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="8905b-117">Нажмите кнопку **Добавить правило**.</span><span class="sxs-lookup"><span data-stu-id="8905b-117">Select **Add rule**.</span></span>  
    
    > ##### <span data-ttu-id="8905b-118">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="8905b-118">Figure 1</span></span>  
    > <span data-ttu-id="8905b-119">Добавление правила переадресации портов</span><span class="sxs-lookup"><span data-stu-id="8905b-119">Adding a port forwarding rule</span></span>  
    > ![Добавление правила переадресации портов][ImageAddRule]  
    
1.  <span data-ttu-id="8905b-121">В поле " **порт устройства** " слева введите `localhost` номер порта, с которого вы хотите получить доступ к сайту на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="8905b-122">Например, если вы хотите получить доступ к сайту из `localhost:5000` ввода `5000` .</span><span class="sxs-lookup"><span data-stu-id="8905b-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="8905b-123">В текстовом поле " **локальный адрес** " щелкните правой кнопкой мыши IP-адрес или имя узла, на котором расположен сайт, который находится на компьютере разработчика, а затем укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="8905b-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="8905b-124">Например, если ваш веб-сайт запущен на `localhost:7331` входе `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="8905b-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="8905b-125">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="8905b-125">Select **Add**.</span></span>  

<span data-ttu-id="8905b-126">Переадресация порта теперь настроена.</span><span class="sxs-lookup"><span data-stu-id="8905b-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="8905b-127">Просмотрите индикатор состояния для порта на вкладке на вашем устройстве в диалоговом окне **Проверка устройств** .</span><span class="sxs-lookup"><span data-stu-id="8905b-127">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

> ##### <span data-ttu-id="8905b-128">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="8905b-128">Figure 2</span></span>  
> <span data-ttu-id="8905b-129">Состояние переадресации порта</span><span class="sxs-lookup"><span data-stu-id="8905b-129">Port forwarding status</span></span>  
> ![Состояние переадресации порта][ImagePortForwardingStatus]  

<span data-ttu-id="8905b-131">Чтобы просмотреть содержимое, откройте приложение Microsoft EDGE на устройстве с Android и перейдите к `localhost` порту, который вы указали в поле " **порт устройства** ".</span><span class="sxs-lookup"><span data-stu-id="8905b-131">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="8905b-132">Например, если вы ввели `5000` поле, перейдите на страницу `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="8905b-132">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="8905b-133">Сопоставление с пользовательскими локальными доменами</span><span class="sxs-lookup"><span data-stu-id="8905b-133">Map to custom local domains</span></span>   

<span data-ttu-id="8905b-134">С помощью настраиваемого сопоставления доменов вы можете просматривать содержимое на устройстве с Android с веб-сервера на компьютере разработчика, использующем настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="8905b-134">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="8905b-135">Например, предположим, что ваш сайт использует библиотеку JavaScript стороннего поставщика, которая работает только в домене `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="8905b-135">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="8905b-136">Таким образом, вы создаете запись в `hosts` файле на компьютере разработчика, чтобы сопоставить этот домен с доменом `localhost` (например, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="8905b-136">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="8905b-137">После настройки сопоставления домена и переадресации порта просмотрите сайт на своем устройстве с Android по URL-адресу `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="8905b-137">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="8905b-138">Настройка пересылки порта на прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="8905b-138">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="8905b-139">Для сопоставления собственного домена необходимо запустить прокси-сервер на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="8905b-139">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="8905b-140">Ниже приведены примеры прокси-серверов: [Чарльз][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]и [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="8905b-140">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="8905b-141">Чтобы настроить перенаправление порта на прокси-сервер, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8905b-141">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="8905b-142">Запустите прокси-сервер и запишите порт, который он использует.</span><span class="sxs-lookup"><span data-stu-id="8905b-142">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8905b-143">Прокси-сервер и веб-сервер должны работать на разных портах.</span><span class="sxs-lookup"><span data-stu-id="8905b-143">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="8905b-144">Настройка [пересылки порта](#set-up-port-forwarding) на устройство с Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-144">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="8905b-145">В поле **Local Address (локальный адрес** ) введите `localhost:` за ним порт, на котором работает прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="8905b-145">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="8905b-146">Например, если он запущен на порте `8000` , перейдите на страницу `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="8905b-146">For example, if it is running on port `8000`, visit `localhost:8000`.</span></span>  <span data-ttu-id="8905b-147">В поле **порт устройства** введите номер, который будет прослушивать ваше устройство с Android, например `3333` .</span><span class="sxs-lookup"><span data-stu-id="8905b-147">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  

### <span data-ttu-id="8905b-148">Настройка параметров прокси-сервера на устройстве</span><span class="sxs-lookup"><span data-stu-id="8905b-148">Configure proxy settings on your device</span></span>  

<span data-ttu-id="8905b-149">Затем необходимо настроить устройство Android для взаимодействия с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="8905b-149">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="8905b-150">На устройстве с Android перейдите в раздел **Параметры**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="8905b-150">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="8905b-151">Long-нажимайте имя сети, к которой вы подключены в данный момент.</span><span class="sxs-lookup"><span data-stu-id="8905b-151">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8905b-152">Параметры прокси-сервера применяются к каждой сети.</span><span class="sxs-lookup"><span data-stu-id="8905b-152">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="8905b-153">Выберите команду **изменить сеть**.</span><span class="sxs-lookup"><span data-stu-id="8905b-153">Select **Modify network**.</span></span>  
1.  <span data-ttu-id="8905b-154">Выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="8905b-154">Select **Advanced options**.</span></span>  <span data-ttu-id="8905b-155">Отображение параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="8905b-155">The proxy settings display.</span></span>  
1.  <span data-ttu-id="8905b-156">Откройте меню **прокси** и выберите пункт **вручную**.</span><span class="sxs-lookup"><span data-stu-id="8905b-156">Select the **Proxy** menu and select **Manual**.</span></span>  
1.  <span data-ttu-id="8905b-157">В поле **имя HostName прокси-сервера** введите `localhost` .</span><span class="sxs-lookup"><span data-stu-id="8905b-157">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="8905b-158">В поле порт **прокси-сервера** введите номер порта, который вы ввели для **порта устройства** в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="8905b-158">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="8905b-159">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8905b-159">Select **Save**.</span></span>  

<span data-ttu-id="8905b-160">С помощью этих параметров устройство перенаправляет все свои запросы на прокси-сервер на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="8905b-160">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="8905b-161">Прокси-сервер создает запросы от имени вашего устройства, поэтому запросы к своему пользовательскому домену разрешаются надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="8905b-161">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="8905b-162">Теперь вы можете получать доступ к настраиваемым доменам на устройстве с Android так же, как и на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="8905b-162">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="8905b-163">Если веб-сервер не работает с нестандартным портом, не забудьте указать порт при запросе содержимого с устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="8905b-163">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="8905b-164">Например, если ваш веб-сервер использует собственный домен `microsoft-edge.devtools` для порта, то `7331` при просмотре сайта с устройства Android вы должны использовать URL-адрес `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="8905b-164">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="8905b-165">Чтобы возобновить обычный просмотр, не забудьте вернуть параметры прокси-сервера на устройстве с Android после отключения от компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="8905b-165">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

<!--  -->  



<!-- image links -->  

[ImageAddRule]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png "Рисунок 1: Добавление правила переадресации портов"  
[ImagePortForwardingStatus]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png "Рисунок 2: состояние переадресации порта"  

<!-- links -->  

[RemoteDebuggingGettingStarted]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленными отладкой устройств с Android"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Прокси-сервер отладчика Чарльз"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: оптимизация веб-доставки"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Прокси-сервер для Fiddler без поддержки бесплатной отладки"  

> [!NOTE]
> <span data-ttu-id="8905b-172">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8905b-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8905b-173">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="8905b-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8905b-175">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8905b-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
