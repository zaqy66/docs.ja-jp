---
title: 型 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- types [C#]
- data types [C#], type system
ms.assetid: 16b984df-f417-4e02-b1e6-4589d4a614ea
ms.openlocfilehash: 41406e74a207f289968017f1f9869b23b165c34b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236662"
---
# <a name="types-c-reference"></a><span data-ttu-id="8ed40-102">型 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="8ed40-102">Types (C# Reference)</span></span>

<span data-ttu-id="8ed40-103">C# の型指定システムには次のカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="8ed40-103">The C# typing system contains the following categories:</span></span>

- [<span data-ttu-id="8ed40-104">値型</span><span class="sxs-lookup"><span data-stu-id="8ed40-104">Value types</span></span>](value-types.md)

- [<span data-ttu-id="8ed40-105">参照型</span><span class="sxs-lookup"><span data-stu-id="8ed40-105">Reference types</span></span>](reference-types.md)

- [<span data-ttu-id="8ed40-106">ポインター型</span><span class="sxs-lookup"><span data-stu-id="8ed40-106">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)

 <span data-ttu-id="8ed40-107">値型の変数はデータを格納し、参照型の変数は実データへの参照を格納します。</span><span class="sxs-lookup"><span data-stu-id="8ed40-107">Variables that are value types store data, and those that are reference types store references to the actual data.</span></span> <span data-ttu-id="8ed40-108">参照型のインスタンスはオブジェクトとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8ed40-108">Instances of reference types are also referred to as objects.</span></span> <span data-ttu-id="8ed40-109">ポインター型は [unsafe](unsafe.md) モードでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ed40-109">Pointer types can be used only in [unsafe](unsafe.md) mode.</span></span>

 <span data-ttu-id="8ed40-110">[ボックス化とボックス化解除](../../../csharp/programming-guide/types/boxing-and-unboxing.md)を使用して、値型を参照型に変換でき、参照型から値型に変換して戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="8ed40-110">It's possible to convert a value type to a reference type, and back again to a value type, by using [boxing and unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span></span> <span data-ttu-id="8ed40-111">ボックス化された値型の場合を除き、参照型を値型に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="8ed40-111">With the exception of a boxed value type, you cannot convert a reference type to a value type.</span></span>

 <span data-ttu-id="8ed40-112">このセクションでは [void](void.md) についても説明します。</span><span class="sxs-lookup"><span data-stu-id="8ed40-112">This section also introduces [void](void.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8ed40-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ed40-113">See also</span></span>

- [<span data-ttu-id="8ed40-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="8ed40-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="8ed40-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="8ed40-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="8ed40-116">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="8ed40-116">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="8ed40-117">型のリファレンス表</span><span class="sxs-lookup"><span data-stu-id="8ed40-117">Reference Tables for Types</span></span>](reference-tables-for-types.md)
- [<span data-ttu-id="8ed40-118">キャストと型変換</span><span class="sxs-lookup"><span data-stu-id="8ed40-118">Casting and Type Conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
- [<span data-ttu-id="8ed40-119">型</span><span class="sxs-lookup"><span data-stu-id="8ed40-119">Types</span></span>](../../programming-guide/types/index.md)
