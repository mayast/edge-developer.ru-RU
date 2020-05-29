---
description: 'Сведения о том, как ориентироваться на разные механизмы JavaScript для Windows 10. '
title: Настройка Microsoft EDGE и устаревших модулей в API JsRT | Документы Microsoft
ms.custom: ''
ms.date: 03/05/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ed0dc8c67b8189a7433d52185aa995997edb70a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571319"
---
# <span data-ttu-id="a4809-103">Настройка Microsoft EDGE и устаревших обработчиков в API JsRT</span><span class="sxs-lookup"><span data-stu-id="a4809-103">Targeting Microsoft Edge vs. Legacy Engines in JsRT APIs</span></span>

<span data-ttu-id="a4809-104">Windows 10 поддерживает два разных обработчика JavaScript:</span><span class="sxs-lookup"><span data-stu-id="a4809-104">Windows 10 supports two different JavaScript engines:</span></span>

-   <span data-ttu-id="a4809-105">Старый обработчик Chakra (также называемый *устаревшим модулем* или Jscript9. dll ниже), который поставляется вместе с Internet Explorer 11 и поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="a4809-105">The old Chakra engine (also called the *legacy engine* or jscript9.dll below) that ships with and supports Internet Explorer 11.</span></span> <span data-ttu-id="a4809-106">Этот обработчик зафиксирован в течение времени и останется без изменений в выпуске Win 8.1/IE11.</span><span class="sxs-lookup"><span data-stu-id="a4809-106">This engine is frozen in time and will remain fundamentally unchanged from Win8.1/IE11 release.</span></span>  
  
-   <span data-ttu-id="a4809-107">Новый обработчик Chakra (также называемый *ядром пограничного* приложения или Chakra. dll), который поставляется вместе с новым браузером в Windows 10, Microsoft EDGE, и поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="a4809-107">The new Chakra engine (also called the *Edge engine* or chakra.dll below) that ships with and supports the new browser in Windows 10, Microsoft Edge.</span></span> <span data-ttu-id="a4809-108">Этот обработчик будет постоянно обновляться и будет поддерживать обработчик [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) "живых".</span><span class="sxs-lookup"><span data-stu-id="a4809-108">This engine will be continually updated and will support a "living" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) engine.</span></span> <span data-ttu-id="a4809-109">Работа работающего подсистемы Microsoft EDGE, в отличие от устаревшего обработчика, не перенесет функцию Microsoft Edge Engine, чтобы принять участие в программе.</span><span class="sxs-lookup"><span data-stu-id="a4809-109">A living Microsoft Edge engine implies that unlike the legacy engine, the Microsoft Edge engine would not carry forward any form of versioning script functionality to opt into.</span></span>  
  
 <span data-ttu-id="a4809-110">Когда вы создаете приложение с помощью API размещения среды выполнения JavaScript (JsRT), вы можете выбрать для него назначение либо устаревшей, либо обработчиком Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4809-110">When creating an app using the JavaScript Runtime Hosting (JsRT) API, you can choose to target either the legacy or the Microsoft Edge engine.</span></span>  
  
-   <span data-ttu-id="a4809-111">Если необходимо обменяться обратной совместимостью с существующими приложениями, необходимо выбрать старый механизм.</span><span class="sxs-lookup"><span data-stu-id="a4809-111">If you need to emphasize backward compatibility of your existing applications, target the legacy engine.</span></span>  
  
-   <span data-ttu-id="a4809-112">Если вы хотите, чтобы ваше приложение было переадресовано для просмотра и поддерживало новые возможности JavaScript по мере их выпуска (например, ECMAScript 6), нацеливание на ядро Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4809-112">If you want your app to be forward looking and support new JavaScript features as they are released (for example, ECMAScript 6), target the Microsoft Edge engine.</span></span>  
  
 <span data-ttu-id="a4809-113">Этот раздел содержит подробные сведения о том, как ориентироваться на разные ядра.</span><span class="sxs-lookup"><span data-stu-id="a4809-113">This topic includes details that describe how to target the different engines.</span></span>  
  
