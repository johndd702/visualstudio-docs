---
title: "Compiler Error CS0531"
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
ms.assetid: 54c2a98b-84e3-481a-a934-7cd6dffa7677
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
# Compiler Error CS0531
'member' : interface members cannot have a definition  
  
 Methods that are declared in an [interface](../Topic/interface%20\(C%23%20Reference\).md) must be implemented in a class that inherits from it and not in the interface itself.  
  
 The following sample generates CS0531:  
  
```  
// CS0531.cs  
namespace x  
{  
   public interface clx  
   {  
      int xclx()   // CS0531, cannot define xclx  
      // Try the following declaration instead:  
      // int xclx();  
      {  
         return 0;  
      }  
   }  
  
   public class cly  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```