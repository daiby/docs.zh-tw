---
title: "ICorRuntimeHost::CurrentDomain 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorRuntimeHost.CurrentDomain
api_location: mscoree.dll
api_type: COM
f1_keywords: ICorRuntimeHost::CurrentDomain
helpviewer_keywords:
- ICorRuntimeHost::CreateDomain method [.NET Framework hosting]
- CurrentDomain method [.NET Framework hosting]
ms.assetid: dd2afb38-675b-4c3c-a9f3-8ab3b133eb02
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 592b604f5e873f479f2e0489144240c3f021c270
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icorruntimehostcurrentdomain-method"></a><span data-ttu-id="e724e-102">ICorRuntimeHost::CurrentDomain 方法</span><span class="sxs-lookup"><span data-stu-id="e724e-102">ICorRuntimeHost::CurrentDomain Method</span></span>
<span data-ttu-id="e724e-103">取得類型的介面指標<xref:System.AppDomain?displayProperty=nameWithType>，代表目前執行緒上載入的網域。</span><span class="sxs-lookup"><span data-stu-id="e724e-103">Gets an interface pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the domain loaded on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e724e-104">語法</span><span class="sxs-lookup"><span data-stu-id="e724e-104">Syntax</span></span>  
  
```  
HRESULT CurrentDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e724e-105">參數</span><span class="sxs-lookup"><span data-stu-id="e724e-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="e724e-106">[out]類型的指標<xref:System.AppDomain?displayProperty=nameWithType>代表執行緒的目前應用程式定義域。</span><span class="sxs-lookup"><span data-stu-id="e724e-106">[out] A pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the thread's current application domain.</span></span> <span data-ttu-id="e724e-107">此指標為型別`IUnknown`，因此呼叫端通常應該呼叫`QueryInterface`取得型別的指標<xref:System._AppDomain>。</span><span class="sxs-lookup"><span data-stu-id="e724e-107">This pointer is typed `IUnknown`, so callers should generally call `QueryInterface` to obtain a pointer of type <xref:System._AppDomain>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e724e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e724e-108">Return Value</span></span>  
  
|<span data-ttu-id="e724e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e724e-109">HRESULT</span></span>|<span data-ttu-id="e724e-110">描述</span><span class="sxs-lookup"><span data-stu-id="e724e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e724e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e724e-111">S_OK</span></span>|<span data-ttu-id="e724e-112">此作業成功。</span><span class="sxs-lookup"><span data-stu-id="e724e-112">The operation was successful.</span></span>|  
|<span data-ttu-id="e724e-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e724e-113">S_FALSE</span></span>|<span data-ttu-id="e724e-114">無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="e724e-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="e724e-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e724e-115">E_FAIL</span></span>|<span data-ttu-id="e724e-116">發生未知的嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="e724e-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="e724e-117">若方法會傳回 E_FAIL，common language runtime (CLR) 就不會再處理序中。</span><span class="sxs-lookup"><span data-stu-id="e724e-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="e724e-118">任何裝載的應用程式開發介面的後續呼叫會傳回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="e724e-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="e724e-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e724e-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e724e-120">CLR 尚未載入到處理程序，或 CLR 正在中它無法執行 managed 程式碼，或成功地處理呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="e724e-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e724e-121">需求</span><span class="sxs-lookup"><span data-stu-id="e724e-121">Requirements</span></span>  
 <span data-ttu-id="e724e-122">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e724e-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e724e-123">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e724e-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e724e-124">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="e724e-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e724e-125">**.NET framework 版本：** 1.0、 1.1</span><span class="sxs-lookup"><span data-stu-id="e724e-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e724e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e724e-126">See Also</span></span>  
 <xref:System._AppDomain>  
 <xref:System.AppDomain>  
 [<span data-ttu-id="e724e-127">ICorRuntimeHost 介面</span><span class="sxs-lookup"><span data-stu-id="e724e-127">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)