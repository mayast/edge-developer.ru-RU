---
description: Сделайте расширение доступным для разных языков и протестируйте строки языка с помощью руководства по интернационализации.
title: Расширения-Международная связь
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571534"
---
# <span data-ttu-id="39657-104">Интернационализация</span><span class="sxs-lookup"><span data-stu-id="39657-104">Internationalization</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="39657-105">Для того чтобы расширение было доступно разным людям, важно учитывать особенности работы в других странах.</span><span class="sxs-lookup"><span data-stu-id="39657-105">In order to make your extension accessible to a variety of different people, it is important to develop with other countries in mind.</span></span> <span data-ttu-id="39657-106">С помощью расширений Microsoft EDGE можно добавлять в расширения различные языковые строки, чтобы их можно было легко изменить.</span><span class="sxs-lookup"><span data-stu-id="39657-106">Microsoft Edge extensions allows you to add different language strings to your extensions so that their language can easily be changed.</span></span>

<span data-ttu-id="39657-107">Дополнительные сведения о internationalizing вашего расширения можно найти в [руководстве по локализации](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)MDN.</span><span class="sxs-lookup"><span data-stu-id="39657-107">For more information on internationalizing your extension, check out MDN's [Internationalization guide](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization).</span></span>


## <span data-ttu-id="39657-108">Языки тестирования</span><span class="sxs-lookup"><span data-stu-id="39657-108">Testing languages</span></span>

<span data-ttu-id="39657-109">Чтобы протестировать языковые строки, сначала необходимо установить для языка интерфейса Windows язык, на котором вы хотите протестировать.</span><span class="sxs-lookup"><span data-stu-id="39657-109">To test your language strings, you first need to set the Windows display language to the language that you want to test for.</span></span>

<span data-ttu-id="39657-110">Чтобы изменить язык интерфейса Windows, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="39657-110">Follow the steps below to change the Windows display language:</span></span>

1. <span data-ttu-id="39657-111">Откройте приложение параметры.</span><span class="sxs-lookup"><span data-stu-id="39657-111">Open the Settings app.</span></span>

   ![приложение параметров](./../media/loc-settings.png)
2. <span data-ttu-id="39657-113">Выберите "язык & времени".</span><span class="sxs-lookup"><span data-stu-id="39657-113">Select "Time & language".</span></span>
3. <span data-ttu-id="39657-114">Выберите пункт "регион & язык".</span><span class="sxs-lookup"><span data-stu-id="39657-114">Select "Region & language".</span></span>
4. <span data-ttu-id="39657-115">Выберите "+ добавить язык", чтобы добавить язык в список возможных языков.</span><span class="sxs-lookup"><span data-stu-id="39657-115">Select "+ Add a language" to add the language to the list of possible languages.</span></span>
5. <span data-ttu-id="39657-116">Выберите язык из списка "языки", который вы хотите протестировать.</span><span class="sxs-lookup"><span data-stu-id="39657-116">Choose the language from the "Languages" list that you want to test.</span></span>
6. <span data-ttu-id="39657-117">Нажмите кнопку "по умолчанию" (возможно, потребуется перезагрузить компьютер).</span><span class="sxs-lookup"><span data-stu-id="39657-117">Select the "Set as default" button (you may need to restart your PC).</span></span>
7. <span data-ttu-id="39657-118">Откройте Microsoft EDGE и убедитесь в том, что строки, определенные для языкового стандарта, отображаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="39657-118">Open Microsoft Edge and verify that the strings defined for the locale appear as expected.</span></span>

<span data-ttu-id="39657-119">С помощью свойства [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) вы можете убедиться, что язык, который Microsoft Edge определяет, правильно установлен на языке интерфейса Windows.</span><span class="sxs-lookup"><span data-stu-id="39657-119">By using the [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) property, you can verify that the language Microsoft Edge has determined to be the Windows display language is correct.</span></span>

<span data-ttu-id="39657-120">Нажмите кнопку в CodePen ниже, чтобы увидеть язык интерфейса браузера.</span><span class="sxs-lookup"><span data-stu-id="39657-120">Click the button in the CodePen below to see the display language of your browser.</span></span>

<iframe height='300' scrolling='no' title='<span data-ttu-id="39657-121">Получить языковой стандарт</span><span class="sxs-lookup"><span data-stu-id="39657-121">Get locale</span></span>' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="39657-122">Ознакомьтесь со <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> статьей получение региональных параметров в </a> MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) на <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="39657-122">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'>Get locale</a>by MSEdgeDev (<a href='http://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span>
</iframe>
