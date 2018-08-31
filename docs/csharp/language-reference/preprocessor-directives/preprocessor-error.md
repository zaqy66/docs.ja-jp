---
title: '#error (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '#error'
helpviewer_keywords:
- '#error directive [C#]'
ms.assetid: f2a7f3af-4cf9-4111-b369-70204d24b26b
ms.openlocfilehash: ed43c1f85142ec6c54e44db5e3b0b7de3ef36bb8
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935295"
---
# <a name="error-c-reference"></a><span data-ttu-id="b7c30-102">#error (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b7c30-102">#error (C# Reference)</span></span>
<span data-ttu-id="b7c30-103">`#error` を使用すると、コード内の特定の場所からユーザー定義の [CS1029](../compiler-messages/cs1029.md) エラーを生成できます。</span><span class="sxs-lookup"><span data-stu-id="b7c30-103">`#error` lets you generate a [CS1029](../compiler-messages/cs1029.md) user-defined error from a specific location in your code.</span></span> <span data-ttu-id="b7c30-104">例:</span><span class="sxs-lookup"><span data-stu-id="b7c30-104">For example:</span></span>  
  
```csharp
#error Deprecated code in this method.  
```  
  
## <a name="remarks"></a><span data-ttu-id="b7c30-105">コメント</span><span class="sxs-lookup"><span data-stu-id="b7c30-105">Remarks</span></span>  
 <span data-ttu-id="b7c30-106">`#error` は条件付きディレクティブ内で一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7c30-106">A common use of `#error` is in a conditional directive.</span></span>  
  
 <span data-ttu-id="b7c30-107">[#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md) を使用してユーザー定義の警告を生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b7c30-107">It is also possible to generate a user-defined warning with [#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7c30-108">例</span><span class="sxs-lookup"><span data-stu-id="b7c30-108">Example</span></span>  
  
```csharp
// preprocessor_error.cs  
// CS1029 expected  
#define DEBUG  
class MainClass   
{  
    static void Main()   
    {  
#if DEBUG  
#error DEBUG is defined  
#endif  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="b7c30-109">参照</span><span class="sxs-lookup"><span data-stu-id="b7c30-109">See Also</span></span>

- [<span data-ttu-id="b7c30-110">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b7c30-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b7c30-111">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="b7c30-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b7c30-112">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="b7c30-112">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
