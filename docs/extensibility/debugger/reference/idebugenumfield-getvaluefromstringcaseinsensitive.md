---
title: IDebugEnumField::GetValueFromStringCaseInsensitive | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugEnumField::GetValueFromStringCaseInsensitive
helpviewer_keywords:
- IDebugEnumField::GetValueFromStringCaseInsensitive method
ms.assetid: ef95b38e-d9b2-4fb5-a166-7c2e14641dc7
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 05d838bc91949ea5023fe61c6eb0c1b5c5220e68
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31116531"
---
# <a name="idebugenumfieldgetvaluefromstringcaseinsensitive"></a>IDebugEnumField::GetValueFromStringCaseInsensitive
이 메서드에서 열거형 상수의 이름에 연결 된 값을 반환 하는 대/소문자 구분 검색을 사용 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT GetValueFromStringCaseInsensitive(  
   LPCOLESTR  pszValue,  
   ULONGLONG* pvalue  
);  
```  
  
```csharp  
int GetValueFromStringCaseInsensitive(  
   string    pszValue,   
   out ulong pValue  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pszValue`  
 [in] 값을 얻을 수 있는 이름을 지정 하는 문자열입니다. C + +에 대 한를 와이드 문자 문자열입니다.  
  
 `pValue`  
 [out] 연결 된 숫자 값을 반환합니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`, 그렇지 않으면 반환 `S_FALSE`이름을 열거형 또는 오류 코드의 일부가 아닌 경우, 합니다.  
  
## <a name="remarks"></a>설명  
 이 메서드는 대/소문자 구분. 대/소문자 구분 검색 (예를 들어 이름이 대/소문자 구분 하는 c + +와 같은 언어)에서 필요한 경우 사용 하 여 [GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)   
 [GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)