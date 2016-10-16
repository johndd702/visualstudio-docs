---
title: "Programs"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "debugging [Debugging SDK], programs"
  - "programs, debugging"
ms.assetid: e1f955d8-95da-493b-837e-e97741a26d7e
caps.latest.revision: 12
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Programs
In terms of the debugger architecture, a **program**:  
  
-   Is a container for both a set of threads and a set of modules. A program has no single analogy in the Windows operating system.  
  
     A program is a kind of subprocess. For example, when you are debugging a Web site, a script can be seen as a program. While a script runs in the scripting engine process, independent of other scripts, it also has its own set of threads. A debug engine (DE) attaches to a program, and not to a process or a thread.  
  
-   Can identify itself and the process it is running in, and can be attached to, be detached from, and describe the DE that created it, if any. A program can execute, stop, continue, and be terminated.  
  
-   Can enumerate all its threads. A program can also supply its own disassembly stream, and can enumerate all the code contexts of a given document position.  
  
-   Is represented by an [IDebugProgram2](../extensibility/idebugprogram2.md) interface, created before the program is attached, or as part of the attach process, depending on the implementation. When a port enumerates the programs of a process, each program is created in accordance with a corresponding [IDebugProgramNode2](../extensibility/idebugprogramnode2.md) interface passed as an argument to [AddProgramNode](../extensibility/idebugportnotify2--addprogramnode.md). While debug engines also create `IDebugProgram2` interfaces to represent programs, these programs are not created in accordance with a program node. The `IDebugProgramNode2` interfaces created by a DE are used for actual debugging, while those created by a port are used only for discovering which programs are running in a process.  
  
## See Also  
 [Processes](../extensibility/processes.md)   
 [Program Nodes](../extensibility/program-nodes.md)   
 [Modules](../extensibility/modules.md)   
 [Debugger Concepts](../extensibility/debugger-concepts.md)   
 [Debug Engine](../extensibility/debug-engine.md)   
 [Document Position](../extensibility/document-position.md)   
 [Code Context](../extensibility/code-context.md)   
 [IDebugProgram2](../extensibility/idebugprogram2.md)   
 [IDebugProgramNode2](../extensibility/idebugprogramnode2.md)   
 [AddProgramNode](../extensibility/idebugportnotify2--addprogramnode.md)