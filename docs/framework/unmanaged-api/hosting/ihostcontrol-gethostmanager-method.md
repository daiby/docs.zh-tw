---
title: "IHostControl::GetHostManager 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostControl.GetHostManager
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostControl::GetHostManager
helpviewer_keywords:
- GetHostManager method [.NET Framework hosting]
- IHostControl::GetHostManager method [.NET Framework hosting]
ms.assetid: 0fa34bca-ed18-4626-9e78-d33684d18edb
topic_type: apiref
caps.latest.revision: "19"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c711fb2ddf5d21cd8e122a35ebd0b8a5ce0e752f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="ihostcontrolgethostmanager-method"></a><span data-ttu-id="3bbd3-102">IHostControl::GetHostManager 方法</span><span class="sxs-lookup"><span data-stu-id="3bbd3-102">IHostControl::GetHostManager Method</span></span>
<span data-ttu-id="3bbd3-103">取得具有指定的介面指標主機的介面實作`IID`。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-103">Gets an interface pointer to the host's implementation of the interface with the specified `IID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3bbd3-104">語法</span><span class="sxs-lookup"><span data-stu-id="3bbd3-104">Syntax</span></span>  
  
```  
HRESULT GetHostManager (  
    [in] REFIID riid,  
    [out, iid_is(riid)] void** ppObject  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3bbd3-105">參數</span><span class="sxs-lookup"><span data-stu-id="3bbd3-105">Parameters</span></span>  
 `riid`  
 <span data-ttu-id="3bbd3-106">[in]`IID` Common language runtime (CLR) 查詢的介面。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-106">[in] The `IID` of the interface that the common language runtime (CLR) is querying for.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="3bbd3-107">[out]主機實作的介面或如果主機不支援此介面為 null 指標。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-107">[out] A pointer to the host-implemented interface, or null if the host does not support this interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3bbd3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bbd3-108">Return Value</span></span>  
  
|<span data-ttu-id="3bbd3-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3bbd3-109">HRESULT</span></span>|<span data-ttu-id="3bbd3-110">描述</span><span class="sxs-lookup"><span data-stu-id="3bbd3-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3bbd3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bbd3-111">S_OK</span></span>|<span data-ttu-id="3bbd3-112">`GetHostManager`已成功傳回。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-112">`GetHostManager` returned successfully.</span></span>|  
|<span data-ttu-id="3bbd3-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3bbd3-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3bbd3-114">CLR 尚未載入到處理程序，或 CLR 正在中它無法執行 managed 程式碼，或成功地處理呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3bbd3-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3bbd3-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3bbd3-116">呼叫已逾時。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-116">The call timed out.</span></span>|  
|<span data-ttu-id="3bbd3-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3bbd3-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3bbd3-118">呼叫端未擁有鎖定。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3bbd3-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3bbd3-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3bbd3-120">事件已取消時封鎖的執行緒或 fiber 等候它。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3bbd3-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3bbd3-121">E_FAIL</span></span>|<span data-ttu-id="3bbd3-122">發生未知的嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3bbd3-123">方法會傳回 E_FAIL CLR 已不再可用的處理序內。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3bbd3-124">裝載方法的後續呼叫會傳回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="3bbd3-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3bbd3-125">E_INVALIDARG</span></span>|<span data-ttu-id="3bbd3-126">要求`IID`不正確。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-126">The requested `IID` is not valid.</span></span>|  
|<span data-ttu-id="3bbd3-127">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="3bbd3-127">E_NOINTERFACE</span></span>|<span data-ttu-id="3bbd3-128">不支援要求的介面。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-128">The requested interface is not supported.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3bbd3-129">備註</span><span class="sxs-lookup"><span data-stu-id="3bbd3-129">Remarks</span></span>  
 <span data-ttu-id="3bbd3-130">CLR 會查詢主機判斷是否支援一或多個下列介面：</span><span class="sxs-lookup"><span data-stu-id="3bbd3-130">The CLR queries the host to determine whether it supports one or more of the following interfaces:</span></span>  
  
-   [<span data-ttu-id="3bbd3-131">IHostMemoryManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-131">IHostMemoryManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-132">IHostTaskManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-132">IHostTaskManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-133">IHostThreadPoolManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-133">IHostThreadPoolManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-134">IHostIoCompletionManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-134">IHostIoCompletionManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-135">IHostSyncManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-135">IHostSyncManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-136">IHostAssemblyManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-136">IHostAssemblyManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-137">IHostGCManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-137">IHostGCManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-138">IHostPolicyManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-138">IHostPolicyManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)  
  
-   [<span data-ttu-id="3bbd3-139">IHostSecurityManager</span><span class="sxs-lookup"><span data-stu-id="3bbd3-139">IHostSecurityManager</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
  
 <span data-ttu-id="3bbd3-140">如果主機支援指定的介面，它會設定`ppObject`到它的實作該介面。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-140">If the host supports the specified interface, it sets `ppObject` to its implementation of that interface.</span></span> <span data-ttu-id="3bbd3-141">否則，它會將`ppObject`為 null。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-141">Otherwise, it sets `ppObject` to null.</span></span>  
  
 <span data-ttu-id="3bbd3-142">CLR 不會呼叫`Release`主應用程式管理員，即使您關閉上。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-142">The CLR does not call `Release` on host managers, even when you shut it down.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3bbd3-143">需求</span><span class="sxs-lookup"><span data-stu-id="3bbd3-143">Requirements</span></span>  
 <span data-ttu-id="3bbd3-144">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3bbd3-144">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3bbd3-145">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3bbd3-145">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3bbd3-146">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="3bbd3-146">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3bbd3-147">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3bbd3-147">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3bbd3-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bbd3-148">See Also</span></span>  
 [<span data-ttu-id="3bbd3-149">IHostControl 介面</span><span class="sxs-lookup"><span data-stu-id="3bbd3-149">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)