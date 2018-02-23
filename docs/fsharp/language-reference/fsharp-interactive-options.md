---
title: "F# Interactive 選項"
description: "了解命令列選項支援 F # Interactive fsi.exe。"
keywords: "Visual F#, F#, 函式程式設計"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: f9f3e39b-ce6c-41ff-991f-0625f46441ae
ms.openlocfilehash: f0a8893abca0435307907aa9c169646bf3dec2d5
ms.sourcegitcommit: adcf9bdafeaa6bc243af7bf70b45f3df954f256a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2018
---
# <a name="f-interactive-options"></a><span data-ttu-id="02460-104">F# Interactive 選項</span><span class="sxs-lookup"><span data-stu-id="02460-104">F# Interactive Options</span></span>

> [!NOTE]
<span data-ttu-id="02460-105">本文目前僅描述 Windows 的體驗。</span><span class="sxs-lookup"><span data-stu-id="02460-105">This article currently describes the experience for Windows only.</span></span>  <span data-ttu-id="02460-106">將會加以重新撰寫。</span><span class="sxs-lookup"><span data-stu-id="02460-106">It will be rewritten.</span></span>

<span data-ttu-id="02460-107">本主題描述支援 F # Interactive 命令列選項`fsi.exe`。</span><span class="sxs-lookup"><span data-stu-id="02460-107">This topic describes the command-line options supported by F# Interactive, `fsi.exe`.</span></span> <span data-ttu-id="02460-108">F # Interactive 接受許多相同的命令列選項為 F # 編譯器，但也可接受一些其他選項。</span><span class="sxs-lookup"><span data-stu-id="02460-108">F# Interactive accepts many of the same command line options as the F# compiler, but also accepts some additional options.</span></span>

## <a name="using-f-interactive-for-scripting"></a><span data-ttu-id="02460-109">使用 F # Interactive 來編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="02460-109">Using F# Interactive for Scripting</span></span>
<span data-ttu-id="02460-110">F # Interactive， `fsi.exe`、 以互動方式，來啟動或從命令列執行指令碼啟動。</span><span class="sxs-lookup"><span data-stu-id="02460-110">F# Interactive, `fsi.exe`, can be launched interactively, or it can be launched from the command line to run a script.</span></span> <span data-ttu-id="02460-111">命令列語法</span><span class="sxs-lookup"><span data-stu-id="02460-111">The command line syntax is</span></span>

```
> fsi.exe [options] [ script-file [arguments] ]
```

<span data-ttu-id="02460-112">F # 指令碼檔案的副檔名是`.fsx`。</span><span class="sxs-lookup"><span data-stu-id="02460-112">The file extension for F# script files is `.fsx`.</span></span>

## <a name="table-of-f-interactive-options"></a><span data-ttu-id="02460-113">F # Interactive 選項的資料表</span><span class="sxs-lookup"><span data-stu-id="02460-113">Table of F# Interactive Options</span></span>
<span data-ttu-id="02460-114">下表摘要說明支援 F # Interactive 選項。</span><span class="sxs-lookup"><span data-stu-id="02460-114">The following table summarizes the options supported by F# Interactive.</span></span> <span data-ttu-id="02460-115">在命令列上或透過 Visual Studio IDE，您可以設定這些選項。</span><span class="sxs-lookup"><span data-stu-id="02460-115">You can set these options on the command-line or through the Visual Studio IDE.</span></span> <span data-ttu-id="02460-116">若要在 Visual Studio IDE 中設定這些選項，開啟**工具**功能表上，選取**選項...**，然後展開**F # 工具**節點，然後選取**F # Interactive**。</span><span class="sxs-lookup"><span data-stu-id="02460-116">To set these options in the Visual Studio IDE, open the **Tools** menu, select **Options...**, then expand the **F# Tools** node and select **F# Interactive**.</span></span>

<span data-ttu-id="02460-117">清單項目清單會出現在 F # Interactive 選項引數，其中以分號分隔 (`;`)。</span><span class="sxs-lookup"><span data-stu-id="02460-117">Where lists appear in F# Interactive option arguments, list elements are separated by semicolons (`;`).</span></span>

