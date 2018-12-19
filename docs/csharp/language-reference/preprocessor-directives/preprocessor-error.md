---
title: '#error - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#error'
helpviewer_keywords:
- '#error directive [C#]'
ms.assetid: f2a7f3af-4cf9-4111-b369-70204d24b26b
ms.openlocfilehash: b335dfeed23d43938c66f0753590af55ac99b12a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235594"
---
# <a name="error-c-reference"></a><span data-ttu-id="40882-102">#error (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="40882-102">#error (C# Reference)</span></span>
<span data-ttu-id="40882-103">`#error` を使用すると、コード内の特定の場所からユーザー定義の [CS1029](../compiler-messages/cs1029.md) エラーを生成できます。</span><span class="sxs-lookup"><span data-stu-id="40882-103">`#error` lets you generate a [CS1029](../compiler-messages/cs1029.md) user-defined error from a specific location in your code.</span></span> <span data-ttu-id="40882-104">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="40882-104">For example:</span></span>  
  
```csharp
#error Deprecated code in this method.  
```  
  
## <a name="remarks"></a><span data-ttu-id="40882-105">コメント</span><span class="sxs-lookup"><span data-stu-id="40882-105">Remarks</span></span>  
 <span data-ttu-id="40882-106">`#error` は条件付きディレクティブ内で一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="40882-106">A common use of `#error` is in a conditional directive.</span></span>  
  
 <span data-ttu-id="40882-107">[#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md) を使用してユーザー定義の警告を生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="40882-107">It is also possible to generate a user-defined warning with [#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="40882-108">例</span><span class="sxs-lookup"><span data-stu-id="40882-108">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="40882-109">参照</span><span class="sxs-lookup"><span data-stu-id="40882-109">See Also</span></span>

- [<span data-ttu-id="40882-110">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="40882-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="40882-111">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="40882-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="40882-112">C# プリプロセッサ ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="40882-112">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
