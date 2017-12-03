---
title: "&lt;AppContextSwitchOverrides&gt;項目"
ms.custom: 
ms.date: 10/17/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-bcl
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- AppContextSwitchOverrides
- compatibility switches
- configuration switches
- configuration
ms.assetid: 4ce07f47-7ddb-4d91-b067-501bd8b88752
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d0c87092786e1057bb925f55cfe46e3f4ef58b9d
ms.sourcegitcommit: 5177d6ae2e9baf026f07ee0631556700a5a193f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/28/2017
---
# <a name="ltappcontextswitchoverridesgt-element"></a><span data-ttu-id="b23a1-102">&lt;AppContextSwitchOverrides&gt;項目</span><span class="sxs-lookup"><span data-stu-id="b23a1-102">&lt;AppContextSwitchOverrides&gt; Element</span></span>
<span data-ttu-id="b23a1-103">定義一或多個由 <xref:System.AppContext> 類別所使用的參數，以提供新功能的退出機制。</span><span class="sxs-lookup"><span data-stu-id="b23a1-103">Defines one or more switches used by the <xref:System.AppContext> class to provide an opt-out mechanism for new functionality.</span></span>  
  
 <span data-ttu-id="b23a1-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="b23a1-104">\<configuration></span></span>  
 <span data-ttu-id="b23a1-105">\<執行階段 ></span><span class="sxs-lookup"><span data-stu-id="b23a1-105">\<runtime></span></span>  
<span data-ttu-id="b23a1-106">\<AppContextSwitchOverrides ></span><span class="sxs-lookup"><span data-stu-id="b23a1-106">\<AppContextSwitchOverrides></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b23a1-107">語法</span><span class="sxs-lookup"><span data-stu-id="b23a1-107">Syntax</span></span>  
  
