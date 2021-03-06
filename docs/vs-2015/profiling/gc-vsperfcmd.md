---
title: "GC (VSPerfCmd) | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7c81e88b-a748-4cf5-a7a1-3429608e1b54
caps.latest.revision: 17
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# GC (VSPerfCmd)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [GC (VSPerfCmd)](https://docs.microsoft.com/visualstudio/profiling/gc-vsperfcmd).  
  
The **GC** option enables the collection of .NET Framework memory allocation and object lifetime data. The **GC** option can only be used with the sampling profiling method and only with the **Launch** option.  
  
 When you are using the **GC** option, the VSPerfClrEnv **/sampleon** command is not required.  
  
 If no parameters are specified, or if the **Allocation** parameter is specified, only .NET Framework memory allocation data is collected. If the **Lifetime** parameter is specified, both .NET Framework memory allocation and .NET Framework object lifetime data is collected.  
  
## Syntax  
  
```  
VSPerfCmd.exe /Launch:AppName /GC[:{Allocation|Lifetime}] [Options]  
```  
  
#### Parameters  
 **Allocation**  
 Default. Collects .NET Framework memory allocation data.  
  
 **Lifetime**  
 Collects both .NET Framework memory allocation data and .NET Framework object lifetime data.  
  
## Required Options  
 The **GC** option can only be used with the **Launch** option.  
  
 **Launch:** `AppName`  
 Starts the specified application and begins profiling with the sampling method.  
  
## Example  
 The following example launches an application and collects .NET Framework memory allocation data.  
  
```  
VSPerfCmd.exe /Launch:TestApp.exe /gc  
```  
  
## See Also  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profiling Stand-Alone Applications](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profiling ASP.NET Web Applications](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profiling Services](../profiling/command-line-profiling-of-services.md)



