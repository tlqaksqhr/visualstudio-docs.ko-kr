---
title: IActiveScriptDebug::GetScriptletTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptDebug.GetScriptletTextAttributes
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptDebug::GetScriptletTextAttributes
ms.assetid: b3990d86-5fdf-4c9f-9678-3f4b808c7ca8
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 909879030e5c6d26353d2003279d5c1ca7bacb74
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2017
ms.locfileid: "24724433"
---
# <a name="iactivescriptdebuggetscriptlettextattributes"></a>IActiveScriptDebug::GetScriptletTextAttributes
임의의 스크립틀릿에 대 한 텍스트 특성을 반환합니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT GetScriptletTextAttributes(  
   LPCOLESTR          pstrCode,  
   ULONG              uNumCodeChars,  
   LPCOLESTR          pstrDelimiter,  
   DWORD              dwFlags,  
   SOURCE_TEXT_ATTR*  pattr  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pstrCode`  
 [in] 스크립틀릿 텍스트입니다. 이 문자열에는 null 종료 아니어도 됩니다.  
  
 `uNumCodeChars`  
 [in] 스크립틀릿 텍스트의 문자 수입니다.  
  
 `pstrDelimiter`  
 [in] 주소는 스크립틀릿 끝 구분 기호입니다. 때 `pstrCode` 구문 분석 되 텍스트의 스트림에서 호스트 일반적으로 사용 하 여 구분 기호, 예: 두 개의 작은 따옴표 (")는 스크립틀릿의 끝을 검색 합니다. 이 매개 변수 지정 호스트 사용 조건부 몇 가지 기본 전처리를 제공 하는 스크립팅 엔진 수 있도록 하는 구분 기호 (예를 들어 작은따옴표로 구분 기호로 사용 하기 위해 두 개의 작은따옴표 ['] 교체) 됩니다. 방식을 정확 하 게 (및 if)의 스크립팅 엔진이 사용 하는 스크립팅 엔진에이 정보에 따라 달라 집니다. 호스트는 스크립틀릿의 끝을 표시 하는 구분 기호를 사용 하지 않은 경우이 매개 변수를 NULL로 설정 합니다.  
  
 `dwFlags`  
 [in] 스크립틀릿와 관련 된 플래그입니다. 이러한 값의 조합 될 수 있습니다.  
  
|상수|값|설명|  
|--------------|-----------|-----------------|  
|GETATTRTYPE_DEPSCAN|0x0001|식별자 및 점 연산자 식별 해야 SOURCETEXT_ATTR_IDENTIFIER 및 SOURCETEXT_ATTR_MEMBERLOOKUP 플래그와 함께 각각 나타냅니다.|  
|GETATTRFLAG_THIS|0x0100|현재 개체에 대 한 식별자 SOURCETEXT_ATTR_THIS 플래그로 식별 되어야 합니다를 나타냅니다.|  
|GETATTRFLAG_HUMANTEXT|0x8000|문자열 콘텐츠 및 메모 텍스트 SOURCETEXT_ATTR_HUMANTEXT 플래그로 식별 되어야 합니다를 나타냅니다.|  
  
 `pattr`  
 [out에서] 반환 된 특성이 포함 될 버퍼입니다.  
  
## <a name="return-value"></a>반환 값  
 이 메서드는 `HRESULT`를 반환합니다. 가능한 값에는 다음 표에 있는 값이 포함되지만, 이에 국한되는 것은 아닙니다.  
  
|값|설명|  
|-----------|-----------------|  
|`S_OK`|메서드가 성공했으며|  
  
## <a name="remarks"></a>설명  
 구현 하는 스마트 호스트로 `IDebugDocumentText` 인터페이스에 대 한 호출을 위임 하려면이 메서드를 사용할 수는 `IDebugDocumentText::GetText` 메서드.  
  
 이 호출은 스크립틀릿 식 이어야 하 고 가질 수 스크립트 블록 보다 서로 다른 구문을 제공 됩니다. 이 메서드 구현은의 구현으로 동일할 경우 동일한 구문이 있는 경우는 `GetScriptTextAttributes` 메서드.  
  
## <a name="see-also"></a>참고 항목  
 [IActiveScriptDebug 인터페이스](../../winscript/reference/iactivescriptdebug-interface.md)   
 [IActiveScriptDebug::GetScriptTextAttributes](../../winscript/reference/iactivescriptdebug-getscripttextattributes.md)   
 [IDebugDocumentText 인터페이스](../../winscript/reference/idebugdocumenttext-interface.md)   
 [IDebugDocumentText::GetText](../../winscript/reference/idebugdocumenttext-gettext.md)   
 [SOURCE_TEXT_ATTR 열거형](../../winscript/reference/source-text-attr-enumeration.md)