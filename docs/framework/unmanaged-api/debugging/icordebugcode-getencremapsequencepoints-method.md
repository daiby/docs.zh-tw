---
title: "ICorDebugCode::GetEnCRemapSequencePoints 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugCode.GetEnCRemapSequencePoints
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugCode::GetEnCRemapSequencePoints
helpviewer_keywords:
- GetEnCRemapSequencePoints method [.NET Framework debugging]
- ICorDebugCode::GetEnCRemapSequencePoints method [.NET Framework debugging]
ms.assetid: 8463a98a-de4a-418e-beb0-9611885ae6b0
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 512a39f55fec7b7246fe5e20008af594028c89dc
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugcodegetencremapsequencepoints-method"></a><span data-ttu-id="53f17-102">ICorDebugCode::GetEnCRemapSequencePoints 方法</span><span class="sxs-lookup"><span data-stu-id="53f17-102">ICorDebugCode::GetEnCRemapSequencePoints Method</span></span>
<span data-ttu-id="53f17-103">在目前版本的.NET framework 不實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="53f17-103">This method is not implemented in the current version of the .NET Framework.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53f17-104">語法</span><span class="sxs-lookup"><span data-stu-id="53f17-104">Syntax</span></span>  
  
```  
HRESULT GetEnCRemapSequencePoints(  
    [in] ULONG32 cMap,  
    [out] ULONG32 *pcMap,  
    [out, size_is(cMap), length_is(*pcMap)]  
        ULONG32 offsets[]  
);  
```  
  
## <a name="see-also"></a><span data-ttu-id="53f17-105">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53f17-105">See Also</span></span>  
 