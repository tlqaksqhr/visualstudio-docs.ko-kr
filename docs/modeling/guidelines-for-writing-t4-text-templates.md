---
title: T4 텍스트 템플릿 작성 지침
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: 08e18d654023dbf92f5c9e52fcd82f0c2ac3471c
ms.sourcegitcommit: 5b767247b3d819a99deb0dbce729a0562b9654ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/20/2018
ms.locfileid: "39178464"
---
# <a name="guidelines-for-writing-t4-text-templates"></a>T4 텍스트 템플릿 작성 지침
다음 일반 지침 프로그램 코드 또는 기타 응용 프로그램 리소스에서 생성 하는 경우에 유용할 수 있습니다 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]합니다. 규칙 고정 되지 것입니다.

## <a name="guidelines-for-design-time-t4-templates"></a>디자인 타임 T4 템플릿에 대 한 지침
 디자인 타임 T4 템플릿은 템플릿 코드에서 생성 하는 프로그램 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 디자인 타임에 프로젝트입니다. 자세한 내용은 [T4 텍스트 템플릿을 사용 하 여 디자인 타임 코드 생성](../modeling/design-time-code-generation-by-using-t4-text-templates.md)합니다.

 응용 프로그램의 가변 측면을 생성 합니다.
코드를 생성 하는 동안 프로젝트에 변경 될 수 있습니다 또는 응용 프로그램의 서로 다른 버전 간에 변경 될 응용 프로그램의 이러한 측면에 대 한 가장 유용 합니다. 생성할에 어떤를 보다 쉽게 확인할 수 있도록 더 고정 측면에서 이러한 가변 측면을 구분 합니다. 예를 들어, 응용 프로그램 웹 사이트에서 제공 하는 경우 표준 페이지 함수에서 다른 페이지로 탐색 경로 정의 하는 논리에서 처리를 구분 합니다.

 하나 이상의 원본 모델에 가변 측면을 인코딩하십시오.
모델은 파일이 나 데이터베이스 생성 되는 코드의 변수 부분에 대 한 특정 값을 가져오려면 각 템플릿에 읽는 경우 모델은 데이터베이스, 사용자 고유의 디자인, 다이어그램 또는 도메인 특정 언어의 XML 파일 일 수 있습니다. 여러 파일을 생성 한 모델을 사용 하는 일반적으로 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 프로젝트입니다. 각 파일은 별도 템플릿에서 생성 됩니다.

 프로젝트에서 하나 이상의 모델을 사용할 수 있습니다. 예를 들어, 웹 페이지 및 페이지의 레이아웃에 대 한 별도 모델 간의 탐색에 대 한 모델을 정의할 수 있습니다.

 사용자의 요구 사항 및 어휘에서 구현에 모델 중점을 둡니다.
예를 들어, 웹 사이트 응용 프로그램에서 예상한 모델을 웹 페이지 및 하이퍼링크를 참조 하십시오.

 이상적으로 모델에서 나타내는 정보의 종류에 적합 한 표현 폼을 선택 합니다. 예를 들어 모델을 통해 웹 사이트 탐색 경로의 상자와 화살표의 다이어그램을 수 있습니다.

 생성된 된 코드를 테스트 합니다.
수동 또는 자동화 된 테스트를 사용 하 여 결과 코드는 사용자가 필요로 하는 대로 작동 하는지 확인 합니다. 코드 생성 되는 동일한 모델에서 테스트를 생성 하지 마세요.

 경우에 따라 일반 테스트 모델에서 직접 수행할 수 있습니다. 예를 들어 시스템에서 다른 탐색 하 여 웹 사이트의 모든 페이지에 연결할 수 있는지 확인 하는 테스트를 작성할 수 있습니다.

 사용자 지정 코드에 대 한 허용: 부분 클래스를 생성 합니다.
작성 하는 코드를 직접 또한 생성된 된 코드를 허용 합니다. 코드 생성 체계에서 발생할 수 있는 모든 가능한 변형을 계정 수에 대 한 일반적인 것입니다. 따라서를 추가 하거나 생성된 된 코드의 일부를 재정의 하는 기대할 수 있습니다. 여기서 생성된 된 자료는.NET 언어에서와 같은 [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] 또는 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)], 두 가지 전략은 특히 유용 합니다.

-   생성된 된 클래스를 부분 이어야 합니다. 이렇게 하면 생성된 된 코드에 내용을 추가할 수 있습니다.

