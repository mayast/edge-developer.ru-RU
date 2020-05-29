---
ms.assetid: ef705c70-73f8-445b-84ed-4f83679f1980
description: Сведения о том, как объект связи в реальном времени (ORTC) обеспечивает потоковую передачу мультимедиа в режиме реального времени напрямую между веб-браузерами, мобильными устройствами или серверами.
title: Руководство по разработке — объект API RTC
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: ac033ea26fa7c1eb435b0164e5dbd2a3a5428474
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570893"
---
# <span data-ttu-id="9971f-104">API объекта RTC</span><span class="sxs-lookup"><span data-stu-id="9971f-104">Object RTC API</span></span>

<span data-ttu-id="9971f-105">Объектная связь в реальном времени (ORTC) обеспечивает потоковую передачу мультимедиа (звуковых и видеофайлов) в реальном времени напрямую между веб-браузерами, мобильными устройствами и серверами с помощью собственных API JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9971f-105">Object Real-Time Communications (ORTC) enables media (audio and/or video) to be streamed (sent and received) in real-time directly between web browsers, mobile devices, and servers via native Javascript APIs.</span></span>

> [!NOTE]
> <span data-ttu-id="9971f-106">Microsoft EDGE теперь использует ORTC для устройств с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9971f-106">Microsoft Edge now implements ORTC for Windows 10 devices.</span></span> <span data-ttu-id="9971f-107">Однако эта реализация отличается от последней версии [API ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span><span class="sxs-lookup"><span data-stu-id="9971f-107">However, this implementation differs from the most recent version of the [ORTC API](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span></span> <span data-ttu-id="9971f-108">ORTC продолжает развиваться с момента разработки и выпуска Microsoft Edge — браузер не реализует каждый объект или метод в API ORTC и включает расширения, не включенные в данный момент в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="9971f-108">ORTC has continued to evolve since the development and release of Microsoft Edge -- the browser does not implement every object or method within the ORTC API, and includes extensions not currently incorporated within the specification.</span></span> <span data-ttu-id="9971f-109">Дальнейшее развитие поможет разработчикам во всем мире для создания опыта, включающего возможность общения с пользователями Skype и другими WebRTC, совместимыми со службами связи.</span><span class="sxs-lookup"><span data-stu-id="9971f-109">Further development will continue with the goal to enable developers around the world to build experiences that include the ability to talk to Skype users and other WebRTC compatible communication services.</span></span>



