---
title: -removeintchecks
ms.date: 03/13/2018
f1_keywords:
- removeintchecks
- -removeintchecks
helpviewer_keywords:
- removeintchecks compiler option [Visual Basic]
- /removeintchecks compiler option [Visual Basic]
- -removeintchecks compiler option [Visual Basic]
ms.assetid: c1835bd5-1e38-4fba-bd2f-6984774765d4
ms.openlocfilehash: f061497083dc23fd07f61108938a4129c0af5f3a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188536"
---
# <a name="-removeintchecks"></a><span data-ttu-id="983f0-102">-removeintchecks</span><span class="sxs-lookup"><span data-stu-id="983f0-102">-removeintchecks</span></span>
<span data-ttu-id="983f0-103">オーバーフロー エラーのオンまたはオフ、整数演算のチェックをオンにします。</span><span class="sxs-lookup"><span data-stu-id="983f0-103">Turns overflow-error checking for integer operations on or off.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="983f0-104">構文</span><span class="sxs-lookup"><span data-stu-id="983f0-104">Syntax</span></span>  
  
```  
-removeintchecks[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="983f0-105">引数</span><span class="sxs-lookup"><span data-stu-id="983f0-105">Arguments</span></span>  
  
|<span data-ttu-id="983f0-106">用語</span><span class="sxs-lookup"><span data-stu-id="983f0-106">Term</span></span>|<span data-ttu-id="983f0-107">定義</span><span class="sxs-lookup"><span data-stu-id="983f0-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="983f0-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="983f0-108">`+` &#124; `-`</span></span>|<span data-ttu-id="983f0-109">任意。</span><span class="sxs-lookup"><span data-stu-id="983f0-109">Optional.</span></span> <span data-ttu-id="983f0-110">`-removeintchecks-`オプションは、すべての整数の計算でオーバーフロー エラーをチェックするコンパイラ。</span><span class="sxs-lookup"><span data-stu-id="983f0-110">The `-removeintchecks-` option causes the compiler to check all integer calculations for overflow errors.</span></span> <span data-ttu-id="983f0-111">既定値は `-removeintchecks-` です。</span><span class="sxs-lookup"><span data-stu-id="983f0-111">The default is `-removeintchecks-`.</span></span><br /><br /> <span data-ttu-id="983f0-112">指定する`-removeintchecks`または`-removeintchecks+`エラー チェックを防止しより高速の整数の計算を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="983f0-112">Specifying `-removeintchecks` or `-removeintchecks+` prevents error checking and can make integer calculations faster.</span></span> <span data-ttu-id="983f0-113">ただし、エラー チェックを行わないと、エラーを発生させず不適切な結果を格納できるデータ型の容量がオーバーフローした場合。</span><span class="sxs-lookup"><span data-stu-id="983f0-113">However, without error checking, and if data type capacities are overflowed, incorrect results may be stored without raising an error.</span></span>|  
  
|<span data-ttu-id="983f0-114">Visual Studio 統合開発環境で-removeintchecks を設定するには</span><span class="sxs-lookup"><span data-stu-id="983f0-114">To set -removeintchecks in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="983f0-115">1.**ソリューション エクスプローラー**でプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="983f0-115">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="983f0-116">**[プロジェクト]** メニューの **[プロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="983f0-116">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="983f0-117">2.**[コンパイル]** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="983f0-117">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="983f0-118">3.**[詳細設定]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="983f0-118">3.  Click the **Advanced** button.</span></span><br /><span data-ttu-id="983f0-119">4.値を変更、**整数オーバーフローのチェックを解除**ボックス。</span><span class="sxs-lookup"><span data-stu-id="983f0-119">4.  Modify the value of the **Remove integer overflow checks** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="983f0-120">例</span><span class="sxs-lookup"><span data-stu-id="983f0-120">Example</span></span>  
 <span data-ttu-id="983f0-121">次のコードのコンパイル`Test.vb`し整数オーバーフロー エラー チェックをオフにします。</span><span class="sxs-lookup"><span data-stu-id="983f0-121">The following code compiles `Test.vb` and turns off integer overflow-error checking.</span></span>  
  
```console
vbc -removeintchecks+ test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="983f0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="983f0-122">See Also</span></span>  
 [<span data-ttu-id="983f0-123">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="983f0-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="983f0-124">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="983f0-124">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
