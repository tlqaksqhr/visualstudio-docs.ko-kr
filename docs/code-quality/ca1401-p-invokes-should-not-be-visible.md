---
title: 'CA1401: P 호출 안 됩니다.'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- PInvokesShouldNotBeVisible
- CA1401
helpviewer_keywords:
- CA1401
- PInvokesShouldNotBeVisible
ms.assetid: 0f4d96c1-f9de-414e-b223-4dc7f691bee3
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c2aaadb0570e47e5ef41614925c20f8dc30f1620
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/26/2018
ms.locfileid: "31900606"
---
# <a name="ca1401-pinvokes-should-not-be-visible"></a>CA1401: P/Invoke는 노출되지 않아야 합니다.
|||
|-|-|
|TypeName|PInvokesShouldNotBeVisible|
|CheckId|CA1401|
|범주|Microsoft.Interoperability|
|변경 수준|주요 변경|

## <a name="cause"></a>원인
 공용 형식에서 public 또는 protected 메서드에 <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName> 특성 (으로 구현는 `Declare` 키워드 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]).

## <a name="rule-description"></a>규칙 설명
 로 표시 된 메서드는 <xref:System.Runtime.InteropServices.DllImportAttribute> 특성 (또는 사용 하 여 정의 된 메서드를는 `Declare` 키워드 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) 플랫폼 호출 서비스를 사용 하 여 비관리 코드에 액세스 합니다. 이러한 메서드는 노출되지 않아야 합니다. Private 또는 internal이 방법으로든 함으로써 수 있도록 호출자 그렇지 않으면 호출 하지 못했습니다 관리 되지 않는 Api에 대 한 액세스를 허용 하 여 보안 정책을 위반 하 여 라이브러리를 사용할 수 없습니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반 문제를 해결 하는 방법의 액세스 수준을 변경 합니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 이 규칙에서는 경고를 표시해야 합니다.

## <a name="example"></a>예제
 다음 예제에서는이 규칙을 위반 하는 메서드를 선언 합니다.

 [!code-vb[FxCop.Interoperability.DllImports#1](../code-quality/codesnippet/VisualBasic/ca1401-p-invokes-should-not-be-visible_1.vb)]
 [!code-csharp[FxCop.Interoperability.DllImports#1](../code-quality/codesnippet/CSharp/ca1401-p-invokes-should-not-be-visible_1.cs)]