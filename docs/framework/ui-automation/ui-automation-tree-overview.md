---
title: UI オートメーション ツリーの概要
ms.date: 03/30/2017
helpviewer_keywords:
- automation tree
- UI Automation, tree
ms.assetid: 03b98058-bdb3-47a0-8ff7-45e6cdf67166
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 042f3f82a88e987131145f38c1d8f5ecfa8dc487
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44508661"
---
# <a name="ui-automation-tree-overview"></a>UI オートメーション ツリーの概要
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]に関する最新情報については[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)をご覧ください。  
  
 支援技術製品とテスト スクリプトは、移動、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーに関する情報を収集、[!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)]とその要素。  
  
 内で、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーがありますが、ルート要素 (<xref:System.Windows.Automation.AutomationElement.RootElement%2A>) を表す、現在のデスクトップとその子要素は、windows アプリケーションを表します。 これらの子要素のそれぞれの構成部分を表す要素を含めることができます[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]メニュー、ボタン、ツールバー、リスト ボックスなどです。 さらに、これらの要素には、リスト項目などの要素を含めることができます。  
  
 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーが固定された構造ではなく、何千もの要素が含まれるため、その全体像を見る に表示されることはほとんどありません。 その一部は必要に応じてビルドされ、要素の追加、移動、削除に伴って変更されます。  
  
 UI オートメーション プロバイダーのサポート、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ルート (通常は、ウィンドウでホストされている) とサブツリーで構成される、フラグメント内の項目間のナビゲーションを実装することによってツリー。 ただし、プロバイダーは、コントロール間のナビゲーションには関与しません。 によって管理されて、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]コア、既定のウィンドウ プロバイダーから情報を使用します。  
  
<a name="uiautomation_tree_view"></a>   
## <a name="views-of-the-automation-tree"></a>オートメーション ツリーのビュー  
 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]をツリーのフィルターだけが含まれるビューを作成して<xref:System.Windows.Automation.AutomationElement>特定のクライアントに関連するオブジェクト。 このアプローチにより、クライアントで表示される構造をカスタマイズする[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]特定のニーズにします。  
  
 クライアントがビューをカスタマイズする方法には、スコープ設定とフィルター処理の 2 つがあります。 スコープ設定では、基本要素を起点としてビューの範囲を定義します。たとえば、アプリケーションがデスクトップの直接の子だけを検索するか、アプリケーション ウィンドウのすべての子孫を検索するかを定義できます。 フィルター処理では、ビューに含める要素の種類を定義します。  
  
 UI オートメーション プロバイダーのサポートなどの要素のプロパティを定義することでフィルター処理、<xref:System.Windows.Automation.AutomationElementIdentifiers.IsControlElementProperty>と<xref:System.Windows.Automation.AutomationElementIdentifiers.IsContentElementProperty>プロパティ。  
  
 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 次の 3 つの既定のビューを提供します。 これらのビューは、実行されるフィルター処理の種類によって定義されます。すべてのビューのスコープは、アプリケーションによって定義されます。 さらに、アプリケーションではプロパティに他のフィルターを適用して、たとえば有効にされているコントロールだけをコントロール ビューに含めることもできます。  
  
<a name="uiautomation_raw_view"></a>   
### <a name="raw-view"></a>列ビュー  
 未加工のビュー、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーは、完全なツリーの<xref:System.Windows.Automation.AutomationElement>デスクトップは、ルート オブジェクト。 未加工ビューは、アプリケーションのネイティブ プログラムによる構造に忠実に従っているため、使用できるビューの中では最も詳細なビューです。 また、ツリーの他のビューは、未加工ビューに基づいて構築されます。 このビューが、基になる依存[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]framework の未加工のビューを[!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)]よりも、別の未加工ビューをあるボタンを[!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)]ボタン。  
  
 未加工のビューを取得すると、プロパティを指定せずに要素を検索またはを使用して、<xref:System.Windows.Automation.TreeWalker.RawViewWalker>ツリーを移動します。  
  
<a name="uiautomation_control_view"></a>   
### <a name="control-view"></a>コントロール ビュー  
 コントロール ビュー、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリーを記述する支援技術製品のタスクを簡略化、[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]エンドユーザーを支援するエンド ユーザー アプリケーションの対話に密接に対応するため、[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]構造体エンドユーザーによって認識されます。  
  
 コントロール ビューは、未加工ビューのサブセットです。 すべてが含まれています[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]対話型または内のコントロールの論理構造に貢献すると、エンドユーザーが理解できるようにする、未加工ビューの項目、[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]します。 例の[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]の論理構造に影響を与える項目、 [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]、ただしではありません対話型自体がリスト ビューのヘッダー、ツールバー、メニューのおよびステータス バーなどの項目コンテナー。 レイアウトや装飾の目的のためだけに使用される非対話型項目は、コントロール ビューには表示されません。 その一例は、パネルです。パネルは、ダイアログでコントロールをレイアウトするためだけに使用され、情報はまったく含まれません。 コントロール ビューに表示される非対話型の項目は、情報を提供するグラフィックとダイアログ内の静的テキストです。 コントロール ビューに含まれる非対話型の項目がキーボード フォーカスを受け取ることはできません。  
  
 コントロールのビューを持つ要素を検索して取得した、<xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.IsControlElement%2A>プロパティに設定`true`、またはを使用して、<xref:System.Windows.Automation.TreeWalker.ControlViewWalker>ツリーを移動します。  
  
<a name="uiautomation_content_view"></a>   
### <a name="content-view"></a>コンテンツ ビュー  
 コンテンツ ビュー、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]ツリー コントロールのビューのサブセットであります。 含まれている[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]、ユーザー インターフェイスで実際の情報を伝達する項目を含む[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]を受信できる項目はキーボード フォーカスとではない、ラベルにいくつかのテキスト、[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]項目。 たとえば、ドロップダウン コンボ ボックス内の値は、エンドユーザーが使用する情報を表すため、コンテンツ ビューに表示されます。 コンテンツ ビューでは、コンボ ボックスとリスト ボックスが両方表現のコレクションとして[!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]項目または 1 つ以上のおそらく 1 つの項目を選択できます。 コンテンツ ビューの目的は、ユーザーに提示するデータ (つまりコンテンツ) を表示することなので、このビューは、どの項目が常に開かれていて、どの項目が展開または折りたたむことができるかは重要ではありません。  
  
 コンテンツのビューを取得する要素を検索することによって、<xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.IsContentElement%2A>プロパティに設定`true`、またはを使用して、<xref:System.Windows.Automation.TreeWalker.ContentViewWalker>ツリーを移動します。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Automation.AutomationElement>  
 [UI オートメーションの概要](../../../docs/framework/ui-automation/ui-automation-overview.md)
