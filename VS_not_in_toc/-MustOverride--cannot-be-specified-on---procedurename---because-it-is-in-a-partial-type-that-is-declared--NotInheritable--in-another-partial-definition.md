---
title: "&#39;MustOverride&#39; cannot be specified on &#39;&lt;procedurename&gt;&#39; because it is in a partial type that is declared &#39;NotInheritable&#39; in another partial definition"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5798dfda-3d7b-4f30-9715-40cbf52d6dc4
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
# &#39;MustOverride&#39; cannot be specified on &#39;&lt;procedurename&gt;&#39; because it is in a partial type that is declared &#39;NotInheritable&#39; in another partial definition
A procedure or property is declared as `MustOverride` within a class that is defined in multiple partial declarations, but one of the partial definitions specifies `NotInheritable` for the class.  
  
 When you divide the definition of a class among several partial declarations, the compiler treats the class as the union of all its partial declarations. This applies not only to the members but also to the implementation, inheritance, and access level.  
  
 To override a procedure or property, a class must inherit it from a base class. Therefore, to specify `MustOverride` for a procedure or property in a base class, you must specify `MustInherit` for the class. Because they are mutually contradictory, you cannot specify both `MustInherit` and `NotInheritable` for the same class.  
  
 **Error ID:** BC30927  
  
### To correct this error  
  
-   If the property or procedure must be overridden, then remove the `NotInheritable` keyword from the partial declaration in which it appears.  
  
-   If the class must be `NotInheritable`, then remove the `MustOverride` keyword from the procedure or property. You cannot override it because you cannot inherit the class.  
  
## See Also  
 [Partial](../Topic/Partial%20\(Visual%20Basic\).md)   
 [MustOverride](../Topic/MustOverride%20\(Visual%20Basic\).md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [NotInheritable](../Topic/NotInheritable%20\(Visual%20Basic\).md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)