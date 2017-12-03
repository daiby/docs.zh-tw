---
title: "ISymUnmanagedNamespace 介面"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedNamespace
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedNamespace
helpviewer_keywords: ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: d42bea4e-5848-4e43-a883-69af7a313ce9
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 8500eb7a9f1762402567e9352a3ce84f5a672a45
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagednamespace-interface"></a><span data-ttu-id="5e932-102">ISymUnmanagedNamespace 介面</span><span class="sxs-lookup"><span data-stu-id="5e932-102">ISymUnmanagedNamespace Interface</span></span>
<span data-ttu-id="5e932-103">代表命名空間。</span><span class="sxs-lookup"><span data-stu-id="5e932-103">Represents a namespace.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5e932-104">方法</span><span class="sxs-lookup"><span data-stu-id="5e932-104">Methods</span></span>  
  
|<span data-ttu-id="5e932-105">方法</span><span class="sxs-lookup"><span data-stu-id="5e932-105">Method</span></span>|<span data-ttu-id="5e932-106">說明</span><span class="sxs-lookup"><span data-stu-id="5e932-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5e932-107">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="5e932-107">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-getname-method.md)|<span data-ttu-id="5e932-108">取得這個命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e932-108">Gets the name of this namespace.</span></span>|  
|[<span data-ttu-id="5e932-109">GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="5e932-109">GetNamespaces Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-getnamespaces-method.md)|<span data-ttu-id="5e932-110">取得這個命名空間的子系。</span><span class="sxs-lookup"><span data-stu-id="5e932-110">Gets the children of this namespace.</span></span>|  
|[<span data-ttu-id="5e932-111">GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="5e932-111">GetVariables Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-getvariables-method.md)|<span data-ttu-id="5e932-112">傳回在此命名空間內的全域範圍中定義的所有變數。</span><span class="sxs-lookup"><span data-stu-id="5e932-112">Returns all variables defined at global scope within this namespace.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5e932-113">需求</span><span class="sxs-lookup"><span data-stu-id="5e932-113">Requirements</span></span>  
 <span data-ttu-id="5e932-114">**標頭：**於 CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5e932-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e932-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e932-115">See Also</span></span>  
 [<span data-ttu-id="5e932-116">診斷符號存放區介面</span><span class="sxs-lookup"><span data-stu-id="5e932-116">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)