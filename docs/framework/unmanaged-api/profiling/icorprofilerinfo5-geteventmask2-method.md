---
title: "ICorProfilerInfo5::GetEventMask2 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: ICorProfilerInfo5.GetEventMask2
api_location: mscorwks.dll
api_type: COM
ms.assetid: f854b68f-009c-4ffb-89cd-ca874d1c0fb7
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: da1c4c11adaac21e9769330ee24beceff64e020b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo5geteventmask2-method"></a><span data-ttu-id="d4a78-102">ICorProfilerInfo5::GetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="d4a78-102">ICorProfilerInfo5::GetEventMask2 Method</span></span>
<span data-ttu-id="d4a78-103">[在 .NET Framework 4.5.2 及更新版本中支援]</span><span class="sxs-lookup"><span data-stu-id="d4a78-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="d4a78-104">取得分析工具想要從 Common Language Runtime (CLR) 接收通知的目前事件分類。</span><span class="sxs-lookup"><span data-stu-id="d4a78-104">Gets the current event categories for which the profiler wants to receive notifications from the common language runtime (CLR).</span></span>  <span data-ttu-id="d4a78-105">它會提供不是由提供的功能[icorprofilerinfo:: Geteventmask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="d4a78-105">It provides functionality not provided by the [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4a78-106">語法</span><span class="sxs-lookup"><span data-stu-id="d4a78-106">Syntax</span></span>  
  
```cpp
HRESULT GetEventMask2(  
        [out] DWORD* pdwEventsLow,  
        [out] DWORD* pdwEventsHigh  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d4a78-107">參數</span><span class="sxs-lookup"><span data-stu-id="d4a78-107">Parameters</span></span>  
 `pdwEventsLow`  
 <span data-ttu-id="d4a78-108">[out] 指定事件分類的 4 位元組值的指標。</span><span class="sxs-lookup"><span data-stu-id="d4a78-108">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="d4a78-109">每個位元分別控制不同的功能、行為或事件類型。</span><span class="sxs-lookup"><span data-stu-id="d4a78-109">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="d4a78-110">中所述的位元[COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md)列舉型別。</span><span class="sxs-lookup"><span data-stu-id="d4a78-110">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 `pdwEventsHigh`  
 <span data-ttu-id="d4a78-111">[out] 指定事件分類的 4 位元組值的指標。</span><span class="sxs-lookup"><span data-stu-id="d4a78-111">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span>  <span data-ttu-id="d4a78-112">每個位元分別控制不同的功能、行為或事件類型。</span><span class="sxs-lookup"><span data-stu-id="d4a78-112">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="d4a78-113">中所述的位元[COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md)列舉型別。</span><span class="sxs-lookup"><span data-stu-id="d4a78-113">The bits are described in the [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d4a78-114">備註</span><span class="sxs-lookup"><span data-stu-id="d4a78-114">Remarks</span></span>  
 <span data-ttu-id="d4a78-115">`GetEventMask2` 方法可用於判斷分析工具已訂閱哪些回呼。</span><span class="sxs-lookup"><span data-stu-id="d4a78-115">The `GetEventMask2` method is used to determine which callbacks the profiler has subscribed to.</span></span> <span data-ttu-id="d4a78-116">一般而言，您可以執行的邏輯 OR`pdwEventsLow`和`pdwEventsHigh`值和您想要設定，然後再呼叫任何新位元[SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="d4a78-116">Typically, you perform a logical OR of the `pdwEventsLow` and `pdwEventsHigh` values and any new bits you want to set, and then call the [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
 <span data-ttu-id="d4a78-117">這個方法會以建議的替代做法[GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="d4a78-117">This method is the recommended alternative to the [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4a78-118">需求</span><span class="sxs-lookup"><span data-stu-id="d4a78-118">Requirements</span></span>  
 <span data-ttu-id="d4a78-119">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a78-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4a78-120">**標頭：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d4a78-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d4a78-121">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d4a78-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d4a78-122">**.NET framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4a78-122">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4a78-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4a78-123">See Also</span></span>  
 [<span data-ttu-id="d4a78-124">ICorProfilerInfo5 介面</span><span class="sxs-lookup"><span data-stu-id="d4a78-124">ICorProfilerInfo5 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md)  
 [<span data-ttu-id="d4a78-125">SetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="d4a78-125">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)