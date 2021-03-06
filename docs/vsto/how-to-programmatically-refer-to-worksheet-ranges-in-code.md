---
title: '방법: 프로그래밍 방식으로 코드에서 워크시트 범위 참조 | Microsoft Docs'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, referring to
- worksheets, referring to ranges
- referring to worksheet ranges
- Excel [Office development in Visual Studio], referring to worksheet ranges
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 68845904a349a94df6ee09c05ca262434b847bbc
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
---
# <a name="how-to-programmatically-refer-to-worksheet-ranges-in-code"></a>방법: 프로그래밍 방식으로 코드에서 워크시트 범위 참조
  비슷한 프로세스를 사용 하 여의 내용을 참조 하는 <xref:Microsoft.Office.Tools.Excel.NamedRange> 컨트롤 또는 네이티브 Excel 범위 개체입니다.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="using-a-namedrange-control"></a>NamedRange 컨트롤을 사용 하 여  
 다음 예제에서는 추가 <xref:Microsoft.Office.Tools.Excel.NamedRange> 워크시트에 추가한 다음에 있는 셀 범위에 텍스트를 추가 합니다.  
  
#### <a name="to-refer-to-a-namedrange-control"></a>NamedRange 컨트롤 참조 하려면  
  
1.  문자열을 할당는 <xref:Microsoft.Office.Tools.Excel.NamedRange.Value2%2A> 의 속성은 <xref:Microsoft.Office.Tools.Excel.NamedRange> 제어 합니다. 이 코드는 `ThisWorkbook` 클래스가 아니라 시트 클래스에 배치해야 합니다.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#46](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#46)]
     [!code-vb[Trin_VstcoreExcelAutomation#46](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#46)]  
  
## <a name="using-native-excel-ranges"></a>네이티브 Excel 범위를 사용 하 여  
 다음 예제에서는 워크시트에 네이티브 Excel 범위를 추가 하 고에 있는 셀 범위에 텍스트를 추가 합니다.  
  
#### <a name="to-refer-to-a-native-range-object"></a>네이티브 범위 개체를 참조 하려면  
  
1.  문자열을 할당는 <xref:Microsoft.Office.Interop.Excel.Range.Value2%2A> 속성의 범위.  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#47](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#47)]
     [!code-vb[Trin_VstcoreExcelAutomation#47](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#47)]  
  
## <a name="see-also"></a>참고 항목  
 [범위 작업](../vsto/working-with-ranges.md)   
 [방법: 프로그래밍 방식으로 워크시트에서 맞춤법 검사](../vsto/how-to-programmatically-check-spelling-in-worksheets.md)   
 [방법: 프로그래밍 방식으로 통합 문서에서 범위에 스타일을 적용](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md)   
 [방법: 증분 변경 되는 데이터를 사용한 프로그래밍 방식으로 자동으로 범위를 입력](../vsto/how-to-programmatically-automatically-fill-ranges-with-incrementally-changing-data.md)   
 [방법: 프로그래밍 방식으로 워크시트 범위에서 텍스트 검색](../vsto/how-to-programmatically-search-for-text-in-worksheet-ranges.md)   
 [NamedRange 컨트롤](../vsto/namedrange-control.md)   
 [호스트 항목 및 호스트 컨트롤 개요](../vsto/host-items-and-host-controls-overview.md)   
 [호스트 항목 및 호스트 컨트롤의 프로그래밍에 대한 제한 사항](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)   
 [Office 솔루션의 선택적 매개 변수](../vsto/optional-parameters-in-office-solutions.md)  
  
  