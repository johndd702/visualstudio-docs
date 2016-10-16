---
title: "Compiler Warning (level 3) CS0282"
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
ms.assetid: fd4cda5d-81c7-40e3-8424-c938b3447356
caps.latest.revision: 14
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
# Compiler Warning (level 3) CS0282
There is no defined ordering between fields in multiple declarations of partial class or struct 'type'. To specify an ordering, all instance fields must be in the same declaration.  
  
 To resolve this error, put all member variables in a single partial class definition.  
  
 A common way to get this error is by having a partial `struct` defined in more than one place, with some of the member variables in one definition, and some in another.  
  
 The following code generates CS0282.  
  
## Example  
 This code contains one description of a `struct`. Compile these two modules together in a single step by means of the command:  
  
 `csc /targt:library cs0282_1.cs cs0282_2.cs`  
  
```  
partial struct A  
{  
    int i;  
}  
```  
  
## Example  
 This code contains a conflicting description of the same `struct`.  
  
```  
partial struct A  
{  
    int j;  
}  
```