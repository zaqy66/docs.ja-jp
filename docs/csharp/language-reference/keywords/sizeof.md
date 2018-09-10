---
title: sizeof (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- sizeof_CSharpKeyword
- sizeof
helpviewer_keywords:
- sizeof keyword [C#]
ms.assetid: c548592c-677c-4f40-a4ce-e613f7529141
ms.openlocfilehash: f2507dd8528e2e66016524873ada890227a74ed8
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517039"
---
# <a name="sizeof-c-reference"></a><span data-ttu-id="30f61-102">sizeof (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="30f61-102">sizeof (C# Reference)</span></span>
<span data-ttu-id="30f61-103">アンマネージ型のサイズ (バイト単位) を取得するときに使用します。</span><span class="sxs-lookup"><span data-stu-id="30f61-103">Used to obtain the size in bytes for an unmanaged type.</span></span>

<span data-ttu-id="30f61-104">アンマネージド型には次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="30f61-104">Unmanaged types include:</span></span>

-   <span data-ttu-id="30f61-105">次の表は単純型の一覧です。</span><span class="sxs-lookup"><span data-stu-id="30f61-105">The simple types that are listed in the following table:</span></span>
  
   |<span data-ttu-id="30f61-106">正規表現</span><span class="sxs-lookup"><span data-stu-id="30f61-106">Expression</span></span>|<span data-ttu-id="30f61-107">定数値</span><span class="sxs-lookup"><span data-stu-id="30f61-107">Constant value</span></span>|  
   |----------------|--------------------|  
   |`sizeof(sbyte)`|<span data-ttu-id="30f61-108">1</span><span class="sxs-lookup"><span data-stu-id="30f61-108">1</span></span>|  
   |`sizeof(byte)`|<span data-ttu-id="30f61-109">1</span><span class="sxs-lookup"><span data-stu-id="30f61-109">1</span></span>|  
   |`sizeof(short)`|<span data-ttu-id="30f61-110">2</span><span class="sxs-lookup"><span data-stu-id="30f61-110">2</span></span>|  
   |`sizeof(ushort)`|<span data-ttu-id="30f61-111">2</span><span class="sxs-lookup"><span data-stu-id="30f61-111">2</span></span>|  
   |`sizeof(int)`|<span data-ttu-id="30f61-112">4</span><span class="sxs-lookup"><span data-stu-id="30f61-112">4</span></span>|  
   |`sizeof(uint)`|<span data-ttu-id="30f61-113">4</span><span class="sxs-lookup"><span data-stu-id="30f61-113">4</span></span>|  
   |`sizeof(long)`|<span data-ttu-id="30f61-114">8</span><span class="sxs-lookup"><span data-stu-id="30f61-114">8</span></span>|  
   |`sizeof(ulong)`|<span data-ttu-id="30f61-115">8</span><span class="sxs-lookup"><span data-stu-id="30f61-115">8</span></span>|  
   |`sizeof(char)`|<span data-ttu-id="30f61-116">2 (Unicode)</span><span class="sxs-lookup"><span data-stu-id="30f61-116">2 (Unicode)</span></span>|  
   |`sizeof(float)`|<span data-ttu-id="30f61-117">4</span><span class="sxs-lookup"><span data-stu-id="30f61-117">4</span></span>|  
   |`sizeof(double)`|<span data-ttu-id="30f61-118">8</span><span class="sxs-lookup"><span data-stu-id="30f61-118">8</span></span>|  
   |`sizeof(decimal)`|<span data-ttu-id="30f61-119">16</span><span class="sxs-lookup"><span data-stu-id="30f61-119">16</span></span>|  
   |`sizeof(bool)`|<span data-ttu-id="30f61-120">1</span><span class="sxs-lookup"><span data-stu-id="30f61-120">1</span></span>| 
  
-   <span data-ttu-id="30f61-121">列挙型。</span><span class="sxs-lookup"><span data-stu-id="30f61-121">Enum types.</span></span>
  
-   <span data-ttu-id="30f61-122">ポインター型。</span><span class="sxs-lookup"><span data-stu-id="30f61-122">Pointer types.</span></span>
  
-   <span data-ttu-id="30f61-123">参照型または構築された型である任意のインスタンス フィールドまたは自動実装インスタンス プロパティが含まれていないユーザー定義の構造体。</span><span class="sxs-lookup"><span data-stu-id="30f61-123">User-defined structs that do not contain any instance fields or auto-implemented instance properties that are reference types or constructed types.</span></span>
  
 <span data-ttu-id="30f61-124">次の例は、`int` のサイズを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="30f61-124">The following example shows how to retrieve the size of an `int`:</span></span>  
  
```csharp  
// Constant value 4:  
int intSize = sizeof(int);   
```  
  
## <a name="remarks"></a><span data-ttu-id="30f61-125">コメント</span><span class="sxs-lookup"><span data-stu-id="30f61-125">Remarks</span></span>  
 <span data-ttu-id="30f61-126">C# のバージョン 2.0 以降、`sizeof` を単純型または列挙型に適用する場合、そのコードを [unsafe](unsafe.md) コンテキストでコンパイルする必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="30f61-126">Starting with version 2.0 of C#, applying `sizeof` to simple or enum types no longer requires that code be compiled in an [unsafe](unsafe.md) context.</span></span>
  
 <span data-ttu-id="30f61-127">`sizeof` 演算子はオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="30f61-127">The `sizeof` operator cannot be overloaded.</span></span> <span data-ttu-id="30f61-128">`sizeof` 演算子により返される値の型は `int` です。</span><span class="sxs-lookup"><span data-stu-id="30f61-128">The values returned by the `sizeof` operator are of type `int`.</span></span> <span data-ttu-id="30f61-129">上記の表に、特定の単純型をオペランドとする `sizeof` 式と、代用される定数値を示します。</span><span class="sxs-lookup"><span data-stu-id="30f61-129">The previous table shows the constant values that are substituted for `sizeof` expressions that have certain simple types as operands.</span></span>  
    
 <span data-ttu-id="30f61-130">struct など、その他の型については、`sizeof` 演算子はアンセーフ コード ブロックでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="30f61-130">For all other types, including structs, the `sizeof` operator can be used only in unsafe code blocks.</span></span> <span data-ttu-id="30f61-131"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> メソッドを使用できますが、このメソッドによって返される値は常に `sizeof` によって返される値と同じとは限りません。</span><span class="sxs-lookup"><span data-stu-id="30f61-131">Although you can use the <xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> method, the value returned by this method is not always the same as the value returned by `sizeof`.</span></span> <span data-ttu-id="30f61-132"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> は、型のマーシャリング後にサイズを返します。一方、`sizeof` は、共通言語ランタイムによって割り当てられたサイズ (埋め込みを含む) を返します。</span><span class="sxs-lookup"><span data-stu-id="30f61-132"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> returns the size after the type has been marshaled, whereas `sizeof` returns the size as it has been allocated by the common language runtime, including any padding.</span></span>  
  
## <a name="example"></a><span data-ttu-id="30f61-133">例</span><span class="sxs-lookup"><span data-stu-id="30f61-133">Example</span></span>  
 [!code-csharp[csrefKeywordsOperator#11](../../../csharp/language-reference/keywords/codesnippet/CSharp/sizeof_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="30f61-134">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="30f61-134">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="30f61-135">参照</span><span class="sxs-lookup"><span data-stu-id="30f61-135">See Also</span></span>

- [<span data-ttu-id="30f61-136">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="30f61-136">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="30f61-137">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="30f61-137">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="30f61-138">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="30f61-138">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="30f61-139">演算子のキーワード</span><span class="sxs-lookup"><span data-stu-id="30f61-139">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)  
- [<span data-ttu-id="30f61-140">enum</span><span class="sxs-lookup"><span data-stu-id="30f61-140">enum</span></span>](../../../csharp/language-reference/keywords/enum.md)  
- [<span data-ttu-id="30f61-141">アンセーフ コードとポインター</span><span class="sxs-lookup"><span data-stu-id="30f61-141">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
- [<span data-ttu-id="30f61-142">構造体</span><span class="sxs-lookup"><span data-stu-id="30f61-142">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
- [<span data-ttu-id="30f61-143">定数</span><span class="sxs-lookup"><span data-stu-id="30f61-143">Constants</span></span>](../../../csharp/programming-guide/classes-and-structs/constants.md)
