---
title: struct (C# 參考)
ms.date: 07/20/2015
f1_keywords:
- struct_CSharpKeyword
helpviewer_keywords:
- struct keyword [C#]
- structs [C#], struct keyword
ms.assetid: ff3dd9b7-dc93-4720-8855-ef5558f65c7c
ms.openlocfilehash: 7931da2e5f5c493b54eb1f33a1d6f57b38592f6e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2018
ms.locfileid: "43530188"
---
# <a name="struct-c-reference"></a>struct (C# 參考)
`struct` 類型是實值類型，通常可用來封裝一小組相關變數，例如矩形的座標，或詳細目錄中某個項目的特性。 下列範例示範簡單結構宣告：  
  
```csharp  
public struct Book  
{  
    public decimal price;  
    public string title;  
    public string author;  
}  
```  
  
## <a name="remarks"></a>備註  
 結構還包含[建構函式](../../../csharp/programming-guide/classes-and-structs/constructors.md)、[常數](../../../csharp/programming-guide/classes-and-structs/constants.md)、[欄位](../../../csharp/programming-guide/classes-and-structs/fields.md)、[方法](../../../csharp/programming-guide/classes-and-structs/methods.md)、[屬性](../../../csharp/programming-guide/classes-and-structs/properties.md)、[索引子](../../../csharp/programming-guide/indexers/index.md)、[運算子](../../../csharp/programming-guide/statements-expressions-operators/operators.md)、[事件](../../../csharp/programming-guide/events/index.md)和[巢狀型別](../../../csharp/programming-guide/classes-and-structs/nested-types.md)，不過如果需要數個這類成員，您應該考慮以類別來取代類型。  
  
 如需範例，請參閱[使用結構](../../../csharp/programming-guide/classes-and-structs/using-structs.md)。  
  
 結構可以實作介面，但無法繼承自其他結構。 因此，結構成員無法宣告為 `protected`。  
  
 如需詳細資訊，請參閱[結構](../../../csharp/programming-guide/classes-and-structs/structs.md)。  
  
## <a name="examples"></a>範例  
 如需範例和詳細資訊，請參閱[使用結構](../../../csharp/programming-guide/classes-and-structs/using-structs.md)。  
  
## <a name="c-language-specification"></a>C# 語言規格  
 如需範例，請參閱[使用結構](../../../csharp/programming-guide/classes-and-structs/using-structs.md)。  
  
## <a name="see-also"></a>請參閱

- [C# 參考](../../../csharp/language-reference/index.md)  
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
- [C# 關鍵字](../../../csharp/language-reference/keywords/index.md)  
- [預設值表](../../../csharp/language-reference/keywords/default-values-table.md)  
- [內建型別表](../../../csharp/language-reference/keywords/built-in-types-table.md)  
- [型別](../../../csharp/language-reference/keywords/types.md)  
- [實值型別](../../../csharp/language-reference/keywords/value-types.md)  
- [class](../../../csharp/language-reference/keywords/class.md)  
- [interface](../../../csharp/language-reference/keywords/interface.md)  
- [類別和結構](../../../csharp/programming-guide/classes-and-structs/index.md)
