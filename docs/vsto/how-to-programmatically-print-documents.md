---
title: '방법: 프로그래밍 방식으로 문서를 인쇄 | Microsoft Docs'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], printing documents
- documents [Office development in Visual Studio], printing
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 1a5364bd2cf0f0ea6d5e7ceb7c8a427c5aea301d
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
---
# <a name="how-to-programmatically-print-documents"></a>방법: 프로그래밍 방식으로 문서 인쇄
  전체 Microsoft Office Word 문서 또는 일부 문서를 기본 프린터에 인쇄할 수 있습니다.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
## <a name="printing-a-document-that-is-part-of-a-document-level-customization"></a>문서 수준 사용자 지정의 일부인 문서 인쇄  
  
#### <a name="to-print-the-entire-document"></a>전체 문서를 인쇄하려면  
  
1.  프로젝트의 <xref:Microsoft.Office.Tools.Word.Document.PrintOut%2A> 클래스의 `ThisDocument` 메서드를 호출하여 전체 문서를 인쇄합니다. 이 예제를 사용하려면 `ThisDocument` 클래스에서 코드를 실행합니다.  
  
     [!code-vb[Trin_VstcoreWordAutomation#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#11)]
     [!code-csharp[Trin_VstcoreWordAutomation#11](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#11)]  
  
#### <a name="to-print-the-current-page-of-the-document"></a>문서의 현재 페이지를 인쇄하려면  
  
1.  프로젝트의 <xref:Microsoft.Office.Tools.Word.Document.PrintOut%2A> 클래스의 `ThisDocument` 메서드를 호출하고 현재 페이지의 복사본 하나를 인쇄하도록 지정합니다. 이 예제를 사용하려면 `ThisDocument` 클래스에서 코드를 실행합니다.  
  
     [!code-vb[Trin_VstcoreWordAutomation#12](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#12)]
     [!code-csharp[Trin_VstcoreWordAutomation#12](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#12)]  
  
## <a name="printing-a-document-by-using-an-vsto-add-in"></a>VSTO 추가 기능을 사용하여 문서 인쇄  
  
#### <a name="to-print-an-entire-document"></a>전체 문서를 인쇄하려면  
  
1.  인쇄하려는 <xref:Microsoft.Office.Interop.Word._Document.PrintOut%2A> 개체의 <xref:Microsoft.Office.Interop.Word.Document> 메서드를 호출합니다. 다음 코드 예제에서는 활성 문서를 인쇄합니다. 이 예제를 사용하려면 프로젝트의 `ThisAddIn` 클래스에서 코드를 실행합니다.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#11)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#11](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#11)]  
  
#### <a name="to-print-the-current-page-of-a-document"></a>문서의 현재 페이지를 인쇄하려면  
  
1.  인쇄하려는 <xref:Microsoft.Office.Interop.Word._Document.PrintOut%2A> 개체의 <xref:Microsoft.Office.Interop.Word.Document> 메서드를 호출하고 현재 페이지의 복사본 하나를 인쇄하도록 지정합니다. 다음 코드 예제에서는 활성 문서를 인쇄합니다. 이 예제를 사용하려면 프로젝트의 `ThisAddIn` 클래스에서 코드를 실행합니다.  
  
     [!code-vb[Trin_VstcoreWordAutomationAddIn#12](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#12)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#12](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#12)]  
  
## <a name="see-also"></a>참고 항목  
 [Office 솔루션의 선택적 매개 변수](../vsto/optional-parameters-in-office-solutions.md)  
  
  