---
title: 型 (C# リファレンス)
ms.date: 07/20/2015
helpviewer_keywords:
- types [C#]
- data types [C#], type system
ms.assetid: 16b984df-f417-4e02-b1e6-4589d4a614ea
ms.openlocfilehash: c5c29f5d9a1a4e25e2d5f8816a0df31fa9a91fb1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43463313"
---
# <a name="types-c-reference"></a><span data-ttu-id="af35a-102">型 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="af35a-102">Types (C# Reference)</span></span>
<span data-ttu-id="af35a-103">C# の型指定システムには次のカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="af35a-103">The C# typing system contains the following categories:</span></span>  
  
-   [<span data-ttu-id="af35a-104">値型</span><span class="sxs-lookup"><span data-stu-id="af35a-104">Value types</span></span>](../../../csharp/language-reference/keywords/value-types.md)  
  
-   [<span data-ttu-id="af35a-105">参照型</span><span class="sxs-lookup"><span data-stu-id="af35a-105">Reference types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
  
-   [<span data-ttu-id="af35a-106">ポインター型</span><span class="sxs-lookup"><span data-stu-id="af35a-106">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
  
 <span data-ttu-id="af35a-107">値型の変数はデータを格納し、参照型の変数は実データへの参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="af35a-107">Variables that are value types store data, and those that are reference types store references to the actual data.</span></span> <span data-ttu-id="af35a-108">参照型はオブジェクトとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="af35a-108">Reference types are also referred to as objects.</span></span> <span data-ttu-id="af35a-109">ポインター型は [unsafe](../../../csharp/language-reference/keywords/unsafe.md) モードでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="af35a-109">Pointer types can be used only in [unsafe](../../../csharp/language-reference/keywords/unsafe.md) mode.</span></span>  
  
 <span data-ttu-id="af35a-110">[ボックス化とボックス化解除](../../../csharp/programming-guide/types/boxing-and-unboxing.md)を使用して、値型を参照型に変換でき、参照型から値型に変換して戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="af35a-110">It is possible to convert a value type to a reference type, and back again to a value type, by using [boxing and unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span></span> <span data-ttu-id="af35a-111">ボックス化された値型の場合を除き、参照型を値型に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="af35a-111">With the exception of a boxed value type, you cannot convert a reference type to a value type.</span></span>  
  
 <span data-ttu-id="af35a-112">このセクションでは [void](../../../csharp/language-reference/keywords/void.md) についても説明します。</span><span class="sxs-lookup"><span data-stu-id="af35a-112">This section also introduces [void](../../../csharp/language-reference/keywords/void.md).</span></span>  
  
 <span data-ttu-id="af35a-113">値型は null 許容型でもあります。つまり、値がない状態を追加で格納することができます。</span><span class="sxs-lookup"><span data-stu-id="af35a-113">Value types are also nullable, which means they can store an additional non-value state.</span></span> <span data-ttu-id="af35a-114">詳細については、「[Null 許容型](../../../csharp/programming-guide/nullable-types/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="af35a-114">For more information, see [Nullable Types](../../../csharp/programming-guide/nullable-types/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af35a-115">参照</span><span class="sxs-lookup"><span data-stu-id="af35a-115">See Also</span></span>

- [<span data-ttu-id="af35a-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="af35a-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="af35a-117">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="af35a-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="af35a-118">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="af35a-118">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="af35a-119">型のリファレンス表</span><span class="sxs-lookup"><span data-stu-id="af35a-119">Reference Tables for Types</span></span>](../../../csharp/language-reference/keywords/reference-tables-for-types.md)  
- [<span data-ttu-id="af35a-120">キャストと型変換</span><span class="sxs-lookup"><span data-stu-id="af35a-120">Casting and Type Conversions</span></span>](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
- [<span data-ttu-id="af35a-121">型</span><span class="sxs-lookup"><span data-stu-id="af35a-121">Types</span></span>](../../../csharp/programming-guide/types/index.md)
