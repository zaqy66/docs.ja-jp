---
title: '方法: チャネル ファクトリを作成し、使用して作成および管理チャネル'
ms.date: 03/30/2017
ms.assetid: 018dcc30-9f61-419e-af8e-412a85e8d282
ms.openlocfilehash: 37ba8db3084f8d90aab33a08f6b52ddaee4545f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649532"
---
# <a name="how-to-create-a-channel-factory-and-use-it-to-create-and-manage-channels"></a>方法: チャネル ファクトリを作成し、使用して作成および管理チャネル
<xref:System.ServiceModel.DuplexChannelFactory%601> クラスは、クライアントがサービス エンドポイントとの間でメッセージを送受信するために使用する、さまざまな種類の双方向チャネルを作成したり、管理したりする手段を提供します。  
  
## <a name="example"></a>例  
 次のコードは、チャネル ファクトリを作成および使用して、チャネルを作成および管理する方法を示しています。  
  
 [!code-csharp[S_CustomAuthentication#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_customauthentication/cs/instance.cs#1)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.DuplexChannelFactory%601>
