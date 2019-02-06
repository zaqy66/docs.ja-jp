---
title: -baseaddress
ms.date: 08/09/2018
f1_keywords:
- /baseaddress
- baseaddress
helpviewer_keywords:
- -baseaddress compiler option [Visual Basic]
- /baseaddress compiler option [Visual Basic]
- baseaddress compiler option [Visual Basic]
ms.assetid: c982bcf2-46e5-47a2-bc8f-a5cc32b7dc47
ms.openlocfilehash: 733013c8eca75bad0dc0bdf1d76f1468b1d903a8
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2019
ms.locfileid: "55759393"
---
# <a name="-baseaddress"></a><span data-ttu-id="fe67f-102">-baseaddress</span><span class="sxs-lookup"><span data-stu-id="fe67f-102">-baseaddress</span></span>
<span data-ttu-id="fe67f-103">DLL を作成するときに、既定のベース アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe67f-103">Specifies a default base address when creating a DLL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe67f-104">構文</span><span class="sxs-lookup"><span data-stu-id="fe67f-104">Syntax</span></span>  
  
```  
-baseaddress:address  
```  
  
## <a name="arguments"></a><span data-ttu-id="fe67f-105">引数</span><span class="sxs-lookup"><span data-stu-id="fe67f-105">Arguments</span></span>  
  
|<span data-ttu-id="fe67f-106">用語</span><span class="sxs-lookup"><span data-stu-id="fe67f-106">Term</span></span>|<span data-ttu-id="fe67f-107">定義</span><span class="sxs-lookup"><span data-stu-id="fe67f-107">Definition</span></span>|  
|---|---|  
|`address`|<span data-ttu-id="fe67f-108">必須。</span><span class="sxs-lookup"><span data-stu-id="fe67f-108">Required.</span></span> <span data-ttu-id="fe67f-109">DLL のベース アドレス。</span><span class="sxs-lookup"><span data-stu-id="fe67f-109">The base address for the DLL.</span></span> <span data-ttu-id="fe67f-110">このアドレスは、16 進数として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe67f-110">This address must be specified as a hexadecimal number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe67f-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="fe67f-111">Remarks</span></span>  
 <span data-ttu-id="fe67f-112">DLL の既定のベース アドレスの設定、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="fe67f-112">The default base address for a DLL is set by the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span>  
  
 <span data-ttu-id="fe67f-113">このアドレスの下位ワードは丸められますことに注意します。</span><span class="sxs-lookup"><span data-stu-id="fe67f-113">Be aware that the lower-order word in this address is rounded.</span></span> <span data-ttu-id="fe67f-114">たとえば、0x11110001 とを指定する場合は丸められて 0x11110000 に丸められます。</span><span class="sxs-lookup"><span data-stu-id="fe67f-114">For example, if you specify 0x11110001, it is rounded to 0x11110000.</span></span>  
  
 <span data-ttu-id="fe67f-115">DLL の署名プロセスを完了するには使用、`–R`厳密名ツール (Sn.exe) のオプション。</span><span class="sxs-lookup"><span data-stu-id="fe67f-115">To complete the signing process for a DLL, use the `–R` option of the Strong Naming tool (Sn.exe).</span></span>  
  
 <span data-ttu-id="fe67f-116">このオプションには、ターゲットが DLL ではない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="fe67f-116">This option is ignored if the target is not a DLL.</span></span>  
  
|<span data-ttu-id="fe67f-117">Visual Studio IDE で-baseaddress を設定するには</span><span class="sxs-lookup"><span data-stu-id="fe67f-117">To set -baseaddress in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="fe67f-118">1.**ソリューション エクスプローラー**でプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe67f-118">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="fe67f-119">**[プロジェクト]** メニューの **[プロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe67f-119">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="fe67f-120">2.**[コンパイル]** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe67f-120">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="fe67f-121">3.**[詳細設定]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fe67f-121">3.  Click **Advanced**.</span></span><br /><span data-ttu-id="fe67f-122">4.値を変更、 **DLL ベース アドレス:** ボックス。</span><span class="sxs-lookup"><span data-stu-id="fe67f-122">4.  Modify the value in the **DLL base address:** box.</span></span> <span data-ttu-id="fe67f-123">**注:**    **DLL ベース アドレス:** ターゲットが DLL でない限り、ボックスは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="fe67f-123">**Note:**      The **DLL base address:** box is read-only unless the target is a DLL.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fe67f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe67f-124">See also</span></span>
- [<span data-ttu-id="fe67f-125">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="fe67f-125">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="fe67f-126">-ターゲット (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fe67f-126">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="fe67f-127">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="fe67f-127">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- <span data-ttu-id="fe67f-128">[Sn.exe (厳密名ツール)](../../../framework/tools/sn-exe-strong-name-tool.md))</span><span class="sxs-lookup"><span data-stu-id="fe67f-128">[Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md))</span></span>
