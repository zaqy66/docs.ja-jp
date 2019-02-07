---
title: <paramref> - C# プログラミング ガイド
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- paramref
- <paramref>
helpviewer_keywords:
- <paramref> C# XML tag
- paramref C# XML tag
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
ms.openlocfilehash: 4fd0770bfe6c15c0e9b10239019ec265550dc372
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262836"
---
# <a name="paramref-c-programming-guide"></a>\<paramref> (C# プログラミング ガイド)
## <a name="syntax"></a>構文  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `name`  
 参照されるパラメーターの名前です。 名前は二重引用符 (" ") で囲みます。  
  
## <a name="remarks"></a>コメント  
 \<paramref> タグを使用すると、\<summary> または \<remarks> ブロックなどのコード コメント内の単語がパラメーターを参照することを示すことができます。 この単語を、太字や斜体のフォントを使うなど、何らかの独自の方法で書式設定するために XML ファイルを処理できます。  
  
 コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideDocComments#7](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/paramref_1.cs)]  
  
## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [ドキュメント コメントとして推奨されるタグ](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
