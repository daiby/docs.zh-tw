---
title: "CorDebugDebugEventKind 列舉"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugDebugEventKind
api_location: mscordbi.dll
api_type: COM
ms.assetid: 6075a6cd-97e6-4472-a090-0dd14860d1f3
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5aeb6085671e645e12713944d6456b9581a3886f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="cordebugdebugeventkind-enumeration"></a><span data-ttu-id="d53e7-102">CorDebugDebugEventKind 列舉</span><span class="sxs-lookup"><span data-stu-id="d53e7-102">CorDebugDebugEventKind Enumeration</span></span>
<span data-ttu-id="d53e7-103">表示由解碼其資訊的事件類型[DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="d53e7-103">Indicates the type of event whose information is decoded by the [DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d53e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="d53e7-104">Syntax</span></span>  
  
```  
typedef enum CorDebugDebugEventKind {  
    DEBUG_EVENT_KIND_MODULE_LOADED                          = 1,  
    DEBUG_EVENT_KIND_MODULE_UNLOADED                        = 2,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE         = 3,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE    = 4,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND  = 5,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED            = 6  
} CorDebugRecordFormat;  
```  
  
## <a name="members"></a><span data-ttu-id="d53e7-105">成員</span><span class="sxs-lookup"><span data-stu-id="d53e7-105">Members</span></span>  
  
|<span data-ttu-id="d53e7-106">成員</span><span class="sxs-lookup"><span data-stu-id="d53e7-106">Member</span></span>|<span data-ttu-id="d53e7-107">描述</span><span class="sxs-lookup"><span data-stu-id="d53e7-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EVENT_KIND_MODULE_LOADED`|<span data-ttu-id="d53e7-108">模組載入事件。</span><span class="sxs-lookup"><span data-stu-id="d53e7-108">A module load event.</span></span>|  
|`DEBUG_EVENT_KIND_MODULE_UNLOADED`|<span data-ttu-id="d53e7-109">模組卸載事件。</span><span class="sxs-lookup"><span data-stu-id="d53e7-109">A module unload event.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE`|<span data-ttu-id="d53e7-110">第一個可能發生的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d53e7-110">A first-chance exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE`|<span data-ttu-id="d53e7-111">第一個可能發生的使用者例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d53e7-111">A first-chance user exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND`|<span data-ttu-id="d53e7-112">存在 `catch` 處理常式的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d53e7-112">An exception for which a `catch` handler exists.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED`|<span data-ttu-id="d53e7-113">未處理的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d53e7-113">An unhandled exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d53e7-114">備註</span><span class="sxs-lookup"><span data-stu-id="d53e7-114">Remarks</span></span>  
 <span data-ttu-id="d53e7-115">成員`CorDebugDebugEventKind`列舉型別由呼叫[icordebugdebugevent:: Geteventkind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="d53e7-115">A member of the `CorDebugDebugEventKind` enumeration is returned by calling the [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d53e7-116">這個列舉僅適用於 .NET 原生偵錯案例。</span><span class="sxs-lookup"><span data-stu-id="d53e7-116">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d53e7-117">需求</span><span class="sxs-lookup"><span data-stu-id="d53e7-117">Requirements</span></span>  
 <span data-ttu-id="d53e7-118">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d53e7-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d53e7-119">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d53e7-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d53e7-120">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d53e7-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d53e7-121">**.NET framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d53e7-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d53e7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d53e7-122">See Also</span></span>  
 [<span data-ttu-id="d53e7-123">偵錯列舉</span><span class="sxs-lookup"><span data-stu-id="d53e7-123">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)