---
title: "ICLRHostBindingPolicyManager::EvaluatePolicy 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRHostBindingPolicyManager.EvaluatePolicy
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRHostBindingPolicyManager::EvaluatePolicy
helpviewer_keywords:
- ICLRHostBindingPolicyManager::EvaluatePolicy method [.NET Framework hosting]
- EvaluatePolicy method [.NET Framework hosting]
ms.assetid: 3a3a9446-7a4e-4836-9b27-5c536c15993d
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7471b77deca7b66ba0a30b08ccf934704a7ac61d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="iclrhostbindingpolicymanagerevaluatepolicy-method"></a><span data-ttu-id="37e9c-102">ICLRHostBindingPolicyManager::EvaluatePolicy 方法</span><span class="sxs-lookup"><span data-stu-id="37e9c-102">ICLRHostBindingPolicyManager::EvaluatePolicy Method</span></span>
<span data-ttu-id="37e9c-103">代表主機評估繫結原則。</span><span class="sxs-lookup"><span data-stu-id="37e9c-103">Evaluates binding policy on behalf of the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37e9c-104">語法</span><span class="sxs-lookup"><span data-stu-id="37e9c-104">Syntax</span></span>  
  
```  
HRESULT EvaluatePolicy (  
    [in] LPCWSTR     pwzReferenceIdentity,  
    [in] BYTE       *pbApplicationPolicy,  
    [in] DWORD       cbAppPolicySize,  
    [out, size_is(*pcchPostPolicyReferenceIdentity)] LPWSTR pwzPostPolicyReferenceIdentity,  
    [in, out] DWORD *pcchPostPolicyReferenceIdentity,  
    [out] DWORD     *pdwPoliciesApplied  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="37e9c-105">參數</span><span class="sxs-lookup"><span data-stu-id="37e9c-105">Parameters</span></span>  
 `pwzReferenceIdentity`  
 <span data-ttu-id="37e9c-106">[in]之前的原則評估的組件的參考。</span><span class="sxs-lookup"><span data-stu-id="37e9c-106">[in] A reference to the assembly before the policy evaluation.</span></span>  
  
 `pbApplicationPolicy`  
 <span data-ttu-id="37e9c-107">[in]包含原則的資料緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="37e9c-107">[in] A pointer to a buffer that contains the policy data.</span></span>  
  
 `cbAppPolicySize`  
 <span data-ttu-id="37e9c-108">[in]大小`pbApplicationPolicy`緩衝區。</span><span class="sxs-lookup"><span data-stu-id="37e9c-108">[in] The size of the `pbApplicationPolicy` buffer.</span></span>  
  
 `pwzPostPolicyReferenceIdentity`  
 <span data-ttu-id="37e9c-109">[out]新的原則資料評估後的組件的參考。</span><span class="sxs-lookup"><span data-stu-id="37e9c-109">[out] A reference to the assembly after the evaluation of the new policy data.</span></span>  
  
 `pcchPostPolicyReferenceIdentity`  
 <span data-ttu-id="37e9c-110">[in、 out]新的原則資料評估後的組件識別參考緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="37e9c-110">[in, out] A pointer to the size of the assembly identity reference buffer after the evaluation of the new policy data.</span></span>  
  
 `pdwPoliciesApplied`  
 <span data-ttu-id="37e9c-111">[out]指標的邏輯 OR 組合[EBindPolicyLevels](../../../../docs/framework/unmanaged-api/hosting/ebindpolicylevels-enumeration.md)值，表示已套用的原則。</span><span class="sxs-lookup"><span data-stu-id="37e9c-111">[out] A pointer to a logical OR combination of [EBindPolicyLevels](../../../../docs/framework/unmanaged-api/hosting/ebindpolicylevels-enumeration.md) values, indicating which policies have been applied.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="37e9c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="37e9c-112">Return Value</span></span>  
  
|<span data-ttu-id="37e9c-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="37e9c-113">HRESULT</span></span>|<span data-ttu-id="37e9c-114">描述</span><span class="sxs-lookup"><span data-stu-id="37e9c-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="37e9c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="37e9c-115">S_OK</span></span>|<span data-ttu-id="37e9c-116">已成功完成評估。</span><span class="sxs-lookup"><span data-stu-id="37e9c-116">The evaluation completed successfully.</span></span>|  
|<span data-ttu-id="37e9c-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="37e9c-117">E_INVALIDARG</span></span>|<span data-ttu-id="37e9c-118">可能是`pwzReferenceIdentity`或`pbApplicationPolicy`為 null 參考。</span><span class="sxs-lookup"><span data-stu-id="37e9c-118">Either `pwzReferenceIdentity` or `pbApplicationPolicy` is a null reference.</span></span>|  
|<span data-ttu-id="37e9c-119">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="37e9c-119">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="37e9c-120">`cbAppPolicySize`為太小。</span><span class="sxs-lookup"><span data-stu-id="37e9c-120">`cbAppPolicySize` is too small.</span></span>|  
|<span data-ttu-id="37e9c-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="37e9c-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="37e9c-122">Common language runtime (CLR) 尚未載入到處理程序，或 CLR 正在中它無法執行 managed 程式碼，或成功地處理呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="37e9c-122">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="37e9c-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="37e9c-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="37e9c-124">呼叫已逾時。</span><span class="sxs-lookup"><span data-stu-id="37e9c-124">The call timed out.</span></span>|  
|<span data-ttu-id="37e9c-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="37e9c-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="37e9c-126">呼叫端未擁有鎖定。</span><span class="sxs-lookup"><span data-stu-id="37e9c-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="37e9c-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="37e9c-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="37e9c-128">事件已取消時封鎖的執行緒或 fiber 等候它。</span><span class="sxs-lookup"><span data-stu-id="37e9c-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="37e9c-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="37e9c-129">E_FAIL</span></span>|<span data-ttu-id="37e9c-130">發生未知的嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="37e9c-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="37e9c-131">方法會傳回 E_FAIL 之後，CLR 就不再可用的處理序內。</span><span class="sxs-lookup"><span data-stu-id="37e9c-131">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="37e9c-132">裝載方法的後續呼叫會傳回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="37e9c-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="37e9c-133">備註</span><span class="sxs-lookup"><span data-stu-id="37e9c-133">Remarks</span></span>  
 <span data-ttu-id="37e9c-134">`EvaluatePolicy`方法可讓主機來維護主機特定的組件繫結原則會影響版本控制需求。</span><span class="sxs-lookup"><span data-stu-id="37e9c-134">The `EvaluatePolicy` method allows the host to influence binding policy to maintain host-specific assembly versioning requirements.</span></span> <span data-ttu-id="37e9c-135">原則引擎本身會維持在 CLR 中。</span><span class="sxs-lookup"><span data-stu-id="37e9c-135">The policy engine itself remains inside the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="37e9c-136">需求</span><span class="sxs-lookup"><span data-stu-id="37e9c-136">Requirements</span></span>  
 <span data-ttu-id="37e9c-137">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="37e9c-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="37e9c-138">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="37e9c-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="37e9c-139">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="37e9c-139">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="37e9c-140">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37e9c-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37e9c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37e9c-141">See Also</span></span>  
 [<span data-ttu-id="37e9c-142">ICLRHostBindingPolicyManager 介面</span><span class="sxs-lookup"><span data-stu-id="37e9c-142">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)