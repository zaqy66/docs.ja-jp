---
title: value コンテキスト キーワード - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- value_CSharpKeyword
helpviewer_keywords:
- value keyword [C#]
ms.assetid: c99d6468-687f-4a46-89b4-a95e1b00bf6d
ms.openlocfilehash: ee80888a57e999fa44e891dd6e0d64caa698009c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612063"
---
# <a name="value-c-reference"></a><span data-ttu-id="2b747-102">value (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="2b747-102">value (C# Reference)</span></span>

<span data-ttu-id="2b747-103">コンテキスト キーワード `value` は、set アクセサーの通常のプロパティ宣言で使用します。</span><span class="sxs-lookup"><span data-stu-id="2b747-103">The contextual keyword `value` is used in the set accessor in ordinary property declarations.</span></span> <span data-ttu-id="2b747-104">これは、メソッドの入力パラメーターに似ています。</span><span class="sxs-lookup"><span data-stu-id="2b747-104">It is similar to an input parameter on a method.</span></span> <span data-ttu-id="2b747-105">`value` というキーワードは、クライアント コードでプロパティに割り当てる値を表します。</span><span class="sxs-lookup"><span data-stu-id="2b747-105">The word `value` references the value that client code is attempting to assign to the property.</span></span> <span data-ttu-id="2b747-106">次の例の `MyDerivedClass` には、`Name` というプロパティがあります。このプロパティは `value` パラメーターを使用して、バッキング フィールド `name` に新しい文字列を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2b747-106">In the following example, `MyDerivedClass` has a property called `Name` that uses the `value` parameter to assign a new string to the backing field `name`.</span></span> <span data-ttu-id="2b747-107">クライアント コードから見ると、演算は簡単な代入演算として記述されます。</span><span class="sxs-lookup"><span data-stu-id="2b747-107">From the point of view of client code, the operation is written as a simple assignment.</span></span>

[!code-csharp[csrefKeywordsModifiers#26](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#26)]

<span data-ttu-id="2b747-108">`value` の使用に関する詳細については、「[プロパティ](../../programming-guide/classes-and-structs/properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b747-108">For more information about the use of `value`, see [Properties](../../programming-guide/classes-and-structs/properties.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="2b747-109">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="2b747-109">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="2b747-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b747-110">See also</span></span>

- [<span data-ttu-id="2b747-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="2b747-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="2b747-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="2b747-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="2b747-113">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="2b747-113">C# Keywords</span></span>](index.md)