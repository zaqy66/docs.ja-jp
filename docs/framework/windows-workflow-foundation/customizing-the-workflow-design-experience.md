---
title: ワークフロー デザイン操作のカスタマイズ
ms.date: 03/30/2017
helpviewer_keywords:
- extending [WF], Workflow Designer
ms.assetid: 98135077-0f5d-4d16-9337-01094e843537
ms.openlocfilehash: ed4ccb45e4470eb03cec856e865d4b50220816e3
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48777540"
---
# <a name="customizing-the-workflow-design-experience"></a>ワークフロー デザイン操作のカスタマイズ

[!INCLUDE[wfd1](../../../includes/wfd1-md.md)] では、カスタム アクティビティを設計するシナリオや [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)]を再ホストするシナリオが大幅に簡略化されました。 開発も配置も簡単になり、柔軟性も向上しました。 キーのインフラストラクチャの変更は、新しいアクティビティ デザイナー プログラミング モデルで Windows Presentation Foundation (WPF) とが構築されています。 そのため、アクティビティ デザイナーを宣言によって定義することや、他のアプリケーションに[!INCLUDE[wfd2](../../../includes/wfd2-md.md)]を再ホストすることが比較的簡単にできます。 再ホストするときに、カスタム式エディターを開発して、IntelliSense や簡略化された式ドメインをサポートできます。 Windows Communication Foundation (WCF) との統合は、ワークフロー サービスの使用よりシームレスになっています。 カスタム アクティビティ デザイナーおよびモデル アイテム ツリーを使用して、再ホストされたワークフロー デザイナーのデザイン時の操作を拡張できます。

## <a name="in-this-section"></a>このセクションの内容

 [カスタム アクティビティ デザイナーおよびテンプレートの使用](../../../docs/framework/windows-workflow-foundation/using-custom-activity-designers-and-templates.md)

 新しいカスタム アクティビティ デザイナーおよびテンプレートを作成する方法について説明します。

 [ワークフロー デザイナーのホスト変更](../../../docs/framework/windows-workflow-foundation/rehosting-the-workflow-designer.md)

 再ホストする方法について説明します、[!INCLUDE[wfd1](../../../includes/wfd1-md.md)]検証エラーを表示する方法と Visual Studio の外部でします。

 [カスタム式エディターの使用](../../../docs/framework/windows-workflow-foundation/using-a-custom-expression-editor.md)

 Visual Studio 2010 の外部で再ホストされたワークフロー デザイナーで使用するカスタム式エディターを実装する方法について説明します。

## <a name="reference"></a>参照

<xref:System.Activities.Presentation.ActivityDesigner>

## <a name="see-also"></a>関連項目

- [Windows Workflow Foundation の拡張](../../../docs/framework/windows-workflow-foundation/extend.md)
- [デザイナー](../../../docs/framework/windows-workflow-foundation/samples/designer.md)
- [カスタム アクティビティ デザイナー](../../../docs/framework/windows-workflow-foundation/samples/custom-activity-designers.md)
- [デザイナーのホスト変更](../../../docs/framework/windows-workflow-foundation/samples/designer-rehosting.md)