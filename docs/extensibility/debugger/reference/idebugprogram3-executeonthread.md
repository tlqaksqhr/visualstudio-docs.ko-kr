---
title: IDebugProgram3::ExecuteOnThread | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- IDebugProgram3::ExecuteOnThread
ms.assetid: 2f5211e3-7a3f-47bf-9595-dfc8b4895d0d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8aff643014da16ed9644573a77cb8444836d713d
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31117064"
---
# <a name="idebugprogram3executeonthread"></a>IDebugProgram3::ExecuteOnThread
디버거가 프로그램을 실행합니다. 스레드를 사용자가 프로그램을 실행 하는 경우 보고 디버거 정보를 제공 하는 스레드 반환 됩니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT ExecuteOnThread(  
   [in] IDebugThread2* pThread)  
```  
  
```csharp  
int ExecuteOnThread(  
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pThread`  
 [in] [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) 개체입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`, 그러지 않으면 오류 코드가 반환 됩니다.  
  
## <a name="remarks"></a>설명  
 디버거 중지 한 후 실행을 재개할 수는 세 가지 방법으로  
  
-   실행: 이전 단계를 취소 하 고 등 다음 중단점까지 실행 합니다.  
  
-   단계: 이전 단계를 취소 하 고 새 단계 완료 될 때까지 실행 합니다.  
  
-   계속: 다시 실행 하 고 이전 단계를 활성 상태로 유지 합니다.  
  
 에 전달 되는 스레드 `ExecuteOnThread` 취소 하려면 단계를 결정할 때 유용 합니다. 스레드를 실행 중인 실행 알 수 없는 모든 단계를 취소 합니다. 스레드 정보를 현재 스레드에서 단계 취소 하기만 하면 됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [실행](../../../extensibility/debugger/reference/idebugprogram2-execute.md)   
 [IDebugProgram3](../../../extensibility/debugger/reference/idebugprogram3.md)