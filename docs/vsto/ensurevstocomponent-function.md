---
title: EnsureVSTOComponent 함수
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 20c4e363b11647609b67a898878dd4b4e59ba180
ms.sourcegitcommit: 1466ac0f49ebf7448ea4507ae3f79acb25d51d3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2018
---
# <a name="ensurevstocomponent-function"></a>EnsureVSTOComponent 함수
  이 API는 Office 인프라를 지원 하며 사용자 코드에서 직접 사용할 되지 않습니다.  
  
## <a name="syntax"></a>구문  
  
```c  
HRESULT EnsureVSTOComponent(  
    IVSTProject *pProject  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|*pProject*|사용 하지 마십시오.|  
  
## <a name="return-value"></a>반환 값  
 함수가 성공 하면 반환 **S_OK**합니다. 함수가 실패 하면 오류 코드가 반환 됩니다.  
  
  