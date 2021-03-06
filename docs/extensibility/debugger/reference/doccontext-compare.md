---
title: DOCCONTEXT_COMPARE | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- DOCCONTEXT_COMPARE
helpviewer_keywords:
- DOCCONTEXT_COMPARE enumeration
ms.assetid: ed947c34-b07e-4b69-8381-b6e7cb842862
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 966d31889d7979732af20f5e3f95546e87af6598
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31103655"
---
# <a name="doccontextcompare"></a>DOCCONTEXT_COMPARE
두 문서 컨텍스트를 비교 하기 위한 조건을 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
enum enum_DOCCONTEXT_COMPARE {   
   DOCCONTEXT_EQUAL         = 0x0001,  
   DOCCONTEXT_LESS_THAN     = 0x0002,  
   DOCCONTEXT_GREATER_THAN  = 0x0003,  
   DOCCONTEXT_SAME_DOCUMENT = 0x0004  
};  
typedef DWORD DOCCONTEXT_COMPARE;  
```  
  
```csharp  
enum enum_DOCCONTEXT_COMPARE {   
   DOCCONTEXT_EQUAL         = 0x0001,  
   DOCCONTEXT_LESS_THAN     = 0x0002,  
   DOCCONTEXT_GREATER_THAN  = 0x0003,  
   DOCCONTEXT_SAME_DOCUMENT = 0x0004  
};  
```  
  
## <a name="members"></a>멤버  
 DOCCONTEXT_EQUAL  
 해당 대상 문서 컨텍스트를 사용 하는 목록에서 첫 번째 문서 컨텍스트를 찾습니다.  
  
 DOCCONTEXT_LESS_THAN  
 대상 문서 컨텍스트에서 가져왔습니다 보다 작은 목록에서 첫 번째 문서 컨텍스트를 찾습니다.  
  
 DOCCONTEXT_GREATER_THAN  
 대상 문서 컨텍스트에서 가져왔습니다 보다 큰 목록에서 첫 번째 문서 컨텍스트를 찾습니다.  
  
 DOCCONTEXT_SAME_DOCUMENT  
 대상 문서 컨텍스트에서 가져왔습니다와 동일한 문서에 있는 목록의 첫 번째 문서 컨텍스트를 찾습니다.  
  
## <a name="remarks"></a>설명  
 에 대 한 인수로 전달 되는 [비교](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md) 메서드.  
  
 이러한 값은 목록에서 첫 번째 문서 컨텍스트를 찾는 데 필요한 비교 기준을 지정 하는 데 사용 됩니다. 문서 컨텍스트를 통해 자체 작업에 대해 비교할 문서 컨텍스트의 목록을 제공할는 `IDebugDocumentContext2::Compare` 메서드. 비교 연산자는 목록의 첫 번째 문서 컨텍스트 `true` 반환 됩니다.  
  
## <a name="requirements"></a>요구 사항  
 헤더: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>참고 항목  
 [열거형](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Compare](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md)