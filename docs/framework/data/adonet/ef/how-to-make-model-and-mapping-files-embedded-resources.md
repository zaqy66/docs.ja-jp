---
title: モデル ファイルとマッピング ファイルを組み込みリソースにする方法
ms.date: 03/30/2017
ms.assetid: 20dfae4d-e95a-4264-9540-f5ad23b462d3
ms.openlocfilehash: 35507f92d0ba9f434156773c8dc5621ed3c423c0
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43776890"
---
# <a name="how-to-make-model-and-mapping-files-embedded-resources"></a>モデル ファイルとマッピング ファイルを組み込みリソースにする方法
[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]モデル ファイルとマッピング ファイルをアプリケーションの埋め込みリソースとしてデプロイすることができます。 モデル ファイルとマッピング ファイルが組み込まれたアセンブリは、エンティティ接続と同じアプリケーション ドメインに読み込む必要があります。 詳細については、「[Connection Strings (接続文字列)](../../../../../docs/framework/data/adonet/ef/connection-strings.md)」をご覧ください。 既定では、[!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)] ツールによって、モデル ファイルとマッピング ファイルが組み込まれます。 モデル ファイルとマッピング ファイルを手動で定義する場合は、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] アプリケーションと共にモデル ファイルとマッピング ファイルが組み込みリソースとして確実に配置されるように、この手順を使用します。  
  
> [!NOTE]
>  組み込みリソースを保持するには、モデル ファイルとマッピング ファイルを変更するたびに、この手順を繰り返す必要があります。  
  
### <a name="to-embed-model-and-mapping-files"></a>モデル ファイルとマッピング ファイルを組み込むには  
  
1.  **ソリューション エクスプ ローラー**、概念 (.csdl) ファイルを選択します。  
  
2.  **プロパティ**ペインで、設定**ビルド アクション**に**埋め込まれたリソース**します。  
  
3.  ストレージ (.ssdl) ファイルとマッピング (.msl) ファイルに対して手順 1. と手順 2. を繰り返します。  
  
4.  **ソリューション エクスプ ローラー**、App.config ファイルをダブルクリックし、変更、`Metadata`パラメーター、`connectionString`属性は、次の形式のいずれかに基づきます。  
  
    -   `Metadata=` `res://<assemblyFullName>/<resourceName>;`  
  
    -   `Metadata=` `res://*/<resourceName>;`  
  
    -   `Metadata=res://*;`  
  
     詳細については、「[Connection Strings (接続文字列)](../../../../../docs/framework/data/adonet/ef/connection-strings.md)」をご覧ください。  
  
## <a name="example"></a>例  
 埋め込みモデルとマッピング ファイルを次の接続文字列が参照、 [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832)します。 この接続文字列は、プロジェクトの App.config ファイルに格納されています。  
  
  
  
## <a name="see-also"></a>関連項目  
 [モデリングとマッピング](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)  
 [接続文字列を定義する方法](../../../../../docs/framework/data/adonet/ef/how-to-define-the-connection-string.md)  
 [EntityConnection の接続文字列を作成する方法](../../../../../docs/framework/data/adonet/ef/how-to-build-an-entityconnection-connection-string.md)  
 [ADO.NET Entity Data Model ツール](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)
