---
title: Доступ к локальным серверам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: fb8f8aabaf426685417f90e25295f3e8e7b08994
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984913"
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





# <span data-ttu-id="cce20-103">Доступ к локальным серверам</span><span class="sxs-lookup"><span data-stu-id="cce20-103">Access local servers</span></span>   




<span data-ttu-id="cce20-104">Размещение сайта на веб-сервере разработчика, а затем доступ к содержимому с устройства Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-104">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="cce20-105">С помощью USB-кабеля и Microsoft Edge DevTools, запустите сайт с компьютера для разработки и просмотрите сайт на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-105">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="cce20-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cce20-106">Summary</span></span>  

*   <span data-ttu-id="cce20-107">Переадресация портов позволяет просматривать контент, размещенный на вашем компьютере, на котором работает веб-сервер, на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-107">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="cce20-108">Если веб-сервер использует настраиваемый домен, настройте на устройстве с Android доступ к контенту в этом домене с помощью собственного сопоставления доменов.</span><span class="sxs-lookup"><span data-stu-id="cce20-108">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="cce20-109">Настройка переадресации портов</span><span class="sxs-lookup"><span data-stu-id="cce20-109">Set up port forwarding</span></span>   

<span data-ttu-id="cce20-110">Переадресация портов позволяет устройству Android получать доступ к содержимому, размещенному на веб-сервере, работающем на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="cce20-110">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="cce20-111">Переадресация порта работает путем создания прослушивающего порта TCP на устройстве с Android, которое сопоставляется с портом TCP на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="cce20-111">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="cce20-112">Трафик между портами проходит через USB-соединение между устройством с Android и компьютером для разработки, поэтому подключение не зависит от конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="cce20-112">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="cce20-113">Чтобы включить перенаправление портов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cce20-113">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="cce20-114">Настройка [удаленной отладки][RemoteDebuggingGettingStarted] между компьютером разработчика и устройством с Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-114">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="cce20-115">Когда вы закончите работу, вы увидите устройство с Android в левом меню диалогового окна **Проверка устройств** и индикатор состояния **подключен** .</span><span class="sxs-lookup"><span data-stu-id="cce20-115">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="cce20-116">В диалоговом окне **Проверка устройств** в DevTools включите **переадресацию порта**.</span><span class="sxs-lookup"><span data-stu-id="cce20-116">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="cce20-117">Нажмите кнопку **Добавить правило**.</span><span class="sxs-lookup"><span data-stu-id="cce20-117">Select **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Добавление правила переадресации портов" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="cce20-119">Добавление правила переадресации портов</span><span class="sxs-lookup"><span data-stu-id="cce20-119">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cce20-120">В поле " **порт устройства** " слева введите `localhost` номер порта, с которого вы хотите получить доступ к сайту на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-120">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="cce20-121">Например, если вы хотите получить доступ к сайту из `localhost:5000` ввода `5000` .</span><span class="sxs-lookup"><span data-stu-id="cce20-121">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="cce20-122">В текстовом поле " **локальный адрес** " щелкните правой кнопкой мыши IP-адрес или имя узла, на котором расположен сайт, который находится на компьютере разработчика, а затем укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="cce20-122">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="cce20-123">Например, если ваш веб-сайт запущен на `localhost:7331` входе `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="cce20-123">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="cce20-124">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cce20-124">Select **Add**.</span></span>  
    
<span data-ttu-id="cce20-125">Переадресация порта теперь настроена.</span><span class="sxs-lookup"><span data-stu-id="cce20-125">Port forwarding is now set up.</span></span>  <span data-ttu-id="cce20-126">Просмотрите индикатор состояния для порта на вкладке на вашем устройстве в диалоговом окне **Проверка устройств** .</span><span class="sxs-lookup"><span data-stu-id="cce20-126">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Состояние переадресации порта" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="cce20-128">Состояние переадресации порта</span><span class="sxs-lookup"><span data-stu-id="cce20-128">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="cce20-129">Чтобы просмотреть содержимое, откройте приложение Microsoft EDGE на устройстве с Android и перейдите к `localhost` порту, который вы указали в поле " **порт устройства** ".</span><span class="sxs-lookup"><span data-stu-id="cce20-129">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="cce20-130">Например, если вы ввели `5000` поле, перейдите на страницу `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="cce20-130">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="cce20-131">Сопоставление с пользовательскими локальными доменами</span><span class="sxs-lookup"><span data-stu-id="cce20-131">Map to custom local domains</span></span>   

