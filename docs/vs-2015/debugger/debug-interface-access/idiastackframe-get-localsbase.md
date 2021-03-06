---
title: "IDiaStackFrame::get_localsBase | Microsoft Docs"
ms.custom: ""
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "IDiaStackFrame::get_localsBase method"
ms.assetid: eb0bd73e-d92d-468e-a0b1-fbc279919f54
caps.latest.revision: 14
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# IDiaStackFrame::get_localsBase
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Retrieves the base address of the local variables for the frame.  
  
## Syntax  
  
```cpp#  
HRESULT get_localsBase (   
   ULONGLONG* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the base address of the local variables.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if the property is not supported. Otherwise, returns an error code.  
  
## See Also  
 [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)



