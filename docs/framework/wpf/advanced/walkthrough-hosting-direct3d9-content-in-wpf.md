---
title: 'チュートリアル : WPF での Direct3D9 コンテンツのホスト'
ms.date: 03/30/2017
helpviewer_keywords:
- Direct3D9 [WPF interoperability], hosting Direct3D9 content
- WPF [WPF], hosting Direct3D9 content
ms.assetid: 60983736-0ab5-42cc-8b16-e9fbde261a43
ms.openlocfilehash: 5e7edfbeb9a3cddcdcd81d9c87e5e85bfc947339
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44188710"
---
# <a name="walkthrough-hosting-direct3d9-content-in-wpf"></a>チュートリアル : WPF での Direct3D9 コンテンツのホスト
このチュートリアルでは、Windows Presentation Foundation (WPF) アプリケーションでの Direct3D9 コンテンツをホストする方法を示します。  
  
 このチュートリアルでは次のタスクを実行します。  
  
-   Direct3D9 コンテンツをホストする WPF プロジェクトを作成します。  
  
-   Direct3D9 コンテンツをインポートします。  
  
-   使用しての Direct3D9 コンテンツの表示、<xref:System.Windows.Interop.D3DImage>クラス。  
  
 完了したら、WPF アプリケーションでの Direct3D9 コンテンツをホストする方法がわかります。  
  
## <a name="prerequisites"></a>必須コンポーネント  
 このチュートリアルを実行するには、次のコンポーネントが必要です。  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)]。  
  
-   DirectX 9 以降の SDK です。  
  
-   WPF と互換性のある形式での Direct3D9 コンテンツを含む DLL です。 詳細については、次を参照してください。 [WPF と Direct3D9 の相互運用性](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md)と[チュートリアル: WPF でのホストの Direct3D9 のコンテンツを作成する](../../../../docs/framework/wpf/advanced/walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md)します。  
  
## <a name="creating-the-wpf-project"></a>WPF プロジェクトを作成します。  
 最初の手順では、WPF アプリケーションのプロジェクトを作成します。  
  
#### <a name="to-create-the-wpf-project"></a>WPF プロジェクトを作成するには  
  
-   新しい WPF アプリケーション プロジェクトを作成するという名前の Visual c# で`D3DHost`します。 詳細については、次を参照してください。[方法: 新しい WPF アプリケーション プロジェクトを作成する](https://msdn.microsoft.com/library/1f6aea7a-33e1-4d3f-8555-1daa42e95d82)します。  
  
     MainWindow.xaml を開きます、[!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)]します。  
  
## <a name="importing-the-direct3d9-content"></a>Direct3D9 コンテンツのインポート  
 使用してアンマネージ DLL から Direct3D9 コンテンツをインポートする、`DllImport`属性。  
  
#### <a name="to-import-direct3d9-content"></a>Direct3D9 コンテンツをインポートするには  
  
1.  コード エディターでの MainWindow.xaml.cs を開きます。  
  
2.  自動的に生成されたコードを次のコードに置き換えます。  
  
     [!code-csharp[System.Windows.Interop.D3DImage#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/CS/window1.xaml.cs#1)]  
  
## <a name="hosting-the-direct3d9-content"></a>Direct3D9 コンテンツのホスト  
 最後に、使用して、 <xref:System.Windows.Interop.D3DImage> Direct3D9 コンテンツをホストするクラス。  
  
#### <a name="to-host-the-direct3d9-content"></a>Direct3D9 コンテンツをホストするには  
  
1.  MainWindow.xaml で、自動的に生成された XAML を次の XAML に置き換えます。  
  
     [!code-xaml[System.Windows.Interop.D3DImage#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/CS/window1.xaml#10)]  
  
2.  プロジェクトをビルドします。  
  
3.  Bin/debug フォルダーに Direct3D9 コンテンツを含んでいる DLL をコピーします。  
  
4.  F5 キーを押してプロジェクトを実行します。  
  
     WPF アプリケーション内での Direct3D9 コンテンツが表示されます。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Interop.D3DImage>  
 [Direct3D9 および WPF の相互運用性のパフォーマンスに関する考慮事項](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md)
