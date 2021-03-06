---
title: 如何：使用放射狀漸層繪製區域
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], painting with radial gradients
- radial gradients [WPF], painting with
- painting [WPF], with radial gradients
ms.assetid: b5d0fc8a-8986-4796-b003-a75b41a48928
ms.openlocfilehash: 75c28cd19ec0423589b6485884842468b89b5e8c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526787"
---
# <a name="how-to-paint-an-area-with-a-radial-gradient"></a>如何：使用放射狀漸層繪製區域
此範例示範如何使用<xref:System.Windows.Media.RadialGradientBrush>類別，以使用放射狀漸層繪製區域。  
  
## <a name="example"></a>範例  
 下列範例會使用<xref:System.Windows.Media.RadialGradientBrush>來繪製從黃色會轉換成紅色變成藍色變成淡黃綠色放射狀漸層的矩形。  
  
 [!code-csharp[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/RadialGradientBrushSnippet.cs#simpleradialgradientexamplewholepage)]
 [!code-vb[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/radialgradientbrushsnippet.vb#simpleradialgradientexamplewholepage)]
 [!code-xaml[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/RadialGradientBrushSnippet.xaml#simpleradialgradientexamplewholepage)]  
  
 下圖顯示前述範例中的漸層。 漸層停駐點已反白顯示。  
  
 ![放射狀漸層中的漸層停駐點](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-4gradientstops-rg.png "wcpsdk_graphicsmm_4gradientstops_rg")  
  
> [!NOTE]
>  本主題中的範例會使用預設座標系統設定的控制點。 預設座標系統是相對於週框方塊： 0 表示 0%的週框方塊中，而 1 表示週框方塊的 100%。 您可以設定來變更這個座標系統<xref:System.Windows.Media.GradientBrush.MappingMode%2A>屬性設為值<xref:System.Windows.Media.BrushMappingMode.Absolute>。 絕對座標系統不會相對於週框方塊。 值會直接在本機空間中解譯。  
  
 針對其他<xref:System.Windows.Media.RadialGradientBrush>範例，請參閱[筆刷範例](https://go.microsoft.com/fwlink/?LinkID=159973)。 如需有關漸層和其他類型的筆刷的詳細資訊，請參閱[使用純色和漸層概觀繪製](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)。
