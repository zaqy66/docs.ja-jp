---
title: ワークフロー ソリューションでのサービス参照の追加
ms.date: 03/30/2017
ms.assetid: 83574cf3-9803-49bc-837f-432936dc9c76
ms.openlocfilehash: f9bbe017b44563ae92c20c1f7b8c9a374456abad
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47197319"
---
# <a name="adding-a-service-reference-in-a-workflow-solution"></a>ワークフロー ソリューションでのサービス参照の追加

ワークフロー アプリケーションでのサービス参照の追加は、通常の WCF アプリケーションとは動作が少し異なります。 選択すると**追加 > サービス参照の**とサービスの URL を指定、メタデータをダウンロードおよびカスタム アクティビティが生成されることが WCF サービスまたはへの参照を追加した WCF ワークフロー サービスを呼び出すことができます。 サービス参照を追加した後、生成されたアクティビティがビルドされるように、ソリューションを再ビルドします。 これにより、アクティビティがワークフロー デザイナー ツールボックスに表示されます。 ただし、この方法が機能するのはワークフロー ソリューション内でサービス参照を追加する場合だけであることに注意してください。 次の web キャストは、その他の種類のプロジェクトでサービス参照を追加する方法を示します: [Web プロジェクトでのワークフローから WCF サービスを呼び出す](https://go.microsoft.com/fwlink/?LinkId=207725)します。

同じ操作名が含まれるサービスへのサービス参照を複数追加すると、問題が発生します。 生成されたアクティビティは最初のサービス操作しか呼び出しません。 この問題を回避するには、サービス操作を別々の名前に変更するか、生成された各アクティビティ内でエンドポイント構成名を変更します。

## <a name="see-also"></a>関連項目

- [ワークフロー サービス](../../../../docs/framework/wcf/feature-details/workflow-services.md)
- [Web プロジェクトでのワークフローから WCF サービスの呼び出し](https://go.microsoft.com/fwlink/?LinkId=207725)