## <span data-ttu-id="a4809-114">Назначение предпочтительной версии</span><span class="sxs-lookup"><span data-stu-id="a4809-114">Target your preferred version</span></span>  
 <span data-ttu-id="a4809-115">При создании приложения вы можете выбрать версию JsRT, которая поддерживает либо обработчик Microsoft EDGE, либо старый механизм.</span><span class="sxs-lookup"><span data-stu-id="a4809-115">When creating an app, you can select the version of the JsRT that supports either the Microsoft Edge engine or the legacy engine.</span></span> <span data-ttu-id="a4809-116">Вы можете выбрать версию JsRT в соответствии с приведенными выше рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="a4809-116">You can choose the JsRT version based on the guidelines above.</span></span> <span data-ttu-id="a4809-117">Для использования этих различий в них были внесены указанные ниже изменения `JsCreateRuntime` `JsCreateContext` и `JsStartDebugging` .</span><span class="sxs-lookup"><span data-stu-id="a4809-117">To accommodate these distinctions, the following changes have been made to `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging`.</span></span>  
  
 <span data-ttu-id="a4809-118">Для `JsCreateRuntime` :</span><span class="sxs-lookup"><span data-stu-id="a4809-118">For `JsCreateRuntime`:</span></span>  
  
-   <span data-ttu-id="a4809-119">При нацеливании на устаревшее ядро `JsRuntimeVersionEdge` значение перечисления считается устаревшим, а `JsRuntimeVersionInternetExplorer11` вместо него предлагается использование значения.</span><span class="sxs-lookup"><span data-stu-id="a4809-119">When targeting the legacy engine, the `JsRuntimeVersionEdge` enumeration value is deprecated, and a message will suggest using the `JsRuntimeVersionInternetExplorer11` value instead.</span></span>  
  
-   <span data-ttu-id="a4809-120">При нацеливании на обработчик Microsoft Edge параметр version не указывается в `JsCreateRuntime` функции.</span><span class="sxs-lookup"><span data-stu-id="a4809-120">When targeting the Microsoft Edge engine, the version parameter is omitted from the `JsCreateRuntime` function.</span></span>  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 <span data-ttu-id="a4809-121">Для `JsCreateContext` и `JsStartDebugging` :</span><span class="sxs-lookup"><span data-stu-id="a4809-121">For `JsCreateContext` and `JsStartDebugging`:</span></span>  
  
-   <span data-ttu-id="a4809-122">При нацеливании на устаревшее ядро `IDebugApplication` интерфейс используется для предоставления собственных неудаленными методами отладки.</span><span class="sxs-lookup"><span data-stu-id="a4809-122">When targeting the legacy engine, the `IDebugApplication` interface is used to supply your own non-remote debugging methods.</span></span> <span data-ttu-id="a4809-123">Для целей отладки `JsCreateContext` и `JsStartDebugging` функции принимаются `IDebugApplication` в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a4809-123">For debugging purposes, `JsCreateContext` and `JsStartDebugging` functions take `IDebugApplication` as parameter.</span></span>  
  
