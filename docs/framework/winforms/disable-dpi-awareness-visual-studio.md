---
title: Visual Studio では、DPI の認識を無効にします。
description: HDPI モニターは、Windows フォーム デザイナーと DPI に対応していないプロセスとして Visual Studio を実行する方法の制限事項について説明します。
ms.date: 08/14/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-designers
author: gewarren
ms.author: gewarren
ms.openlocfilehash: 7ecffedbe536f293945227d817e507f012816737
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48037042"
---
# <a name="disable-dpi-awareness-in-visual-studio"></a>Visual Studio では、DPI の認識を無効にします。

Visual Studio では、表示スケールを自動的に意味インチ (DPI) 対応アプリケーションあたりのドットです。 アプリケーションでは、DPI 対応ではないことを示す、オペレーティング システムは、ビットマップとしてアプリケーションをスケーリングします。 この動作は、DPI の仮想化とも呼ばれます。 アプリケーションは引き続き、100% に拡大縮小、または 96 dpi で実行されていると認識します。

## <a name="windows-forms-designer-on-hdpi-monitors"></a>HDPI のモニターでの Windows フォーム デザイナー

**Windows フォーム デザイナー** Visual Studio ではありませんスケーリングをサポートします。 表示の問題は、一部のフォームを開いたときにこれにより、 **Windows フォーム デザイナー** high dots per インチ (HDPI) モニターです。 例については、コントロールは、次の図のように重複する表示できます。

![HDPI のモニターでの Windows フォーム デザイナー](media/disable-dpi-awareness-visual-studio/win-forms-designer-hdpi.png)

Visual Studio 2017 15.8 でフォームを開くと、以降のバージョンで、 **Windows フォーム デザイナー** HDPI モニターで、Visual Studio は、デザイナーの上部にある黄色のバーの情報を表示します。

![DPI に対応していないモードで再起動する Visual Studio での情報バー](media/disable-dpi-awareness-visual-studio/scaling-gold-bar.png)

メッセージを読み取り**メイン ディスプレイのスケーリングを 200% (192 dpi) に設定します。デザイナー ウィンドウのレンダリングの問題があります。**

場合は、デザイナーを使用していないし、フォームのレイアウトを調整する必要はありません、情報バーを無視し、コード エディターまたはデザイナーの他の種類では、作業を続行できます。 のみ、 **Windows フォーム デザイナー**が影響を受けます。 作業する必要がある場合、 **Windows フォーム デザイナー**、次のセクションでは[、問題を解決する](#to-resolve-the-problem)します。

## <a name="to-resolve-the-problem"></a>この問題を解決するのには

表示に関する問題を解決するのには次の 3 つのオプションがあります。

### <a name="restart-visual-studio-as-a-dpi-unaware-process"></a>DPI に対応していないプロセスとして Visual Studio を再起動します。

DPI に対応していないプロセスとして Visual Studio を再起動するには、黄色の情報バーのオプションを選択します。 これは、問題を解決することをお勧めします。

Visual Studio を DPI に対応していないプロセスとして実行すると、デザイナーのレイアウトの問題を解決するが、フォントがぼやけて表示される可能性があります。 Visual Studio は、ことを示す DPI に対応していないプロセスとして実行した場合に、別の黄色の情報メッセージを表示します**Visual Studio の DPI に対応していないプロセスとして実行します。WPF および XAML デザイナーが正しく表示されない場合があります。** 情報バーは、するためのオプションも用意されています。 **DPI 対応のプロセスとして Visual Studio を再起動**します。

> [!NOTE]
> - DPI に対応していないプロセスとして再起動するオプションを選択したときに、Visual Studio でツール ウィンドウをドッキング解除が、これらのツール ウィンドウの位置は変更可能性があります。
> - 既定の Visual Basic のプロファイルを使用する場合、またはがある場合、**作成時に新しいプロジェクトを保存**でオプションを選択解除**ツール** > **オプション** > **プロジェクトおよびソリューション**DPI に対応していないプロセスとして再起動するとき、Visual Studio がプロジェクトを再び開くことはできません。 ただし、それを選択してプロジェクトを開く**ファイル** > **最近使ったプロジェクトおよびソリューション**します。

作業が完了したら、DPI 対応のプロセスとして Visual Studio を再起動することが重要、 **Windows フォーム デザイナー**します。 DPI に対応していないプロセスとして実行されているフォントがぼやけてし、など他のデザイナーでの問題が発生する可能性があります、 **XAML デザイナー**します。 DPI に対応していないモードで実行されている Visual Studio を再度開くを起動する場合が DPI 対応もう一度です。 クリックすることも、 **DPI 対応のプロセスとして Visual Studio を再起動**の情報バーのオプション。

### <a name="add-a-registry-entry"></a>レジストリ エントリを追加します。

Visual Studio は、レジストリを変更して DPI 対応としてマークできます。 開いている**レジストリ エディター**にエントリを追加し、 **HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers**サブキー。

**エントリ**: % %programfiles (x86) %\Microsoft Visual Studio\2017\Community\Common7\IDE\devenv.exe

   > [!NOTE]
   > Visual Studio 2017 の Professional または Enterprise edition を使用している場合は置き換えます**コミュニティ**で**Professional**または**Enterprise**エントリにします。

**型**: REG_SZ

**値**: DPIUNAWARE

> [!NOTE]
> Visual Studio は、レジストリ エントリを削除するまでに、DPI に対応していないモードでは残ります。

### <a name="set-your-display-scaling-setting-to-100"></a>設定、画面のスケーリングを 100% に設定します。

100% に設定を Windows 10 にスケールイン ディスプレイを設定する入力**表示設定**タスク バー、クリックして [検索] ボックスに**表示設定を変更**します。 **設定**ウィンドウで、設定**テキスト、アプリ、およびその他のアイテムのサイズを変更**に**100%** します。

100% に拡大縮小、表示を設定できない可能性があります、ため、使用するのには小さすぎてユーザー インターフェイスをことができます。

## <a name="see-also"></a>関連項目

- [Windows フォームにおける自動スケーリング](automatic-scaling-in-windows-forms.md)