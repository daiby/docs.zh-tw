---
title: 如何：取得列印系統物件屬性但不使用反映
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PrintSystemObject [WPF], getting properties
ms.assetid: 43560f28-183d-41c1-b9d1-de7c2552273e
ms.openlocfilehash: 1fa8029b8245aef5e10e9082a1038fd89fc1c84e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544726"
---
# <a name="how-to-get-print-system-object-properties-without-reflection"></a>如何：取得列印系統物件屬性但不使用反映
使用反映詳細列出的物件上的屬性 （和這些屬性的類型） 不會降低應用程式的效能。 <xref:System.Printing.IndexedProperties>命名空間提供方法來取得這項資訊與使用反映。  
  
## <a name="example"></a>範例  
 執行此作業的步驟如下所示。  
  
1.  建立類型的執行個體。 在下列範例中，此類型是<xref:System.Printing.PrintQueue>隨附於 Microsoft.NET Framework，但幾乎完全相同的程式碼的類型應該能用於類型衍生自<xref:System.Printing.PrintSystemObject>。  
  
2.  建立<xref:System.Printing.IndexedProperties.PrintPropertyDictionary>的型別<xref:System.Printing.PrintSystemObject.PropertiesCollection%2A>。 <xref:System.Collections.DictionaryEntry.Value%2A>此字典中的每個項目的屬性是物件的其中一個衍生自類型<xref:System.Printing.IndexedProperties.PrintProperty>。  
  
3.  列舉字典的成員。 針對每一項，執行下列作業。  
  
4.  向上轉型至每個項目的值<xref:System.Printing.IndexedProperties.PrintProperty>並用它來建立<xref:System.Printing.IndexedProperties.PrintProperty>物件。  
  
5.  取得類型的<xref:System.Printing.IndexedProperties.PrintProperty.Value%2A>的每個<xref:System.Printing.IndexedProperties.PrintProperty>物件。  
  
 [!code-csharp[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/CSharp/Program.cs#showpropertytypeswithoutreflection)]
 [!code-vb[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/visualbasic/program.vb#showpropertytypeswithoutreflection)]  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Printing.IndexedProperties.PrintProperty>  
 <xref:System.Printing.PrintSystemObject>  
 <xref:System.Printing.IndexedProperties>  
 <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>  
 <xref:System.Printing.LocalPrintServer>  
 <xref:System.Printing.PrintQueue>  
 <xref:System.Collections.DictionaryEntry>  
 [WPF 中的文件](../../../../docs/framework/wpf/advanced/documents-in-wpf.md)  
 [列印概觀](../../../../docs/framework/wpf/advanced/printing-overview.md)
