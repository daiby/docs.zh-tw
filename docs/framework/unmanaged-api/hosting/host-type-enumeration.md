---
title: "HOST_TYPE 列舉"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: HOST_TYPE
api_location: mscoree.dll
api_type: COM
f1_keywords: HOST_TYPE
helpviewer_keywords: HOST_TYPE enumeration [.NET Framework hosting]
ms.assetid: 51f848be-84c5-4036-9839-c762c576bbf5
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e191293ff7bde6b1be2210af4e7830fec0d7290d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="hosttype-enumeration"></a><span data-ttu-id="2b706-102">HOST_TYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="2b706-102">HOST_TYPE Enumeration</span></span>
<span data-ttu-id="2b706-103">包含指定的啟動應用程式的主機類型的值。</span><span class="sxs-lookup"><span data-stu-id="2b706-103">Contains values that specify the type of host that is launching an application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b706-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b706-104">Syntax</span></span>  
  
```  
typedef enum {  
    HOST_TYPE_DEFAULT     = 0x0,  
    HOST_TYPE_APPLAUNCH   = 0x1,  
    HOST_TYPE_CORFLAG     = 0x2  
} HOST_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="2b706-105">成員</span><span class="sxs-lookup"><span data-stu-id="2b706-105">Members</span></span>  
  
|<span data-ttu-id="2b706-106">成員</span><span class="sxs-lookup"><span data-stu-id="2b706-106">Member</span></span>|<span data-ttu-id="2b706-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b706-107">Description</span></span>|  
|------------|-----------------|  
|`HOST_TYPE_APPLAUNCH`|<span data-ttu-id="2b706-108">啟動應用程式從 AppLaunch.exe。</span><span class="sxs-lookup"><span data-stu-id="2b706-108">Launch the application from AppLaunch.exe.</span></span><br /><br /> <span data-ttu-id="2b706-109">部分信任應用程式使用此值。</span><span class="sxs-lookup"><span data-stu-id="2b706-109">Use this value for partially-trusted applications.</span></span>|  
|`HOST_TYPE_CORFLAG`|<span data-ttu-id="2b706-110">直接啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="2b706-110">Launch the application directly.</span></span> <span data-ttu-id="2b706-111">也就是啟動應用程式從其本身的.exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="2b706-111">That is, launch the application from its own .exe file.</span></span><br /><br /> <span data-ttu-id="2b706-112">使用此值為完全信任的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2b706-112">Use this value for fully-trusted applications.</span></span>|  
|`HOST_TYPE_DEFAULT`|<span data-ttu-id="2b706-113">HOST_TYPE_APPLAUNCH 相同。</span><span class="sxs-lookup"><span data-stu-id="2b706-113">Same as HOST_TYPE_APPLAUNCH.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2b706-114">需求</span><span class="sxs-lookup"><span data-stu-id="2b706-114">Requirements</span></span>  
 <span data-ttu-id="2b706-115">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2b706-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b706-116">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2b706-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2b706-117">**程式庫：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2b706-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2b706-118">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b706-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b706-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b706-119">See Also</span></span>  
 [<span data-ttu-id="2b706-120">裝載列舉</span><span class="sxs-lookup"><span data-stu-id="2b706-120">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)