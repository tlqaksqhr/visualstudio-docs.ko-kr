---
title: IDiaPropertyStorage::ReadULONGLONG | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadULONGLONG
ms.assetid: f80a2e24-5744-4fec-bab0-3ed51aef6e58
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 35cff5f92f0ceeb15c185316aeb9b9fde155a1ec
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31468858"
---
# <a name="idiapropertystoragereadulonglong"></a>IDiaPropertyStorage::ReadULONGLONG
읽고 `ULONGLONG` 속성 집합에 있는 값입니다.  
  
## <a name="syntax"></a>구문  
  
```C++  
HRESULT ReadULONGLONG (   
   PROPID     id,  
   ULONGLONG* pValue  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `id`  
 [in] 읽을 속성의 식별자 (`PROPID` 으로 WTypes.h에 정의 되어 있는 한 `ULONG`).  
  
 `pValue`  
 [out] 속성 값을 반환 합니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`; 그렇지 않으면 오류 코드가 반환 됩니다. 반환 `E_INVALIDARG` 형식의 속성이 없으면 `ULONGLONG`합니다.  
  
## <a name="remarks"></a>설명  
 A `ULONGLONG` 64 비트 부호 없는 정수로 Windows에 의해 정의 됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)