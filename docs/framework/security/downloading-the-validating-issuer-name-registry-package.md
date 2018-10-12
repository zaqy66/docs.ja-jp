---
title: 発行者名レジストリの検証パッケージのダウンロード
ms.date: 10/10/2018
ms.assetid: ff8b0014-c5d4-4614-90f0-13fcc0ba777a
ms.openlocfilehash: 654a513e06f528f617bc19fbc59961c5b0e16049
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49121156"
---
# <a name="download-the-validating-issuer-name-registry-package"></a>発行者名レジストリの検証パッケージをダウンロードします。

このトピックでは、Validating Issuer Name Registry (VINR) をダウンロードしてプロジェクトで使用する方法について説明します。

VINR は、プロジェクトに必要なアセンブリと参照を追加する NuGet パッケージとして入手できます。 まだ NuGet がインストールされていない場合は、[nuget.org](http://nuget.org) にアクセスしてインストールしてください。 NuGet の「[Microsoft Validating Issuer Name Registry](https://nuget.org/packages/System.IdentityModel.Tokens.ValidatingIssuerNameRegistry/)」ページにアクセスすると、拡張機能のバージョン履歴を参照できます。

## <a name="use-the-package-manager-gui"></a>パッケージ マネージャー GUI を使用します。

1. Visual Studio の**ソリューション エクスプローラー**でプロジェクトを右クリックし、**[NuGet パッケージの管理]** を選択します。

2. **[NuGet パッケージの管理]** ウィンドウで、検索ボックスをクリックし、「`ValidatingIssuerNameRegistry`」と入力して **Enter** キーを押します。

3. 結果ペインから、最初の結果の **[インストール]** をクリックします。

4. パッケージのダウンロードが開始されます。 プロジェクトに追加される前に、[License Acceptance] ダイアログ ボックスが表示されます。 ライセンス条項に同意する場合は、**[I Accept]** をクリックします。

5. 最新の VINR アセンブリがダウンロードされ、プロジェクトに追加されます。

## <a name="use-the-package-manager-console"></a>パッケージ マネージャー コンソールを使用してください。

1. Visual Studio で、次のようにクリックします。**ツール** > **NuGet パッケージ マネージャー** > **パッケージ マネージャー コンソール**します。

2. **[パッケージ マネージャー コンソール]** が表示されます。 次のテキストを入力し、**Enter** キーを押します。

    ```powershell
    Install-Package System.IdentityModel.Tokens.ValidatingIssuerNameRegistry
    ```

3. 最新の VINR アセンブリがダウンロードされ、プロジェクトに追加されます。
