---
description: 'Сведения о том, как ориентироваться на разные механизмы JavaScript для Windows 10. '
title: Настройка Microsoft EDGE и устаревших обработчиков в API JsRT
ms.date: 06/18/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 99a3143dd5f995332524a99e5c6c5019b955fea8
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752229"
---
# Настройка Microsoft EDGE и устаревших обработчиков в API JsRT  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Windows 10 поддерживает два разных обработчика JavaScript:  

*   Старый обработчик Chakra (также называемый *устаревшим модулем* или jscript9.dll ниже), который поставляется вместе с браузером Internet Explorer 11 и поддерживает его. Этот обработчик зафиксирован в течение времени и останется без изменений в выпуске Win 8.1/IE11.  
*   Новый обработчик Chakra (также называемый *подсистемой Edge* или chakra.dll ниже), который поставляется вместе с новым браузером в Windows 10, Microsoft EDGE и поддерживает его. Этот обработчик будет постоянно обновляться и будет поддерживать обработчик [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) "живых". Работа работающего подсистемы Microsoft EDGE, в отличие от устаревшего обработчика, не перенесет функцию Microsoft Edge Engine, чтобы принять участие в программе.  

 Когда вы создаете приложение с помощью API размещения среды выполнения JavaScript (JsRT), вы можете выбрать для него назначение либо устаревшей, либо обработчиком Microsoft Edge.  

*   Если необходимо обменяться обратной совместимостью с существующими приложениями, необходимо выбрать старый механизм.  
*   Если вы хотите, чтобы ваше приложение было переадресовано для просмотра и поддерживало новые возможности JavaScript по мере их выпуска (например, ECMAScript 6), нацеливание на ядро Microsoft Edge.  

Этот раздел содержит подробные сведения о том, как ориентироваться на разные ядра.  

## Назначение предпочтительной версии  

При создании приложения вы можете выбрать версию JsRT, которая поддерживает либо обработчик Microsoft EDGE, либо старый механизм. Вы можете выбрать версию JsRT в соответствии с приведенными выше рекомендациями. Для использования этих различий в них были внесены указанные ниже изменения `JsCreateRuntime` `JsCreateContext` и `JsStartDebugging` .  

Для `JsCreateRuntime` :  

*   При нацеливании на устаревшее ядро `JsRuntimeVersionEdge` значение перечисления считается устаревшим, а `JsRuntimeVersionInternetExplorer11` вместо него предлагается использование значения.  
*   При нацеливании на обработчик Microsoft Edge параметр version не указывается в `JsCreateRuntime` функции.  
    
    ```cpp
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);
    ```  
    
 Для `JsCreateContext` и `JsStartDebugging` :  

*   При нацеливании на устаревшее ядро `IDebugApplication` интерфейс используется для предоставления собственных неудаленными методами отладки. Для целей отладки `JsCreateContext` и `JsStartDebugging` функции принимаются `IDebugApplication` в качестве параметра.  
*   При нацеливании на подсистему Microsoft Edge `IDebugApplication` интерфейс является устаревшим. Обработчик Chakra позволяет выполнять отладку в машинном коде и сценарии с помощью отладчика Visual Studio, не требуя реализации `IDebugApplication` от пользователя. Интерфейс больше не является параметром `JsCreateContext` и `JsStartDebugging` в результате.  

Для предыдущих API-интерфейсов в устаревшем обработчике используются следующие подписи:  

```cpp
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);

JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);

JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);
```  

Для предыдущих API-интерфейсов в обработчике Microsoft Edge используются следующие подписи:  

```cpp
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);

JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);

JsErrorCode JsStartDebugging();
```  

## Компиляция для основной версии с помощью Visual C++  

При использовании Visual C++ импортируйте API JsRT, включив заголовок JsRT. h, и убедитесь в том, что JsRT. lib входит в список входных файлов компоновщика.  

```cpp
#include <jsrt.h>
```  

