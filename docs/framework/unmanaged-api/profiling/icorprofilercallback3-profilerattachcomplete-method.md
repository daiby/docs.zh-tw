---
title: "ICorProfilerCallback3::ProfilerAttachComplete 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback3.ProfilerAttachComplete Method
api_location: Mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback3::ProfilerAttachComplete
helpviewer_keywords:
- ProfilerAttachComplete method [.NET Framework profiling]
- ICorProfilerCallback3::ProfilerAttachComplete method [.NET Framework profiling]
ms.assetid: 257d6076-06e0-4d93-bb33-651fbb2b92d7
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 0bf1e535c6270660797554c38a0b031df82f0925
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback3profilerattachcomplete-method"></a><span data-ttu-id="07780-102">ICorProfilerCallback3::ProfilerAttachComplete 方法</span><span class="sxs-lookup"><span data-stu-id="07780-102">ICorProfilerCallback3::ProfilerAttachComplete Method</span></span>
<span data-ttu-id="07780-103">由 common language runtime (CLR)，表示分析工具現在可以呼叫呼叫[icorprofilerinfo3:: Enumjitedfunctions](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enumjitedfunctions-method.md)和[icorprofilerinfo3:: Enummodules](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enummodules-method.md)更新方法。</span><span class="sxs-lookup"><span data-stu-id="07780-103">Called by the common language runtime (CLR) to indicate that the profiler can now call the [ICorProfilerInfo3::EnumJITedFunctions](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enumjitedfunctions-method.md) and [ICorProfilerInfo3::EnumModules](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enummodules-method.md) catch-up methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07780-104">語法</span><span class="sxs-lookup"><span data-stu-id="07780-104">Syntax</span></span>  
  
```  
HRESULT ProfilerAttachComplete ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="07780-105">備註</span><span class="sxs-lookup"><span data-stu-id="07780-105">Remarks</span></span>  
 <span data-ttu-id="07780-106">`ProfilerAttachComplete`回呼之後，會發出[icorprofilercallback3:: Initializeforattach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md)方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="07780-106">The `ProfilerAttachComplete` callback is issued after the [ICorProfilerCallback3::InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) method is called.</span></span> <span data-ttu-id="07780-107">這表示：</span><span class="sxs-lookup"><span data-stu-id="07780-107">It indicates the following:</span></span>  
  
-   <span data-ttu-id="07780-108">`InitializeForAttach` 中分析工具所要求的回呼已啟動。</span><span class="sxs-lookup"><span data-stu-id="07780-108">The callbacks that were requested by the profiler in `InitializeForAttach` have been activated.</span></span>  
  
-   <span data-ttu-id="07780-109">分析工具現在可以對關聯的 ID 執行更新，而不必擔心遺漏通知。</span><span class="sxs-lookup"><span data-stu-id="07780-109">The profiler can now perform catch-up on the associated IDs without being concerned about missing notifications.</span></span>  
  
 <span data-ttu-id="07780-110">CLR 會忽略這個回呼的傳回值。</span><span class="sxs-lookup"><span data-stu-id="07780-110">The CLR ignores the return value from this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07780-111">需求</span><span class="sxs-lookup"><span data-stu-id="07780-111">Requirements</span></span>  
 <span data-ttu-id="07780-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="07780-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="07780-113">**標頭：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="07780-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="07780-114">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="07780-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="07780-115">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="07780-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07780-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07780-116">See Also</span></span>  
 [<span data-ttu-id="07780-117">ICorProfilerCallback 介面</span><span class="sxs-lookup"><span data-stu-id="07780-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="07780-118">ICorProfilerInfo3 介面</span><span class="sxs-lookup"><span data-stu-id="07780-118">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)  
 [<span data-ttu-id="07780-119">分析介面</span><span class="sxs-lookup"><span data-stu-id="07780-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="07780-120">程式碼剖析</span><span class="sxs-lookup"><span data-stu-id="07780-120">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)