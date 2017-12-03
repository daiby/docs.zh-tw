---
title: "ICorThreadpool::CorUnregisterWait 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorThreadpool.CorUnregisterWait
api_location: mscoree.dll
api_type: COM
f1_keywords: CorUnregisterWait
helpviewer_keywords:
- CorUnregisterWait method [.NET Framework hosting]
- ICorThreadpool::CorUnregisterWait method [.NET Framework hosting]
ms.assetid: 42c933f1-30a8-4011-bdea-e117f3c3265e
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: db8de73324073f9b2e970a7ee17ba7c9ba23f84e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icorthreadpoolcorunregisterwait-method"></a><span data-ttu-id="a1f52-102">ICorThreadpool::CorUnregisterWait 方法</span><span class="sxs-lookup"><span data-stu-id="a1f52-102">ICorThreadpool::CorUnregisterWait Method</span></span>
<span data-ttu-id="a1f52-103">此方法支援 .NET Framework 結構而且並非設計直接從程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="a1f52-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1f52-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1f52-104">Syntax</span></span>  
  
```  
HRESULT CorUnregisterWait (  
    [in] HANDLE hWaitObject,  
    [in] HANDLE CompletionEvent,  
    [out] BOOL* result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="a1f52-105">需求</span><span class="sxs-lookup"><span data-stu-id="a1f52-105">Requirements</span></span>  
 <span data-ttu-id="a1f52-106">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1f52-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1f52-107">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a1f52-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a1f52-108">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="a1f52-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a1f52-109">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1f52-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1f52-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1f52-110">See Also</span></span>  
 [<span data-ttu-id="a1f52-111">ICorThreadpool 介面</span><span class="sxs-lookup"><span data-stu-id="a1f52-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)