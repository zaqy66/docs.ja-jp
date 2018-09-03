---
title: -fullpaths (C# コンパイラ オプション)
ms.date: 07/20/2015
f1_keywords:
- /fullpaths
helpviewer_keywords:
- /fullpaths compiler option [C#]
- absolute paths [C#]
- fullpaths compiler option [C#]
- full paths [C#]
- -fullpaths compiler option [C#]
ms.assetid: d2a5f857-cbb2-430b-879c-d648aaf0b8c4
ms.openlocfilehash: 8f23bb683067c55f5b5213065c3082b843dd7dce
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43388280"
---
# <a name="-fullpaths-c-compiler-options"></a><span data-ttu-id="f8cbe-102">-fullpaths (C# コンパイラ オプション)</span><span class="sxs-lookup"><span data-stu-id="f8cbe-102">-fullpaths (C# Compiler Options)</span></span>
<span data-ttu-id="f8cbe-103">**-fullpaths** オプションを指定すると、コンパイルのエラーや警告を一覧表示するとき、コンパイラはファイルの完全なパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8cbe-103">The **-fullpaths** option causes the compiler to specify the full path to the file when listing compilation errors and warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8cbe-104">構文</span><span class="sxs-lookup"><span data-stu-id="f8cbe-104">Syntax</span></span>  
  
```console  
-fullpaths  
```  
  
## <a name="remarks"></a><span data-ttu-id="f8cbe-105">コメント</span><span class="sxs-lookup"><span data-stu-id="f8cbe-105">Remarks</span></span>  
 <span data-ttu-id="f8cbe-106">既定では、コンパイルの結果として発生したエラーや警告には、エラーが見つかったファイルの名前が指定されます。</span><span class="sxs-lookup"><span data-stu-id="f8cbe-106">By default, errors and warnings that result from compilation specify the name of the file in which an error was found.</span></span> <span data-ttu-id="f8cbe-107">**-fullpaths** オプションを指定すると、コンパイラはファイルの完全なパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8cbe-107">The **-fullpaths** option causes the compiler to specify the full path to the file.</span></span>  
  
 <span data-ttu-id="f8cbe-108">このコンパイラ オプションは Visual Studio では使用できず、プログラムで変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="f8cbe-108">This compiler option is unavailable in Visual Studio and cannot be changed programmatically.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8cbe-109">参照</span><span class="sxs-lookup"><span data-stu-id="f8cbe-109">See Also</span></span>  

- [<span data-ttu-id="f8cbe-110">C# コンパイラ オプション</span><span class="sxs-lookup"><span data-stu-id="f8cbe-110">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
