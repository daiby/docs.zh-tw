---
title: "ICorDebugAppDomain2::GetArrayOrPointerType 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugAppDomain2.GetArrayOrPointerType
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugAppDomain2::GetArrayOrPointerType
helpviewer_keywords:
- GetArrayOrPointerType method [.NET Framework debugging]
- ICorDebugAppDomain2::GetArrayOrPointerType method [.NET Framework debugging]
ms.assetid: 97e493f5-3a62-4ec7-b42f-4af57bf71f57
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c08a56ff7f6bd109c5568a7f992850708a22a4b0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugappdomain2getarrayorpointertype-method"></a><span data-ttu-id="64a5f-102">ICorDebugAppDomain2::GetArrayOrPointerType 方法</span><span class="sxs-lookup"><span data-stu-id="64a5f-102">ICorDebugAppDomain2::GetArrayOrPointerType Method</span></span>
<span data-ttu-id="64a5f-103">取得指定的型別，或是指標或參考指定之類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="64a5f-103">Gets an array of the specified type, or a pointer or reference to the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64a5f-104">語法</span><span class="sxs-lookup"><span data-stu-id="64a5f-104">Syntax</span></span>  
  
```  
HRESULT GetArrayOrPointerType (  
    [in]  CorElementType    elementType,  
    [in]  ULONG32           nRank,  
    [in]  ICorDebugType     *pTypeArg,  
    [out] ICorDebugType     **ppType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="64a5f-105">參數</span><span class="sxs-lookup"><span data-stu-id="64a5f-105">Parameters</span></span>  
 `elementType`  
 <span data-ttu-id="64a5f-106">[in]指定基礎原生類型 （陣列、 指標或參考） 來建立 CorElementType 列舉值。</span><span class="sxs-lookup"><span data-stu-id="64a5f-106">[in] A value of the CorElementType enumeration that specifies the underlying native type (an array, pointer, or reference) to be created.</span></span>  
  
 `nRank`  
 <span data-ttu-id="64a5f-107">[in]陣列陣序 （亦即，維度數目）。</span><span class="sxs-lookup"><span data-stu-id="64a5f-107">[in] The rank (that is, number of dimensions) of the array.</span></span> <span data-ttu-id="64a5f-108">此值必須是 0，如果`elementType`指定指標或參考類型。</span><span class="sxs-lookup"><span data-stu-id="64a5f-108">This value must be 0 if `elementType` specifies a pointer or reference type.</span></span>  
  
 `pTypeArg`  
 <span data-ttu-id="64a5f-109">[in]ICorDebugType 物件代表的類型陣列的指標、 指標或建立參考。</span><span class="sxs-lookup"><span data-stu-id="64a5f-109">[in] A pointer to an ICorDebugType object that represents the type of array, pointer, or reference to be created.</span></span>  
  
 `ppType`  
 <span data-ttu-id="64a5f-110">[out]位址指標`ICorDebugType`代表建構的陣列、 指標類型或參考的物件類型。</span><span class="sxs-lookup"><span data-stu-id="64a5f-110">[out] A pointer to the address of an `ICorDebugType` object that represents the constructed array, pointer type, or reference type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="64a5f-111">備註</span><span class="sxs-lookup"><span data-stu-id="64a5f-111">Remarks</span></span>  
 <span data-ttu-id="64a5f-112">值*elementType*必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="64a5f-112">The value of *elementType* must be one of the following:</span></span>  
  
-   <span data-ttu-id="64a5f-113">ELEMENT_TYPE_PTR</span><span class="sxs-lookup"><span data-stu-id="64a5f-113">ELEMENT_TYPE_PTR</span></span>  
  
-   <span data-ttu-id="64a5f-114">ELEMENT_TYPE_BYREF</span><span class="sxs-lookup"><span data-stu-id="64a5f-114">ELEMENT_TYPE_BYREF</span></span>  
  
-   <span data-ttu-id="64a5f-115">ELEMENT_TYPE_ARRAY 或 ELEMENT_TYPE_SZARRAY</span><span class="sxs-lookup"><span data-stu-id="64a5f-115">ELEMENT_TYPE_ARRAY or ELEMENT_TYPE_SZARRAY</span></span>  
  
 <span data-ttu-id="64a5f-116">如果值*elementType* ELEMENT_TYPE_PTR 或 ELEMENT_TYPE_BYREF， *nRank*必須為零。</span><span class="sxs-lookup"><span data-stu-id="64a5f-116">If the value of *elementType* is ELEMENT_TYPE_PTR or ELEMENT_TYPE_BYREF, *nRank* must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64a5f-117">需求</span><span class="sxs-lookup"><span data-stu-id="64a5f-117">Requirements</span></span>  
 <span data-ttu-id="64a5f-118">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="64a5f-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64a5f-119">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="64a5f-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="64a5f-120">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="64a5f-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="64a5f-121">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64a5f-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>