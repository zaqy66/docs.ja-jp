---
title: '&lt;param&gt; - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: fb31e1d4c39888765fe3e55674d5b6d18b9d5b65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54641019"
---
# <a name="ltparamgt-c-programming-guide"></a>&lt;param&gt; (C# プログラミング ガイド)
## <a name="syntax"></a>構文  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a>パラメーター  
 `name`  
 メソッド パラメーターの名前です。 名前は二重引用符 (" ") で囲みます。  
  
 `description`  
 パラメーターの説明です。  
  
## <a name="remarks"></a>コメント  
 \<param> タグは、メソッドのいずれか 1 つのパラメーターを説明するためにメソッドの宣言のコメントで使用する必要があります。 複数のパラメーターをドキュメント化するには、複数の \<param> タグを使用します。  
  
 \<param> タグのテキストは、IntelliSense、オブジェクト ブラウザー、コード コメント Web レポートに表示されます。  
  
 コンパイル時に [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) を指定して、ドキュメント コメントをファイルに出力します。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [ドキュメント コメントとして推奨されるタグ](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
