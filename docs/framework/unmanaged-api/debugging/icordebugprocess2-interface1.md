---
title: ICorDebugProcess2 Interface1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess2
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess2
helpviewer_keywords: ICorDebugProcess2 interface [.NET Framework debugging]
ms.assetid: 73332138-5fea-441f-b893-61af87d45a42
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ca1a73874f6ca2f839639cbaf731a59721b2aede
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugprocess2-interface1"></a><span data-ttu-id="b0f08-102">ICorDebugProcess2 Interface1</span><span class="sxs-lookup"><span data-stu-id="b0f08-102">ICorDebugProcess2 Interface1</span></span>
<span data-ttu-id="b0f08-103">ICorDebugProcess 介面，表示處理程序執行 managed 程式碼的邏輯擴充。</span><span class="sxs-lookup"><span data-stu-id="b0f08-103">A logical extension of the ICorDebugProcess interface, which represents a process running managed code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b0f08-104">方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-104">Methods</span></span>  
  
|<span data-ttu-id="b0f08-105">方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-105">Method</span></span>|<span data-ttu-id="b0f08-106">說明</span><span class="sxs-lookup"><span data-stu-id="b0f08-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b0f08-107">ClearUnmanagedBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-107">ClearUnmanagedBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-clearunmanagedbreakpoint-method.md)|<span data-ttu-id="b0f08-108">移除指定的位移之前呼叫所設定的中斷點`ICorDebugProcess2::SetUnmanagedBreakpoint`。</span><span class="sxs-lookup"><span data-stu-id="b0f08-108">Removes a breakpoint at the specified offset that was set by an earlier call to `ICorDebugProcess2::SetUnmanagedBreakpoint`.</span></span>|  
|[<span data-ttu-id="b0f08-109">GetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-109">GetDesiredNGENCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getdesiredngencompilerflags-method.md)|<span data-ttu-id="b0f08-110">取得必須設為 common language runtime (CLR) 將影像載入處理序所參考的旗標`ICorDebugProcess2`。</span><span class="sxs-lookup"><span data-stu-id="b0f08-110">Gets the flags that must be set for the common language runtime (CLR) to load the image into the process referenced by this `ICorDebugProcess2`.</span></span>|  
|[<span data-ttu-id="b0f08-111">GetReferenceValueFromGCHandle 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-111">GetReferenceValueFromGCHandle Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getreferencevaluefromgchandle-method.md)|<span data-ttu-id="b0f08-112">取得已回收控制代碼指定的受管理物件的參考指標。</span><span class="sxs-lookup"><span data-stu-id="b0f08-112">Gets a reference pointer to the specified managed object that has a garbage collection handle.</span></span>|  
|[<span data-ttu-id="b0f08-113">GetThreadForTaskID 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-113">GetThreadForTaskID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getthreadfortaskid-method.md)|<span data-ttu-id="b0f08-114">取得具有指定識別碼的工作執行所在的執行緒。</span><span class="sxs-lookup"><span data-stu-id="b0f08-114">Gets the thread upon which the task with the specified identifier is executing.</span></span>|  
|[<span data-ttu-id="b0f08-115">GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-115">GetVersion Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getversion-method.md)|<span data-ttu-id="b0f08-116">取得正在偵錯處理序正在執行的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="b0f08-116">Gets the version of the CLR upon which the process being debugged is running.</span></span>|  
|[<span data-ttu-id="b0f08-117">SetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-117">SetDesiredNGENCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setdesiredngencompilerflags-method.md)|<span data-ttu-id="b0f08-118">設定所需的映像載入偵錯程序在 just-in-time (JIT) 編譯器旗標。</span><span class="sxs-lookup"><span data-stu-id="b0f08-118">Sets the flags that are required for the just-in-time (JIT) compiler to load an image into the process being debugged.</span></span>|  
|[<span data-ttu-id="b0f08-119">SetUnmanagedBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="b0f08-119">SetUnmanagedBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md)|<span data-ttu-id="b0f08-120">在指定的原生映像位移設定未受管理的中斷點。</span><span class="sxs-lookup"><span data-stu-id="b0f08-120">Sets an unmanaged breakpoint at the specified native image offset.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b0f08-121">備註</span><span class="sxs-lookup"><span data-stu-id="b0f08-121">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b0f08-122">這個介面不支援跨電腦或跨處理序的遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0f08-122">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0f08-123">需求</span><span class="sxs-lookup"><span data-stu-id="b0f08-123">Requirements</span></span>  
 <span data-ttu-id="b0f08-124">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b0f08-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0f08-125">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b0f08-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b0f08-126">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b0f08-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b0f08-127">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0f08-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0f08-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0f08-128">See Also</span></span>  
 [<span data-ttu-id="b0f08-129">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="b0f08-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)