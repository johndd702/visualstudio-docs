---
title: "&#39;ReDim&#39; statements can no longer be used to declare array variables"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9227a06e-a997-4b16-9977-19e2bce9035b
caps.latest.revision: 8
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
# &#39;ReDim&#39; statements can no longer be used to declare array variables
`ReDim` can only be used to change the size of an existing array.  
  
 **Error ID:** BC30811  
  
### To correct this error  
  
-   Specify the size of arrays when they are declared; for example:  
  
    ```  
    Dim X(20) As Integer  
    ```  
  
## See Also  
 [Arrays Summary](../Topic/Arrays%20Summary%20\(Visual%20Basic\).md)   
 [ReDim Statement](../Topic/ReDim%20Statement%20\(Visual%20Basic\).md)   
 [ReDim Statement Changes in Visual Basic](assetId:///b4da14db-ff23-490f-b3c6-d7ae1b649532)