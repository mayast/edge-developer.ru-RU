---
title: Сопоставление предварительно обработанного кода с исходным кодом
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: b48c67584b3f3253ada99e32c5dabfdccb2fa4de
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581798"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="14938-103">Сопоставление предварительно обработанного кода с исходным кодом</span><span class="sxs-lookup"><span data-stu-id="14938-103">Map Preprocessed Code to Source Code</span></span>   




<span data-ttu-id="14938-104">Код на стороне клиента будет читаемым и отлаженным даже после того, как вы объедините, minify или компилируете его.</span><span class="sxs-lookup"><span data-stu-id="14938-104">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="14938-105">С помощью карт исходного кода сопоставьте исходный код с скомпилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="14938-105">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="14938-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="14938-106">Summary</span></span>  

*   <span data-ttu-id="14938-107">С помощью карт исходного кода сопоставьте minified код с исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="14938-107">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="14938-108">После этого вы сможете прочитать и отладить скомпилированный код в исходном источнике.</span><span class="sxs-lookup"><span data-stu-id="14938-108">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="14938-109">Используйте только предварительные процессоры, которые могут создавать карты исходного кода.</span><span class="sxs-lookup"><span data-stu-id="14938-109">Only use preprocessors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="14938-110">Убедитесь в том, что веб-сервер может служить исходными картами.</span><span class="sxs-lookup"><span data-stu-id="14938-110">Verify that your web server is able to serve Source Maps.</span></span>  

<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="14938-111">Приступая к работе с препроцессорами</span><span class="sxs-lookup"><span data-stu-id="14938-111">Get started with preprocessors</span></span>  

<span data-ttu-id="14938-112">В этой статье объясняется, как взаимодействовать с исходными картами JavaScript на панели "DevTools источники".</span><span class="sxs-lookup"><span data-stu-id="14938-112">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="14938-113">Использование поддерживаемой предварительной обработки</span><span class="sxs-lookup"><span data-stu-id="14938-113">Use a supported preprocessor</span></span>  