-   클래스 상속을 다른 하나는 쌍으로 생성 되어야 합니다. 기본 클래스는 생성 된 메서드 및 속성을 모두 포함 해야 하 고 파생된 클래스는 생성자만 포함 해야 합니다. 따라서 생성된 된 메서드 중 하나를 재정의 하 여 직접 작성 한 코드.

 XML과 같은 다른 생성 된 언어를 사용 하 여는 `<#@include#>` 지시문을 직접 작성 하 고 생성 된 콘텐츠의 간단한 조합을 확인 합니다. 더 복잡 한 경우에 직접 작성 된 파일을 사용 하 여 생성된 된 파일을 결합 하는 후 처리 단계를 작성 해야 합니다.

 포함 파일에 공통 자료를 이동 하거나 방지 하려면 런타임 템플릿 사용 하 여 유사한 텍스트 및 여러 서식 파일에서 코드 블록을 반복 합니다 `<#@ include #>` 지시문입니다. 자세한 내용은 [T4 Include 지시문](../modeling/t4-include-directive.md)합니다.

 별도 프로젝트에서 런타임 텍스트 템플릿 빌드하고 디자인 타임 템플릿의 부르도 있습니다. 이 위해 사용 하 여는 `<#@ assembly #>` 지시문 별도 프로젝트에 액세스할 수 있습니다. 예제를 보려면 [상속에 텍스트 "템플릿" Gareth Jones 블로그의](http://go.microsoft.com/fwlink/?LinkId=208373)합니다.

 큰 코드 블록을 별도 어셈블리로 이동 하는 것이 좋습니다.
 대규모 코드 블록과 클래스 기능 블록에 있는 경우에 별도 프로젝트에서 컴파일되지 메서드로 이동 하는이 코드의 일부에 유용할 수 있습니다. 사용할 수는 `<#@ assembly #>` 템플릿에서 코드에 액세스 하는 지시문입니다. 자세한 내용은 [T4 Assembly 지시문](../modeling/t4-assembly-directive.md)합니다.

 서식 파일을 상속할 수 있는 추상 클래스에서 메서드를 넣을 수 있습니다. 추상 클래스에서 상속 해야 <xref:Microsoft.VisualStudio.TextTemplating.TextTransformation?displayProperty=fullName>합니다. 자세한 내용은 [T4 템플릿 지시문](../modeling/t4-template-directive.md)합니다.

 코드를 생성, 하지 구성 파일 하나 변수 응용 프로그램을 작성 하는 방법은 구성 파일을 허용 하는 일반 프로그램 코드를 작성 합니다. 이 방식으로 작성 된 응용 프로그램은 매우 유연 하 고 응용 프로그램을 다시 작성 하지 않고 비즈니스 요구 사항이 변경 되 면 다시 구성할 수 있습니다. 그러나이 방법의 단점은 응용 프로그램에 보다 구체적인 응용 프로그램을 보다 커지고 수행 되는 점입니다. 또한, 대부분의 제네릭 형식으로 처리 하기 위해 항상 있기 때문에 부분적으로 프로그램 코드를 읽고 유지 관리 하기가 더 어렵습니다 수 있습니다.

 반면, 해당 변수 부분 컴파일 전에 생성 된 응용 프로그램 강력 하 게 입력할 수 있습니다. 따라서이 소프트웨어의 부분을 훨씬 더 쉽고 안정를 직접 작성 한 코드를 작성 하 여 생성 된 통합 합니다.

 코드 생성의 모든 이점을 얻으려면, 구성 파일 대신 프로그램 코드를 생성 하려고 합니다.

 사용 하 여 Generated Code 폴더 라는 프로젝트 폴더에는 템플릿 및 생성된 된 파일을 배치할 **생성 된 코드**, 있도록 이러한 되지 않는다는 사실을 직접 편집 해야 하는 파일의 선택을 취소 합니다. 재정의 생성된 된 클래스에 추가 하거나 사용자 지정 코드를 만드는 경우 해당 클래스 라는 폴더에 배치 **사용자 지정 코드**합니다. 일반적인 프로젝트의 구조는 다음과 같습니다.

```
MyProject
   Custom Code
      Class1.cs
      Class2.cs
   Generated Code
      Class1.tt
          Class1.cs
      Class2.tt
          Class2.cs
   AnotherClass.cs

```

## <a name="guidelines-for-run-time-preprocessed-t4-templates"></a>런타임 전처리 된 T4 템플릿에 대 한 지침
 공통 자료 이동를 상속 된 템플릿으로 메서드 및 T4 텍스트 템플릿 간에 텍스트 블록을 공유 하려면 상속을 사용할 수 있습니다. 자세한 내용은 [T4 템플릿 지시문](../modeling/t4-template-directive.md)합니다.

 사용할 수도 있습니다 런타임 템플릿 파일이 포함 됩니다.

 큰 코드 본문을 partial 클래스로 이동 합니다.
각 런타임 템플릿은 템플릿으로 동일한 이름을 갖는 partial 클래스 정의 생성 합니다. 동일한 클래스의 다른 부분 정의 포함 하는 코드 파일을 작성할 수 있습니다. 이 방식으로 클래스에 메서드, 필드 및 생성자를 추가할 수 있습니다. 이러한 멤버 템플릿의 코드 블록에서 호출할 수 있습니다.

 이 작업을 수행 하는 이점은 점 IntelliSense를 사용할 수 있으므로 코드를 작성할 수입니다. 또한 더 나은 구분을 프레젠테이션과 기본 논리를 수행할 수 있습니다.

 예를 들어 **MyReportText.tt**:

 `The total is: <#= ComputeTotal() #>`

 **MyReportText Methods.cs**:

 `private string ComputeTotal() { ... }`

 사용자 지정 코드에 대 한 허용:에서 생성할 가상 메서드는 것이 좋습니다 확장 지점을 제공 \<#+ 클래스 기능 블록 #>. 이렇게 하면 단일 템플릿을 수정 하지 않고 여러 컨텍스트에서 사용할 수 있습니다. 템플릿을 수정 하는 대신 최소한의 추가 논리를 제공 하는 파생된 클래스를 생성할 수 있습니다. 파생된 클래스에는 일반 코드 이거나 수 또는 런타임 템플릿으로 수 있습니다.

 MyStandardRunTimeTemplate.tt의 예를 들어:

```
This page is copyright <#= CompanyName() #>.
<#+ protected virtual string CompanyName() { return ""; } #>
```

 응용 프로그램의 코드:

```
class FabrikamTemplate : MyStandardRunTimeTemplate
{
  protected override string CompanyName() { return "Fabrikam"; }
}
...
  string PageToDisplay = new FabrikamTemplate().TextTransform();

```

## <a name="guidelines-for-all-t4-templates"></a>모든 T4 템플릿 지침
 텍스트 생성에서 별도 데이터 수집 계산 및 텍스트 블록이 혼합 하지 마십시오. 각 텍스트 템플릿에서 첫 번째를 사용 하 여 \<# 코드가 차단 #> 변수를 설정 하 여 복잡 한 계산을 수행 합니다. 첫 번째 텍스트 블록의 템플릿 또는 첫 번째 끝까지 \<#+ 클래스 기능 블록 #>, 긴 식이 방지 및 텍스트 블록이 포함 되지 않으면 루프 및 조건문을 방지 합니다. 이렇게 하면 템플릿을 보다 쉽게 읽고 유지 관리 합니다.

 사용 하지 마세요 `.tt` 포함에 대 한 파일 사용 하 여 다른 파일 이름 확장명을 같은 `.ttinclude` 포함 파일입니다. 사용 하 여 `.tt` 되도록 원하는 파일을 같은 런타임 또는 디자인 타임 텍스트 템플릿 처리에 대 한만 합니다. 경우에 따라 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 인식 `.tt` 파일을 자동으로 처리를 위해 해당 속성을 설정 합니다.

 고정 된 프로토타입으로 각 서식 파일을 시작 합니다.
코드 또는 텍스트를 생성 하 고 정확한 지 확인 하려는 예제를 작성 합니다. 확장명이.tt을 변경 하 고 증분 방식으로 모델을 참조 하 여 콘텐츠를 수정 하는 코드를 삽입 합니다.

 형식화 된 모델을 사용 하는 것이 좋습니다.
모델에 대해 XML 또는 데이터베이스 스키마를 만들 수 있습니다, 있지만 도메인 특정 언어 (DSL)를 만드는 것이 유용할 수 있습니다. DSL은 스키마 및 속성을 특성을 나타내는 각 노드를 나타내는 클래스를 생성 하는 이점이 있습니다. 즉, 비즈니스 모델을 기준으로 프로그래밍할 수 있습니다. 예를 들어:

```
Team Members:
<# foreach (Person p in team.Members)
 { #>
    <#= p.Name #>
<# } #>
```

 모델에 대 한 다이어그램을 사용 하는 것이 좋습니다.
가장 효과적으로 많은 모델이 표시 하 고 매우 큰 경우에 특히 텍스트 테이블로 간단히 관리는 합니다.

 그러나 일부 종류의 비즈니스 요구 사항에 대 한 것이 복잡 한 작업 흐름 및 관계 집합을 명확 하 게 중요 및 다이어그램은 가장 적합 한 미디어입니다. 다이어그램의 장점은 사용자 및 기타 관련자와 쉽게 논의할 수 것입니다. 비즈니스 요구 사항 수준 모델에서 코드를 생성, 있게 코드 보다 유연한 요구 사항이 변경 됩니다.

 도메인 특정 언어 (DSL)로 다이어그램의 고유한 형식을 디자인할 수도 있습니다. UML 및 Dsl에서 코드를 생성할 수 있습니다. 자세한 내용은 [아키텍처 분석 및 모델링](../modeling/analyze-and-model-your-architecture.md)합니다.

## <a name="see-also"></a>참고 항목

- [T4 텍스트 템플릿을 사용하여 디자인 타임 코드 생성](../modeling/design-time-code-generation-by-using-t4-text-templates.md)
- [T4 텍스트 템플릿을 사용하여 런타임 텍스트 생성](../modeling/run-time-text-generation-with-t4-text-templates.md)
