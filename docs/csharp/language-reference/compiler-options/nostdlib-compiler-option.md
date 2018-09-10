---
title: -nostdlib (C# コンパイラ オプション)
ms.date: 07/20/2015
f1_keywords:
- /nostdlib
helpviewer_keywords:
- nostdlib compiler option [C#]
- -nostdlib compiler option [C#]
- /nostdlib compiler option [C#]
ms.assetid: ec197989-fa49-4725-a455-e06b551eb65f
ms.openlocfilehash: 70007c74efe9a41bdfc15e8fa7daf3c8fc0221ed
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43506696"
---
# <a name="-nostdlib-c-compiler-options"></a><span data-ttu-id="13aac-102">-nostdlib (C# コンパイラ オプション)</span><span class="sxs-lookup"><span data-stu-id="13aac-102">-nostdlib (C# Compiler Options)</span></span>

<span data-ttu-id="13aac-103">**-nostdlib** は、System 名前空間の全体を定義する mscorlib.dll がインポートされないようにします。</span><span class="sxs-lookup"><span data-stu-id="13aac-103">**-nostdlib** prevents the import of mscorlib.dll, which defines the entire System namespace.</span></span>

## <a name="syntax"></a><span data-ttu-id="13aac-104">構文</span><span class="sxs-lookup"><span data-stu-id="13aac-104">Syntax</span></span>

```console
-nostdlib[+ | -]
```

## <a name="remarks"></a><span data-ttu-id="13aac-105">コメント</span><span class="sxs-lookup"><span data-stu-id="13aac-105">Remarks</span></span>

<span data-ttu-id="13aac-106">独自の System 名前空間およびオブジェクトを定義または作成する場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="13aac-106">Use this option if you want to define or create your own System namespace and objects.</span></span>

<span data-ttu-id="13aac-107">**/nostdlib** を指定しない場合、(**-nostdlib-** を指定したことと同じで) mscorlib.dll がプログラムにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="13aac-107">If you do not specify **-nostdlib**, mscorlib.dll is imported into your program (same as specifying **-nostdlib-**).</span></span> <span data-ttu-id="13aac-108">**-nostdlib** を指定することは、**-nostdlib+** を指定することと同じです。</span><span class="sxs-lookup"><span data-stu-id="13aac-108">Specifying **-nostdlib** is the same as specifying **-nostdlib+**.</span></span>

### <a name="to-set-this-compiler-option-in-visual-studio"></a><span data-ttu-id="13aac-109">このコンパイラ オプションを Visual Studio で使用するには</span><span class="sxs-lookup"><span data-stu-id="13aac-109">To set this compiler option in Visual Studio</span></span>

> [!NOTE]
> <span data-ttu-id="13aac-110">次の手順は、Visual Studio 2015 (および以前のバージョン) のみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="13aac-110">The following instructions apply to Visual Studio 2015 (and earlier versions) only.</span></span> <span data-ttu-id="13aac-111">**Do not reference mscorlib.dll** ビルド プロパティは、Visual Studio 2017 には存在しません。</span><span class="sxs-lookup"><span data-stu-id="13aac-111">The **Do not reference mscorlib.dll** build property doesn't exist in Visual Studio 2017.</span></span>

1. <span data-ttu-id="13aac-112">プロジェクトの **[プロパティ]** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="13aac-112">Open the **Properties** page for the project.</span></span>

2. <span data-ttu-id="13aac-113">**[ビルド]** プロパティ ページをクリックします。</span><span class="sxs-lookup"><span data-stu-id="13aac-113">Click the **Build** properties page.</span></span>

3. <span data-ttu-id="13aac-114">**[詳細設定]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="13aac-114">Click the **Advanced** button.</span></span>

4. <span data-ttu-id="13aac-115">**[mscorlib.dll を参照しない]** プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="13aac-115">Modify the **Do not reference mscorlib.dll** property.</span></span>

### <a name="to-set-this-compiler-option-programmatically"></a><span data-ttu-id="13aac-116">このコンパイラ オプションをコードから設定するには</span><span class="sxs-lookup"><span data-stu-id="13aac-116">To set this compiler option programmatically</span></span>

<span data-ttu-id="13aac-117">このコンパイラ オプションをプログラムで設定する方法については、「 <xref:VSLangProj80.CSharpProjectConfigurationProperties3.NoStdLib%2A>」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="13aac-117">For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.NoStdLib%2A>.</span></span>

## <a name="see-also"></a><span data-ttu-id="13aac-118">参照</span><span class="sxs-lookup"><span data-stu-id="13aac-118">See Also</span></span>

- [<span data-ttu-id="13aac-119">C# コンパイラ オプション</span><span class="sxs-lookup"><span data-stu-id="13aac-119">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