<span data-ttu-id="9971f-110">Чтобы получить практический опыт с помощью ORTC, ознакомьтесь с приведенными ниже демонстрациями на тестовом диске.</span><span class="sxs-lookup"><span data-stu-id="9971f-110">To get a hands-on experience with ORTC, try out these demos on Test Drive:</span></span>
-  [<span data-ttu-id="9971f-111">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="9971f-111">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [<span data-ttu-id="9971f-112">ORTC (телефонный звонок)</span><span class="sxs-lookup"><span data-stu-id="9971f-112">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [<span data-ttu-id="9971f-113">Демонстрация с ORTC</span><span class="sxs-lookup"><span data-stu-id="9971f-113">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


<span data-ttu-id="9971f-114">Дополнительные сведения о функции ORTC можно найти на веб [-интерфейсе API ortc в Microsoft](https://go.microsoft.com/fwlink/p/?LinkID=627564) EDGE в блоге по достороне Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9971f-114">For more information about ORTC, check out [ORTC API is now available in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) on the Microsoft Edge dev blog.</span></span>


## <span data-ttu-id="9971f-115">Схема "Общие"</span><span class="sxs-lookup"><span data-stu-id="9971f-115">Overview Diagram</span></span>


<span data-ttu-id="9971f-116">На приведенной ниже схеме показана сводка по связям между объектами ORTC.</span><span class="sxs-lookup"><span data-stu-id="9971f-116">The diagram below provides a summary describing relationships between ORTC objects.</span></span> <span data-ttu-id="9971f-117">Горизонтальные или наклонные стрелки обозначают поток мультимедиа или данные, в то время как вертикальные стрелки обозначают взаимодействие с помощью методов и событий.</span><span class="sxs-lookup"><span data-stu-id="9971f-117">Horizontal or slanted arrows denote the flow of media or data, whereas vertical arrows denote interactions via methods and events.</span></span>

<span data-ttu-id="9971f-118">В параметре ORTC используются объекты "*отправитель*", "*получатель*" и "*транспорт*", которые имеют "*возможности*", описывающие, что они способны выполнить, а также "*Параметры*", которые определяют, что они используют.</span><span class="sxs-lookup"><span data-stu-id="9971f-118">ORTC uses "*sender*", "*receiver*" and "*transport*" objects, which have "*capabilities*" describing what they are capable of doing, as well as "*parameters*" which define what they are configured to do.</span></span> <span data-ttu-id="9971f-119">"*Отслеживает*", записывает и кодирует потоки мультимедиа отправителями, пересылаются по транспортам, а затем декодируется приемниками, которые визуализируют поток мультимедиа для видео-и звуковых тегов.</span><span class="sxs-lookup"><span data-stu-id="9971f-119">"*Tracks*" capture and encode media streams by senders, traveling over transports, then decoded by receivers that render the media stream tracks to video/audio tags.</span></span>

![<span data-ttu-id="9971f-120">Блок-схема Microsoft EDGE, показанная на ](./../media/ortc_diagram.png) рисунке выше, [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) кодирует дорожку, предоставленную в виде входных данных, которая переносится поверх [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) или с [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) .</span><span class="sxs-lookup"><span data-stu-id="9971f-120">Microsoft Edge ORTC Flow Diagram](./../media/ortc_diagram.png) In the figure above, the [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) encodes the track provided as input, which is transported over a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) or an [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527).</span></span> <span data-ttu-id="9971f-121">Доставка сигналов двух тонов с частотой множественной частоты (DTMF) поддерживается через [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .</span><span class="sxs-lookup"><span data-stu-id="9971f-121">Sending of Dual Tone Multi Frequency (DTMF) tones is supported via the [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496).</span></span>

<span data-ttu-id="9971f-122">Параметр [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) и используется [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) для выбора пути связи, чтобы достичь принимающего узла `RTCIceTransport` , который, в свою очередь, связан с `RTCDtlsTransport` диском a или с которого идет отключение `RTCSrtpSdesTransport` [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="9971f-122">The [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) and [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilize an [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) to select a communication path to reach the receiving peer's `RTCIceTransport`, which is in turn associated with an `RTCDtlsTransport` or `RTCSrtpSdesTransport` which de-multiplexes media to the [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span> <span data-ttu-id="9971f-123">`RTCRtpReceiver`Затем декодирует носители, создавая дорожку, которая отображается в виде звукового или видеоролика.</span><span class="sxs-lookup"><span data-stu-id="9971f-123">The `RTCRtpReceiver` then decodes media, producing a track which is rendered by an audio or video tag.</span></span>

<span data-ttu-id="9971f-124">Некоторые другие объекты также воспроизводят роль.</span><span class="sxs-lookup"><span data-stu-id="9971f-124">Several other objects also play a role.</span></span> <span data-ttu-id="9971f-125">В этой статье [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) собираются местные кандидаты ICE для использования одним [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) объектом.</span><span class="sxs-lookup"><span data-stu-id="9971f-125">The [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) gathers local ICE candidates for use by a single [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) object.</span></span> <span data-ttu-id="9971f-126">Оставшиеся разделы API-интерфейса: сведения о возможностях и *параметрах*RTP, а также о *функции* *статистики* и совместимости с [API WebRTC 1,0](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span><span class="sxs-lookup"><span data-stu-id="9971f-126">Remaining sections of the API fill in details relating to RTP *capabilities* and *parameters*, *operational statistics* and compatibility with the [WebRTC 1.0 API](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span></span>

> [!NOTE]
> <span data-ttu-id="9971f-127">Так как Microsoft EDGE не реализует канал данных, то `RTCDataChannel` и `RTCSctpTransport` объекты не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9971f-127">Since Microsoft Edge does not implement the data channel, the `RTCDataChannel` and `RTCSctpTransport` objects are not supported.</span></span>




## <span data-ttu-id="9971f-128">Компоненты, поддерживаемые в исходной реализации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9971f-128">Components supported in the initial Microsoft Edge implementation</span></span>


* **<span data-ttu-id="9971f-129">Поддержка API ORTC.</span><span class="sxs-lookup"><span data-stu-id="9971f-129">ORTC API support.</span></span>** <span data-ttu-id="9971f-130">Аудио-и видеосвязь является основным фокусом, включая следующие объекты:,,,, [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) а также [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) интерфейсы, которые не отображаются непосредственно на схеме.</span><span class="sxs-lookup"><span data-stu-id="9971f-130">Audio/video communications is the primary focus, including the following objects: [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107), [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112), [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495), [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516), [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508), as well as the [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces that are not shown directly in the diagram.</span></span>
* **<span data-ttu-id="9971f-131">Поддержка мультиплексора RTP/RTCP.</span><span class="sxs-lookup"><span data-stu-id="9971f-131">RTP/RTCP multiplexing support.</span></span>** <span data-ttu-id="9971f-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)требуется для использования с [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) .</span><span class="sxs-lookup"><span data-stu-id="9971f-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503) is required for use with the [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495).</span></span> <span data-ttu-id="9971f-133">Также поддерживается мультиплексирование/V.</span><span class="sxs-lookup"><span data-stu-id="9971f-133">A/V multiplexing is also supported.</span></span>
* **<span data-ttu-id="9971f-134">Поддержка STUN/onturn/ICE.</span><span class="sxs-lookup"><span data-stu-id="9971f-134">STUN/TURN/ICE support.</span></span>** <span data-ttu-id="9971f-135">Поддерживаются STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) , а также Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621).</span><span class="sxs-lookup"><span data-stu-id="9971f-135">STUN [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), TURN [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) as well as ICE [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621), are supported.</span></span> <span data-ttu-id="9971f-136">В рамках ICE поддерживается регулярный Nomination, при условии, что активно Nomination частично поддерживается (получатель).</span><span class="sxs-lookup"><span data-stu-id="9971f-136">Within ICE, regular nomination is supported, with aggressive nomination partially supported (as a receiver).</span></span> <span data-ttu-id="9971f-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) поддерживается на основе DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span><span class="sxs-lookup"><span data-stu-id="9971f-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) is supported, based on DTLS 1.0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span></span>
* **<span data-ttu-id="9971f-138">Поддержка кодека.</span><span class="sxs-lookup"><span data-stu-id="9971f-138">Codec support.</span></span>** <span data-ttu-id="9971f-139">Для [audio codecs](https://msdn.microsoft.com/library/Mt599587)аудиокодеков поддерживаются g. 711, g. 722, Opus и Silk.</span><span class="sxs-lookup"><span data-stu-id="9971f-139">For [audio codecs](https://msdn.microsoft.com/library/Mt599587), we support G.711, G.722, Opus and SILK.</span></span> <span data-ttu-id="9971f-140">Кроме того, мы поддерживаем помехи (CN) и DTMF в соответствии с требованиями к звуку в RTCWEB.</span><span class="sxs-lookup"><span data-stu-id="9971f-140">We also support Comfort Noise (CN) and DTMF according to the RTCWEB audio requirements.</span></span> <span data-ttu-id="9971f-141">Для видео в настоящее время поддерживается [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) кодек, используемый в службах Skype, поддерживающий расширенные функции, такие как Simulcast, масштабируемый код видео и исправление ошибок переадресации.</span><span class="sxs-lookup"><span data-stu-id="9971f-141">For video we currently support the [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec used by Skype services, supporting advanced features such as simulcast, scalable video coding and forward error correction.</span></span> <span data-ttu-id="9971f-142">Мы работаем над тем, чтобы обеспечить взаимодействие с видео с помощью функции H. 264.</span><span class="sxs-lookup"><span data-stu-id="9971f-142">We're working toward to enabling interoperable video with H.264.</span></span>

> [!NOTE]
> <span data-ttu-id="9971f-143">Если вы знакомы с реализациями WebRTC 1,0 и заинтересованы в эволюции поддержки объектов в WebRTC 1,0 и ORTC, мы рекомендуем использовать следующую презентацию на веб-сайте Google, Microsoft и Hookflash из конференции 2014 IIT RTC: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".</span><span class="sxs-lookup"><span data-stu-id="9971f-143">If you are familiar with WebRTC 1.0 implementations, and are interested in the evolution of object support within WebRTC 1.0 and ORTC, we recommend the following presentation by Google, Microsoft, and Hookflash from the 2014 IIT RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)."</span></span>




## <span data-ttu-id="9971f-144">Потоки кода на уровне приложения для связи с 1:1</span><span class="sxs-lookup"><span data-stu-id="9971f-144">App level code flow for 1:1 communications</span></span>


<span data-ttu-id="9971f-145">В этом сценарии два компьютера с Windows 10 будут выступать в качестве канала передачи данных между одноранговыми компьютерами с помощью веб-сервера в качестве каналов сигналов для обмена данными между одноранговой связью, чтобы между ними можно было установить соединение.</span><span class="sxs-lookup"><span data-stu-id="9971f-145">For this scenario, two Windows 10 machines will act as two peers with a webserver as the signaling channel to exchange information between the peers so that a connection may be established between them.</span></span>

<span data-ttu-id="9971f-146">Действия, описанные ниже, выполняются для операций, сделанных одним одноранговым узлом.</span><span class="sxs-lookup"><span data-stu-id="9971f-146">The steps below are scoped to operations taken by one peer.</span></span> <span data-ttu-id="9971f-147">Оба одноранговых элемента должны пройти аналогичные шаги, чтобы настроить связь с 1:1.</span><span class="sxs-lookup"><span data-stu-id="9971f-147">Both peers must go through similar steps in order to set up the 1:1 communications.</span></span> <span data-ttu-id="9971f-148">Чтобы лучше понять фрагменты кода, приведенные ниже, обратитесь к статье [демонстрация тестового диска Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="9971f-148">To make better sense out of the code snippets below, refer to the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

<span data-ttu-id="9971f-149">В этом примере используется мультиплексирование аудио-видео и RTP/RTCP, поэтому вы увидите только один транспорт ICE и DTLS, который используется для передачи пакетов RTP и RTCP для аудио-и видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="9971f-149">This example uses audio-video and RTP/RTCP multiplexing, so you will see only a single ICE and DTLS transport, used to transport RTP and RTCP packets for both audio and video.</span></span>

`Step #1.` <span data-ttu-id="9971f-150">Создание [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) объекта (например, [API для захвата и потоковой передачи мультимедиа](./../multimedia/media-Capture-and-Streams.md)) одной звуковой дорожки и одной видеодорожки.</span><span class="sxs-lookup"><span data-stu-id="9971f-150">Create [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) object (i.e. [Media Capture and Streams API](./../multimedia/media-Capture-and-Streams.md)) with one audio track and one video track.</span></span>

```js
navigator.MediaDevices.getUserMedia ({
    "audio": true,
    "video": {
        width: 640,
        height: 360,
        facingMode: "user"
    }
}).then(
    gotStream
).catch(
    gotMediaError
);

function gotStream(stream) {
    var mediaStreamLocal = stream;
    …
}
```

`Step #2.` <span data-ttu-id="9971f-151">Создавайте [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) и включайте локальную функцию [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) для оповещения на удаленном одноранговом узле.</span><span class="sxs-lookup"><span data-stu-id="9971f-151">Create the [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx), and enable local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) to be signaled to remote peer.</span></span>

```js
var iceOptions = new RTCIceGatherOptions;
iceOptions.gatherPolicy = "all";
iceOptions.iceservers = ... ;
var iceGathr = new RTCIceGatherer(iceOptions);
iceGathr.onlocalcandidate = function(evt) {
    mySignaller.signalMessage({
        "candidate": evt.candidate
    });
};
```

<span data-ttu-id="9971f-152">Для защиты конфиденциальности пользователей в Microsoft Edge появился параметр, позволяющий пользователю управлять тем, какие IP-адреса локальных узлов могут предоставляться [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) объектами.</span><span class="sxs-lookup"><span data-stu-id="9971f-152">To help protect user privacy, Microsoft Edge introduces an option that allows a user to control whether local host IP addresses can be exposed by the [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objects.</span></span> <span data-ttu-id="9971f-153">Для этого параметра будет указан интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9971f-153">An interface option will be provided to toggle this setting.</span></span>

<span data-ttu-id="9971f-154">В [демонстрационном видеоролике Microsoft Edge для тестового диска](https://go.microsoft.com/fwlink/p/?LinkID=627635)установлен сервер.</span><span class="sxs-lookup"><span data-stu-id="9971f-154">In the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635), a TURN server has been set up.</span></span> <span data-ttu-id="9971f-155">Этот сервер имеет очень ограниченную пропускную способность, поэтому она ограничивается только демонстрационной страницей.</span><span class="sxs-lookup"><span data-stu-id="9971f-155">This TURN server has a very limited throughput, so is limited to only demo page use.</span></span>

`Step #3.` <span data-ttu-id="9971f-156">Создание [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) звуковых и видеофайлов и подготовка к удаленному элементу управления [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) с помощью транспорта Ice.</span><span class="sxs-lookup"><span data-stu-id="9971f-156">Create the [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) for audio and video, and prepare to handle remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) on the ICE transport.</span></span>

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

<span data-ttu-id="9971f-157">Еще один способ — собрать все удаленные кандидаты ICE в массив `remoteCandidates` и позвонить `iceTr.setRemoteCandidates(remoteCandidates)` , чтобы добавить все удаленные кандидаты.</span><span class="sxs-lookup"><span data-stu-id="9971f-157">Another option here is to accumulate all the remote ICE candidates into an array `remoteCandidates` and call `iceTr.setRemoteCandidates(remoteCandidates)` to add all the remote candidates together.</span></span>

`Step #4.` <span data-ttu-id="9971f-158">Создайте транспорт DTLS.</span><span class="sxs-lookup"><span data-stu-id="9971f-158">Create the DTLS transport.</span></span>

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` <span data-ttu-id="9971f-159">Создайте объекты отправителя и получателя.</span><span class="sxs-lookup"><span data-stu-id="9971f-159">Create the sender and receiver objects.</span></span>

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

<span data-ttu-id="9971f-160">Шаг #6.</span><span class="sxs-lookup"><span data-stu-id="9971f-160">Step #6.</span></span> <span data-ttu-id="9971f-161">Получение возможностей получателя и отправителя.</span><span class="sxs-lookup"><span data-stu-id="9971f-161">Retrieve the receiver and sender capabilities.</span></span>

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` <span data-ttu-id="9971f-162">Можно обмениваться параметрами ICE/DTLS и функциями отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="9971f-162">ICE/DTLS parameters and Send/Receive capabilities can be exchanged.</span></span>

```js
mySignaller.signalMessage({
    "ice": iceGathr.getLocalParameters(),
    "dtls": dtlsTr.getLocalParameters(),
    "recvAudioCaps": recvAudioCaps,
    "recvVideoCaps": recvVideoCaps,
    "sendAudioCaps": sendAudioCaps,
    "sendVideoCaps": sendVideoCaps
};
```

`Step #8.` <span data-ttu-id="9971f-163">Получение удаленных параметров, запуск [`ICE`](https://msdn.microsoft.com/library/Mt433112) и [`DTLS`](https://msdn.microsoft.com/library/Mt502495) транспортировка, Настройка параметров отправки и получения звука и видео.</span><span class="sxs-lookup"><span data-stu-id="9971f-163">Get remote params, start the [`ICE`](https://msdn.microsoft.com/library/Mt433112) and [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, and set the audio and video send and receive parameters.</span></span>

```js
mySignaller.onRemoteParams = function(params) {
    // The responder answers with its preferences, parameters and capabilities
    // Derive the send and receive parameters.
    var audioSendParams = myCapsToSendParams(sendAudioCaps, params.recvAudioCaps);
    var videoSendParams = myCapsToSendParams(sendVideoCaps, params.recvVideoCaps);
    var audioRecvParams = myCapsToRecvParams(recvAudioCaps, params.sendAudioCaps);
    var videoRecvParams = myCapsToRecvParams(recvVideoCaps, params.sendVideoCaps);
    iceTr.start(iceGathr, params.ice, RTCIceRole.controlling);
    dtlsTr.start(params.dtls);
    audioSender.send(audioSendParams);
    videoSender.send(videoSendParams);
    audioReceiver.receive(audioRecvParams);
    videoReceiver.receive(videoRecvParams);
};
```

<span data-ttu-id="9971f-164">Ниже приведена схема вспомогательных функций.</span><span class="sxs-lookup"><span data-stu-id="9971f-164">Below is a skeleton of the helper functions.</span></span> <span data-ttu-id="9971f-165">Ознакомьтесь с дополнительными сведениями в [демонстрационном видеоролике Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="9971f-165">Find more details in the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

```js
RTCRtpParameters function myCapsToSendParams (RTCRtpCapabilities sendCaps, RTCRtpCapabilities remoteRecvCaps) {
    // Function returning the sender RTCRtpParameters, based on intersection of the local sender and remote receiver capabilities.
    // Steps to be followed:
    // 1. Determine the RTP features that the receiver and sender have in common.
    // 2. Determine the codecs that the sender and receiver have in common.
    // 3. Within each common codec, determine the common formats and rtcpFeedback mechanisms.
    // 4. Determine the payloadType to be used, based on the receiver preferredPayloadType.
    // 5. Set RTCRtcpParameters such as mux to their default values.  
}

RTCRtpParameters function myCapsToRecvParams(RTCRtpCapabilities recvCaps, RTCRtpCapabilities remoteSendCaps) {
    return myCapsToSendParams(remoteSendCaps, recvCaps);
}
```

`Step #9.` <span data-ttu-id="9971f-166">Визуализируйте и воспроизводите удаленные потоки мультимедиа с помощью тега видео.</span><span class="sxs-lookup"><span data-stu-id="9971f-166">Render and play the remote media stream tracks through a video tag.</span></span>

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

<span data-ttu-id="9971f-167">После того как вы знакомы с настройкой вызовов 1:1, примените одинаковые принципы для настройки малых групповых звонков с использованием топологии сетки, в которой каждый из них будет иметь соединение 1:1 с другими членами группы.</span><span class="sxs-lookup"><span data-stu-id="9971f-167">Once familiar with setting up 1:1 calls, apply the same principles to set up small group calls using a mesh topology, where each peer will have a 1:1 connection with the rest of the group.</span></span> <span data-ttu-id="9971f-168">Так как параллельное ветвление не поддерживается в платформе Microsoft EDGE, это должно обрабатываться с помощью сигналов 1:1, поэтому [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) для каждого подключения будут использоваться независимые и объекты.</span><span class="sxs-lookup"><span data-stu-id="9971f-168">Since parallel forking is not supported on the Microsoft Edge platform, this should be handled via 1:1 signaling, so that independent [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) and [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objects will be used for each connection.</span></span>

## <span data-ttu-id="9971f-169">Сведения о реализации в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9971f-169">Implementation details in Microsoft Edge</span></span>


<span data-ttu-id="9971f-170">Спецификация ORTC была сравнительно стабильной, так как Группа сообщества "ORTC" выдавала "вызов для реализаций" и существенные проблемы на уровне API JavaScript не предусмотрены.</span><span class="sxs-lookup"><span data-stu-id="9971f-170">The ORTC spec has been relatively stable since the ORTC Community Group issued the "Call for Implementations," and significant challenges at the JavaScript API level are not expected.</span></span> <span data-ttu-id="9971f-171">На данный момент реализация Microsoft Edge была выпущена для тестирования взаимодействия между браузерами на уровне протоколов.</span><span class="sxs-lookup"><span data-stu-id="9971f-171">Based on this, Microsoft Edge implementation has been released for cross-browser interoperability testing at the protocol level.</span></span>

<span data-ttu-id="9971f-172">Некоторые ограничения в реализации Microsoft Edge должны быть указаны ниже.</span><span class="sxs-lookup"><span data-stu-id="9971f-172">A few limitations in the Microsoft Edge implementation should be noted:</span></span>

* `RTCIceTransportController` <span data-ttu-id="9971f-173">не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9971f-173">is not supported.</span></span> <span data-ttu-id="9971f-174">Реализация Microsoft Edge обстает закреплением и разморожением на основе каждого транспорта, так что заказать все это `IceTransports` не требуется.</span><span class="sxs-lookup"><span data-stu-id="9971f-174">Microsoft Edge implementation handles ICE freezing/unfreezing on a per-transport basis, so that ordering all the `IceTransports` is not necessary.</span></span> <span data-ttu-id="9971f-175">Этот подход должен взаимодействовать с существующими реализациями.</span><span class="sxs-lookup"><span data-stu-id="9971f-175">This approach should interoperate with existing implementations.</span></span>
* `RtpListener` <span data-ttu-id="9971f-176">пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9971f-176">is not yet supported.</span></span> <span data-ttu-id="9971f-177">Это означает, что SSRCs (потоки и источники синхронизации) должны быть указаны заранее в [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="9971f-177">This means that SSRCs (stream and synchronization sources) need to be specified in advance within the [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span>
* <span data-ttu-id="9971f-178">Ветвление пока не поддерживается ни в `IceTransport` , ни в `IceGatherer` `DtlsTransport`</span><span class="sxs-lookup"><span data-stu-id="9971f-178">Forking is not yet supported in either `IceTransport`, `IceGatherer`, or `DtlsTransport`.</span></span> <span data-ttu-id="9971f-179">Решение для `DtlsTransport` разветвления по-прежнему находится в группе сообщество "ORTC".</span><span class="sxs-lookup"><span data-stu-id="9971f-179">The solution to `DtlsTransport` forking is still under discussion in the ORTC Community Group.</span></span>
* <span data-ttu-id="9971f-180">Протокол RTP/RTCP не `DtlsTransport` поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9971f-180">RTP/RTCP non-mux with `DtlsTransport` is not yet supported.</span></span> <span data-ttu-id="9971f-181">При использовании `DtlsTransport` приложения необходимо поддерживать RTP/RTCP мультиплексор.</span><span class="sxs-lookup"><span data-stu-id="9971f-181">When using `DtlsTransport` your application will need to support RTP/RTCP mux.</span></span>
* <span data-ttu-id="9971f-182">В [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) приложение Microsoft EDGE в настоящее время пропускает большинство элементов управления качеством кодирования, но для них требуется установка атрибутов "Active" и "SSRC".</span><span class="sxs-lookup"><span data-stu-id="9971f-182">In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx), Microsoft Edge currently ignores most of the encoding quality controls, but does require setting the 'active' and 'ssrc' attributes.</span></span>
* <span data-ttu-id="9971f-183">`icecandidatepairchanged`Событие пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9971f-183">The `icecandidatepairchanged` event is not yet supported.</span></span> <span data-ttu-id="9971f-184">Сведения о паре кандидатов можно извлечь с помощью [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) метода.</span><span class="sxs-lookup"><span data-stu-id="9971f-184">You can extract the candidate pair information through the [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) method.</span></span>
* <span data-ttu-id="9971f-185">Microsoft EDGE в настоящее время не поддерживает какую бы то ни было из `DataChannel` функциональных возможностей, которые в настоящее время определены в спецификации ORTC.</span><span class="sxs-lookup"><span data-stu-id="9971f-185">Microsoft Edge currently does not support any of the `DataChannel` functionality currently defined in the ORTC spec.</span></span>

#### <span data-ttu-id="9971f-186">Заглядывая вперед</span><span class="sxs-lookup"><span data-stu-id="9971f-186">Looking forward</span></span>

<span data-ttu-id="9971f-187">Реализация Microsoft Edge по-прежнему является ранней, предполагается, что функция продолжает расти в течение ближайших месяцев.</span><span class="sxs-lookup"><span data-stu-id="9971f-187">Microsoft Edge implementation is still early, expect the feature set to continue to grow in the coming months.</span></span> <span data-ttu-id="9971f-188">Цель реализации Microsoft Edge – это взаимодействие через Интернет сегодня, а также с отраслевыми организациями в реальном времени в долгосрочной перспективе.</span><span class="sxs-lookup"><span data-stu-id="9971f-188">The goal for Microsoft Edge implementation is interoperability across the web today as well as with the real-time communications industry in the long term.</span></span>



## <span data-ttu-id="9971f-189">Справочные материалы по API</span><span class="sxs-lookup"><span data-stu-id="9971f-189">API reference</span></span>

[<span data-ttu-id="9971f-190">ORTC (объектная связь в реальном времени)</span><span class="sxs-lookup"><span data-stu-id="9971f-190">ORTC (Object Real-Time Communications)</span></span>](https://msdn.microsoft.com/library/Mt433097)

## <span data-ttu-id="9971f-191">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="9971f-191">Demos</span></span>

[<span data-ttu-id="9971f-192">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="9971f-192">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[<span data-ttu-id="9971f-193">ORTC (телефонный звонок)</span><span class="sxs-lookup"><span data-stu-id="9971f-193">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[<span data-ttu-id="9971f-194">Демонстрация с ORTC</span><span class="sxs-lookup"><span data-stu-id="9971f-194">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## <span data-ttu-id="9971f-195">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9971f-195">Related topics</span></span>

[<span data-ttu-id="9971f-196">API ORTC теперь доступен в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9971f-196">ORTC API is now available in Microsoft Edge</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[<span data-ttu-id="9971f-197">SimpleWebRTC: Используйте API-интерфейсы Microsoft EDGE и API WebRTC в Chrome и Firefox для проведения телеконференций в разных браузерах.</span><span class="sxs-lookup"><span data-stu-id="9971f-197">SimpleWebRTC: Use Microsoft Edge's ORTC API and the WebRTC APIs in Chrome and Firefox to make cross-browser conference calls.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[<span data-ttu-id="9971f-198">Возможность бесперебойной связи через Интернет с помощью Skype, Skype для бизнеса и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9971f-198">Enabling Seamless Communication Experiences for the Web with Skype, Skype for Business, and Microsoft Edge.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[<span data-ttu-id="9971f-199">ГРУППА СООБЩЕСТВА "ORTC (ОБЪЕКТНАЯ СВЯЗЬ В РЕАЛЬНОМ ВРЕМЕНИ)"</span><span class="sxs-lookup"><span data-stu-id="9971f-199">ORTC (OBJECT REAL-TIME COMMUNICATIONS) COMMUNITY GROUP</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## <span data-ttu-id="9971f-200">Specification</span><span class="sxs-lookup"><span data-stu-id="9971f-200">Specification</span></span>

[<span data-ttu-id="9971f-201">API объекта реального времени (ORTC) объектов W3C для WebRTC</span><span class="sxs-lookup"><span data-stu-id="9971f-201">W3C Object RTC (ORTC) API for WebRTC</span></span>](http://draft.ortc.org/)  
