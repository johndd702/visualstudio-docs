---
title: "Compiler Error CS0020"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a54db39-6530-4e34-aa17-a90f85223d08
caps.latest.revision: 7
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
# Compiler Error CS0020
Division by constant zero  
  
 An expression uses a literal (not variable) value of zero in the denominator of a division operation. Division by zero is not defined, and is therefore invalid.  
  
 The following sample generates CS0020:  
  
```  
// CS0020.cs  
namespace x  
{  
   public class b  
   {  
      public static void Main()  
      {  
         1 / 0;   // CS0020  
      }  
   }  
}  
```  
  
## See Also  
 [Operators](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)