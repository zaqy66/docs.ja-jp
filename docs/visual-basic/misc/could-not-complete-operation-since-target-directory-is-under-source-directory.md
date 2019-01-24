---
title: ターゲット ディレクトリがソース ディレクトリ内にあるため、操作を完了できませんでした
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: 253e7ff1d457827a2e1cb9f64eae4bfa971a3798
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645874"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a>ターゲット ディレクトリがソース ディレクトリ内にあるため、操作を完了できませんでした
循環操作が失敗しました。 循環操作は循環しているため、完了できません。 たとえば、オブジェクト A がオブジェクト B の継承を試行し、同様にオブジェクト B がオブジェクト A の継承を試行するような場合です。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   継承を行うときには、参照の循環がないことを確認します。  
  
## <a name="see-also"></a>関連項目
- [エラーの種類](../../visual-basic/programming-guide/language-features/error-types.md)
- [デバッグの基礎:ブレークポイント](https://msdn.microsoft.com/library/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)
