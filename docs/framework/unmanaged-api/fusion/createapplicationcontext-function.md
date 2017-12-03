---
title: "CreateApplicationContext 函式"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CreateApplicationContext
api_location: fusion.dll
api_type: DLLExport
f1_keywords: CreateApplicationContext
helpviewer_keywords: CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c089c32d4bc8474168274186a9303d39976abfca
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="createapplicationcontext-function"></a><span data-ttu-id="a1a08-102">CreateApplicationContext 函式</span><span class="sxs-lookup"><span data-stu-id="a1a08-102">CreateApplicationContext Function</span></span>
<span data-ttu-id="a1a08-103">此功能支援.NET Framework 基礎結構，並不是直接從您的程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="a1a08-103">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1a08-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1a08-104">Syntax</span></span>  
  
```  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a1a08-105">參數</span><span class="sxs-lookup"><span data-stu-id="a1a08-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="a1a08-106">[in]指向的好記的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1a08-106">[in] A pointer to a friendly name.</span></span>  
  
 `ppCtx`  
 <span data-ttu-id="a1a08-107">[out]應用程式內容的指標。</span><span class="sxs-lookup"><span data-stu-id="a1a08-107">[out] A pointer to an application context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1a08-108">需求</span><span class="sxs-lookup"><span data-stu-id="a1a08-108">Requirements</span></span>  
 <span data-ttu-id="a1a08-109">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a08-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1a08-110">**標頭：** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="a1a08-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a1a08-111">**程式庫：**包含為 Fusion.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="a1a08-111">**Library:** Included as a resource in Fusion.dll</span></span>  
  
 <span data-ttu-id="a1a08-112">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1a08-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1a08-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1a08-113">See Also</span></span>  
 [<span data-ttu-id="a1a08-114">IAssemblyCache 介面</span><span class="sxs-lookup"><span data-stu-id="a1a08-114">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)  
 [<span data-ttu-id="a1a08-115">融合全域靜態函式</span><span class="sxs-lookup"><span data-stu-id="a1a08-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)  
 [<span data-ttu-id="a1a08-116">全域組件快取</span><span class="sxs-lookup"><span data-stu-id="a1a08-116">Global Assembly Cache</span></span>](../../../../docs/framework/app-domains/gac.md)