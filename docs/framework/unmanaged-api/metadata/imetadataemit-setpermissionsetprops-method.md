---
title: "IMetaDataEmit::SetPermissionSetProps 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.SetPermissionSetProps
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::SetPermissionSetProps
helpviewer_keywords:
- SetPermissionSetProps method [.NET Framework metadata]
- IMetaDataEmit::SetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 8eaee971-40bf-45e2-a3d8-6e57674213b6
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5666daff143d261160bb90bf31c98d1e1b7ce270
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitsetpermissionsetprops-method"></a><span data-ttu-id="540d5-102">IMetaDataEmit::SetPermissionSetProps 方法</span><span class="sxs-lookup"><span data-stu-id="540d5-102">IMetaDataEmit::SetPermissionSetProps Method</span></span>
<span data-ttu-id="540d5-103">設定或更新功能，在先前呼叫所定義的權限集合的中繼資料簽章[imetadataemit:: Definepermissionset](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepermissionset-method.md)。</span><span class="sxs-lookup"><span data-stu-id="540d5-103">Sets or updates features of the metadata signature of a permission set defined by a prior call to [IMetaDataEmit::DefinePermissionSet](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepermissionset-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="540d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="540d5-104">Syntax</span></span>  
  
```  
HRESULT SetPermissionSetProps (   
    [in]  mdToken         tk,   
    [in]  DWORD           dwAction,   
    [in]  void const      *pvPermission,   
    [in]  ULONG           cbPermission,   
    [out] mdPermission    *ppm   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="540d5-105">參數</span><span class="sxs-lookup"><span data-stu-id="540d5-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="540d5-106">[in]表示要裝飾物件中繼資料語彙基元。</span><span class="sxs-lookup"><span data-stu-id="540d5-106">[in] A metadata token that represents the object to be decorated.</span></span>  
  
 `dwAction`  
 <span data-ttu-id="540d5-107">[in]A [CorDeclSecurity](../../../../docs/framework/unmanaged-api/metadata/cordeclsecurity-enumeration.md)值，指定要使用的宣告式安全性的類型。</span><span class="sxs-lookup"><span data-stu-id="540d5-107">[in] A [CorDeclSecurity](../../../../docs/framework/unmanaged-api/metadata/cordeclsecurity-enumeration.md) value that specifies the type of declarative security to be used.</span></span>  
  
 `pvPermission`  
 <span data-ttu-id="540d5-108">[in]使用權限 BLOB。</span><span class="sxs-lookup"><span data-stu-id="540d5-108">[in] The permission BLOB.</span></span>  
  
 `cbPermission`  
 <span data-ttu-id="540d5-109">[in]大小，以位元組為單位的`pvPermission`。</span><span class="sxs-lookup"><span data-stu-id="540d5-109">[in] The size, in bytes, of `pvPermission`.</span></span>  
  
 `ppm`  
 <span data-ttu-id="540d5-110">[out]`mdPermission`代表更新的權限的中繼資料語彙基元。</span><span class="sxs-lookup"><span data-stu-id="540d5-110">[out] An `mdPermission` metadata token that represents the updated permissions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="540d5-111">需求</span><span class="sxs-lookup"><span data-stu-id="540d5-111">Requirements</span></span>  
 <span data-ttu-id="540d5-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="540d5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="540d5-113">**標頭：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="540d5-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="540d5-114">**程式庫：**做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="540d5-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="540d5-115">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="540d5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="540d5-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="540d5-116">See Also</span></span>  
 [<span data-ttu-id="540d5-117">IMetaDataEmit 介面</span><span class="sxs-lookup"><span data-stu-id="540d5-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="540d5-118">IMetaDataEmit2 介面</span><span class="sxs-lookup"><span data-stu-id="540d5-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)