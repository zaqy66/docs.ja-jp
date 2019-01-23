---
title: "'<interfacename>.<membername>' は、基本クラス '<baseclassname>' によって既に実装されています。&lt;&gt;&lt;&gt;&lt;&gt; <type> の再実装と見なされます。&lt;&gt;"
ms.date: 07/20/2015
f1_keywords:
- vbc42015
- bc42015
helpviewer_keywords:
- BC42015
ms.assetid: 658c070a-113e-4bd8-b294-12c243191160
ms.openlocfilehash: 22a3bd4e8c09c0d070e7fa5e75571a7215c3a274
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54507201"
---
# <a name="39ltinterfacenamegtltmembernamegt39-is-already-implemented-by-the-base-class-39ltbaseclassnamegt39-re-implementation-of-lttypegt-assumed"></a>'<interfacename>.<membername>' は、基本クラス '<baseclassname>' によって既に実装されています。&lt;&gt;&lt;&gt;&lt;&gt; <type> の再実装と見なされます。&lt;&gt;
プロパティ、プロシージャ、または派生クラスでイベントを使用して、`Implements`句は既に基本クラスで実装されているインターフェイス メンバーを指定します。  
  
 派生クラスでは、その基底クラスによって実装されているインターフェイス メンバーを再実装できます。 このことは、基底クラスの実装をオーバーライドすることとは異なります。 詳細については、「 [Implements](../../../visual-basic/language-reference/statements/implements-clause.md)」を参照してください。  
  
 既定では、このメッセージは警告です。 警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。  
  
 **エラー ID:** BC42015  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   インターフェイス メンバーを再実装する場合は、操作を行う必要はありません。 派生クラスのコードで使用しない限り、再実装されたメンバーにアクセスする、`MyBase`キーワードを基底クラスの実装にアクセスします。  
  
-   インターフェイス メンバーを再実装しない場合は、プロパティ、プロシージャ、またはイベント宣言から、 `Implements` 句を削除します。  
  
## <a name="see-also"></a>関連項目
- [インターフェイス](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
