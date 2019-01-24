---
title: '方法: COM + 統合アプリケーションをデプロイします。'
ms.date: 03/30/2017
ms.assetid: 2e5a0510-db3c-4988-a09c-696285836650
ms.openlocfilehash: 0dcaa7d12c7e35170dee155612f824ed22ab8b2f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672800"
---
# <a name="how-to-deploy-a-com-integration-application"></a>方法: COM + 統合アプリケーションをデプロイします。
COM+ 統合アプリケーションを作成した後、これを別のコンピューターに展開する必要が生じる場合があります。 ここでは、COM+ 統合アプリケーションをコンピューター間で移動する方法を説明します。  
  
### <a name="moving-a-com-hosted-integration-app"></a>COM+ ホスト統合アプリケーションの移動  
  
1.  WCF が両方のコンピューターにインストールされていることを確認します。  
  
2.  コンピューター A からアプリケーションをエクスポートします。  
  
3.  コンピューター B にアプリケーションをインポートします。  
  
4.  アプリケーション ルート ディレクトリを設定します。 通常これは %PROGRAMFILES%/ComPlus Applications/{AppGUID} になります。  
  
5.  コンピューター A のアプリケーション ルート ディレクトリにある Application.config ファイルおよび Application.manifest ファイルを、コンピューター B のアプリケーション ルート ディレクトリにコピーします。  
  
6.  コンピューター B の Application.config ファイルのサービス エンドポイント アドレスを編集して、コンピューター B が識別されるようにします。 たとえば、`http://machineA/MyService` を `http://machineB/MyService` に変更します。  
  
### <a name="moving-a-web-hosted-integration-application"></a>Web ホスト統合アプリケーションの移動  
  
1.  WCF が両方のコンピューターにインストールされていることを確認します。  
  
2.  コンピューター A からアプリケーションをエクスポートします。  
  
3.  コンピューター B にアプリケーションをインポートします。  
  
4.  コンピューター B で IIS vroot を作成します。  
  
5.  コンピューター A の vroot にある .svc ファイル (componentName.svc) と Web.config ファイルを、コンピューター B で新しく作成した vroot にコピーします。  
  
## <a name="see-also"></a>関連項目
- [COM+ アプリケーションとの統合の概要](../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications-overview.md)
- [方法: COM + サービス設定を構成します。](../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
- [方法: COM + サービス モデル構成ツールを使用します。](../../../../docs/framework/wcf/feature-details/how-to-use-the-com-service-model-configuration-tool.md)
