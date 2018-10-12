---
title: '&lt;returns&gt; (C# プログラミング ガイド)'
ms.date: 07/20/2015
f1_keywords:
- returns
- <returns>
helpviewer_keywords:
- <returns> C# XML tag
- returns C# XML tag
ms.assetid: bb2d9958-62fc-47c7-9511-6311171f119f
ms.openlocfilehash: fc3254062e4412c2a0640e27ce4d188b83507eea
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44259916"
---
# <a name="ltreturnsgt-c-programming-guide"></a>&lt;returns&gt; (C# プログラミング ガイド)
## <a name="syntax"></a>構文  
  
```xml  
<returns>description</returns>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `description`  
 戻り値の説明。  
  
## <a name="remarks"></a>コメント  
 \<returns> タグは、戻り値を説明するためにメソッドの宣言のコメントで使用する必要があります。  
  
 コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideDocComments#10](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/returns_1.cs)]  
  
## <a name="see-also"></a>参照

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [ドキュメント コメントとして推奨されるタグ](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