<span data-ttu-id="cce20-132">С помощью настраиваемого сопоставления доменов вы можете просматривать содержимое на устройстве с Android с веб-сервера на компьютере разработчика, использующем настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="cce20-132">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="cce20-133">Например, предположим, что ваш сайт использует библиотеку JavaScript стороннего поставщика, которая работает только в домене `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="cce20-133">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="cce20-134">Таким образом, вы создаете запись в `hosts` файле на компьютере разработчика, чтобы сопоставить этот домен с доменом `localhost` (например, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="cce20-134">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="cce20-135">После настройки сопоставления домена и переадресации порта просмотрите сайт на своем устройстве с Android по URL-адресу `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="cce20-135">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="cce20-136">Настройка пересылки порта на прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="cce20-136">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="cce20-137">Для сопоставления собственного домена необходимо запустить прокси-сервер на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="cce20-137">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="cce20-138">Ниже приведены примеры прокси-серверов: [Чарльз][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]и [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="cce20-138">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="cce20-139">Чтобы настроить перенаправление порта на прокси-сервер, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cce20-139">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="cce20-140">Запустите прокси-сервер и запишите порт, который он использует.</span><span class="sxs-lookup"><span data-stu-id="cce20-140">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cce20-141">Прокси-сервер и веб-сервер должны работать на разных портах.</span><span class="sxs-lookup"><span data-stu-id="cce20-141">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="cce20-142">Настройка [пересылки порта](#set-up-port-forwarding) на устройство с Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-142">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="cce20-143">В поле **Local Address (локальный адрес** ) введите `localhost:` за ним порт, на котором работает прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="cce20-143">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="cce20-144">Например, если он запущен на порте `8000` , перейдите на страницу `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="cce20-144">For example, if it is running on port `8000`, visit `localhost:8000`.</span></span>  <span data-ttu-id="cce20-145">В поле **порт устройства** введите номер, который будет прослушивать ваше устройство с Android, например `3333` .</span><span class="sxs-lookup"><span data-stu-id="cce20-145">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <span data-ttu-id="cce20-146">Настройка параметров прокси-сервера на устройстве</span><span class="sxs-lookup"><span data-stu-id="cce20-146">Configure proxy settings on your device</span></span>  

<span data-ttu-id="cce20-147">Затем необходимо настроить устройство Android для взаимодействия с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="cce20-147">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="cce20-148">На устройстве с Android перейдите в раздел **Параметры**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="cce20-148">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="cce20-149">Long-нажимайте имя сети, к которой вы подключены в данный момент.</span><span class="sxs-lookup"><span data-stu-id="cce20-149">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cce20-150">Параметры прокси-сервера применяются к каждой сети.</span><span class="sxs-lookup"><span data-stu-id="cce20-150">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="cce20-151">Выберите команду **изменить сеть**.</span><span class="sxs-lookup"><span data-stu-id="cce20-151">Select **Modify network**.</span></span>  
1.  <span data-ttu-id="cce20-152">Выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="cce20-152">Select **Advanced options**.</span></span>  <span data-ttu-id="cce20-153">Отображение параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cce20-153">The proxy settings display.</span></span>  
1.  <span data-ttu-id="cce20-154">Откройте меню **прокси** и выберите пункт **вручную**.</span><span class="sxs-lookup"><span data-stu-id="cce20-154">Select the **Proxy** menu and select **Manual**.</span></span>  
1.  <span data-ttu-id="cce20-155">В поле **имя HostName прокси-сервера** введите `localhost` .</span><span class="sxs-lookup"><span data-stu-id="cce20-155">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="cce20-156">В поле порт **прокси-сервера** введите номер порта, который вы ввели для **порта устройства** в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="cce20-156">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="cce20-157">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cce20-157">Select **Save**.</span></span>  
    
<span data-ttu-id="cce20-158">С помощью этих параметров устройство перенаправляет все свои запросы на прокси-сервер на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="cce20-158">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="cce20-159">Прокси-сервер создает запросы от имени вашего устройства, поэтому запросы к своему пользовательскому домену разрешаются надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cce20-159">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="cce20-160">Теперь вы можете получать доступ к настраиваемым доменам на устройстве с Android так же, как и на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="cce20-160">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="cce20-161">Если веб-сервер не работает с нестандартным портом, не забудьте указать порт при запросе содержимого с устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="cce20-161">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="cce20-162">Например, если ваш веб-сервер использует собственный домен `microsoft-edge.devtools` для порта, то `7331` при просмотре сайта с устройства Android вы должны использовать URL-адрес `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="cce20-162">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="cce20-163">Чтобы возобновить обычный просмотр, не забудьте вернуть параметры прокси-сервера на устройстве с Android после отключения от компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="cce20-163">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

<!--  
  


-->  
<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Прокси-сервер отладчика Чарльз"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: оптимизация веб-доставки"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Прокси-сервер для Fiddler без поддержки бесплатной отладки"  

> [!NOTE]
> <span data-ttu-id="cce20-168">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cce20-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cce20-169">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="cce20-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cce20-171">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cce20-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
