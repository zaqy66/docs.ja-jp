---
title: .NET Core での単体テスト
description: 単体テストがさらに容易になりました。 .NET Core と .NET Standard プロジェクトでの単体テストの使用方法をご覧ください。
author: ardalis
ms.author: wiwagn
ms.date: 08/30/2017
ms.openlocfilehash: 5b54e7936fb19a94fad9585c00904ae67a59e064
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2018
ms.locfileid: "49314865"
---
# <a name="unit-testing-in-net-core-and-net-standard"></a>.NET Core と .NET Standard の単体テスト

.NET Core は、アプリケーションの単体テストを従来よりも簡単に作成できるように、テストの容易性を考慮して設計されています。 この記事では、単体テスト (およびその他の種類のテストとの違い) について簡単に紹介します。 リンクされたリソースでは、テスト プロジェクトをソリューションに追加してから、コマンド ラインまたは Visual Studio を使用して単体テストを実行する方法を説明します。

.NET Core 2.0 は [.NET Standard 2.0](../../standard/net-standard.md) をサポートしています。 このセクションで単体テストの説明に使用するライブラリは .NET Standard に依存しており、他のプロジェクト タイプでも機能します。

.NET Core 2.0 以降では、C#、F#、および Visual Basic 用の単体テスト プロジェクト テンプレートが用意されています。

## <a name="getting-started-with-testing"></a>テストの概要

自動テストのスイートを備えることは、ソフトウェア アプリケーションが作成者の意図どおりに動作することを確認する最良の方法の 1 つです。 ソフトウェア アプリケーション用のテストには、統合テスト、Web テスト、ロード テストなど、さまざまな種類があります。 最下位レベルには、個々のソフトウェア コンポーネントまたはメソッドをテストする単体テストがあります。 単体テストでは、開発者のコントロール内のコードのみをテストし、データベース、ファイル システム、ネットワーク リソースなどのインフラストラクチャ上の問題はテストしません。 単体テストは、[テスト駆動開発 (TDD)](https://deviq.com/test-driven-development/) を使用して記述することも、既存のコードに追加してその正確性を確認することもできます。 いずれの場合にも、プロジェクトの共有コード リポジトリに変更をプッシュする前に数百もの単体テストを実行できることが理想的なため、単体テストは小規模で高速、かつ適切な名前が付けられている必要があります。

> [!NOTE]
> 多くの場合、開発者はテストのクラスやメソッドに適した名前を考え出すのに苦心します。 開始点として、ASP.NET 製品チームは[これらの規則](https://github.com/aspnet/Home/wiki/Engineering-guidelines#unit-tests-and-functional-tests)に従います。

単体テストを記述するときは、インフラストラクチャに対する依存関係を誤って導入しないように注意してください。 これらを導入すると、テストが低速で不安定になるので、統合テスト用に残しておく必要があります。 アプリケーション コードでこれらの非表示の依存関係を回避するには、[明示的な依存関係の原則](https://deviq.com/explicit-dependencies-principle/)に従い、[依存関係の挿入](/aspnet/core/fundamentals/dependency-injection)を使用して、フレームワークに依存関係を要求します。 また、統合テストとは別個のプロジェクト内に単体テストを保持し、単体テスト プロジェクトがインフラストラクチャ パッケージへの参照または依存関係を確実に含まないようにできます。

.NET Core プロジェクトでの単体テストの詳細については、次を参照してください。

.NET Core の単体テスト プロジェクトは [C#](../../csharp/index.md)、[F#](../../fsharp/index.md)、[Visual Basic](../../visual-basic/index.md) でサポートされています。 また、[xUnit](https://xunit.github.io)、[NUnit](https://nunit.org)、または [MSTest](https://github.com/Microsoft/vstest-docs) を選択することもできます。

これらの組み合わせについては以下のチュートリアルで確認できます。

* [*xUnit* と *C#* を使用して .NET Core CLI で単体テストを作成する](unit-testing-with-dotnet-test.md)。
* [*NUnit* と *C#* を使用して .NET Core CLI で単体テストを作成する](unit-testing-with-nunit.md)。
* [*MSTest* と *C#* を使用して .NET Core CLI で単体テストを作成する](unit-testing-with-mstest.md)。
* [*xUnit* と *F#* を使用して .NET Core CLI で単体テストを作成する](unit-testing-fsharp-with-dotnet-test.md)。
* [*NUnit* と *F#* を使用して .NET Core CLI](unit-testing-fsharp-with-nunit.md) で単体テストを作成する。
* [*MSTest* と *F#* を使用して .NET Core CLI で単体テストを作成する](unit-testing-fsharp-with-mstest.md)。
* [*xUnit* と *Visual Basic* を使用して .NET Core CLI で単体テストを作成する](unit-testing-visual-basic-with-dotnet-test.md)。
* [*NUnit* と *Visual Basic* を使用して .NET Core CLI で単体テストを作成する](unit-testing-visual-basic-with-nunit.md)。
* [*MSTest* と *Visual Basic* を使用して .NET Core CLI で単体テストを作成する](unit-testing-visual-basic-with-mstest.md)。

使用するクラス ライブラリと単体テスト ライブラリには、さまざまな言語を選択できます。 先述のチュートリアルをうまく組み合わせることで、使用方法を学習できます。

* Visual Studio Enterprise は、.NET Core の優れたテスト ツールを提供します。 [Live Unit Testing](/visualstudio/test/live-unit-testing) または[コード カバレッジ](https://github.com/Microsoft/vstest-docs/blob/master/docs/analyze.md#working-with-code-coverage)をご確認ください。
* 選択的単体テストのフィルター処理の使用方法に関する詳細と例については、「[選択的単体テストの実行](selective-unit-tests.md)」のページ、または [Visual Studio を使用したテストの組み込みと除外](/visualstudio/test/live-unit-testing#include-and-exclude-test-projects-and-test-methods)に関するトピックをご覧ください。
* xUnit チームは、[.NET Core および Visual Studio で xUnit を使用する方法](https://xunit.github.io/docs/getting-started-dotnet-core.html)を示すチュートリアルを作成しました。
