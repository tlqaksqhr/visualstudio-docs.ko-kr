---
title: 'Idiaenumframedata:: Item | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData::Item method
ms.assetid: 2761a72d-1868-4f5b-a32e-c2a1d9358c91
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d725c38073b82bc94081b3c27791e88f64343cd3
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31458111"
---
# <a name="idiaenumframedataitem"></a>IDiaEnumFrameData::Item
인덱스를 사용 하 여 프레임 데이터 요소를 검색합니다.  
  
## <a name="syntax"></a>구문  
  
```C++  
HRESULT Item (   
   DWORD           index,  
   IDiaFrameData** section  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 인덱스입니다.  
 [in] 인덱스는 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md) 검색할 개체입니다. 인덱스는 0에서 범위에 `count`-1로, 여기서 `count` 에서 반환 되는 [idiaenumframedata:: Get_count](../../debugger/debug-interface-access/idiaenumframedata-get-count.md) 메서드.  
  
 section  
 [out] 반환 된 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md) 원하는 프레임 데이터 요소를 나타내는 개체입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`, 그러지 않으면 오류 코드가 반환 됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)