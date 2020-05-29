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
# API объекта RTC

Объектная связь в реальном времени (ORTC) обеспечивает потоковую передачу мультимедиа (звуковых и видеофайлов) в реальном времени напрямую между веб-браузерами, мобильными устройствами и серверами с помощью собственных API JavaScript.

> [!NOTE]
> Microsoft EDGE теперь использует ORTC для устройств с Windows 10. Однако эта реализация отличается от последней версии [API ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096). ORTC продолжает развиваться с момента разработки и выпуска Microsoft Edge — браузер не реализует каждый объект или метод в API ORTC и включает расширения, не включенные в данный момент в спецификацию. Дальнейшее развитие поможет разработчикам во всем мире для создания опыта, включающего возможность общения с пользователями Skype и другими WebRTC, совместимыми со службами связи.



Чтобы получить практический опыт с помощью ORTC, ознакомьтесь с приведенными ниже демонстрациями на тестовом диске.
-  [SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [ORTC (телефонный звонок)](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [Демонстрация с ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


Дополнительные сведения о функции ORTC можно найти на веб [-интерфейсе API ortc в Microsoft](https://go.microsoft.com/fwlink/p/?LinkID=627564) EDGE в блоге по достороне Майкрософт.


## Схема "Общие"


На приведенной ниже схеме показана сводка по связям между объектами ORTC. Горизонтальные или наклонные стрелки обозначают поток мультимедиа или данные, в то время как вертикальные стрелки обозначают взаимодействие с помощью методов и событий.

В параметре ORTC используются объекты "*отправитель*", "*получатель*" и "*транспорт*", которые имеют "*возможности*", описывающие, что они способны выполнить, а также "*Параметры*", которые определяют, что они используют. "*Отслеживает*", записывает и кодирует потоки мультимедиа отправителями, пересылаются по транспортам, а затем декодируется приемниками, которые визуализируют поток мультимедиа для видео-и звуковых тегов.

![Блок-схема Microsoft EDGE, показанная на ](./../media/ortc_diagram.png) рисунке выше, [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) кодирует дорожку, предоставленную в виде входных данных, которая переносится поверх [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) или с [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) . Доставка сигналов двух тонов с частотой множественной частоты (DTMF) поддерживается через [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .

Параметр [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) и используется [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) для выбора пути связи, чтобы достичь принимающего узла `RTCIceTransport` , который, в свою очередь, связан с `RTCDtlsTransport` диском a или с которого идет отключение `RTCSrtpSdesTransport` [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) . `RTCRtpReceiver`Затем декодирует носители, создавая дорожку, которая отображается в виде звукового или видеоролика.

Некоторые другие объекты также воспроизводят роль. В этой статье [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) собираются местные кандидаты ICE для использования одним [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) объектом. Оставшиеся разделы API-интерфейса: сведения о возможностях и *параметрах*RTP, а также о *функции* *статистики* и совместимости с [API WebRTC 1,0](https://go.microsoft.com/fwlink/p/?LinkID=627573).

> [!NOTE]
> Так как Microsoft EDGE не реализует канал данных, то `RTCDataChannel` и `RTCSctpTransport` объекты не поддерживаются.




## Компоненты, поддерживаемые в исходной реализации Microsoft Edge


* **Поддержка API ORTC.** Аудио-и видеосвязь является основным фокусом, включая следующие объекты:,,,, [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) а также [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) интерфейсы, которые не отображаются непосредственно на схеме.
* **Поддержка мультиплексора RTP/RTCP.** [`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)требуется для использования с [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) . Также поддерживается мультиплексирование/V.
* **Поддержка STUN/onturn/ICE.** Поддерживаются STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) , а также Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621). В рамках ICE поддерживается регулярный Nomination, при условии, что активно Nomination частично поддерживается (получатель). DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) поддерживается на основе DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).
* **Поддержка кодека.** Для [audio codecs](https://msdn.microsoft.com/library/Mt599587)аудиокодеков поддерживаются g. 711, g. 722, Opus и Silk. Кроме того, мы поддерживаем помехи (CN) и DTMF в соответствии с требованиями к звуку в RTCWEB. Для видео в настоящее время поддерживается [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) кодек, используемый в службах Skype, поддерживающий расширенные функции, такие как Simulcast, масштабируемый код видео и исправление ошибок переадресации. Мы работаем над тем, чтобы обеспечить взаимодействие с видео с помощью функции H. 264.

> [!NOTE]
> Если вы знакомы с реализациями WebRTC 1,0 и заинтересованы в эволюции поддержки объектов в WebRTC 1,0 и ORTC, мы рекомендуем использовать следующую презентацию на веб-сайте Google, Microsoft и Hookflash из конференции 2014 IIT RTC: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".




## Потоки кода на уровне приложения для связи с 1:1


В этом сценарии два компьютера с Windows 10 будут выступать в качестве канала передачи данных между одноранговыми компьютерами с помощью веб-сервера в качестве каналов сигналов для обмена данными между одноранговой связью, чтобы между ними можно было установить соединение.

Действия, описанные ниже, выполняются для операций, сделанных одним одноранговым узлом. Оба одноранговых элемента должны пройти аналогичные шаги, чтобы настроить связь с 1:1. Чтобы лучше понять фрагменты кода, приведенные ниже, обратитесь к статье [демонстрация тестового диска Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).

В этом примере используется мультиплексирование аудио-видео и RTP/RTCP, поэтому вы увидите только один транспорт ICE и DTLS, который используется для передачи пакетов RTP и RTCP для аудио-и видеофайлов.

`Step #1.` Создание [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) объекта (например, [API для захвата и потоковой передачи мультимедиа](./../multimedia/media-Capture-and-Streams.md)) одной звуковой дорожки и одной видеодорожки.

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

`Step #2.` Создавайте [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) и включайте локальную функцию [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) для оповещения на удаленном одноранговом узле.

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

Для защиты конфиденциальности пользователей в Microsoft Edge появился параметр, позволяющий пользователю управлять тем, какие IP-адреса локальных узлов могут предоставляться [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) объектами. Для этого параметра будет указан интерфейс.

В [демонстрационном видеоролике Microsoft Edge для тестового диска](https://go.microsoft.com/fwlink/p/?LinkID=627635)установлен сервер. Этот сервер имеет очень ограниченную пропускную способность, поэтому она ограничивается только демонстрационной страницей.

`Step #3.` Создание [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) звуковых и видеофайлов и подготовка к удаленному элементу управления [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) с помощью транспорта Ice.

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

Еще один способ — собрать все удаленные кандидаты ICE в массив `remoteCandidates` и позвонить `iceTr.setRemoteCandidates(remoteCandidates)` , чтобы добавить все удаленные кандидаты.

`Step #4.` Создайте транспорт DTLS.

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` Создайте объекты отправителя и получателя.

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

Шаг #6. Получение возможностей получателя и отправителя.

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` Можно обмениваться параметрами ICE/DTLS и функциями отправки и получения.

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

`Step #8.` Получение удаленных параметров, запуск [`ICE`](https://msdn.microsoft.com/library/Mt433112) и [`DTLS`](https://msdn.microsoft.com/library/Mt502495) транспортировка, Настройка параметров отправки и получения звука и видео.

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

Ниже приведена схема вспомогательных функций. Ознакомьтесь с дополнительными сведениями в [демонстрационном видеоролике Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).

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

`Step #9.` Визуализируйте и воспроизводите удаленные потоки мультимедиа с помощью тега видео.

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

После того как вы знакомы с настройкой вызовов 1:1, примените одинаковые принципы для настройки малых групповых звонков с использованием топологии сетки, в которой каждый из них будет иметь соединение 1:1 с другими членами группы. Так как параллельное ветвление не поддерживается в платформе Microsoft EDGE, это должно обрабатываться с помощью сигналов 1:1, поэтому [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) для каждого подключения будут использоваться независимые и объекты.

## Сведения о реализации в Microsoft Edge


Спецификация ORTC была сравнительно стабильной, так как Группа сообщества "ORTC" выдавала "вызов для реализаций" и существенные проблемы на уровне API JavaScript не предусмотрены. На данный момент реализация Microsoft Edge была выпущена для тестирования взаимодействия между браузерами на уровне протоколов.

Некоторые ограничения в реализации Microsoft Edge должны быть указаны ниже.

* `RTCIceTransportController` не поддерживается. Реализация Microsoft Edge обстает закреплением и разморожением на основе каждого транспорта, так что заказать все это `IceTransports` не требуется. Этот подход должен взаимодействовать с существующими реализациями.
* `RtpListener` пока не поддерживается. Это означает, что SSRCs (потоки и источники синхронизации) должны быть указаны заранее в [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .
* Ветвление пока не поддерживается ни в `IceTransport` , ни в `IceGatherer` `DtlsTransport` Решение для `DtlsTransport` разветвления по-прежнему находится в группе сообщество "ORTC".
* Протокол RTP/RTCP не `DtlsTransport` поддерживается. При использовании `DtlsTransport` приложения необходимо поддерживать RTP/RTCP мультиплексор.
* В [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) приложение Microsoft EDGE в настоящее время пропускает большинство элементов управления качеством кодирования, но для них требуется установка атрибутов "Active" и "SSRC".
* `icecandidatepairchanged`Событие пока не поддерживается. Сведения о паре кандидатов можно извлечь с помощью [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) метода.
* Microsoft EDGE в настоящее время не поддерживает какую бы то ни было из `DataChannel` функциональных возможностей, которые в настоящее время определены в спецификации ORTC.

#### Заглядывая вперед

Реализация Microsoft Edge по-прежнему является ранней, предполагается, что функция продолжает расти в течение ближайших месяцев. Цель реализации Microsoft Edge – это взаимодействие через Интернет сегодня, а также с отраслевыми организациями в реальном времени в долгосрочной перспективе.



## Справочные материалы по API

[ORTC (объектная связь в реальном времени)](https://msdn.microsoft.com/library/Mt433097)

## Демонстрационные примеры

[SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[ORTC (телефонный звонок)](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[Демонстрация с ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## Статьи по теме

[API ORTC теперь доступен в Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[SimpleWebRTC: Используйте API-интерфейсы Microsoft EDGE и API WebRTC в Chrome и Firefox для проведения телеконференций в разных браузерах.](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[Возможность бесперебойной связи через Интернет с помощью Skype, Skype для бизнеса и Microsoft Edge.](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[ГРУППА СООБЩЕСТВА "ORTC (ОБЪЕКТНАЯ СВЯЗЬ В РЕАЛЬНОМ ВРЕМЕНИ)"](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## Specification

[API объекта реального времени (ORTC) объектов W3C для WebRTC](http://draft.ortc.org/)  
