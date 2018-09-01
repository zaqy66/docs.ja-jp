---
title: UI オートメーション TableItem コントロール パターンの実装
ms.date: 03/30/2017
helpviewer_keywords:
- control patterns, Table Item
- UI Automation, Table Item control pattern
- TableItem control pattern
ms.assetid: ac178408-1485-436f-8d3e-eee3bf80cb24
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: db94a1a4588c2f889da8adb1cb3e47e208ce1211
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43393718"
---
# <a name="implementing-the-ui-automation-tableitem-control-pattern"></a>UI オートメーション TableItem コントロール パターンの実装
> [!NOTE]
>  このドキュメントは、[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 名前空間で定義されているマネージド <xref:System.Windows.Automation> クラスを使用する .NET Framework 開発者を対象としています。 に関する最新情報については[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]を参照してください[Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746)します。  
  
 このトピックのガイドラインと規則を実装するための紹介<xref:System.Windows.Automation.Provider.ITableItemProvider>、イベントおよびプロパティに関する情報などです。 その他のリファレンスへのリンクは、概要の最後に記載します。  
  
 <xref:System.Windows.Automation.TableItemPattern>コントロール パターンが実装するコンテナーの子コントロールをサポートするために使用される<xref:System.Windows.Automation.Provider.ITableProvider>します。 個々 のセル機能へのアクセスが必要な同時実装によって提供される<xref:System.Windows.Automation.Provider.IGridItemProvider>します。 このコントロール パターンに似ています<xref:System.Windows.Automation.Provider.IGridItemProvider>実装するコントロールを除いて<xref:System.Windows.Automation.Provider.ITableItemProvider>プログラムで、個々 のセルとその行および列情報間のリレーションシップを公開する必要があります。 このコントロール パターンを実装するコントロールの例については、「 [Control Pattern Mapping for UI Automation Clients](../../../docs/framework/ui-automation/control-pattern-mapping-for-ui-automation-clients.md)」をご覧ください。  
  
<a name="Implementation_Guidelines_and_Conventions"></a>   
## <a name="implementation-guidelines-and-conventions"></a>実装のガイドラインと規則  
  
-   関連するグリッド項目の機能を参照してください。 [UI オートメーション GridItem コントロール パターンを実装する](../../../docs/framework/ui-automation/implementing-the-ui-automation-griditem-control-pattern.md)します。  
  
<a name="Required_Members_for_ITableItemProvider"></a>   
## <a name="required-members-for-itableitemprovider"></a>ITableItemProvider の必須メンバー  
  
|必須メンバー|メンバーの型|メモ|  
|---------------------|-----------------|-----------|  
|<xref:System.Windows.Automation.Provider.ITableItemProvider.GetColumnHeaderItems%2A>|メソッド|なし|  
|<xref:System.Windows.Automation.Provider.ITableItemProvider.GetRowHeaderItems%2A>|メソッド|なし|  
  
 このコントロール パターンに関連付けられるプロパティやイベントはありません。  
  
<a name="Exceptions"></a>   
## <a name="exceptions"></a>例外  
 このコントロール パターンに関連付けられた例外はありません。  
  
## <a name="see-also"></a>関連項目  
 [UI Automation コントロール パターンの概要](../../../docs/framework/ui-automation/ui-automation-control-patterns-overview.md)  
 [UI オートメーション プロバイダーでのコントロール パターンのサポート](../../../docs/framework/ui-automation/support-control-patterns-in-a-ui-automation-provider.md)  
 [クライアントの UI オートメーション コントロール パターン](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)  
 [UI オートメーション Table コントロール パターンの実装](../../../docs/framework/ui-automation/implementing-the-ui-automation-table-control-pattern.md)  
 [UI オートメーション GridItem コントロール パターンの実装](../../../docs/framework/ui-automation/implementing-the-ui-automation-griditem-control-pattern.md)  
 [UI Automation ツリーの概要](../../../docs/framework/ui-automation/ui-automation-tree-overview.md)  
 [UI オートメーションにおけるキャッシュの使用](../../../docs/framework/ui-automation/use-caching-in-ui-automation.md)
