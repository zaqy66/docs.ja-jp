---
title: GUID '<attribute>' の形式が正しくないため、'<number>' を適用できません。
ms.date: 07/20/2015
f1_keywords:
- vbc32500
- bc32500
helpviewer_keywords:
- BC32500
ms.assetid: 6fa34c55-368e-4d7d-b488-07a3fffe045f
ms.openlocfilehash: 1e92c77e6138bbd546d9b837e095e41d5dfaf30c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279865"
---
# <a name="attribute-cannot-be-applied-because-the-format-of-the-guid-number-is-not-correct"></a>'\<属性 >' 適用できません GUID の形式'\<数 >' が正しくありません。
A`COMClassAttribute`属性ブロックを GUID の適切な形式に準拠しないグローバル一意識別子 (GUID) を指定します。 `COMClassAttribute` クラス、インターフェイス、および作成イベントを一意に識別するのに Guid を使用します。  
  
 GUID は、16 バイトで構成されます。前半の 8 バイトは数値、後半の 8 バイトはバイナリです。 Uuidgen.exe などの Microsoft ユーティリティによって生成され、領域と時間で一意であることが保証されます。  
  
 **エラー ID:** BC32500  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  適切な GUID または COM オブジェクトを識別するために必要な Guid を決定します。  
  
2.  `COMClassAttribute` 属性ブロックに表示される GUID 文字列が正しくコピーされていることを確認します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Guid>
- [属性の概要](../../../visual-basic/programming-guide/concepts/attributes/index.md)

