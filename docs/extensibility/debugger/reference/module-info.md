---
title: MODULE_INFO | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- MODULE_INFO
helpviewer_keywords:
- MODULE_INFO structure
ms.assetid: f2e06180-1ab3-4eb5-a428-7994cceb61b6
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 6e28756873339d504efba417d9e2fe2cc00000b4
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31126718"
---
# <a name="moduleinfo"></a>MODULE_INFO
특정 모듈 (DLL, EXE 또는 어셈블리)에 대해 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
typedef struct tagMODULE_INFO {   
   MODULE_INFO_FIELDS dwValidFields;  
   BSTR               m_bstrName;  
   BSTR               m_bstrUrl;  
   BSTR               m_bstrVersion;  
   BSTR               m_bstrDebugMessage;  
   UINT64             m_addrLoadAddress;  
   UINT64             m_addrPreferredLoadAddress;  
   DWORD              m_dwSize;  
   DWORD              m_dwLoadOrder;  
   FILETIME           m_TimeStamp;  
   BSTR               m_bstrUrlSymbolLocation;  
   MODULE_FLAGS       m_dwModuleFlags;  
} MODULE_INFO;  
```  
  
```csharp  
public struct MODULE_INFO {   
   public uint     dwValidFields;  
   public string   m_bstrName;  
   public string   m_bstrUrl;  
   public string   m_bstrVersion;  
   public string   m_bstrDebugMessage;  
   public ulong    m_addrLoadAddress;  
   public ulong    m_addrPreferredLoadAddress;  
   public uint     m_dwSize;  
   public uint     m_dwLoadOrder;  
   public FILETIME m_TimeStamp;  
   public string   m_bstrUrlSymbolLocation;  
   public uint     m_dwModuleFlags;  
};  
```  
  
## <a name="members"></a>멤버  
 dwValidFields  
 플래그의 조합 된 [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md) 채워진 필드를 지정 하는 열거형입니다.  
  
 m_bstrName  
 모듈 이름입니다.  
  
 m_bstrUrl  
 모듈 URL입니다.  
  
 m_bstrVersion  
 모듈 버전입니다.  
  
 m_bstrDebugMessage  
 선택적 메시지는 모듈에 대 한 예를 들어 "기호 로드할 수 없습니다."  
  
 m_addrLoadAddress  
 모듈 로드 주소입니다.  
  
 m_addrPreferredLoadAddress  
 모듈의 기본 로드 주소입니다.  
  
 m_dwSize  
 모듈 크기입니다.  
  
 m_dwLoadOrder  
 모듈 로드 순서입니다.  
  
 m_TimeStamp  
 기호 파일을 마지막으로 수정한 시간입니다.  
  
 m_bstrUrlSymbolLocation  
 기호 파일의 위치 (예를 들어, ".\\") 모듈에 지정 합니다. 모듈의 기호를 찾는 시작 위치로 사용 합니다.  
  
 m_dwModuleFlags  
 플래그의 조합 된 [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md) 모듈에 설명 하는 열거형입니다.  
  
## <a name="remarks"></a>설명  
 이 구조에 전달 되는 [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md) 으로 채워지면 메서드.  
  
 에 나열 된 각 모듈에 해당 하는이 구조는 **모듈** 창.  
  
## <a name="requirements"></a>요구 사항  
 헤더: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>참고 항목  
 [구조체 및 공용 구조체](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md)   
 [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)