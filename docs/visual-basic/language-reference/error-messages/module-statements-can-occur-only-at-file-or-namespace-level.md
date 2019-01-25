---
title: '&#39;モジュール&#39;ステートメントはファイルまたは名前空間レベルでのみ発生します'
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: bdbf8df5942e9df4b9696aeea4e3492121efe21a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54746313"
---
# <a name="39module39-statements-can-occur-only-at-file-or-namespace-level"></a>&#39;モジュール&#39;ステートメントはファイルまたは名前空間レベルでのみ発生します
`Module` ステートメントは、ソース ファイルの上部に表示する必要がありますの直後に`Option`と`Imports`ステートメント、グローバル属性および名前空間の宣言が、その他のすべての宣言の前にします。  
  
 **エラー ID:** BC30617  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   `Module` ステートメントを名前空間の宣言またはソース ファイルの先頭に移動します。  
  
## <a name="see-also"></a>関連項目
- [Module ステートメント](../../../visual-basic/language-reference/statements/module-statement.md)
