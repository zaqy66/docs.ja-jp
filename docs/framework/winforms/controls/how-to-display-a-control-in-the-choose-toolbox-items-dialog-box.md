---
title: '方法: 内のコントロールを表示、ツールボックス項目 ダイアログ ボックスの選択'
ms.date: 03/30/2017
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
ms.openlocfilehash: 56dad16b7a0bd8f0e7423b4a70e7173578150cbe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520452"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a>方法: 内のコントロールを表示、ツールボックス項目 ダイアログ ボックスの選択
を作成およびコントロールを配置することがそれらのコントロールに表示される、**ツールボックス アイテムの選択**] ダイアログ ボックスで、右クリックしたときに表示される、**ツールボックス**選択 **[アイテムの選択**します。 AssemblyFoldersEx の登録手順を使用して、このダイアログ ボックスに表示されるコントロールを有効にすることができます。  
  
### <a name="to-display-your-control-in-the-choose-toolbox-items-dialog-box"></a>ツールボックス アイテムの選択 ダイアログ ボックスで、コントロールを表示するには  
  
-   コントロール アセンブリをグローバル アセンブリ キャッシュにインストールします。 詳細については、「[方法 :グローバル アセンブリ キャッシュにアセンブリをインストールします。](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)  
  
     - または -  
  
-   AssemblyFoldersEx の登録手順を使用して、コントロールとその関連付けられたデザイン時アセンブリを登録します。 AssemblyFoldersEx は、サード パーティ ベンダーがサポートされるフレームワークの各バージョンのパスを格納する場所のレジストリの場所です。 デザイン時の解像度は、この参照アセンブリを検索するレジストリの場所で確認できます。 レジストリ スクリプトでは、ツールボックスに表示するコントロールを指定できます。 詳細については、次を参照してください。[カスタム コントロールとデザイン時アセンブリ (Visual Studio 2013) の展開](https://msdn.microsoft.com/library/96158eb0-b691-4ae1-9e7b-3c65a1b798cb)します。  
  
## <a name="see-also"></a>関連項目
- [[ツールボックス アイテムの選択] ダイアログ ボックス (Visual Studio)](https://msdn.microsoft.com/library/bd07835f-18a8-433e-bccc-7141f65263bb)
- [カスタム コントロールとデザイン時アセンブリ (Visual Studio 2013) の展開](https://msdn.microsoft.com/library/96158eb0-b691-4ae1-9e7b-3c65a1b798cb)
- [デザイン時の Windows フォーム コントロールの開発](../../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
- [方法: グローバル アセンブリ キャッシュにアセンブリをインストールします。](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)
- [チュートリアル: カスタム コンポーネントでツールボックスが自動的に入力](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
