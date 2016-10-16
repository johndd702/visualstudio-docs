---
title: "How to: Use the Expression Editor"
ms.custom: na
ms.date: 10/10/2016
ms.prod: .net-framework-4.6
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: b5f961dd-6dda-41a9-9cae-0383d479ef3d
caps.latest.revision: 13
manager: erikre
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# How to: Use the Expression Editor
The Expression Editor is a Windows Workflow Designer control that is used in many workflow activities as a means of entering and evaluating these expressions. The Expression Editor provides a full-fledged IDE editing experience including IntelliSense, colorization, ParamInfo, error squiggles, among other features. The compiler validates the expression after it is entered. If the expression is invalid, an error icon is displayed. The editor can also be opened as an **Expression Editor** dialog box.  
  
 Expressions are literal values or Visual Basic code bound to arguments or properties. They contain value elements (e.g. variables, constants, literals, properties) that are combined with operations to yield a new value. Expressions are written using VB.NET syntax even if the application is in a program using C#. This means capitalization does not matter, comparison is performed using a single equals (“=”) sign instead of (“==”), the Boolean operators are the words "and" and "or" instead of the symbols "&&" and "&#124;&#124;", and **Nothing** is used instead of **null**. For more information on expressions and operators in Visual Basic and for some samples, see [Operators and Expressions in Visual Basic](http://go.microsoft.com/fwlink/?LinkId=186818).  
  
 The **Expression Editor** behaves as follows:  
  
-   If the focus is not on the Expression Editor, it looks like a regular TextBlock control.  
  
-   Once the focus is on the Expression Editor, it looks and behaves like the Expression Editor control. After it loses focus, the it looks like a regular TextBlock again.  
  
-   If you focus on the Expression Editor in a rehosted workflow designer, then it behaves like a TextBox. When focus is lost in the rehosted workflow designer, the Expression Editor looks like a regular TextBlock again.  
  
> [!NOTE]
>  IntelliSense for the Expression Editor is available only inside of Visual Studio 2010. In both the Visual Studio 2010 and the rehosted scenarios, the compiler validates the expression after it is entered and the expression editor displays an error icon if the expression is invalid.  
  
### Using the Expression editor  
  
1.  In Visual Studio 2010, open a new or existing workflow project.  
  
2.  Add, for example, the <xref:System.Activities.Statements.Assign?qualifyHint=False> activity to your workflow.  
  
    > [!NOTE]
    >  Multiple workflow activities have expression editors. Expression TextBlocks also appear in the variable designer, argument designer, and the dynamic argument designer. The <xref:System.Activities.Statements.Assign?qualifyHint=False> activity is used as an example.  
  
3.  Click the left expression editor in the activity designer for the <xref:System.Activities.Statements.Assign?qualifyHint=False> activity.  
  
     The grey watermark strings **<To\>** and **<Enter a VB Expression\>** are the default text strings for expression editors in the <xref:System.Activities.Statements.Assign?qualifyHint=False> activity.  
  
4.  Enter your expression. If you enter a string, make sure to put quotation marks around the string. If you choose to bind the expression argument to a variable, leave the quotation marks off.  
  
     When you are done, select a region or area outside of the Expression Editor to shift the focus to another part of the designer. This will cause the compiler to validate the expression as described previously.  
  
     An Alternative way to enter/edit an expression is to click the ellipsis next to the property name in the property grid. This will open the **Expression Editor** as dialog box.  
  
## See Also  
 <xref:System.Activities.Presentation.View.ExpressionTextBox?qualifyHint=False>