---
title: 厳密な名前付けおよび .NET ライブラリ
description: 厳密な名前付けの .NET ライブラリの推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/16/2018
ms.openlocfilehash: e3f7d443eb9acc84c800ea2611b803733085391c
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49372807"
---
# <a name="strong-naming"></a>厳密な名前付け

生成キーを持つアセンブリの署名とは厳密な名前付け、[アセンブリの厳密な名前](../../framework/app-domains/strong-named-assemblies.md)します。 アセンブリは、厳密な名前が、名前とアセンブリのバージョン番号に基づく一意の id を作成し、アセンブリの競合を防止できます。

厳密な名前付けの欠点は、Windows 上の .NET Framework により、アセンブリが厳密な名前とアセンブリの厳密な読み込みことです。 厳密な名前付きのアセンブリの参照を強制的に開発者が、アセンブリによって参照されているバージョンと一致する必要があります[バインド リダイレクトを構成する](../../framework/configure-apps/redirect-assembly-versions.md)アセンブリを使用する場合。

```xml
<configuration>
   <runtime>
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
         <dependentAssembly>
            <assemblyIdentity name="myAssembly" publicKeyToken="32ab4ba45e0a69a1" culture="neutral" />
            <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
         </dependentAssembly>
      </assemblyBinding>
   </runtime>
</configuration>
```

.NET 開発者は、厳密な名前付けに関する警告を出したり、ときに、厳密なアセンブリの読み込みにはどのようないる通常気候について文句です。 さいわい、この問題は、.NET Framework に分離されます。 .NET core、Xamarin、UWP、およびその他のほとんどの .NET 実装は、厳密なアセンブリの読み込みに必要はありませんし、厳密な名前付けの主な欠点を削除します。

厳密な名前付けの 1 つの重要な側面はウイルスである: 強力なという名前のアセンブリが唯一の参照の他の厳密な名前付きアセンブリ。 ライブラリが厳密な名前付きしていない場合は、アプリケーションまたはそれを使用してから、厳密な名前付けが必要なライブラリを構築する開発者を除外います。

厳密な名前付けの利点は次のとおりです。

1. アセンブリの参照し、その他の厳密な名前のアセンブリで使用されることができます。
2. アセンブリはグローバル アセンブリ キャッシュ (GAC) に格納できます。
3. アセンブリは、アセンブリの他のバージョンと並行読み込まれることができます。 サイド バイ サイド アセンブリの読み込みは一般に、プラグイン アーキテクチャを持つアプリケーションが必要です。

## <a name="create-strong-named-net-libraries"></a>強力な .NET ライブラリをという名前の作成します。

オープン ソース .NET ライブラリは、厳密な名前必要があります。 厳密なアセンブリの名前を付けにより、ほとんどの人がそれを使用し、厳密なアセンブリの読み込みのみが、.NET Framework に影響します。

> [!NOTE]
> このガイダンスは、.NET ライブラリは、NuGet.org に公開など、公開されている分散型の .NET ライブラリに固有です。厳密な名前付けと、ほとんどの .NET アプリケーションでは必要ありません、されません既定で行う必要があります。

**✔️ をご検討ください**ライブラリのアセンブリの名前付け強力な。

**✔️ をご検討ください**でソース管理システムに厳密な名前に使用するキーを確認します。

> 公開キーには、開発者は変更し、同じキーを持つライブラリのソース コードを再コンパイルができます。

> [!IMPORTANT]
> 暗号化、id が必要なときに[Authenticode](/windows-hardware/drivers/install/authenticode)と[NuGet パッケージに署名](/nuget/create-packages/sign-a-package)はお勧めします。 セキュリティに関する考慮事項厳密な名前付けを使用しない必要があります。

**✔️ をご検討ください**バインディングのリダイレクト、および更新される頻度を減らすユーザーを支援する唯一のメジャー バージョンの変更でアセンブリのバージョンをインクリメントします。

> 詳細をご覧ください[バージョン管理とアセンブリのバージョン](./versioning.md#assembly-version)します。

**❌ しない**を追加、削除、または厳密な名前付けのキーを変更します。

> アセンブリの厳密な名前付けキーの変更では、アセンブリの id を変更し、それを使用するコンパイル済みコードを中断します。 詳細については、次を参照してください。[バイナリの互換性に影響する変更](./breaking-changes.md#binary-breaking-change)します。

**❌ しない**ライブラリの厳密な名前し、厳密な名前を持たないバージョンを発行します。 たとえば、`Contoso.Api` と`Contoso.Api.StrongNamed` です。

> 開発者の環境のシステム パッケージの 2 つの分岐を発行します。 また、両方のパッケージによって最終的に、アプリケーションの場合、開発者には型名の競合が発生する可能性です。 .NET のに関してはさまざまなアセンブリ内のさまざまな種類です。

>[!div class="step-by-step"]
[前へ](./cross-platform-targeting.md)
[次へ](./nuget.md)