-   <span data-ttu-id="a4809-124">При нацеливании на подсистему Microsoft Edge `IDebugApplication` интерфейс является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="a4809-124">When targeting the Microsoft Edge engine, the `IDebugApplication` interface is deprecated.</span></span> <span data-ttu-id="a4809-125">Обработчик Chakra позволяет выполнять отладку в машинном коде и сценарии с помощью отладчика Visual Studio, не требуя реализации `IDebugApplication` от пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4809-125">The Chakra engine enables native and script debugging capability with Visual Studio debugger without requiring an implementation of `IDebugApplication` from user.</span></span> <span data-ttu-id="a4809-126">Интерфейс больше не является параметром `JsCreateContext` и `JsStartDebugging` в результате.</span><span class="sxs-lookup"><span data-stu-id="a4809-126">The interface is no longer a parameter for `JsCreateContext` and `JsStartDebugging` as a result.</span></span>  
  
 <span data-ttu-id="a4809-127">Для предыдущих API-интерфейсов в устаревшем обработчике используются следующие подписи:</span><span class="sxs-lookup"><span data-stu-id="a4809-127">The signatures for the preceding APIs in the legacy engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 <span data-ttu-id="a4809-128">Для предыдущих API-интерфейсов в обработчике Microsoft Edge используются следующие подписи:</span><span class="sxs-lookup"><span data-stu-id="a4809-128">The signatures for the preceding APIs in the Microsoft Edge engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## <span data-ttu-id="a4809-129">Компиляция для основной версии с помощью Visual C++</span><span class="sxs-lookup"><span data-stu-id="a4809-129">Compile for your preferred version using Visual C++</span></span>  
 <span data-ttu-id="a4809-130">При использовании Visual C++ импортируйте API JsRT, включив заголовок JsRT. h, и убедитесь в том, что JsRT. lib входит в список входных файлов компоновщика.</span><span class="sxs-lookup"><span data-stu-id="a4809-130">When using Visual C++, import the JsRT API by including the jsrt.h header, and ensure that jsrt.lib is included in your linker input files list:</span></span>  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Добавление jsrt. lib в качестве входного файла компоновщика](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 <span data-ttu-id="a4809-132">Если вы хотите нацелить двоичные файлы ядра Microsoft EDGE, необходимо определить макрос `USE_EDGEMODE_JSRT` перед тем, как включить jsrt. h, а не связывать его с jsrt. lib, вы должны создать связь с chakrart. lib.</span><span class="sxs-lookup"><span data-stu-id="a4809-132">If you want to target the Microsoft Edge engine binaries, you need to define the macro `USE_EDGEMODE_JSRT` before including jsrt.h, and instead of linking against jsrt.lib, you should link against chakrart.lib:</span></span>  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Добавление chakrart. lib в качестве входного файла компоновщика](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 <span data-ttu-id="a4809-134">Если вы начинаете работу с новым приложением, вы можете приступить к написанию кода для API JsRT.</span><span class="sxs-lookup"><span data-stu-id="a4809-134">If you're starting with a new application, you are now ready to start writing code against the JsRT API.</span></span>  
  
## <span data-ttu-id="a4809-135">Компиляция для основной версии с помощью .NET</span><span class="sxs-lookup"><span data-stu-id="a4809-135">Compile for your preferred version using .NET</span></span>  
 <span data-ttu-id="a4809-136">Если вы используете .NET и P/Invoke, вы должны изменить объявления API JsRT [DllImport], чтобы импортировать Chakra. dll, а не Jscript9. dll.</span><span class="sxs-lookup"><span data-stu-id="a4809-136">If you're using .NET and P/Invoke, you must change your JsRT API [DllImport] declarations to import chakra.dll instead of jscript9.dll.</span></span> <span data-ttu-id="a4809-137">Кроме того, можно изменить определение, `JsCreateRuntime` чтобы удалить `JsRuntimeVersion` параметр, определение `JsCreateContext` и `JsStartDebugging` удалить `IDebugApplication` параметр.</span><span class="sxs-lookup"><span data-stu-id="a4809-137">In addition, change the definition of `JsCreateRuntime` to remove the `JsRuntimeVersion` parameter and the definition of `JsCreateContext` and `JsStartDebugging` to remove the `IDebugApplication` parameter.</span></span>  
  
 <span data-ttu-id="a4809-138">Для устаревшего модуля используйте следующий код.</span><span class="sxs-lookup"><span data-stu-id="a4809-138">For the legacy engine, use the following code.</span></span>  
  
```c#  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsRuntimeVersion version,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    IDebugApplication debugApplication,  
    out JsContextRef newContext  
);   
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsStartDebugging(  
    IDebugApplication debugApplication,  
);  
```  
  
 <span data-ttu-id="a4809-139">Для подсистемы Microsoft Edge используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="a4809-139">For the Microsoft Edge engine, use the following code.</span></span>  
  
```c#  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    out JsContextRef newContext  
);   
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsStartDebugging();  
```  
  
> [!CAUTION]
>  <span data-ttu-id="a4809-140">Если вы вручную маршалирует указатель на функцию (например, с помощью LoadLibrary/GetProcAddress), очень важно, чтобы вы не намерены использовать объявления метода, или, в противном случае, вы будете раскрывать стек, что приводит к непредсказуемому поведению, например вызывающему сбой приложения.</span><span class="sxs-lookup"><span data-stu-id="a4809-140">If you are manually marshaling the function pointer (such as via LoadLibrary/GetProcAddress), it is critical that you do not mix the declarations of the method, or else you will unbalance the stack, which will result in unpredictable behavior such as causing your app to crash.</span></span> <span data-ttu-id="a4809-141">Эта проблема возникает при выполнении глобального поиска и замене экземпляров Jscript9. dll в коде импорта, так как при этом `version` параметр будет пропущен.</span><span class="sxs-lookup"><span data-stu-id="a4809-141">The same problem will occur if you perform a global search-and-replace of instances of jscript9.dll in your import code, because you'll miss the `version` parameter being dropped.</span></span>  
  
## <span data-ttu-id="a4809-142">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a4809-142">Summary</span></span>  
 <span data-ttu-id="a4809-143">В Windows 10 API размещения среды выполнения JavaScript разбиваются на два.</span><span class="sxs-lookup"><span data-stu-id="a4809-143">In Windows 10, the JavaScript Runtime Hosting APIs are splitting into two.</span></span> <span data-ttu-id="a4809-144">Эти API теперь поддерживают "живых" обработчиком Microsoft EDGE, для которого возможности языка будут выровнены с помощью подсистемы Microsoft EDGE в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4809-144">These APIs now support a "living" Microsoft Edge engine, whose language capabilities will be aligned with the "living" Microsoft Edge engine in the Microsoft Edge.</span></span> <span data-ttu-id="a4809-145">Вы можете использовать эти возможности из приложения для настольных компьютеров или из магазина, чтобы создавать новые и замечательные способы расширить приложение и использовать современные веб-навыки в существующей базе кода.</span><span class="sxs-lookup"><span data-stu-id="a4809-145">You can leverage these capabilities from your desktop or Store apps to create new and exciting ways to extend your application and to leverage modern Web skills in your existing code base.</span></span> <span data-ttu-id="a4809-146">Однако из-за различий между предыдущими версиями необходимо учитывать следующие моменты при нацеливании на крайний или старый механизм.</span><span class="sxs-lookup"><span data-stu-id="a4809-146">However, because there are subtle differences between previous versions, you must be aware of the following points when targeting the Edge or legacy engine.</span></span>  
  
-   <span data-ttu-id="a4809-147">Ваше приложение может поддерживать только одну версию JsRT на процесс.</span><span class="sxs-lookup"><span data-stu-id="a4809-147">Your app can support only one version of JsRT per process.</span></span>  
  
     <span data-ttu-id="a4809-148">Например, вы не можете создать среду выполнения Microsoft Edge Engine, а затем в устаревшей среде выполнения и ожидать, что они правильно работают в том же процессе.</span><span class="sxs-lookup"><span data-stu-id="a4809-148">For example, you can't create a Microsoft Edge engine runtime and then a legacy engine runtime and expect them to run correctly in the same process.</span></span> <span data-ttu-id="a4809-149">Это не поддерживается, и это может привести к недокументированному поведению, например при загрузке второй библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a4809-149">This is unsupported and may result in undocumented behavior, such as failure to load the second DLL.</span></span>  
  
-   <span data-ttu-id="a4809-150">При нацеливании на обработчик Microsoft Edge приложение может неожиданно получить новые возможности при автоматическом обновлении базовой платформы.</span><span class="sxs-lookup"><span data-stu-id="a4809-150">When targeting the Microsoft Edge engine, your app may unexpectedly acquire new features when the underlying platform is automatically updated.</span></span>  
  
     <span data-ttu-id="a4809-151">Например, в Internet Explorer 11 устаревшая версия среды выполнения поддерживает объявления переменных областей, такие как `let` и `const` .</span><span class="sxs-lookup"><span data-stu-id="a4809-151">For example, the Internet Explorer 11 mode of the legacy runtime supports block-scoping variable declarations such as `let` and `const`.</span></span> <span data-ttu-id="a4809-152">Если ранее поведение системы автоматического управления версиями в Microsoft Edge существовало раньше, код, работающий в режиме Internet Explorer 10, у которого нет правил ограничения области, мог начать работу со сбоем, если платформа была автоматически обновлена.</span><span class="sxs-lookup"><span data-stu-id="a4809-152">If the Microsoft Edge engine automatic versioning behavior had been the standard previously, code that had worked in Internet Explorer 10 mode, which did not have block-scoping rules, may have started failing when the platform had automatically upgraded.</span></span> <span data-ttu-id="a4809-153">Это должно учитываться при выборе используемой модели среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4809-153">This must be a consideration when choosing which runtime model to use.</span></span> <span data-ttu-id="a4809-154">Несмотря на то, что вам следует использовать ядро Microsoft EDGE, везде, где это возможно, необходимо соблюдать осторожность при использовании структур кода JavaScript, которые могут стать недопустимыми в будущем.</span><span class="sxs-lookup"><span data-stu-id="a4809-154">While we believe you should target the Microsoft Edge engine whenever possible, you must be careful about using JavaScript code structures that may become invalid in the future.</span></span>  
  
-   <span data-ttu-id="a4809-155">JsRT для Магазина Windows поддерживает только обработчик Microsoft EDGE (Chakra. dll).</span><span class="sxs-lookup"><span data-stu-id="a4809-155">JsRT for the Windows Store only supports the Microsoft Edge engine (chakra.dll).</span></span> <span data-ttu-id="a4809-156">Приложения, пытающиеся установить связь с любым API JsRT в Jscript9. dll, не смогут пройти сертификацию.</span><span class="sxs-lookup"><span data-stu-id="a4809-156">Apps attempting to link against any JsRT API in jscript9.dll will fail certification.</span></span>  
  
-   <span data-ttu-id="a4809-157">Очень важно, чтобы не путать объявление `JsCreateRuntime` , `JsCreateContext` а также `JsStartDebugging` между Jscript9. dll и Chakra. dll, так как это приводит к появлению балансировки стека.</span><span class="sxs-lookup"><span data-stu-id="a4809-157">It is critical that you do not confuse the declaration of `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging` between jscript9.dll and chakra.dll, because it will result in imbalancing the stack.</span></span>  
  
     <span data-ttu-id="a4809-158">При использовании C и C++ вы получаете сообщение об ошибке компоновщика при попытке использовать неверное объявление, если не выполняется что-то вроде звонка, `LoadLibrary` а затем `GetProcAddress` .</span><span class="sxs-lookup"><span data-stu-id="a4809-158">When using C and C++, you will receive a linker error if you try to use the wrong declaration, as long as you're not doing something like calling `LoadLibrary` and then `GetProcAddress`.</span></span> <span data-ttu-id="a4809-159">Разработчики .NET могут не найти эту проблему с легкостью, поэтому при использовании этой функции дважды проверьте свой код.</span><span class="sxs-lookup"><span data-stu-id="a4809-159">.NET developers may not find this problem as easily, so double-check your code when using this feature.</span></span>  
  
## <span data-ttu-id="a4809-160">См. также</span><span class="sxs-lookup"><span data-stu-id="a4809-160">See Also</span></span>  
 [<span data-ttu-id="a4809-161">Размещение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="a4809-161">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)
 