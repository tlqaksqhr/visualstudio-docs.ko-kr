---
title: 단위 테스트 만들기 명령을 사용하여 단위 테스트 메서드 스텁 만들기
ms.date: 05/02/2017
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: conceptual
helpviewer_keywords:
- IntelliTest, Get started
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 72bba467bae5528333b520bdb40f5f4593982df2
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/26/2018
ms.locfileid: "31966502"
---
# <a name="get-started-with-microsoft-intellitest"></a>Microsoft IntelliTest 시작

* IntelliTest를 처음 사용하는 경우 다음과 같이 하세요.
  * [Channel 9 비디오](https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Intellitest) 시청
  * 이 [MSDN Magazine 개요](https://msdn.microsoft.com/magazine/dn904672.aspx) 읽기
  * [설명서](../../test/generate-unit-tests-for-your-code-with-intellitest.md) 읽기
* [Stack Overflow](http://stackoverflow.com/questions/tagged/intellitest)에 대한 질문하기
* 이 참조 설명서의 나머지 부분 읽기
* 빠른 참조용으로 이 페이지 인쇄

## <a name="important-attributes"></a>중요한 특성

* [PexClass](attribute-glossary.md#pexclass)는 **PUT**가 포함된 형식을 표시합니다.
* [PexMethod](attribute-glossary.md#pexmethod)는 **PUT**를 표시합니다.
* [PexAssumeNotNull](attribute-glossary.md#pexassumenotnull)은 null이 아닌 매개 변수를 표시합니다.

```csharp
using Microsoft.Pex.Framework;

[..., PexClass(typeof(Foo))]
public partial class FooTest {
    [PexMethod]
    public void Bar([PexAssumeNotNull]Foo target, int i) {
        target.Bar(i);
    }
}
```

* [PexAssemblyUnderTest](attribute-glossary.md#pexassemblyundertest)는 테스트 프로젝트를 프로젝트에 바인딩합니다.
* [PexInstrumentAssembly](attribute-glossary.md#pexinstrumentassemblyattribute)는 계측할 어셈블리를 지정합니다.

```csharp
[assembly: PexAssemblyUnderTest("MyAssembly")] // also instruments "MyAssembly"
[assembly: PexInstrumentAssembly("Lib")]
```

## <a name="helper-classes"></a> 중요한 정적 도우미 클래스

* [PexAssume](static-helper-classes.md#pexassume)은 가정을 평가합니다(입력 필터링).
* [PexAssert](static-helper-classes.md#pexassert)는 어설션을 평가합니다.
* [PexChoose](static-helper-classes.md#pexchoose)는 새 선택 항목을 생성합니다(추가 입력).
* [PexObserve](static-helper-classes.md#pexobserve)는 생성된 테스트에 대한 라이브 값을 기록합니다.

```csharp
[PexMethod]
void StaticHelpers(Foo target) {
    PexAssume.IsNotNull(target);

    int i = PexChoose.Value<int>("i");
    string result = target.Bar(i);

    PexObserve.ValueForViewing<string>("result", result);
    PexAssert.IsNotNull(result);
}
```

## <a name="got-feedback"></a>피드백이 있으신가요?

아이디어와 기능 요청을 [UserVoice](https://visualstudio.uservoice.com/forums/121579-visual-studio-2015/category/157869-test-tools?query=IntelliTest)에 게시하세요.