|<span data-ttu-id="02460-118">選項</span><span class="sxs-lookup"><span data-stu-id="02460-118">Option</span></span>|<span data-ttu-id="02460-119">描述</span><span class="sxs-lookup"><span data-stu-id="02460-119">Description</span></span>|
|------|-----------|
|**--**|<span data-ttu-id="02460-120">用來指示 F # Interactive 命令列引數其餘引數視為 F # 程式或指令碼，您可以存取程式碼中使用清單**fsi.commandlineargs 存取**。</span><span class="sxs-lookup"><span data-stu-id="02460-120">Used to instruct F# Interactive to treat remaining arguments as command line arguments to the F# program or script, which you can access in code by using the list **fsi.CommandLineArgs**.</span></span>|
|<span data-ttu-id="02460-121">**--checked**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-121">**--checked**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-122">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-122">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-123">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-123">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-124">**--codepage:&lt;int&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-124">**--codepage:&lt;int&gt;**</span></span>|<span data-ttu-id="02460-125">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-125">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-126">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-126">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-127">**--consolecolors**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-127">**--consolecolors**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-128">輸出警告和錯誤訊息中的色彩。</span><span class="sxs-lookup"><span data-stu-id="02460-128">Outputs warning and error messages in color.</span></span>|
|<span data-ttu-id="02460-129">**--crossoptimize**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-129">**--crossoptimize**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-130">啟用或停用跨模組最佳化。</span><span class="sxs-lookup"><span data-stu-id="02460-130">Enable or disable cross-module optimizations.</span></span>|
|<span data-ttu-id="02460-131">**--debug**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-131">**--debug**[**+**&#124;**-**]</span></span><br /><br /><span data-ttu-id="02460-132">**--debug:**[**full**&#124;**pdbonly**&#124;**portable**&#124;**embedded**]</span><span class="sxs-lookup"><span data-stu-id="02460-132">**--debug:**[**full**&#124;**pdbonly**&#124;**portable**&#124;**embedded**]</span></span><br /><br /><span data-ttu-id="02460-133">**-g**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-133">**-g**[**+**&#124;**-**]</span></span><br /><br /><span data-ttu-id="02460-134">**-g:**[**完整**&#124;**pdbonly**&#124;**可攜式**&#124;**內嵌**]</span><span class="sxs-lookup"><span data-stu-id="02460-134">**-g:**[**full**&#124;**pdbonly**&#124;**portable**&#124;**embedded**]</span></span>|<span data-ttu-id="02460-135">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-135">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-136">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-136">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-137">**--define:&lt;string&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-137">**--define:&lt;string&gt;**</span></span>|<span data-ttu-id="02460-138">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-138">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-139">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-139">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-140">**--deterministic**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-140">**--deterministic**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-141">產生的具決定性的組件 （包括模組版本 GUID 與時間戳記）。</span><span class="sxs-lookup"><span data-stu-id="02460-141">Produces a deterministic assembly (including module version GUID and timestamp).</span></span>|
|<span data-ttu-id="02460-142">**--exec**</span><span class="sxs-lookup"><span data-stu-id="02460-142">**--exec**</span></span>|<span data-ttu-id="02460-143">指示 F # interactive 結束之後載入檔案或執行命令列上指定的指令碼檔案。</span><span class="sxs-lookup"><span data-stu-id="02460-143">Instructs F# interactive to exit after loading the files or running the script file given on the command line.</span></span>|
|<span data-ttu-id="02460-144">**--fullpaths**</span><span class="sxs-lookup"><span data-stu-id="02460-144">**--fullpaths**</span></span>|<span data-ttu-id="02460-145">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-145">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-146">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-146">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-147">**--gui**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-147">**--gui**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-148">啟用或停用 Windows Form 事件迴圈。</span><span class="sxs-lookup"><span data-stu-id="02460-148">Enables or disables the Windows Forms event loop.</span></span> <span data-ttu-id="02460-149">會啟用預設值。</span><span class="sxs-lookup"><span data-stu-id="02460-149">The default is enabled.</span></span>|
|<span data-ttu-id="02460-150">**--help**</span><span class="sxs-lookup"><span data-stu-id="02460-150">**--help**</span></span><br /><br /><span data-ttu-id="02460-151">**-?**</span><span class="sxs-lookup"><span data-stu-id="02460-151">**-?**</span></span>|<span data-ttu-id="02460-152">用來顯示命令列語法和每個選項的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="02460-152">Used to display the command line syntax and a brief description of each option.</span></span>|
|<span data-ttu-id="02460-153">**--lib:&lt;folder-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-153">**--lib:&lt;folder-list&gt;**</span></span><br /><br /><span data-ttu-id="02460-154">**-I:&lt;folder-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-154">**-I:&lt;folder-list&gt;**</span></span>|<span data-ttu-id="02460-155">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-155">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-156">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-156">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-157">**--load:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-157">**--load:&lt;filename&gt;**</span></span>|<span data-ttu-id="02460-158">編譯指定的來源處的程式碼啟動，並將已編譯的 F # 建構載入到工作階段。</span><span class="sxs-lookup"><span data-stu-id="02460-158">Compiles the given source code at startup and loads the compiled F# constructs into the session.</span></span> <span data-ttu-id="02460-159">如果包含指令碼的指示詞，例如目標來源**#use**或**#load**，則您必須使用**-使用**或**#use**而不是**-載入**或**#load**。</span><span class="sxs-lookup"><span data-stu-id="02460-159">If the target source contains scripting directives such as **#use** or **#load**, then you must use **--use** or **#use** instead of **--load** or **#load**.</span></span>|
|<span data-ttu-id="02460-160">**--mlcompatibility**</span><span class="sxs-lookup"><span data-stu-id="02460-160">**--mlcompatibility**</span></span>|<span data-ttu-id="02460-161">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-161">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-162">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-162">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-163">**--noframework**</span><span class="sxs-lookup"><span data-stu-id="02460-163">**--noframework**</span></span>|<span data-ttu-id="02460-164">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-164">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-165">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)</span><span class="sxs-lookup"><span data-stu-id="02460-165">For more information, see [Compiler Options](compiler-options.md)</span></span>|
|<span data-ttu-id="02460-166">**--nologo**</span><span class="sxs-lookup"><span data-stu-id="02460-166">**--nologo**</span></span>|<span data-ttu-id="02460-167">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-167">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-168">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-168">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-169">**--nowarn:&lt;warning-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-169">**--nowarn:&lt;warning-list&gt;**</span></span>|<span data-ttu-id="02460-170">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-170">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-171">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-171">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-172">**--optimize**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-172">**--optimize**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-173">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-173">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-174">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-174">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-175">**--preferreduilang:&lt;lang&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-175">**--preferreduilang:&lt;lang&gt;**</span></span>| <span data-ttu-id="02460-176">指定慣用的輸出語言文化特性名稱 （例如 ES-ES、 JA-JP）。</span><span class="sxs-lookup"><span data-stu-id="02460-176">Specifies the preferred output language culture name (for example, es-ES, ja-JP).</span></span> |
|<span data-ttu-id="02460-177">**--quiet**</span><span class="sxs-lookup"><span data-stu-id="02460-177">**--quiet**</span></span>|<span data-ttu-id="02460-178">隱藏 F # Interactive 的輸出到**stdout**資料流。</span><span class="sxs-lookup"><span data-stu-id="02460-178">Suppress F# Interactive's output to the **stdout** stream.</span></span>|
|<span data-ttu-id="02460-179">**--quotations-debug**</span><span class="sxs-lookup"><span data-stu-id="02460-179">**--quotations-debug**</span></span>|<span data-ttu-id="02460-180">指定的額外偵錯資訊應該發出對衍生自 F # 引號常值，而且反映定義的運算式。</span><span class="sxs-lookup"><span data-stu-id="02460-180">Specifies that extra debugging information should be emitted for expressions that are derived from F# quotation literals and reflected definitions.</span></span> <span data-ttu-id="02460-181">偵錯資訊已加入至 F # 運算式樹狀結構節點的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="02460-181">The debug information is added to the custom attributes of an F# expression tree node.</span></span> <span data-ttu-id="02460-182">請參閱[程式碼引號](code-quotations.md)和[Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3)。</span><span class="sxs-lookup"><span data-stu-id="02460-182">See [Code Quotations](code-quotations.md) and [Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3).</span></span>|
|<span data-ttu-id="02460-183">**--readline**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-183">**--readline**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-184">啟用或停用在互動模式中的 tab 鍵自動完成。</span><span class="sxs-lookup"><span data-stu-id="02460-184">Enable or disable tab completion in interactive mode.</span></span>|
|<span data-ttu-id="02460-185">**--reference:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-185">**--reference:&lt;filename&gt;**</span></span><br /><br /><span data-ttu-id="02460-186">**-r:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-186">**-r:&lt;filename&gt;**</span></span>|<span data-ttu-id="02460-187">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-187">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-188">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-188">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-189">**--shadowcopyreferences**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-189">**--shadowcopyreferences**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-190">可避免參考遭 F # 互動式處理序。</span><span class="sxs-lookup"><span data-stu-id="02460-190">Prevents references from being locked by the F# Interactive process.</span></span>|
|<span data-ttu-id="02460-191">**--simpleresolution**</span><span class="sxs-lookup"><span data-stu-id="02460-191">**--simpleresolution**</span></span>|<span data-ttu-id="02460-192">解決使用目錄為基礎的規則，而不是 MSBuild 解析的組件參考。</span><span class="sxs-lookup"><span data-stu-id="02460-192">Resolves assembly references using directory-based rules rather than MSBuild resolution.</span></span>|
|<span data-ttu-id="02460-193">**--tailcalls**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-193">**--tailcalls**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-194">啟用或停用造成可重複使用之結尾遞迴函式的堆疊框架結尾 IL 指令的使用。</span><span class="sxs-lookup"><span data-stu-id="02460-194">Enable or disable the use of the tail IL instruction, which causes the stack frame to be reused for tail recursive functions.</span></span> <span data-ttu-id="02460-195">這個選項預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="02460-195">This option is enabled by default.</span></span>|
|<span data-ttu-id="02460-196">**--targetprofile:&lt;string&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-196">**--targetprofile:&lt;string&gt;**</span></span>|<span data-ttu-id="02460-197">指定這個組件的目標 framework 設定檔。</span><span class="sxs-lookup"><span data-stu-id="02460-197">Specifies target framework profile of this assembly.</span></span> <span data-ttu-id="02460-198">有效值是 mscorlib、 netcore 或 netstandard。</span><span class="sxs-lookup"><span data-stu-id="02460-198">Valid values are mscorlib, netcore or netstandard.</span></span>  <span data-ttu-id="02460-199">預設值是 mscorlib。</span><span class="sxs-lookup"><span data-stu-id="02460-199">The default is mscorlib.</span></span>|
|<span data-ttu-id="02460-200">**--use:&lt;filename&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-200">**--use:&lt;filename&gt;**</span></span>|<span data-ttu-id="02460-201">會告知使用指定的檔案，在啟動做為初始輸入的直譯器。</span><span class="sxs-lookup"><span data-stu-id="02460-201">Tells the interpreter to use the given file on startup as initial input.</span></span>|
|<span data-ttu-id="02460-202">**--utf8output**</span><span class="sxs-lookup"><span data-stu-id="02460-202">**--utf8output**</span></span>|<span data-ttu-id="02460-203">Fsc.exe 編譯器選項相同。</span><span class="sxs-lookup"><span data-stu-id="02460-203">Same as the fsc.exe compiler option.</span></span> <span data-ttu-id="02460-204">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-204">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-205">**--warn:&lt;warning-level&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-205">**--warn:&lt;warning-level&gt;**</span></span>|<span data-ttu-id="02460-206">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-206">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-207">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-207">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-208">**--warnaserror**[**+**&#124;**-**]</span><span class="sxs-lookup"><span data-stu-id="02460-208">**--warnaserror**[**+**&#124;**-**]</span></span>|<span data-ttu-id="02460-209">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-209">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-210">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-210">For more information, see [Compiler Options](compiler-options.md).</span></span>|
|<span data-ttu-id="02460-211">**--warnaserror**[**+**&#124;**-**]:**&lt;int-list&gt;**</span><span class="sxs-lookup"><span data-stu-id="02460-211">**--warnaserror**[**+**&#124;**-**]:**&lt;int-list&gt;**</span></span>|<span data-ttu-id="02460-212">與相同**fsc.exe**編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="02460-212">Same as the **fsc.exe** compiler option.</span></span> <span data-ttu-id="02460-213">如需詳細資訊，請參閱[編譯器選項](compiler-options.md)。</span><span class="sxs-lookup"><span data-stu-id="02460-213">For more information, see [Compiler Options](compiler-options.md).</span></span>|

## <a name="related-topics"></a><span data-ttu-id="02460-214">相關主題</span><span class="sxs-lookup"><span data-stu-id="02460-214">Related Topics</span></span>

|<span data-ttu-id="02460-215">標題</span><span class="sxs-lookup"><span data-stu-id="02460-215">Title</span></span>|<span data-ttu-id="02460-216">描述</span><span class="sxs-lookup"><span data-stu-id="02460-216">Description</span></span>|
|-----|-----------|
|[<span data-ttu-id="02460-217">編譯器選項</span><span class="sxs-lookup"><span data-stu-id="02460-217">Compiler Options</span></span>](compiler-options.md)|<span data-ttu-id="02460-218">描述對於 F # 編譯器，可用的命令列選項**fsc.exe**。</span><span class="sxs-lookup"><span data-stu-id="02460-218">Describes command line options available for the F# compiler, **fsc.exe**.</span></span>|