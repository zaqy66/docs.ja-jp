---
title: 演算子キーワード - C# リファレンス
ms.custom: seodec18
ms.date: 12/10/2018
helpviewer_keywords:
- keywords [C#], operators
- operators [C#], keywords
ms.assetid: f745c81f-f8d8-4673-86a1-0f3a85cc63c3
ms.openlocfilehash: e03e1c930b452cf5e4f2c4bb1d06d5363f20c991
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243610"
---
# <a name="operator-keywords-c-reference"></a><span data-ttu-id="7a52b-102">演算子キーワード (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="7a52b-102">Operator Keywords (C# Reference)</span></span>

<span data-ttu-id="7a52b-103">オブジェクトの作成、オブジェクトのランタイム型のチェック、型のサイズの取得といった、さまざまなアクションを実行するために使用します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-103">Used to perform miscellaneous actions such as creating objects, checking the run-time type of an object, obtaining the size of a type, and other actions.</span></span> <span data-ttu-id="7a52b-104">このセクションでは、次のキーワードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-104">This section introduces the following keywords:</span></span>

- <span data-ttu-id="7a52b-105">[as](as.md) オブジェクトを互換性のある型に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-105">[as](as.md) Converts an object to a compatible type.</span></span>

- <span data-ttu-id="7a52b-106">[await](await.md) 待機中のタスクが完了するまで[非同期](async.md)メソッドを中断します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-106">[await](await.md) Suspends an [async](async.md) method until an awaited task is completed.</span></span>

- <span data-ttu-id="7a52b-107">[is](is.md) オブジェクトのランタイム型をチェックするか、(C# 7.0 以降では) パターンとの比較によって式をテストします。</span><span class="sxs-lookup"><span data-stu-id="7a52b-107">[is](is.md) Checks the run-time type of an object, or (starting with C# 7.0) tests an expression against a pattern.</span></span>

- [<span data-ttu-id="7a52b-108">new</span><span class="sxs-lookup"><span data-stu-id="7a52b-108">new</span></span>](new.md)

  - <span data-ttu-id="7a52b-109">[new 演算子](new-operator.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-109">[new Operator](new-operator.md) Creates objects.</span></span>

  - <span data-ttu-id="7a52b-110">[new 修飾子](new-modifier.md) 継承されたメンバーを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="7a52b-110">[new Modifier](new-modifier.md) Hides an inherited member.</span></span>

  - <span data-ttu-id="7a52b-111">[new 制約](new-constraint.md) 型パラメーターを修飾します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-111">[new Constraint](new-constraint.md) Qualifies a type parameter.</span></span>

- <span data-ttu-id="7a52b-112">[nameof](nameof.md) 変数、型、またはメンバーの単純な (修飾されていない) 文字列名を取得します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-112">[nameof](nameof.md) Obtains the simple (unqualified) string name of a variable, type, or member.</span></span>

- <span data-ttu-id="7a52b-113">[sizeof](sizeof.md) アンマネージド型のサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-113">[sizeof](sizeof.md) Obtains the size of an unmanaged type.</span></span>  

- <span data-ttu-id="7a52b-114">[typeof](typeof.md) 型の <xref:System.Type?displayProperty=nameWithType> オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-114">[typeof](typeof.md) Obtains the <xref:System.Type?displayProperty=nameWithType> object for a type.</span></span>  

- [<span data-ttu-id="7a52b-115">true</span><span class="sxs-lookup"><span data-stu-id="7a52b-115">true</span></span>](true.md)  

  - <span data-ttu-id="7a52b-116">[true 演算子](true-false-operators.md) オペランドが確実に true であることを示す[ブール](bool.md)値 `true` を返します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-116">[true Operator](true-false-operators.md) Returns the [bool](bool.md) value `true` to indicate that the operand is definitely true.</span></span>

  - <span data-ttu-id="7a52b-117">[true リテラル](true-literal.md) [ブール](bool.md)値 `true` を表します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-117">[true Literal](true-literal.md) Represents the [bool](bool.md) value `true`.</span></span>

- [<span data-ttu-id="7a52b-118">false</span><span class="sxs-lookup"><span data-stu-id="7a52b-118">false</span></span>](false.md)  

  - <span data-ttu-id="7a52b-119">[false 演算子](true-false-operators.md) オペランドが確実に false であることを示す[ブール](bool.md)値 `true` を返します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-119">[false Operator](true-false-operators.md) Returns the [bool](bool.md) value `true` to indicate that the operand is definitely false.</span></span>

  - <span data-ttu-id="7a52b-120">[false リテラル](false-literal.md) [ブール](bool.md)値 `false` を表します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-120">[false Literal](false-literal.md) Represents the [bool](bool.md) value `false`.</span></span>

- <span data-ttu-id="7a52b-121">[stackalloc](stackalloc.md) スタックにメモリ ブロックを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a52b-121">[stackalloc](stackalloc.md) Allocates a block of memory on the stack.</span></span>  

<span data-ttu-id="7a52b-122">演算子およびステートメントとして使用できる次のキーワードは、「[ステートメント](statement-keywords.md)」セクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-122">The following keywords, which can be used as operators and as statements, are covered in the [Statements](statement-keywords.md) section:</span></span>

- <span data-ttu-id="7a52b-123">[checked](checked.md) checked コンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-123">[checked](checked.md) Specifies checked context.</span></span>  

- <span data-ttu-id="7a52b-124">[unchecked](unchecked.md) unchecked コンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7a52b-124">[unchecked](unchecked.md) Specifies unchecked context.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a52b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a52b-125">See also</span></span>

- [<span data-ttu-id="7a52b-126">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="7a52b-126">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7a52b-127">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="7a52b-127">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7a52b-128">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="7a52b-128">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="7a52b-129">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="7a52b-129">C# Operators</span></span>](../operators/index.md)
