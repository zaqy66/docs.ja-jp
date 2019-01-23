---
title: ない&#39;Main&#39;で適切なシグネチャを持つメソッドが見つかりました&#39;&lt;名&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 3398195ef9d503e47ab569ff85cb2a827c4270f1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54501491"
---
# <a name="no-accessible-39main39-method-with-an-appropriate-signature-was-found-in-39ltnamegt39"></a>ない&#39;Main&#39;で適切なシグネチャを持つメソッドが見つかりました&#39;&lt;名&gt;&#39;
コマンド ライン アプリケーションが必要、`Sub Main`定義します。 `Main` として宣言する必要があります`Public Shared`クラス、またはとして定義されている場合`Public`モジュールで定義されている場合。  
  
 **エラー ID:** BC30737  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   定義、`Public Sub Main`プロジェクト用のプロシージャです。 として宣言`Shared`クラス内で定義する場合にのみです。  
  
## <a name="see-also"></a>関連項目
- [Visual Basic プログラムの構造](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [プロシージャ](../../../visual-basic/programming-guide/language-features/procedures/index.md)