<span data-ttu-id="14938-114">Вам необходимо использовать Minifier, который способен создавать карты исходного кода.</span><span class="sxs-lookup"><span data-stu-id="14938-114">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="14938-115">Для расширенного представления просмотрите [исходные карты: языки, инструменты и другие информационные][GitHubWikiSourceMapsLanguagesTools] вики-страницы.</span><span class="sxs-lookup"><span data-stu-id="14938-115">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="14938-116">В сочетании с исходными картами обычно используются следующие типы предварительной обработки:</span><span class="sxs-lookup"><span data-stu-id="14938-116">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="14938-117">Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="14938-117">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="14938-118">Компиляторы \ ([компилятор замыканий][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="14938-118">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="14938-119">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="14938-119">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  

## <span data-ttu-id="14938-120">Карты исходного кода на панели «источники DevTools»</span><span class="sxs-lookup"><span data-stu-id="14938-120">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="14938-121">Карты исходного кода из предварительной обработки заставляют DevTools загрузить исходные файлы в дополнение к minified.</span><span class="sxs-lookup"><span data-stu-id="14938-121">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="14938-122">Затем вы можете использовать оригиналы для задания точек останова и пошагового кода.</span><span class="sxs-lookup"><span data-stu-id="14938-122">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="14938-123">В то же время Microsoft EDGE на самом деле выполняет minified код.</span><span class="sxs-lookup"><span data-stu-id="14938-123">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="14938-124">Это дает вам иллюзию запуска сайта разработки в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="14938-124">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="14938-125">При запуске карт исходного кода в DevTools следует обратить внимание на то, что JavaScript не скомпилирован и вы можете просматривать все отдельные файлы JavaScript, на которые он ссылается.</span><span class="sxs-lookup"><span data-stu-id="14938-125">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="14938-126">Используется сопоставление источника, но в фоновом режиме фактически запускается скомпилированный код.</span><span class="sxs-lookup"><span data-stu-id="14938-126">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="14938-127">Любые ошибки, журналы и точки останова сопоставлены с кодом разработки для Awesome Debugging!</span><span class="sxs-lookup"><span data-stu-id="14938-127">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="14938-128">Таким образом, это дает впечатление, что вы используете сайт разработчика в производстве.</span><span class="sxs-lookup"><span data-stu-id="14938-128">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="14938-129">Включение карт исходного кода в параметрах</span><span class="sxs-lookup"><span data-stu-id="14938-129">Enable Source Maps in settings</span></span>  

<span data-ttu-id="14938-130">Исходные карты включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14938-130">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="14938-131">, но если вы хотите дважды проверить или включить их; Сначала откройте DevTools, нажмите кнопку **Настройка DevTools и** `...` выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="14938-131">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** `...` button, and select **Settings**.</span></span>  <span data-ttu-id="14938-132">В области **Параметры** в разделе **источники**установите флажок **включить сопоставления источников JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="14938-132">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="14938-133">Вы также можете установить флажок **включить сопоставления источников CSS**.</span><span class="sxs-lookup"><span data-stu-id="14938-133">You may also check **Enable CSS Source Maps**.</span></span>  

> ##### <span data-ttu-id="14938-134">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="14938-134">Figure 1</span></span>  
> <span data-ttu-id="14938-135">Включение карт исходного кода</span><span class="sxs-lookup"><span data-stu-id="14938-135">Enable Source Maps</span></span>  
> ![Включение карт исходного кода][ImageSourceMaps]  

### <span data-ttu-id="14938-137">Отладка с помощью карт исходного кода</span><span class="sxs-lookup"><span data-stu-id="14938-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="14938-138">При включении отладки кода и сопоставления источников отображаются два места.</span><span class="sxs-lookup"><span data-stu-id="14938-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="14938-139">На консоли \ (ссылка на источник — это исходный файл, а не созданный).</span><span class="sxs-lookup"><span data-stu-id="14938-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="14938-140">При пошаговом выполнении кода \ (ссылки в стеке вызовов должны открыть исходный исходный файл)</span><span class="sxs-lookup"><span data-stu-id="14938-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  

<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## <span data-ttu-id="14938-141">@sourceURL и displayName</span><span class="sxs-lookup"><span data-stu-id="14938-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="14938-142">Несмотря на то, что она не входит в спецификацию карты источника, она `@sourceURL` позволяет упростить разработку при работе с evalами.</span><span class="sxs-lookup"><span data-stu-id="14938-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="14938-143">Этот вспомогательный элемент выглядит очень похож на `//# sourceMappingURL` свойство и на самом деле упоминается в спецификации исходной карты v3.</span><span class="sxs-lookup"><span data-stu-id="14938-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="14938-144">Включив в код следующее специальное примечание, которое будет вычислено, вы можете присвоить именам и встроенным сценариям и стилям, чтобы они отображались в DevTools с более логичными именами.</span><span class="sxs-lookup"><span data-stu-id="14938-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="14938-145">Перейдите на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="14938-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="14938-146">ролик</span><span class="sxs-lookup"><span data-stu-id="14938-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="14938-147">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="14938-147">Follow these steps.</span></span>  

1.  <span data-ttu-id="14938-148">Откройте DevTools и перейдите на панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="14938-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="14938-149">Введите имя файла в поле **_код:_** input.</span><span class="sxs-lookup"><span data-stu-id="14938-149">Enter in a filename into the **_Name your code:_** input field.</span></span>  
1.  <span data-ttu-id="14938-150">Нажмите кнопку **Compile (компилировать** ).</span><span class="sxs-lookup"><span data-stu-id="14938-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="14938-151">Появится предупреждение с вычисленной суммой из источника CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="14938-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  

<span data-ttu-id="14938-152">Если развернуть раздел **_источники_** , вы увидите новый файл с пользовательским именем, введенным ранее.</span><span class="sxs-lookup"><span data-stu-id="14938-152">If you expand the **_Sources_** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="14938-153">Если дважды щелкнуть для просмотра этого файла, он будет содержать скомпилированный код JavaScript для первоначального источника.</span><span class="sxs-lookup"><span data-stu-id="14938-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="14938-154">Однако в последней строке есть `// @sourceURL` Примечание, указывающее исходный исходный файл.</span><span class="sxs-lookup"><span data-stu-id="14938-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="14938-155">Это может помочь при отладке при работе с языковыми абстракциями.</span><span class="sxs-lookup"><span data-stu-id="14938-155">This may help you with debugging while working with language abstractions.</span></span>  

> ##### <span data-ttu-id="14938-156">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="14938-156">Figure 2</span></span>
> <span data-ttu-id="14938-157">Работа с sourceURL</span><span class="sxs-lookup"><span data-stu-id="14938-157">Working with sourceURL</span></span>  
> ![Работа с sourceURL][ImageCoffeeScript]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageSourceMaps]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png "Рисунок 1: включение карт исходного кода"  
[ImageCoffeeScript]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-coffeeeeeeee.msft.png "Рисунок 2: работа с sourceURL"  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel является компилятором JavaScript"  
[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  
[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Простой пример имени//# sourceURL eval"  
[DartMain]: https://www.dartlang.org "Язык программирования DART"  
[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/замыкание — компилятор | GitHub"  
[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  
[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Карты исходного кода: языки, инструменты и другая информация | Вики-сайт GitHub"  
[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Приступая к работе-"Google/traceur-Compiler | Вики-сайт GitHub"  
[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="14938-170">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="14938-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="14938-171">Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) и разрабатывается с помощью [Meggin Kearney][MegginKearney] \ (технический писатель \) и [пола Bakaus][PaulBakaus] \ (Open Web Developer, Google: Tools, Performance, Animation и UX).</span><span class="sxs-lookup"><span data-stu-id="14938-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="14938-173">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="14938-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
