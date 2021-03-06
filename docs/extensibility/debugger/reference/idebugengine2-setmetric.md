---
title: IDebugEngine2::SetMetric | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugEngine2:::SetMetric
helpviewer_keywords:
- IDebugEngine2:::SetMetric
ms.assetid: dcda4972-c32e-4693-a0e1-25d5c58b9782
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 12e323fe248bc022bcbbd8b9bdd0e628c27a97e1
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31122849"
---
# <a name="idebugengine2setmetric"></a>IDebugEngine2::SetMetric
이 메서드를 기준으로 알려진 레지스트리 값을 설정 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT SetMetric(  
   LPCOLESTR pszMetric,  
   VARIANT   varValue  
);  
```  
  
```csharp  
int SetMetric(  
   string pszMetric,  
   object varValue  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pszMetric`  
 [in] 메트릭 이름입니다.  
  
 `varValue`  
 [in] 메트릭 값을 지정합니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`, 그러지 않으면 오류 코드가 반환 됩니다.  
  
## <a name="remarks"></a>설명  
 디버그 엔진의 동작을 변경 하거나 지원 되는 기능을 보급 하는 데 사용 하는 레지스트리 값은 메트릭이 있습니다. 이 메서드는 적절 한 형식에 대 한 호출을 전달할 수 있습니다는 [디버깅할 수 있도록 SDK 도우미](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md) 함수 `SetMetric`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [디버깅을 위한 SDK 도우미](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)