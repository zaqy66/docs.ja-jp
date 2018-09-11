---
title: '#else (C# リファレンス)'
ms.date: 07/20/2015
f1_keywords:
- '#else'
helpviewer_keywords:
- '#else directive [C#]'
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
ms.openlocfilehash: 000cbaac4458a104214e3197442a21dcb4740a37
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43530225"
---
# <a name="else-c-reference"></a>#else (C# リファレンス)
`#else` を使用すると、複合条件付きディレクティブを作成できるため、先行する [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) または (省略可能な) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) ディレクティブの式がいずれも `true` に評価されない場合は、コンパイラが `#else` と以降の `#endif` の間のすべてのコードを評価します。  
  
## <a name="remarks"></a>コメント  
 [#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) が、`#else` の後の次のプリプロセッサ ディレクティブになる必要があります。 `#else` の使用例については、「[#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)」を参照してください。  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# プリプロセッサ ディレクティブ](../../../csharp/language-reference/preprocessor-directives/index.md)
