---
title: Power Packs コントロール (Visual Studio) を参照するアプリケーションの配置
ms.date: 07/20/2015
helpviewer_keywords:
- Power Packs, deploying
ms.assetid: f2230f53-a745-4731-89e6-033943faa209
ms.openlocfilehash: bd235bc0b4a7f9978333931ae1dce012c0950374
ms.sourcegitcommit: 2d8b7488d94101b534ca3e9780b1c1e840233405
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2018
ms.locfileid: "39198229"
---
# <a name="deploying-applications-that-reference-power-packs-controls-visual-studio"></a>Power Packs コントロール (Visual Studio) を参照するアプリケーションの配置
Power Packs コントロールを参照するアプリケーションをデプロイするかどうか (<xref:Microsoft.VisualBasic.PowerPacks.LineShape>、 <xref:Microsoft.VisualBasic.PowerPacks.OvalShape>、 <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>、または<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>) をコントロールは、セットアップ先のコンピューターにインストールする必要があります。  
  
## <a name="installing-the-power-packs-controls-as-a-prerequisite"></a>前提条件として Power Packs コントロールをインストールします。  
 アプリケーションを正しく配置するためには、アプリケーションによって参照されるすべてのコンポーネントを配置する必要もあります。 必須コンポーネントのインストール プロセスは、 *ブートストラップ*と呼ばれます。  
  
 Visual Studio は開発用コンピューターにインストールすると、Power Pack のブートス トラップ パッケージは、Visual Studio ブートス トラップ ディレクトリに追加されます。 その後、 [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] または Windows インストーラー配置のための必要条件を追加する手順に従うと、このパッケージが使用可能になります。  
  
 既定では、ブートストラップ コンポーネントは、インストール パッケージと同じ場所から配置されます。 または、必要に応じてユーザーがダウンロードできるような URL またはファイルの共有位置からコンポーネントを配置することもできます。  
  
> [!NOTE]
>  ブートストラップ コンポーネントをインストールするには、コンピューターに対する管理者または同様のユーザー アクセス許可が必要になる場合があります。 つまり、 [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] アプリケーションの場合、アプリケーションで指定されたセキュリティ レベルに関係なく、アプリケーションをインストールするために管理アクセス許可が必要です。 アプリケーションのインストール後は、管理アクセス許可がなくてもアプリケーションを実行できます。  
  
 インストール中には対象のコンピューターに存在しない場合は、Power Packs コントロールをインストールするユーザーが求められます。  
  
 ブートス トラップする代わりに、Microsoft Systems Management Server などの電子ソフトウェア配布システムを使用して事前 Power Packs コントロールを展開できます。  
  
## <a name="see-also"></a>関連項目  
 [方法: ClickOnce アプリケーションと共に必須コンポーネントをインストールする](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application)  
 [Visual Basic Power Packs コントロール](../../../visual-basic/developing-apps/windows-forms/power-packs-controls.md)
