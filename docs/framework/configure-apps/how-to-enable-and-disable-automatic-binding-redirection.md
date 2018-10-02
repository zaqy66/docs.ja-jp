---
title: '方法: 自動バインディング リダイレクトを有効/無効にする'
ms.date: 09/12/2018
helpviewer_keywords:
- side-by-side execution, assembly binding redirection
- assemblies [.NET Framework], binding redirection
ms.assetid: 5fca42f3-bdce-4b81-a704-61e42c89d3ba
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 9b9c9cbdb89ccf67942dcccee37ea410c6fa39a5
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48036202"
---
# <a name="how-to-enable-and-disable-automatic-binding-redirection"></a>方法: 自動バインディング リダイレクトを有効/無効にする

Visual studio を対象とするアプリをコンパイルするときに、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)]以降のバージョンでバインド リダイレクトが自動的にアセンブリの統一をオーバーライドするアプリの構成ファイルに追加するとします。 アプリの構成ファイルで手動でバインド リダイレクトを指定している場合でも、アプリまたはそのコンポーネントが同じアセンブリの複数バージョンを参照している場合、バインド リダイレクトが追加されます。 自動バインド リダイレクトの機能に影響を与えます従来のデスクトップ アプリと web アプリを対象とする、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)]以降のバージョンの動作は、web アプリに少しずつ異なります。 以前のバージョンの .NET Framework を対象とする既存のアプリがある場合は、自動バインド リダイレクトを有効にできます。また、手動で作成したバインド リダイレクトを保持する場合は、この機能を無効にできます。

## <a name="disable-automatic-binding-redirects-in-desktop-apps"></a>デスクトップ アプリで自動バインド リダイレクトを無効にします。

自動バインド リダイレクトは、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)] 以上のバージョンを対象とする従来のデスクトップ アプリで、既定で有効になっています。 バインド リダイレクトは、アプリケーションがコンパイルされ、発生する可能性のあるアセンブリの統一をオーバーライドするときに、出力構成ファイル (app.config) に追加されます。 ソース app.config ファイルは変更されません。 アプリのプロジェクト ファイルを変更して、この機能を無効にできます。

1. 次のメソッドのいずれかを使用して編集するためのプロジェクト ファイルを開きます。

   - Visual studio でプロジェクトを選択**ソリューション エクスプ ローラー**を選び、**ファイル エクスプ ローラーでフォルダーを開く**ショートカット メニューから。 ファイル エクスプ ローラーでプロジェクト (.csproj または .vbproj) ファイルを検索し、メモ帳で開きます。
   - Visual Studio での**ソリューション エクスプ ローラー**でプロジェクトを右クリックし、選択**プロジェクトのアンロード**します。 ここでも、アンロードされたプロジェクトを右クリックして **編集 [projectname.csproj]** します。

2. プロジェクト ファイルで、次のプロパティ エントリを検索します。

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

3. `true` を `false` に変更します。

   ```xml
   <AutoGenerateBindingRedirects>false</AutoGenerateBindingRedirects>
   ```

## <a name="enable-automatic-binding-redirects-manually"></a>自動バインド リダイレクトを手動で有効にします。

旧バージョンを対象を自動的に求められたら、リダイレクトを追加する場合や、.NET Framework の既存のアプリで自動バインド リダイレクトを有効にできます。 新しいバージョンの framework を対象としているリダイレクトの追加を自動的に求められません場合は、ビルド出力アセンブリを再マップすることを示す可能性がありますが表示されます。

1. 次のメソッドのいずれかを使用して編集するためのプロジェクト ファイルを開きます。

   - Visual studio でプロジェクトを選択**ソリューション エクスプ ローラー**を選び、**ファイル エクスプ ローラーでフォルダーを開く**ショートカット メニューから。 ファイル エクスプ ローラーでプロジェクト (.csproj または .vbproj) ファイルを検索し、メモ帳で開きます。
   - Visual Studio での**ソリューション エクスプ ローラー**でプロジェクトを右クリックし、選択**プロジェクトのアンロード**します。 ここでも、アンロードされたプロジェクトを右クリックして **編集 [projectname.csproj]** します。

2. 最初の構成プロパティ グループに次の要素を追加 (で、 \<PropertyGroup > タグ)。

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

   次の要素が挿入されたプロジェクト ファイルの例を次に示します。

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <Project ToolsVersion="12.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <Import Project="$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props" Condition="Exists('$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props')" />
       <PropertyGroup>
         <Configuration Condition=" '$(Configuration)' == ''     ">Debug</Configuration>
         <Platform Condition=" '$(Platform)' == '' ">AnyCPU</Platform>
         <ProjectGuid>{123334}</ProjectGuid>
         ...
         <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
       </PropertyGroup>
     ...
   </Project>
   ```

3. アプリをコンパイルします。

## <a name="enable-automatic-binding-redirects-in-web-apps"></a>Web apps での自動バインド リダイレクトを有効にします。

自動バインド リダイレクトは、Web アプリでは異なる方法で実装されます。 ソースの構成 (web.config) ファイルを Web アプリ用に変更する必要があるため、バインド リダイレクトは構成ファイルに自動的に追加されません。 ただし、Visual Studio によってバインドの競合が通知されるため、バインド リダイレクトを追加して競合を解決できます。 常にバインド リダイレクトを追加する指示に従い、ため、web アプリに対してこの機能を明示的に無効にする必要はありません。

Web.config ファイルにバインド リダイレクトを追加するには

1. Visual Studio で、アプリをコンパイルし、ビルドの警告を確認します。

   ![ビルドのアセンブリ参照の競合の警告](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")

2. アセンブリ バインドの競合がある場合、警告が表示されます。 警告をダブルクリックするか、警告とキーを押して選択**Enter**します。

   自動的にソース web.config ファイルに必要なバインド リダイレクトを追加できるダイアログ ボックスが表示されます。

   ![バインド リダイレクトのアクセス許可ダイアログ](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")

## <a name="see-also"></a>関連項目

- [\<bindingRedirect > 要素](../../../docs/framework/configure-apps/file-schema/runtime/bindingredirect-element.md)
- [アセンブリ バージョンのリダイレクト](../../../docs/framework/configure-apps/redirect-assembly-versions.md)
