---
title: <c> - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- c
- <c>
helpviewer_keywords:
- text, marking as code [C#]
- code, marking text as [C#]
- c C# XML tag
- <c> C# XML tag
ms.assetid: aad5b16e-a29e-445e-bd0d-eea0b138d7b2
ms.openlocfilehash: 8471681f979fdd030490a5ecc306c4a4b9f624f9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55276758"
---
# <a name="c-c-programming-guide"></a>\<c> (C# プログラミング ガイド)
## <a name="syntax"></a>構文  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `text`  
 コードとして指定するテキストです。  
  
## <a name="remarks"></a>コメント  
 \<c> タグを使用すると、説明内のテキストをコードとして指定できます。 複数行をコードとして指定する場合は、[\<code>](../../../csharp/programming-guide/xmldoc/code.md) タグを使用します。  
  
 コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideDocComments#2](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/code-inline_1.cs)]  
  
## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [ドキュメント コメントとして推奨されるタグ](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
