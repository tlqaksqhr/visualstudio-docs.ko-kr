---
title: IEEDataStorage::GetSize | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IEEDataStorage::GetSize
helpviewer_keywords:
- IEEDataStorage::GetSize
ms.assetid: 33d232c4-1239-4abc-922b-e1bc5b908169
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9fb6c315971c5d7886626239387d6c6ff501ed0a
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31119830"
---
# <a name="ieedatastoragegetsize"></a>IEEDataStorage::GetSize
이 개체에 포함 된 바이트 수를 반환 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT GetSize(  
   ULONG* size  
);  
```  
  
```csharp  
int GetSize(  
   out uint size  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `size`  
 [out] 이 개체에 포함 된 바이트 수입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`, 그러지 않으면 오류 코드가 반환 됩니다.  
  
## <a name="remarks"></a>설명  
 사용 하 여는 [GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md) 실제 데이터 바이트를 검색 하는 메서드입니다.  
  
## <a name="see-also"></a>참고 항목  
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)