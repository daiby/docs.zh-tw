---
title: ICorDebugStepper2 Interface1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugStepper2
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugStepper2
helpviewer_keywords: ICorDebugStepper2 interface [.NET Framework debugging]
ms.assetid: 7a191c2a-95ea-4d47-83b0-44de2b632d63
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0ddce28e646541ee9e51d02d98834d8def1225ca
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugstepper2-interface1"></a><span data-ttu-id="0f30c-102">ICorDebugStepper2 Interface1</span><span class="sxs-lookup"><span data-stu-id="0f30c-102">ICorDebugStepper2 Interface1</span></span>
<span data-ttu-id="0f30c-103">提供 just my code (JMC) 偵錯的支援。</span><span class="sxs-lookup"><span data-stu-id="0f30c-103">Provides support for just my code (JMC) debugging.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0f30c-104">方法</span><span class="sxs-lookup"><span data-stu-id="0f30c-104">Methods</span></span>  
  
|<span data-ttu-id="0f30c-105">方法</span><span class="sxs-lookup"><span data-stu-id="0f30c-105">Method</span></span>|<span data-ttu-id="0f30c-106">說明</span><span class="sxs-lookup"><span data-stu-id="0f30c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0f30c-107">SetJMC 方法</span><span class="sxs-lookup"><span data-stu-id="0f30c-107">SetJMC Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper2-setjmc-method.md)|<span data-ttu-id="0f30c-108">設定值，指定這個 ICorDebugStepper 是否只能透過應用程式的開發人員所撰寫的程式碼的步驟。</span><span class="sxs-lookup"><span data-stu-id="0f30c-108">Sets a value that specifies whether this ICorDebugStepper steps only through code that is authored by an application's developer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0f30c-109">備註</span><span class="sxs-lookup"><span data-stu-id="0f30c-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0f30c-110">這個介面不支援跨電腦或跨處理序的遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f30c-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f30c-111">需求</span><span class="sxs-lookup"><span data-stu-id="0f30c-111">Requirements</span></span>  
 <span data-ttu-id="0f30c-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0f30c-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f30c-113">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f30c-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f30c-114">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f30c-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f30c-115">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f30c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f30c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f30c-116">See Also</span></span>  
 [<span data-ttu-id="0f30c-117">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="0f30c-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)