---
title: '方法 : スプラッシュ スクリーンを WPF アプリケーションに追加する'
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 46efa041736870c5c0f08baa321ef0dc53cacc0d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43402927"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a>方法 : スプラッシュ スクリーンを WPF アプリケーションに追加する

このトピックでは、スタートアップ ウィンドウを追加する方法または*スプラッシュ スクリーン*、Windows Presentation Foundation (WPF) アプリケーションにします。

## <a name="to-add-an-existing-image-as-a-splash-screen"></a>スプラッシュ スクリーンとして既存のイメージを追加するには

1.  スプラッシュ スクリーンを使用するイメージを作成または選択します。 Windows Imaging Component (WIC) ではサポートされている任意のイメージ形式を使用することができます。 たとえば、BMP、GIF、JPEG、PNG、または TIFF の形式を使用することができます。

2.  WPF アプリケーション プロジェクトにイメージ ファイルを追加します。

3.  **ソリューション エクスプ ローラー**イメージを選択します。

4.  [プロパティ] ウィンドウで、ドロップダウン矢印をクリックします。、**ビルド アクション**プロパティ。

5.  選択**SplashScreen**ドロップダウン リストから。

6.  **F5** キーを押してアプリケーションをビルドし、実行します。

     スプラッシュ スクリーンのイメージは、画面の中央に表示され、メイン アプリケーション ウィンドウが表示されたらをフェードアウトします。

## <a name="to-exclude-the-splash-screen-from-build"></a>スプラッシュ スクリーンをビルドから除外するには

1.  **ソリューション エクスプ ローラー**、スプラッシュ スクリーン イメージを選択します。

2.  **プロパティ**ウィンドウで、設定、**ビルド アクション**に**None**します。

## <a name="to-remove-the-splash-screen-from-an-application"></a>スプラッシュ スクリーンをアプリケーションから削除するには

**ソリューション エクスプ ローラー**、スプラッシュ スクリーン イメージを削除します。

## <a name="see-also"></a>関連項目

- <xref:System.Windows.SplashScreen>
- [方法: 既存の項目をプロジェクトに追加します。](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))
