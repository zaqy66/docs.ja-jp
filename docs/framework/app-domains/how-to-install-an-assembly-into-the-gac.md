---
title: アセンブリを GAC にインストールする
ms.date: 09/20/2018
helpviewer_keywords:
- assemblies [.NET Framework], global assembly cache
- Gacutil.exe
- strong-named assemblies, global assembly cache
- global assembly cache, installing assemblies
- Global Assembly Cache tool
- windows installer, global assembly cache
ms.assetid: a7e6f091-d02c-49ba-b736-7295cb0eb743
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d365ac77fe6cd7fc4fca36705729ec12b06d6830
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2018
ms.locfileid: "46584582"
---
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a>方法: アセンブリをグローバル アセンブリ キャッシュにインストールする

厳密な名前付きのアセンブリをグローバル アセンブリ キャッシュ (GAC) にインストールには、次の 2 つの方法があります。

> [!IMPORTANT]
> GAC にインストールできるのは、厳密な名前付きのアセンブリだけです。 厳密な名前付きのアセンブリを作成する方法については、「[方法: 厳密な名前でアセンブリに署名する](how-to-sign-an-assembly-with-a-strong-name.md)」を参照してください。

## <a name="windows-installer"></a>Windows インストーラー

アセンブリをグローバル アセンブリ キャッシュに追加するための推奨する方法は、[Windows インストーラー](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache)(Windows インストール エンジン) です。 Windows インストーラーを使用すると、グローバル アセンブリ キャッシュ内のアセンブリの参照カウントが示されるなどの利点があります。 [ Visual Studio 2017 用 WiX Toolset 拡張機能](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension)を使用して、Windows インストーラーのインストーラー パッケージを作成できます。

## <a name="global-assembly-cache-tool"></a>グローバル アセンブリ キャッシュ ツール

グローバル アセンブリ キャッシュ ツール [(gacutil.exe)](../tools/gacutil-exe-gac-tool.md) を使用して、厳密な名前付きアセンブリをグローバル アセンブリ キャッシュに追加したり、グローバル アセンブリ キャッシュの内容を表示したりできます。

   > [!NOTE]
   > Gacutil.exe は開発専用です。製品アセンブリをグローバル アセンブリ キャッシュにインストールするためには使用しないでください。

gacutil の構文は次のとおりです。

```shell
gacutil -i <assembly name>
```

このコマンドで、*assembly name* はグローバル アセンブリ キャッシュにインストールされるアセンブリの名前です。

ファイル名 `hello.dll` のアセンブリをグローバル アセンブリ キャッシュにインストールする例を次に示します。

```shell
gacutil -i hello.dll
```

> [!NOTE]
> 以前のバージョンの .NET Framework では、Windows のシェル拡張機能である Shfusion.dll により、**エクスプローラー**でアセンブリをドラッグしてインストールすることができました。 .NET Framework 4 以降、Shfusion.dll は廃止されましたが、互換性のために残されています。

## <a name="see-also"></a>関連項目

- [アセンブリとグローバル アセンブリ キャッシュの使用](working-with-assemblies-and-the-gac.md)
- [方法: グローバル アセンブリ キャッシュからアセンブリを削除する](how-to-remove-an-assembly-from-the-gac.md)
- [Gacutil.exe (グローバル アセンブリ キャッシュ ツール)](../tools/gacutil-exe-gac-tool.md)
- [方法: 厳密な名前でアセンブリに署名する](how-to-sign-an-assembly-with-a-strong-name.md)