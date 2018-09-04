---
title: '#ExternalSource ディレクティブ (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '#Externalsource'
- '#ExternalSource'
- vb.ExternalSource
- Externalsource
- vb.#ExternalSource
- ExternalSource
helpviewer_keywords:
- ExternalSource directive (#ExternalSource)
- '#ExternalSource directive'
ms.assetid: 243bc6a2-34c3-4eeb-a776-9fd2bf988149
ms.openlocfilehash: dcde8507eb033d0a47d5c5d3fa36176cd63b0856
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43556319"
---
# <a name="externalsource-directive"></a>#ExternalSource ディレクティブ
ソース コードの特定の行とソース外部のテキスト間のマッピングを示します。  
  
## <a name="syntax"></a>構文  
  
```  
#ExternalSource( StringLiteral , IntLiteral )  
    [ LogicalLine+ ]  
#End ExternalSource  
```  
  
## <a name="parts"></a>指定項目  
 `StringLiteral`  
 外部ソースへのパス。  
  
 `IntLiteral`  
 外部ソースの最初の行の行番号。  
  
 `LogicalLine`  
 行を外部ソースでエラーが発生します。  
  
 `#End ExternalSource`  
 `#ExternalSource` ブロックを終了します。  
  
## <a name="remarks"></a>Remarks  
 このディレクティブは、コンパイラと、デバッガーでのみ使用されます。  
  
 ソース ファイルには、ソース ファイル内のコードの特定の行と、.aspx ファイルなど、ソースの外部のテキスト間のマッピングを示す外部ソース ディレクティブを含めることができます。 指定されたソース コードでは、コンパイル中にエラーが発生する場合は、外部ソースからのものとして識別されます。  
  
 外部ソース ディレクティブは、コンパイルに影響を与えるありませんし、入れ子にすることはできません。 内部使用のアプリケーションのみが用意されています。  
  
## <a name="see-also"></a>関連項目  
 [条件付きコンパイル](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