```xml  
<AppContextSwitchOverrides value="name1=value1[[;name2=value2];...]" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b23a1-108">屬性和項目</span><span class="sxs-lookup"><span data-stu-id="b23a1-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b23a1-109">下列章節說明屬性、子項目和父項目。</span><span class="sxs-lookup"><span data-stu-id="b23a1-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b23a1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b23a1-110">Attributes</span></span>  
  
|<span data-ttu-id="b23a1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b23a1-111">Attribute</span></span>|<span data-ttu-id="b23a1-112">描述</span><span class="sxs-lookup"><span data-stu-id="b23a1-112">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="b23a1-113">必要屬性。</span><span class="sxs-lookup"><span data-stu-id="b23a1-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="b23a1-114">定義一或多個參數名稱和其相關聯的布林值。</span><span class="sxs-lookup"><span data-stu-id="b23a1-114">Defines one or more switch names and their associated Boolean values.</span></span>|  
  
### <a name="value-attribute"></a><span data-ttu-id="b23a1-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="b23a1-115">value Attribute</span></span>  
  
|<span data-ttu-id="b23a1-116">值</span><span class="sxs-lookup"><span data-stu-id="b23a1-116">Value</span></span>|<span data-ttu-id="b23a1-117">說明</span><span class="sxs-lookup"><span data-stu-id="b23a1-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b23a1-118">「 名稱 = 值 」</span><span class="sxs-lookup"><span data-stu-id="b23a1-118">"name=value"</span></span>|<span data-ttu-id="b23a1-119">預先定義的參數名稱，以及其值 (`true`或`false`)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-119">A predefined switch name along with its value (`true` or `false`).</span></span> <span data-ttu-id="b23a1-120">多個參數名稱/值組以分號分隔 （";"）。</span><span class="sxs-lookup"><span data-stu-id="b23a1-120">Multiple switch name/value pairs are separated by semicolons (";").</span></span> <span data-ttu-id="b23a1-121">如需.NET Framework 所支援的預先定義的參數名稱的清單，請參閱 < 備註 > 一節。</span><span class="sxs-lookup"><span data-stu-id="b23a1-121">For a list of predefined switch names supported by the .NET Framework, see the Remarks section.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b23a1-122">子元素</span><span class="sxs-lookup"><span data-stu-id="b23a1-122">Child Elements</span></span>  
 <span data-ttu-id="b23a1-123">無。</span><span class="sxs-lookup"><span data-stu-id="b23a1-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b23a1-124">父項目</span><span class="sxs-lookup"><span data-stu-id="b23a1-124">Parent Elements</span></span>  
  
|<span data-ttu-id="b23a1-125">項目</span><span class="sxs-lookup"><span data-stu-id="b23a1-125">Element</span></span>|<span data-ttu-id="b23a1-126">描述</span><span class="sxs-lookup"><span data-stu-id="b23a1-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="b23a1-127">通用語言執行平台和 .NET Framework 應用程式所使用之每個組態檔中的根項目。</span><span class="sxs-lookup"><span data-stu-id="b23a1-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="b23a1-128">包含有關執行階段初始化選項的資訊。</span><span class="sxs-lookup"><span data-stu-id="b23a1-128">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b23a1-129">備註</span><span class="sxs-lookup"><span data-stu-id="b23a1-129">Remarks</span></span>  
 <span data-ttu-id="b23a1-130">從.NET Framework 4.6 開始`<AppContextSwitchOverrides>`組態檔中的項目可讓呼叫端的 API，以決定其應用程式可以充分利用新功能或保留與舊版的程式庫相容性。</span><span class="sxs-lookup"><span data-stu-id="b23a1-130">Starting with the .NET Framework 4.6, the `<AppContextSwitchOverrides>` element in a configuration file allows callers of an API to determine whether their app can take advantage of new functionality or preserve compatibility with previous versions of a library.</span></span> <span data-ttu-id="b23a1-131">例如，如果應用程式開發介面的行為已變更的程式庫中，兩個版本之間`<AppContextSwitchOverrides>`項目可讓呼叫端，該 api 來支援新功能的程式庫版本的新行為來選擇退出。</span><span class="sxs-lookup"><span data-stu-id="b23a1-131">For example, if the behavior of an API has changed between two versions of a library, the `<AppContextSwitchOverrides>` element allows callers of that API to opt out of the new behavior on versions of the library that support the new functionality.</span></span> <span data-ttu-id="b23a1-132">在.NET Framework 中，呼叫 Api 的應用程式`<AppContextSwitchOverrides>`項目也可讓呼叫端的應用程式目標的舊版.NET Framework，以選擇加入新功能，如果包含的.NET Framework 版本上執行其應用程式這項功能。</span><span class="sxs-lookup"><span data-stu-id="b23a1-132">For apps that call APIs in the .NET Framework, the `<AppContextSwitchOverrides>` element can also allow callers whose apps target an earlier version of the .NET Framework to opt into new functionality if their app is running on a version of the .NET Framework that includes that functionality.</span></span>  
  
 <span data-ttu-id="b23a1-133">`value`屬性`<AppContextSwitchOverrides>`元素所組成的單一字串，包含一或多個以分號分隔名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="b23a1-133">The `value` attribute of the `<AppContextSwitchOverrides>` element consists of a single string that consists of one or more semicolon-delimited name/value pairs.</span></span>  <span data-ttu-id="b23a1-134">每個名稱識別的相容性參數，且其對應的值為布林值 (`true`或`false`)，指出是否已設定的參數。</span><span class="sxs-lookup"><span data-stu-id="b23a1-134">Each name identifies a compatibility switch, and its corresponding value is a Boolean (`true` or `false`) that indicates whether the switch is set.</span></span> <span data-ttu-id="b23a1-135">根據預設，這個參數是`false`，和程式庫提供的新功能。</span><span class="sxs-lookup"><span data-stu-id="b23a1-135">By default, the switch is `false`, and libraries  provide the new functionality.</span></span> <span data-ttu-id="b23a1-136">它們僅提供先前的功能，如果已設定參數 (亦即，其值是`true`)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-136">They only provide the previous functionality if the switch is set (that is, its value is `true`).</span></span> <span data-ttu-id="b23a1-137">這可讓現有的 api 提供新的行為，同時允許取決於先前的行為，退出新功能的呼叫端程式庫。</span><span class="sxs-lookup"><span data-stu-id="b23a1-137">This allows libraries to provide new behavior for an existing API while allowing callers who depend on the previous behavior to opt out of the new functionality.</span></span>  
  
 <span data-ttu-id="b23a1-138">.NET Framework 支援下列參數：</span><span class="sxs-lookup"><span data-stu-id="b23a1-138">The .NET Framework supports the following switches:</span></span>  
  
|<span data-ttu-id="b23a1-139">參數名稱</span><span class="sxs-lookup"><span data-stu-id="b23a1-139">Switch name</span></span>|<span data-ttu-id="b23a1-140">說明</span><span class="sxs-lookup"><span data-stu-id="b23a1-140">Description</span></span>|<span data-ttu-id="b23a1-141">導入</span><span class="sxs-lookup"><span data-stu-id="b23a1-141">Introduced</span></span>|  
|-----------------|-----------------|----------------|  
|`Switch.MS.Internal.`<br/>`DoNotApplyLayoutRoundingToMarginsAndBorderThickness`|<span data-ttu-id="b23a1-142">控制 Windows Presentation Foundation 是否使用傳統演算法的控制項配置。</span><span class="sxs-lookup"><span data-stu-id="b23a1-142">Controls whether Windows Presentation Foundation uses legacy a algorithm for control layout.</span></span> <span data-ttu-id="b23a1-143">如需詳細資訊，請參閱[風險降低：WPF 版面配置](~/docs/framework/migration-guide/mitigation-wpf-layout.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-143">For more information, see [Mitigation: WPF Layout](~/docs/framework/migration-guide/mitigation-wpf-layout.md).</span></span>|<span data-ttu-id="b23a1-144">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-144">.NET Framework 4.6</span></span>|  
|`Switch.System.Activities.`<br/>`UseMD5CryptoServiceProviderForWFDebugger`|<span data-ttu-id="b23a1-145">當設定為`false`，允許 FIPS 已啟用時，Visual Studio 的 XAML 型工作流程專案的偵錯。</span><span class="sxs-lookup"><span data-stu-id="b23a1-145">When set to `false`, allows debugging of XAML-based workflow projects with Visual Studio when FIPS is enabled.</span></span> <span data-ttu-id="b23a1-146">未安裝， <xref:System.NullReferenceException> System.Activities 組件中的方法的呼叫中是否擲回。</span><span class="sxs-lookup"><span data-stu-id="b23a1-146">Without it, a <xref:System.NullReferenceException> is thrown in calls to methods in the System.Activities assembly.</span></span>|<span data-ttu-id="b23a1-147">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-147">.NET Framework 4.7</span></span>|
|`Switch.System.Drawing.`<br/>`DontSupportPngFramesInIcons`|<span data-ttu-id="b23a1-148">控制項是否<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>方法會擲回的例外狀況時<xref:System.Drawing.Icon>物件具有 PNG 畫面格。</span><span class="sxs-lookup"><span data-stu-id="b23a1-148">Controls whether the <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> method throws an exception when an <xref:System.Drawing.Icon> object has PNG frames.</span></span> <span data-ttu-id="b23a1-149">如需詳細資訊，請參閱[風險降低：Icon 物件中的 PNG 畫面格](~/docs/framework/migration-guide/mitigation-png-frames-in-icon-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-149">For more information, see [Mitigation: PNG Frames in Icon Objects](~/docs/framework/migration-guide/mitigation-png-frames-in-icon-objects.md).</span></span>|<span data-ttu-id="b23a1-150">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-150">.NET Framework 4.6</span></span>|  
|`Switch.System.Globalization.NoAsyncCurrentCulture`|<span data-ttu-id="b23a1-151">控制是否非同步作業不會流動從呼叫的執行緒內容。</span><span class="sxs-lookup"><span data-stu-id="b23a1-151">Controls whether asynchronous operations do not flow from the calling thread's context.</span></span> <span data-ttu-id="b23a1-152">如需詳細資訊，請參閱[CurrentCulture 和 CurrentUICulture 流經工作](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#currentculture-and-currentuiculture-flow-across-tasks)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-152">For more information, see [CurrentCulture and CurrentUICulture flow across tasks](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#currentculture-and-currentuiculture-flow-across-tasks).</span></span>|<span data-ttu-id="b23a1-153">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-153">.NET Framework 4.6</span></span>|  
|`Switch.System.IdentityModel.`<br/>`DisableMultipleDNSEntriesInSANCertificate`|<span data-ttu-id="b23a1-154">控制項是否<xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims%2A?displayProperty=nameWithType>方法會嘗試比對的宣告類型，只能使用最後一個 DNS 項目。</span><span class="sxs-lookup"><span data-stu-id="b23a1-154">Controls whether the <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims%2A?displayProperty=nameWithType> method attempts to match the claim type only with the last DNS entry.</span></span> <span data-ttu-id="b23a1-155">如需詳細資訊，請參閱[風險降低：X509CertificateClaimSet.FindClaims 方法](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-155">For more information, see [Mitigation: X509CertificateClaimSet.FindClaims Method](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md).</span></span>|<span data-ttu-id="b23a1-156">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="b23a1-156">.NET Framework 4.6.1</span></span>|  
|`Switch.System.IO.BlockLongPaths`|<span data-ttu-id="b23a1-157">控制項是否路徑長度超過`MAX_PATH`（260 個字元） 會擲回<xref:System.IO.PathTooLongException>。</span><span class="sxs-lookup"><span data-stu-id="b23a1-157">Controls whether paths longer than `MAX_PATH` (260 characters) throw a <xref:System.IO.PathTooLongException>.</span></span> <span data-ttu-id="b23a1-158">如需詳細資訊，請參閱[長路徑支援](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#long-path-support)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-158">For more information, see [Long Path Support](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#long-path-support).</span></span>|<span data-ttu-id="b23a1-159">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="b23a1-159">.NET Framework 4.6.2</span></span>|  
|`Switch.System.IO.Compression.ZipFile.`<br/>`UseBackslash`|<span data-ttu-id="b23a1-160">使用反斜線 ("\\") 而不是正斜線 （"/"） 為路徑分隔符號<xref:System.IO.Compression.ZipArchiveEntry.FullName%2A?displayProperty=nameWithType>屬性。</span><span class="sxs-lookup"><span data-stu-id="b23a1-160">Uses the backslash ("\\") rather than the forward slash ("/") as the path separator in the <xref:System.IO.Compression.ZipArchiveEntry.FullName%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="b23a1-161">如需詳細資訊，請參閱[風險降低： ZipArchiveEntry.FullName 路徑分隔符號](~/docs/framework/migration-guide/mitigation-ziparchiveentry-fullname-path-separator.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-161">For more information, see  [Mitigation: ZipArchiveEntry.FullName Path Separator](~/docs/framework/migration-guide/mitigation-ziparchiveentry-fullname-path-separator.md).</span></span>|<span data-ttu-id="b23a1-162">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="b23a1-162">.NET Framework 4.6.1</span></span>|  
|`Switch.System.IO.`<br/>`UseLegacyPathHandling`|<span data-ttu-id="b23a1-163">控制是否使用傳統路徑正規化和所支援的 URI 路徑<xref:System.IO.Path.GetDirectoryName%2A?displayProperty=nameWithType>和<xref:System.IO.Path.GetPathRoot%2A?displayProperty=nameWithType>方法。</span><span class="sxs-lookup"><span data-stu-id="b23a1-163">Controls whether legacy path normalization is used and URI paths are supported by the <xref:System.IO.Path.GetDirectoryName%2A?displayProperty=nameWithType> and <xref:System.IO.Path.GetPathRoot%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="b23a1-164">如需詳細資訊，請參閱[風險降低： 路徑正規化](~/docs/framework/migration-guide/mitigation-path-normalization.md)和[風險降低： 路徑冒號會檢查](~/docs/framework/migration-guide/mitigation-path-colon-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-164">For more information, see [Mitigation: Path Normalization](~/docs/framework/migration-guide/mitigation-path-normalization.md) and [Mitigation: Path Colon Checks](~/docs/framework/migration-guide/mitigation-path-colon-checks.md).</span></span>|<span data-ttu-id="b23a1-165">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="b23a1-165">.NET Framework 4.6.2</span></span>|  
|`Switch.System.`<br/>`MemberDescriptorEqualsReturnsFalseIfEquivalent`|<span data-ttu-id="b23a1-166">控制是否為等號比較測試<xref:System.ComponentModel.MemberDescriptor.Category%2A?displayProperty=nameWithType>與某個物件的屬性<xref:System.ComponentModel.MemberDescriptor.Description%2A?displayProperty=nameWithType>第二個物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="b23a1-166">Controls whether a test for equality compares the <xref:System.ComponentModel.MemberDescriptor.Category%2A?displayProperty=nameWithType> property of one object with the <xref:System.ComponentModel.MemberDescriptor.Description%2A?displayProperty=nameWithType> property of the second object.</span></span> <span data-ttu-id="b23a1-167">如需詳細資訊，請參閱[不正確實作 MemberDescriptor.Equals](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#incorrect-implementation-of-memberdescriptorequals)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-167">For more information, see [Incorrect implementation of MemberDescriptor.Equals](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#incorrect-implementation-of-memberdescriptorequals).</span></span>|<span data-ttu-id="b23a1-168">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="b23a1-168">.NET Framework 4.6.2</span></span>|  
 `Switch.System.Net.`<br/>`DontCheckCertificateEKUs`|<span data-ttu-id="b23a1-169">停用憑證增強金鑰使用方法 (EKU) 物件識別碼 (OID) 驗證。</span><span class="sxs-lookup"><span data-stu-id="b23a1-169">Disables certificate enhanced key usage (EKU) object identifier (OID) validation.</span></span> <span data-ttu-id="b23a1-170">增強金鑰使用方法 (EKU) 延伸模組是物件識別碼 (Oid)，以指出應用程式使用金鑰的集合。</span><span class="sxs-lookup"><span data-stu-id="b23a1-170">An enhanced key usage (EKU) extension is a collection of object identifiers (OIDs) that indicate the applications that use the key.</span></span>|<span data-ttu-id="b23a1-171">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-171">.NET Framework 4.6</span></span>|
|`Switch.System.Net.`<br/>`DontEnableSchSendAuxRecord`|<span data-ttu-id="b23a1-172">停用使用 SCH_SEND_AUX_RECORD 停用 TLS1.0 瀏覽器利用針對 SSL/TLS (BEAST) 補救。</span><span class="sxs-lookup"><span data-stu-id="b23a1-172">Disables TLS1.0 Browser Exploit Against SSL/TLS (BEAST) mitigation by disabling the use of SCH_SEND_AUX_RECORD.</span></span>|<span data-ttu-id="b23a1-173">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-173">.NET Framework 4.6</span></span>|
|`Switch.System.Net.`<br/>`DontEnableSchUseStrongCrypto`|<span data-ttu-id="b23a1-174">控制項是否<xref:System.Net.ServicePointManager?displayProperty=nameWithType>和<xref:System.Net.Security.SslStream?displayProperty=nameWithType>類別可以使用 SSL 3.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b23a1-174">Controls whether the <xref:System.Net.ServicePointManager?displayProperty=nameWithType> and <xref:System.Net.Security.SslStream?displayProperty=nameWithType> classes can use the SSL 3.0 protocol.</span></span> <span data-ttu-id="b23a1-175">如需詳細資訊，請參閱[風險降低：TLS 通訊協定](~/docs/framework/migration-guide/mitigation-tls-protocols.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-175">For more information, see [Mitigation: TLS Protocols](~/docs/framework/migration-guide/mitigation-tls-protocols.md).</span></span>|<span data-ttu-id="b23a1-176">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-176">.NET Framework 4.6</span></span>|
|`Switch.System.Net.`<br/>`DontEnableSystemDefaultTlsVersions`|<span data-ttu-id="b23a1-177">停用 SystemDefault TLS 版本還原成預設值是 Tls12、 Tls11、 Tls。</span><span class="sxs-lookup"><span data-stu-id="b23a1-177">Disables SystemDefault TLS versions reverting back to a default of Tls12, Tls11, Tls.</span></span>|<span data-ttu-id="b23a1-178">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-178">.NET Framework 4.7</span></span>|
|`Switch.System.Net.`<br/>`DontEnableTlsAlerts`|<span data-ttu-id="b23a1-179">停用 SslStream TLS 伺服器端的警示。</span><span class="sxs-lookup"><span data-stu-id="b23a1-179">Disables SslStream TLS server-side Alerts.</span></span>|<span data-ttu-id="b23a1-180">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-180">.NET Framework 4.7</span></span>|
|`Switch.System.Runtime.Serialization.`<br/>`DoNotUseECMAScriptV6EscapeControlCharacter` |<span data-ttu-id="b23a1-181">控制項是否[DataContractJsonSerializer](xref:System.Runtime.Serialization.Json.DataContractJsonSerializer)序列化某些 ECMAScript V6 和 V8 標準為基礎的控制字元。</span><span class="sxs-lookup"><span data-stu-id="b23a1-181">Controls whether the [DataContractJsonSerializer](xref:System.Runtime.Serialization.Json.DataContractJsonSerializer) serializes some control characters based on the ECMAScript V6 and V8 standards.</span></span> <span data-ttu-id="b23a1-182">如需詳細資訊，請參閱[風險降低︰使用 DataContractJsonSerializer 控制字元的序列化](Mitigation:%20Serialization%20of%20Control%20Characters%20with%20the%20DataContractJsonSerializer.md)</span><span class="sxs-lookup"><span data-stu-id="b23a1-182">For more information, see [Mitigation: Serialization of Control Characters with the DataContractJsonSerializer](Mitigation:%20Serialization%20of%20Control%20Characters%20with%20the%20DataContractJsonSerializer.md)</span></span>| <span data-ttu-id="b23a1-183">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-183">.NET Framework 4.7</span></span> |
|`Switch.System.Security.ClaimsIdentity.`<br/>`SetActorAsReferenceWhenCopyingClaimsIdentity`|<span data-ttu-id="b23a1-184">控制項是否<xref:System.Security.Claims.ClaimsIdentity.%23ctor%28System.Security.Principal.IIdentity%29?displayProperty=nameWithType>建構函式設定新的物件<xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=nameWithType>與現有的物件參考的屬性。</span><span class="sxs-lookup"><span data-stu-id="b23a1-184">Controls whether the <xref:System.Security.Claims.ClaimsIdentity.%23ctor%28System.Security.Principal.IIdentity%29?displayProperty=nameWithType> constructor sets the  new object's <xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=nameWithType> property with an existing object reference.</span></span> <span data-ttu-id="b23a1-185">如需詳細資訊，請參閱[風險降低︰ClaimsIdentity 建構函式](~/docs/framework/migration-guide/mitigation-claimsidentity-constructor.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-185">For more information, see [Mitigation: ClaimsIdentity Constructor](~/docs/framework/migration-guide/mitigation-claimsidentity-constructor.md).</span></span>|<span data-ttu-id="b23a1-186">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="b23a1-186">.NET Framework 4.6.2</span></span>|  
|`Switch.System.Security.Cryptography.`<br/>`AesCryptoServiceProvider.DontCorrectlyResetDecryptor`|<span data-ttu-id="b23a1-187">控制項是否嘗試重複使用<xref:System.Security.Cryptography.AesCryptoServiceProvider>的解密程式來擲回<xref:System.Security.Cryptography.CryptographicException>。</span><span class="sxs-lookup"><span data-stu-id="b23a1-187">Controls whether the attempt to reuse an <xref:System.Security.Cryptography.AesCryptoServiceProvider> decryptor throws a <xref:System.Security.Cryptography.CryptographicException>.</span></span> <span data-ttu-id="b23a1-188">如需詳細資訊，請參閱 AesCryptoServiceProvider 的解密程式來提供可重複使用 transform](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#aescryptoserviceprovider-decryptor-provides-a-reusable-transform)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-188">For more information, see AesCryptoServiceProvider decryptor provides a reusable transform](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#aescryptoserviceprovider-decryptor-provides-a-reusable-transform).</span></span>|<span data-ttu-id="b23a1-189">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="b23a1-189">.NET Framework 4.6.2</span></span>|
|`Switch.System.Security.Cryptography.`<br/>`DoNotAddrOfCspParentWindowHandle`|<span data-ttu-id="b23a1-190">控制項是否值[CspParameters.ParentWindowHandle](xref:System.Security.Cryptography.CspParameters.ParentWindowHandle)屬性是[IntPtr](xref:System.IntPtr)代表視窗的記憶體位置處理，或它是否視窗控制代碼 (HWND)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-190">Controls whether the value of the [CspParameters.ParentWindowHandle](xref:System.Security.Cryptography.CspParameters.ParentWindowHandle) property is an [IntPtr](xref:System.IntPtr) that represents the memory location of a window handle, or whether it is a window handle (an HWND).</span></span> <span data-ttu-id="b23a1-191">如需詳細資訊，請參閱[風險降低︰CspParameters.ParentWindowHandle 應該有 HWND](Mitigation:%20CspParameters.ParentWindowHandle%20Expects%20an%20HWND.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-191">For more information, see [Mitigation: CspParameters.ParentWindowHandle Expects an HWND](Mitigation:%20CspParameters.ParentWindowHandle%20Expects%20an%20HWND.md).</span></span> |<span data-ttu-id="b23a1-192">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-192">.NET Framework 4.7</span></span>|   
|`Switch.System.ServiceModel.`<br/>`AllowUnsignedToHeader`|<span data-ttu-id="b23a1-193">決定是否`TransportWithMessageCredential`安全性模式可讓訊息與不帶正負號"to"標頭。</span><span class="sxs-lookup"><span data-stu-id="b23a1-193">Determines whether the `TransportWithMessageCredential` security mode allows messages with an unsigned "to" header.</span></span> <span data-ttu-id="b23a1-194">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="b23a1-194">This is an opt-in switch.</span></span> <span data-ttu-id="b23a1-195">如需詳細資訊，請參閱[.NET Framework 4.6.1 中的執行階段變更](https://msdn.microsoft.com/library/mt592686.aspx#WCF)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-195">For more information, see [Runtime Changes in the .NET Framework 4.6.1](https://msdn.microsoft.com/library/mt592686.aspx#WCF).</span></span>|<span data-ttu-id="b23a1-196">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="b23a1-196">.NET Framework 4.6.1</span></span>| 
|`Switch.System.ServiceModel.`<br />`DisableCngCertificates`|<span data-ttu-id="b23a1-197">決定是否嘗試使用 X509 憑證與 CSG 金鑰儲存提供者擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b23a1-197">Determines whether the attempt to use X509 certificates with a CSG key storage provider throws an exception.</span></span> <span data-ttu-id="b23a1-198">如需詳細資訊，請參閱[WCF 傳輸安全性支援儲存使用 CNG 憑證](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#wcf-transport-security-supports-certificates-stored-using-cng)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-198">For more information, see [WCF transport security supports certificates stored using CNG](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#wcf-transport-security-supports-certificates-stored-using-cng).</span></span>|<span data-ttu-id="b23a1-199">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="b23a1-199">.NET Framework 4.6.1</span></span>|
|`Switch.System.ServiceModel.`<br/>`DisableUsingServicePointManagerSecurityProtocols`|<span data-ttu-id="b23a1-200">連同`Switch.System.Net.DontEnableSchUseStrongCrypto`，決定 WCF 訊息安全性使用 TLS 1.1 和 TLS 1.2。</span><span class="sxs-lookup"><span data-stu-id="b23a1-200">Along with `Switch.System.Net.DontEnableSchUseStrongCrypto`, determines whether WCF message security uses TLS 1.1 and TLS 1.2.</span></span>|<span data-ttu-id="b23a1-201">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-201">.NET Framework 4.7</span></span> |    
|`Switch.System.Windows.Controls.Grid.`<br/>`StarDefinitionsCanExceedAvailableSpace` |<span data-ttu-id="b23a1-202">決定 Windows Presentation Foundation 是否適用於舊的演算法 (`true`) 或新的演算法 (`false`) 中配置空間\*-資料行。</span><span class="sxs-lookup"><span data-stu-id="b23a1-202">Determines whether Windows Presentation Foundation applies an old algorithm (`true`) or a new algorithm (`false`) in allocating space to \*-columns.</span></span> <span data-ttu-id="b23a1-203">如需詳細資訊，請參閱[風險降低︰方格控制項對 Star-columns 的空間配置](Mitigation:%20Grid%20Control's%20Space%20Allocation%20to%20Star-columns.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-203">For more information, see [Mitigation: Grid Control's Space Allocation to Star-columns](Mitigation:%20Grid%20Control's%20Space%20Allocation%20to%20Star-columns.md).</span></span> |<span data-ttu-id="b23a1-204">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-204">.NET Framework 4.7</span></span> |
|`Switch.System.Windows.Forms.`<br />`DontSupportReentrantFilterMessage`|<span data-ttu-id="b23a1-205">選擇不允許自訂程式碼<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A?displayProperty=nameWithType>實作安全地篩選訊息，而不擲回例外狀況時<xref:System.Windows.Forms.Application.FilterMessage%2A?displayProperty=nameWithType>方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="b23a1-205">Opts out of the code that allows a custom <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A?displayProperty=nameWithType> implementation to safely filter messages without throwing an exception when the <xref:System.Windows.Forms.Application.FilterMessage%2A?displayProperty=nameWithType> method is called.</span></span> <span data-ttu-id="b23a1-206">如需詳細資訊，請參閱[風險降低：自訂 IMessageFilter.PreFilterMessage 實作](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-206">For more information, see [Mitigation: Custom IMessageFilter.PreFilterMessage Implementations](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md).</span></span>|<span data-ttu-id="b23a1-207">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="b23a1-207">.NET Framework 4.6.1</span></span>|  
|`Switch.System.Windows.Input.Stylus.`<br/>`EnablePointerSupport`|<span data-ttu-id="b23a1-208">決定是否選用`WM_POINTER`-根據的觸控/手寫筆的堆疊 WPF 應用程式中啟用。</span><span class="sxs-lookup"><span data-stu-id="b23a1-208">Determines whether an optional `WM_POINTER`-based touch/stylus stack is enabled in WPF applications.</span></span> <span data-ttu-id="b23a1-209">如需詳細資訊，請參閱[風險降低： 指標為基礎的觸控和手寫筆支援](Mitigation:%20Pointer-based%20Touch%20and%20Stylus%20Support.md)</span><span class="sxs-lookup"><span data-stu-id="b23a1-209">For more information, see [Mitigation: Pointer-based Touch and Stylus Support](Mitigation:%20Pointer-based%20Touch%20and%20Stylus%20Support.md)</span></span> | 
|`Switch.System.Windows.Media.ImageSourceConverter`<br/>`OverrideExceptionWithNullReferenceException`|<span data-ttu-id="b23a1-210">控制是否舊版[NullReferenceException](xref:System.NullReferenceException)而不是更具體地來說指出例外狀況原因的例外狀況擲回 (例如[DirectoryNotFoundException](xref:System.IO.DirectoryNotFoundException)或[FileNotFoundException](xref:System.IO.FileNotFoundException)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-210">Controls whether a legacy [NullReferenceException](xref:System.NullReferenceException) is thrown instead of the exception that more specifically indicates the cause of the exception (such as a [DirectoryNotFoundException](xref:System.IO.DirectoryNotFoundException) or a [FileNotFoundException](xref:System.IO.FileNotFoundException).</span></span> <span data-ttu-id="b23a1-211">適用於由處理所依賴的程式碼[NullReferenceException](xref:System.NullReferenceException)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-211">It is intended for use by code that depends on handling the [NullReferenceException](xref:System.NullReferenceException).</span></span> | <span data-ttu-id="b23a1-212">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="b23a1-212">.NET Framework 4.7</span></span> |
|`System.Xml.`<br /><br /> `IgnoreEmptyKeySequences`|<span data-ttu-id="b23a1-213">控制是否在複合的索引鍵中的空白索引鍵序列會忽略 XSD 結構描述驗證。</span><span class="sxs-lookup"><span data-stu-id="b23a1-213">Controls whether empty key sequences in compound keys are ignored by XSD schema validation.</span></span> <span data-ttu-id="b23a1-214">如需詳細資訊，請參閱[風險降低： XML 結構描述驗證](~/docs/framework/migration-guide/mitigation-xml-schema-validation.md)。</span><span class="sxs-lookup"><span data-stu-id="b23a1-214">For more information, see [Mitigation: XML Schema Validation](~/docs/framework/migration-guide/mitigation-xml-schema-validation.md).</span></span>|<span data-ttu-id="b23a1-215">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="b23a1-215">.NET Framework 4.6</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="b23a1-216">而非新增`AppContextSwitchOverrides`應用程式組態檔項目，您也可以設定參數以程式設計方式透過呼叫`static`（C# 中） 或`Shared`（在 Visual Basic)<xref:System.AppContext.SetSwitch%2A?displayProperty=nameWithType>方法。</span><span class="sxs-lookup"><span data-stu-id="b23a1-216">Instead of adding an `AppContextSwitchOverrides` element to an application configuration file, you can also set the switches programmatically by calling the `static` (in C#) or `Shared` (in Visual Basic) <xref:System.AppContext.SetSwitch%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="b23a1-217">程式庫開發人員也可以定義自訂的參數，以允許呼叫端退出變更他們的程式庫的更新版本中引進的功能。</span><span class="sxs-lookup"><span data-stu-id="b23a1-217">Library developers can also define custom switches to allow callers to opt out of changed functionality introduced  in later versions of their libraries.</span></span> <span data-ttu-id="b23a1-218">如需詳細資訊，請參閱 <xref:System.AppContext> 類別。</span><span class="sxs-lookup"><span data-stu-id="b23a1-218">For more information, see the <xref:System.AppContext> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b23a1-219">範例</span><span class="sxs-lookup"><span data-stu-id="b23a1-219">Example</span></span>  
 <span data-ttu-id="b23a1-220">下列範例會使用`AppContextSwitchOverrides`項目來定義單一應用程式相容性參數， `Switch.System.Globalization.NoAsyncCurrentCulture`，可避免文化特性中的非同步方法呼叫的執行緒之間流動。</span><span class="sxs-lookup"><span data-stu-id="b23a1-220">The following example uses the `AppContextSwitchOverrides` element to define a single application  compatibility switch, `Switch.System.Globalization.NoAsyncCurrentCulture`, that prevents culture from flowing across threads in asynchronous method calls.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <AppContextSwitchOverrides value="Switch.System.Globalization.NoAsyncCurrentCulture=true" />  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="b23a1-221">下列範例會使用`AppContextSwitchOverrides`項目來定義兩個應用程式相容性參數，`Switch.System.Globalization.NoAsyncCurrentCulture`和`Switch.System.IO.BlockLongPaths`。</span><span class="sxs-lookup"><span data-stu-id="b23a1-221">The following example uses the `AppContextSwitchOverrides` element to define two application  compatibility switches, `Switch.System.Globalization.NoAsyncCurrentCulture` and `Switch.System.IO.BlockLongPaths`.</span></span> <span data-ttu-id="b23a1-222">請注意分號分隔的兩個名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="b23a1-222">Note that a semicolon separates the two name/value pairs.</span></span>  
  
```xml  
<configuration>  
    <runtime>  
       <AppContextSwitchOverrides   
          value="Switch.System.Globalization.NoAsyncCurrentCulture=true;Switch.System.IO.BlockLongPaths=true" />  
    </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b23a1-223">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b23a1-223">See Also</span></span>  
<xref:System.AppContext>  
 [<span data-ttu-id="b23a1-224">\<runtime > 項目</span><span class="sxs-lookup"><span data-stu-id="b23a1-224">\<runtime> Element</span></span>](runtime-element.md)  
 [<span data-ttu-id="b23a1-225">\<configuration> 項目</span><span class="sxs-lookup"><span data-stu-id="b23a1-225">\<configuration> Element</span></span>](../configuration-element.md)