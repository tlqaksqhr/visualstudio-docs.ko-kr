---
title: JsGetDataViewStorage 함수 | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6b405fc22e411c343dcd5214495deb0275f5db52
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2017
ms.locfileid: "24568123"
---
# <a name="jsgetdataviewstorage-function"></a>JsGetDataViewStorage 함수
`DataView`에서 사용되는 기본 메모리 저장소를 가져옵니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `dataView`  
 DataView 인스턴스입니다.  
  
 `buffer`  
 DataView의 버퍼입니다. 반환되는 버퍼의 수명은 `DataView`의 수명과 같습니다. 버퍼 포인터는 가비지 수집을 위한 `DataView`에 대한 참조로 계산되지 않습니다.  
  
 `bufferLength`  
 버퍼의 바이트 수입니다.  
  
## <a name="return-value"></a>반환 값  
 작업에 성공한 경우 코드 `JsNoError` 이고, 그렇지 않은 경우 오류 코드입니다.  
  
## <a name="remarks"></a>설명  
 활성 스크립트 컨텍스트가 필요합니다.  
  
 이 API는 가장자리 모드에서만 지원됩니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** jsrt.h  
  
## <a name="see-also"></a>참고 항목  
 [참조(JavaScript 런타임)](../chakra-hosting/reference-javascript-runtime.md)