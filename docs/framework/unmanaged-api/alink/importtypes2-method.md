---
title: "ImportTypes2 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IALink2.ImportTypes2
api_location: alink.dll
api_type: COM
f1_keywords: ImportTypes2
helpviewer_keywords: ImportTypes2 method
ms.assetid: 32f3ba58-9695-41e9-ba58-fd19e45ed396
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 61d707cdd827b5e435c961a14e67170ab0e2bc90
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="importtypes2-method"></a><span data-ttu-id="a7f81-102">ImportTypes2 方法</span><span class="sxs-lookup"><span data-stu-id="a7f81-102">ImportTypes2 Method</span></span>
<span data-ttu-id="a7f81-103">會起始匯入的類型。</span><span class="sxs-lookup"><span data-stu-id="a7f81-103">Initiates the import of types.</span></span> <span data-ttu-id="a7f81-104">呼叫這個方法來開始匯入從透過匯入每個範圍的型別[ImportFile 方法](../../../../docs/framework/unmanaged-api/alink/importfile-method.md)。</span><span class="sxs-lookup"><span data-stu-id="a7f81-104">Call this method to begin importing types from each scope imported via [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7f81-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7f81-105">Syntax</span></span>  
  
```  
HRESULT ImportTypes2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport2** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a7f81-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7f81-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a7f81-107">用來匯入的組件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7f81-107">ID of assembly into which to import.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="a7f81-108">要從中匯入的檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7f81-108">ID of file to from which to import.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="a7f81-109">要從中匯入的以零為起始範圍。</span><span class="sxs-lookup"><span data-stu-id="a7f81-109">Zero-based scope from which to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="a7f81-110">在給定範圍中，接收列舉值類型的控制代碼。</span><span class="sxs-lookup"><span data-stu-id="a7f81-110">Receives enumerator handle for the types in the given scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="a7f81-111">選擇性地接收[IMetaDataImport2 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)介面。</span><span class="sxs-lookup"><span data-stu-id="a7f81-111">Optionally receives [IMetaDataImport2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="a7f81-112">選擇性地指定範圍內接收類型的計數。</span><span class="sxs-lookup"><span data-stu-id="a7f81-112">Optionally receives count of types in the specified scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a7f81-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7f81-113">Return Value</span></span>  
 <span data-ttu-id="a7f81-114">如果方法成功則傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="a7f81-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7f81-115">需求</span><span class="sxs-lookup"><span data-stu-id="a7f81-115">Requirements</span></span>  
 <span data-ttu-id="a7f81-116">需要 alink.h</span><span class="sxs-lookup"><span data-stu-id="a7f81-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7f81-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7f81-117">See Also</span></span>  
 [<span data-ttu-id="a7f81-118">IALink2 介面</span><span class="sxs-lookup"><span data-stu-id="a7f81-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="a7f81-119">IALink 介面</span><span class="sxs-lookup"><span data-stu-id="a7f81-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="a7f81-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="a7f81-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)