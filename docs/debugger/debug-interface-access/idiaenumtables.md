---
title: IDiaEnumTables | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables interface
ms.assetid: 016190c5-09e4-48f2-bf60-9b02603a03e0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4018b347b3fa6989a2dbd2116ac2c234ebfb70f8
ms.sourcegitcommit: 0bf2aff6abe485e3fe940f5344a62a885ad7f44e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/27/2018
ms.locfileid: "37058089"
---
# <a name="idiaenumtables"></a>IDiaEnumTables
데이터 원본에 포함 된 다양 한 테이블을 열거 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
IDiaEnumTables : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable 순서의 메서드  
 다음 표에서의 메서드를 보여 줍니다. `IDiaEnumTables`합니다.  
  
|메서드|설명|  
|------------|-----------------|  
|[IDiaEnumTables::get__NewEnum](../../debugger/debug-interface-access/idiaenumtables-get-newenum.md)|검색 된 [IEnumVARIANT 인터페이스](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) 이 열거자의 버전입니다.|  
|[IDiaEnumTables::get_Count](../../debugger/debug-interface-access/idiaenumtables-get-count.md)|테이블을 검색합니다.|  
|[IDiaEnumTables::Item](../../debugger/debug-interface-access/idiaenumtables-item.md)|인덱스 또는 이름을 사용 하 여 테이블을 검색합니다.|  
|[IDiaEnumTables::Next](../../debugger/debug-interface-access/idiaenumtables-next.md)|열거형 시퀀스에서 테이블의 지정된 된 수를 검색 합니다.|  
|[IDiaEnumTables::Skip](../../debugger/debug-interface-access/idiaenumtables-skip.md)|열거형 시퀀스에는 테이블의 지정 된 수를 건너뜁니다.|  
|[IDiaEnumTables::Reset](../../debugger/debug-interface-access/idiaenumtables-reset.md)|열거형 시퀀스를 처음으로 다시 설정합니다.|  
|[IDiaEnumTables::Clone](../../debugger/debug-interface-access/idiaenumtables-clone.md)|현재 열거자와 열거 상태가 같은 포함 하는 열거자를 만듭니다.|  
  
## <a name="remarks"></a>설명  
  
## <a name="notes-for-callers"></a>호출자에 대 한 정보  
 이 인터페이스를 호출 하 여 가져올는 [idiasession:: Getenumtables](../../debugger/debug-interface-access/idiasession-getenumtables.md) 메서드.  
  
## <a name="example"></a>예  
 가져오는 방법을 보여 주는이 예제는 `IDiaEnumTables` 세션에서 인터페이스입니다. 테이블을 사용 하 여 자세한 예제를 참조 하세요. 합니다 [IDiaTable](../../debugger/debug-interface-access/idiatable.md) 인터페이스입니다.  
  
```C++  
void ShowTableNames(IDiaSession *pSession)  
{  
    CComPtr<IDiaEnumTables> pTables;  
    if ( FAILED( psession->getEnumTables( &pTables ) ) )  
    {  
        Fatal( "getEnumTables" );  
    }  
    // Do something with table  
}  
```  
  
## <a name="requirements"></a>요구 사항  
 헤더: Dia2.h  
  
 라이브러리: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>참고 항목  
 [인터페이스 (디버그 인터페이스 액세스 SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession-getenumtables.md)