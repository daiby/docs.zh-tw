---
title: 如何：為 Windows Form NumericUpDown 控制項設定格式
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
ms.openlocfilehash: 1cb8f8b7d2f86125736c08cd9eadf4eee30063bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33533952"
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a>如何：為 Windows Form NumericUpDown 控制項設定格式
您可以設定 Windows Form 中值的顯示方式<xref:System.Windows.Forms.NumericUpDown>控制項。 <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A>屬性決定多少號碼會出現在小數點後面，則為預設值為 0。 <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A>屬性會決定是否將每隔三個十進位數字之間插入分隔符號，預設值為`false`。 此控制項可以顯示的值而不是十進位格式的十六進位表示的如果<xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A>屬性設定為`true`; 預設值是`false`。  
  
### <a name="to-format-the-numeric-value"></a>若要格式化的數值  
  
-   藉由設定顯示十進位值<xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A>屬性設為整數並設定<xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A>屬性`true`或`false`。  
  
    ```vb  
    NumericUpDown1.DecimalPlaces = 2  
    NumericUpDown1.ThousandsSeparator = True  
    ```  
  
    ```csharp  
    numericUpDown1.DecimalPlaces = 2;  
    numericUpDown1.ThousandsSeparator = true;  
    ```  
  
    ```cpp  
    numericUpDown1->DecimalPlaces = 2;  
    numericUpDown1->ThousandsSeparator = true;  
    ```  
  
     -或-  
  
-   藉由設定顯示的十六進位值<xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A>屬性`true`。  
  
    ```vb  
    NumericUpDown1.Hexadecimal = True  
    ```  
  
    ```csharp  
    numericUpDown1.Hexadecimal = true;  
    ```  
  
    ```cpp  
    numericUpDown1->Hexadecimal = true;  
    ```  
  
    > [!NOTE]
    >  即使將會顯示值為十六進位表單上，任何測試您在上執行<xref:System.Windows.Forms.NumericUpDown.Value%2A>屬性測試其十進位值。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Windows.Forms.NumericUpDown>  
 [NumericUpDown 控制項](../../../../docs/framework/winforms/controls/numericupdown-control-windows-forms.md)  
 [NumericUpDown 控制項概觀](../../../../docs/framework/winforms/controls/numericupdown-control-overview-windows-forms.md)
