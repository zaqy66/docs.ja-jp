---
title: モデリングとマッピング
ms.date: 03/30/2017
ms.assetid: ec8a9515-3708-4cde-a688-4d8e6975f150
ms.openlocfilehash: 81080c416fd18c51be6626cb70a23073e049051d
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45515186"
---
# <a name="modeling-and-mapping"></a>モデリングとマッピング
[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] では、概念モデル、ストレージ モデル、およびこの 2 つのモデル間のマッピングをアプリケーションに最適な方法で定義できます。 Visual Studio で Entity Data Model ツールは、作成することができます。[edmx ファイル](https://msdn.microsoft.com/library/f4c8e7ce-1db6-417e-9759-15f8b55155d4)からデータベースまたはグラフィカルなモデルと、更新、データベースまたはモデルが変更されたときにファイルをします。  
  
 Entity Framework 4.1 以降では、Code First の開発を使用してモデルをプログラムで作成することもできます。 Code First の開発に対しては、2 つの異なるシナリオがあります。 どちらの場合でも、開発者は .NET Framework のクラス定義をコーディングしてモデルを定義し、データ注釈または Fluent API を使用してオプションで追加のマッピングまたは構成を指定します。  
  
 詳細については、次を参照してください。[概念モデルのマッピングの作成と](https://go.microsoft.com/fwlink/?LinkId=235016)します。  
  
 含まれている EDM ジェネレーターを使用することも、[!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)]します。 EdmGen.exe は、既存のデータ ソースから .csdl ファイル、.ssdl ファイル、および .msl ファイルを生成します。 モデルとマッピングの内容を手動で作成することもできます。 詳細については、次を参照してください。 [EDM ジェネレーター (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md)します。
