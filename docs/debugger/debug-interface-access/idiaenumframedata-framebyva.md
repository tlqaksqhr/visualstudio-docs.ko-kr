---
title: 'Idiaenumframedata:: Framebyva | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData::frameByVA method
ms.assetid: 0b1e441b-710a-46d8-8060-bed39071c834
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0d19dcff2890291ca198092314b667cc3a0a7d33
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31458871"
---
# <a name="idiaenumframedataframebyva"></a>IDiaEnumFrameData::frameByVA
가상 주소 VA 여 프레임을 반환합니다.  
  
## <a name="syntax"></a>구문  
  
```C++  
HRESULT frameByVA(   
   ULONGLONG       virtualAddress,  
   IDiaFrameData** frame  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 virtualAddress  
 [in] 관심 있는 프레임의 VA 합니다.  
  
 프레임  
 [out] 반환 된 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md) 제공 되는 주소를 포함 하는 프레임을 나타내는 개체입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`합니다. 반환 `S_FALSE` 프레임 데이터가 지정 된 주소와 일치 합니다. 그러지 않으면 오류 코드가 반환됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)