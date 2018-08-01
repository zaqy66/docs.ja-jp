---
title: global コンテキスト キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- global
- global_CSharpKeyword
helpviewer_keywords:
- global keyword [C#]
ms.assetid: 8932c16a-6959-42c2-86e7-2c4221ab788b
ms.openlocfilehash: 79e0184f58ffc6232038abdd3d9f852147d5732c
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404289"
---
# <a name="global-c-reference"></a>global (C# リファレンス)

[:: 演算子](../operators/namespace-alias-qualifer.md)の前に来るとき、`global` コンテキスト キーワードは、C# プログラムの既定の名前空間であるグローバル名前空間を参照し、そうでない場合は名前のないグローバル名前空間を参照します。 詳細については、「[方法: グローバル名前空間エイリアスを使用する](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)」を参照してください。

## <a name="example"></a>例

次の例では、コンテキスト キーワード `global` を利用し、グローバル名前空間でクラス `TestApp` が定義されることを指定しています。

[!code-csharp[csrefKeywordsContextual#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#13)]

## <a name="see-also"></a>関連項目

[名前空間](../../programming-guide/namespaces/index.md)