---
title: 'Idiaenumsourcefiles:: Item | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSourceFiles::Item method
ms.assetid: 3c19d7ed-0232-4b0e-9b10-f33ed9e0c93b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b1fda746edf51771e7927efd03094f42903141e6
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31458345"
---
# <a name="idiaenumsourcefilesitem"></a>IDiaEnumSourceFiles::Item
인덱스를 사용 하 여 소스 파일을 검색합니다.  
  
## <a name="syntax"></a>구문  
  
```C++  
HRESULT Item (   
   DWORD            index,  
   IDiaSourceFile** sourceFile  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 인덱스입니다.  
 [in] 인덱스는 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md) 검색할 개체입니다. 인덱스는 0에서 범위에 `count`-1로, 여기서 `count` 에서 반환 되는 [idiaenumsourcefiles:: Get_count](../../debugger/debug-interface-access/idiaenumsourcefiles-get-count.md) 메서드.  
  
 원본 파일  
 [out] 반환 된 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md) 원하는 소스 파일을 나타내는 개체입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`, 그러지 않으면 오류 코드가 반환 됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDiaEnumSourceFiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md)   
 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)