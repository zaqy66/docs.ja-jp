---
title: '#Const ディレクティブ (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.#Const
- '#vb.Const'
- '#Const'
helpviewer_keywords:
- '#Const directive'
- conditional compilation [Visual Basic], directives
- Const directive (#Const)
- Visual Basic compiler, compiler directives
- constants [Visual Basic], Const directive
- constants [Visual Basic], declaring
- Const statement [Visual Basic], directive (#Const)
- 'declaring constants [Visual Basic], #const directive'
ms.assetid: 707669e5-23f9-4f17-8622-a0d534429386
ms.openlocfilehash: 58d786c5e16b1e667f7c7c78b0f7857cd9711239
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43541615"
---
# <a name="const-directive"></a>#Const ディレクティブ
Visual basic の条件付きコンパイラ定数を定義します。  
  
## <a name="syntax"></a>構文  
  
```  
#Const constname = expression  
```  
  
## <a name="parts"></a>指定項目  
 `constname`  
 必須。 定義されている定数の名前。  
  
 `expression`  
 必須。 リテラルやその他の条件付きコンパイラ定数、またはすべての算術演算子または論理演算子を除く任意の組み合わせ`Is`します。  
  
## <a name="remarks"></a>Remarks  
 条件付きコンパイラ定数は、表示されるファイルにプライベートでは常にです。 使用してパブリック コンパイラ定数を作成することはできません、`#Const`ディレクティブです。 または、ユーザー インターフェイスでのみ作成できます、`/define`コンパイラ オプション。  
  
 使用できるは、条件付きコンパイラ定数とリテラルのみ`expression`します。 定義されている標準の定数を使用して`Const`エラーが発生します。 逆で定義されている定数を使用することができます、`#Const`条件付きコンパイルのみのキーワード。 定数できますもが定義されていないの値がある場合`Nothing`します。  
  
## <a name="example"></a>例  
 `#Const` ディレクティブの使用例を次に示します。  
  
 [!code-vb[VbVbalrConditionalComp#3](../../../visual-basic/language-reference/directives/codesnippet/VisualBasic/const-directive_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [/define (Visual Basic)](../../../visual-basic/reference/command-line-compiler/define.md)  
 [#If...Then...#Else ディレクティブ](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
 [Const ステートメント](../../../visual-basic/language-reference/statements/const-statement.md)  
 [条件付きコンパイル](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)  
 [If...Then...Else ステートメント](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
