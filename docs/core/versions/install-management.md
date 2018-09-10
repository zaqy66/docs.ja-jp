---
title: .NET Core インストールを管理する
description: サイド バイ サイド インストール戦略を使用して、ご利用のコンピューター上で .NET Core SDK とランタイムの複数のバージョンを管理します
author: leecow
ms.author: wiwagn
ms.date: 08/22/2018
ms.openlocfilehash: 06c3f43e7917efb8fd31898044d8f5d920c2cada
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43485456"
---
# <a name="manage-net-core-installations"></a>.NET Core インストールを管理する

.NET Core では、SDK とランタイムの複数のバージョンを共存させることができます。これにより、.NET Core アプリケーションのビルドと実行の両方で、バージョンの依存関係の柔軟性を実現できます。 このようなインストールおよび自動的なバージョン ロール フォワード動作からは貴重な特典が得られますが、はっきりした欠点が 1 つあります。 .NET Core SDK または .NET Core ランタイムの更新プログラムがインストールされた場合、以前のバージョンはそのままディスク上に残ります。 複数のバージョンがインストールされている場合は、時間の経過と共にディスク使用量が増大します。 50 を超える .NET Core SDK の更新プログラムがリリースされています。 ご利用のシステム上にインストールされている SDK とランタイムのバージョンの中には、削除できるものが多くある場合があります。

## <a name="safe-to-remove"></a>安全な削除

[.NET Core バージョン選択](selection.md)動作および更新プログラム間での .NET Core のランタイム互換性により、以前のバージョンを安全に削除することができます。 1.x や 2.x などのメジャー バージョン 'バンド' 内で .NET Core ランタイム更新プログラムは互換性があります。 さらに、.NET Core SDK のより新しいリリースでは、通常、互換性を保ちながら、ランタイムの前バージョンを対象とするアプリケーションをビルドする機能が維持されます。

通常、必要なのは、ご自分のアプリケーションに必須である最新の SDK および最新のパッチ バージョンのランタイムのみです。 より古い SDK またはランタイムのバージョンが保持されるインスタンスでは、project.json ベースのアプリケーションを管理することも必要になります。  ご利用のアプリケーションには以前の SDK やランタイムを維持する特別な理由がない場合、以前のバージョンを安全に削除することができます。

.NET Core を削除する方法は、プラットフォームによって異なり、.NET Core のバージョン間でもわずかに違いがあります。 .NET Core の不要になったバージョンを削除する方法の詳細については、[.NET Core ドキュメント](../index.md)内の「[How to remove the .NET Core Runtime and SDK](remove-runtime-sdk-versions.md)」(.NET Core ランタイムと SDK を削除する方法) を参照してください。
