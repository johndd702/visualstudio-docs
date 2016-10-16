---
title: "MSBuild Error MSB3166"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f5dff83a-1e41-4c92-a137-89b7e9f3cd93
caps.latest.revision: 5
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# MSBuild Error MSB3166
**MSB3166: Could not find required file '<file\>' for item '<package\>'.**  
  
 This error is generated when an end-user license agreement (EULA) or external check file is missing. Make sure the file exists on disk.  
  
### To correct this error  
  
-   Reinstall the Visual Studio SDK  
  
     \- or -  
  
-   Copy the required files to the appropriate location.  
  
## See Also  
 [<PackageFiles\> Element](../VS_IDE/-PackageFiles--Element--Bootstrapper-.md)