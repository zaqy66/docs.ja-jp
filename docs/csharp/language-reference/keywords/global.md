---
title: global コンテキスト キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- global
- global_CSharpKeyword
helpviewer_keywords:
- global keyword [C#]
ms.assetid: 8932c16a-6959-42c2-86e7-2c4221ab788b
ms.openlocfilehash: 837245e31a9a795aa2f13cfc6c33fefb6402801d
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45664476"
---
# <a name="global-c-reference"></a><span data-ttu-id="56e79-102">global (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="56e79-102">global (C# Reference)</span></span>

<span data-ttu-id="56e79-103">[:: 演算子](../operators/namespace-alias-qualifer.md)の前に来るとき、`global` コンテキスト キーワードは、C# プログラムの既定の名前空間であるグローバル名前空間を参照し、そうでない場合はグローバル名前空間は付加されません。</span><span class="sxs-lookup"><span data-stu-id="56e79-103">The `global` contextual keyword, when it comes before the [:: operator](../operators/namespace-alias-qualifer.md), refers to the global namespace, which is the default namespace for any C# program and is otherwise unnamed.</span></span> <span data-ttu-id="56e79-104">詳細については、「[方法: グローバル名前空間エイリアスを使用する](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56e79-104">For more information, see [How to: Use the Global Namespace Alias](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md).</span></span>

## <a name="example"></a><span data-ttu-id="56e79-105">例</span><span class="sxs-lookup"><span data-stu-id="56e79-105">Example</span></span>

<span data-ttu-id="56e79-106">次の例では、コンテキスト キーワード `global` を利用し、グローバル名前空間でクラス `TestApp` が定義されることを指定しています。</span><span class="sxs-lookup"><span data-stu-id="56e79-106">The following example shows how to use the `global` contextual keyword to specify that the class `TestApp` is defined in the global namespace:</span></span>

[!code-csharp[csrefKeywordsContextual#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#13)]

## <a name="see-also"></a><span data-ttu-id="56e79-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="56e79-107">See also</span></span>

- [<span data-ttu-id="56e79-108">名前空間</span><span class="sxs-lookup"><span data-stu-id="56e79-108">Namespaces</span></span>](../../programming-guide/namespaces/index.md)