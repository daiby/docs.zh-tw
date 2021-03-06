---
title: 操作說明：設定 TileBrush 的並排顯示大小
ms.date: 03/30/2017
helpviewer_keywords:
- TileBrush [WPF], size of tilepropertys
- Viewport property of TileBrush [WPF]
ms.assetid: 04f41090-1b46-4e36-832f-d27d28708b8c
ms.openlocfilehash: e1ba1a25281ffdd1cc00e0bed0efe4f8508780be
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467831"
---
# <a name="how-to-set-the-tile-size-for-a-tilebrush"></a>操作說明：設定 TileBrush 的並排顯示大小
此範例示範如何設定的並排顯示大小<xref:System.Windows.Media.TileBrush>。 根據預設，<xref:System.Windows.Media.TileBrush>會產生單一並排顯示，以完全填滿您所繪製的區域。 您可以藉由設定覆寫這個行為<xref:System.Windows.Media.TileBrush.Viewport%2A>和<xref:System.Windows.Media.TileBrush.ViewportUnits%2A>屬性。  
  
 <xref:System.Windows.Media.TileBrush.Viewport%2A>屬性指定的並排顯示大小<xref:System.Windows.Media.TileBrush>。 根據預設，windows 7<xref:System.Windows.Media.TileBrush.Viewport%2A>屬性是相對於正在繪製之區域的大小。 若要讓<xref:System.Windows.Media.TileBrush.Viewport%2A>屬性指定絕對的並排顯示大小，設定<xref:System.Windows.Media.TileBrush.ViewportUnits%2A>屬性設<xref:System.Windows.Media.BrushMappingMode.Absolute>。  
  
## <a name="example"></a>範例  
 下列範例會使用<xref:System.Windows.Media.ImageBrush>，一種<xref:System.Windows.Media.TileBrush>、 要繪製的圖格的矩形。 這個範例會將每個並排顯示設為輸出區域 (即矩形) 的 50% x 50%。 因此，矩形會以影像的四個投影繪製。  
  
 下圖顯示範例所產生的輸出。
  
 ![使用影像筆刷進行並排顯示的範例](../../../../docs/framework/wpf/graphics-multimedia/media/0.png "0")  
  
 [!code-csharp[UsingImageBrush_snip#RelativeTileSizeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#relativetilesizeexample)]  
  
 下一個範例會建立<xref:System.Windows.Media.ImageBrush>，設定其<xref:System.Windows.Media.TileBrush.Viewport%2A>要`0,0,25,25`及其<xref:System.Windows.Media.TileBrush.ViewportUnits%2A>到<xref:System.Windows.Media.BrushMappingMode.Absolute>，並用它來繪製另一個矩形。 因此，筆刷會產生寬度為 25 個像素，且高度為 25 個像素的並排顯示。  
  
 下圖顯示範例所產生的輸出。  
  
 ![檢視區為 0,0,0.25,0.25 的並排顯示 TileBrush](../../../../docs/framework/wpf/graphics-multimedia/media/25x25viewport.png "25x25viewport")  
  
 [!code-csharp[UsingImageBrush_snip#AbsoluteTileSizeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#absolutetilesizeexample)]  
  
 上述範例是某個完整範例的一部分。 如需完整的範例，請參閱[ImageBrush 範例](https://go.microsoft.com/fwlink/?LinkID=160005)。  
  
 雖然此範例會使用<xref:System.Windows.Media.ImageBrush>類別，<xref:System.Windows.Media.TileBrush.Viewport%2A>並<xref:System.Windows.Media.TileBrush.ViewportUnits%2A>屬性運作方式完全相同的另<xref:System.Windows.Media.TileBrush>物件，也就是如<xref:System.Windows.Media.DrawingBrush>和<xref:System.Windows.Media.VisualBrush>。 如需詳細資訊<xref:System.Windows.Media.ImageBrush>和其他<xref:System.Windows.Media.TileBrush>物件，請參閱[使用影像、 繪圖和視覺效果繪製](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md)。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Windows.Media.TileBrush>  
 [使用影像、繪圖和視覺效果繪製](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md)  
 [使用 TileBrush 建立不同的並排顯示模式](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-different-tile-patterns-with-a-tilebrush.md)