![Добавление jsrt. lib в качестве входного файла компоновщика](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  

Если вы хотите нацелить двоичные файлы ядра Microsoft EDGE, необходимо определить макрос `USE_EDGEMODE_JSRT` перед тем, как включить jsrt. h, а не связывать его с jsrt. lib, вы должны создать связь с chakrart. lib.  

```cpp
#define USE_EDGEMODE_JSRT
#include <jsrt.h>
```  

![Добавление chakrart. lib в качестве входного файла компоновщика](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  

Если вы начинаете работу с новым приложением, вы можете приступить к написанию кода для API JsRT.  

## Компиляция для основной версии с помощью .NET  

Если вы используете .NET и P/Invoke, вы должны изменить объявления API JsRT [DllImport] для импорта chakra.dll вместо jscript9.dll. Кроме того, можно изменить определение, `JsCreateRuntime` чтобы удалить `JsRuntimeVersion` параметр, определение `JsCreateContext` и `JsStartDebugging` удалить `IDebugApplication` параметр.  

Для устаревшего модуля используйте следующий код.  

```csharp
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

Для подсистемы Microsoft Edge используйте следующий код:  

```csharp
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
> Если вы вручную маршалирует указатель на функцию (например, с помощью LoadLibrary/GetProcAddress), очень важно, чтобы вы не намерены использовать объявления метода, или, в противном случае, вы будете раскрывать стек, что приводит к непредсказуемому поведению, например вызывающему сбой приложения. Эта проблема возникает при выполнении глобального поиска и замене экземпляров jscript9.dll в коде импорта, так как при этом `version` параметр будет пропущен.  

## Краткий обзор  

В Windows 10 API размещения среды выполнения JavaScript разбиваются на два. Эти API теперь поддерживают "живых" обработчиком Microsoft EDGE, для которого возможности языка будут выровнены с помощью подсистемы Microsoft EDGE в Microsoft Edge. Вы можете использовать эти возможности из приложения для настольных компьютеров или из магазина, чтобы создавать новые и замечательные способы расширить приложение и использовать современные веб-навыки в существующей базе кода. Однако из-за различий между предыдущими версиями необходимо учитывать следующие моменты при нацеливании на крайний или старый механизм.  

*   Ваше приложение может поддерживать только одну версию JsRT на процесс.  
    
    Например, вы не можете создать среду выполнения Microsoft Edge Engine, а затем в устаревшей среде выполнения и ожидать, что они правильно работают в том же процессе. Это не поддерживается, и это может привести к недокументированному поведению, например при загрузке второй библиотеки DLL.  
    
*   При нацеливании на обработчик Microsoft Edge приложение может неожиданно получить новые возможности при автоматическом обновлении базовой платформы.  
    
    Например, в Internet Explorer 11 устаревшая версия среды выполнения поддерживает объявления переменных областей, такие как `let` и `const` . Если ранее поведение системы автоматического управления версиями в Microsoft Edge существовало раньше, код, работающий в режиме Internet Explorer 10, у которого нет правил ограничения области, мог начать работу со сбоем, если платформа была автоматически обновлена. Это должно учитываться при выборе используемой модели среды выполнения. Несмотря на то, что вам следует использовать ядро Microsoft EDGE, везде, где это возможно, необходимо соблюдать осторожность при использовании структур кода JavaScript, которые могут стать недопустимыми в будущем.  
    
*   JsRT для Магазина Windows поддерживает только обработчик Microsoft EDGE (chakra.dll). Приложения, пытающиеся установить связь с любым API JsRT в jscript9.dll не смогут выполнить сертификацию.  
*   Очень важно, чтобы не путать объявление `JsCreateRuntime` , `JsCreateContext` а также `JsStartDebugging` между jscript9.dll и chakra.dll, так как это приводит к появлению балансировки стека.  
    
    При использовании C и C++ вы получаете сообщение об ошибке компоновщика при попытке использовать неверное объявление, если не выполняется что-то вроде звонка, `LoadLibrary` а затем `GetProcAddress` . Разработчики .NET могут не найти эту проблему с легкостью, поэтому при использовании этой функции дважды проверьте свой код.  
    
## См. также  

*   [Размещение среды выполнения JavaScript](../javascript-runtime-hosting.md)
 