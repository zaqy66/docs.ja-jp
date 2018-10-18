---
title: オープン ソース ライブラリのガイダンス
description: 高品質の .NET ライブラリを作成するための開発者向けのベスト プラクティスとしての推奨事項。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 50fb745f7eb65abcaca76cebaf9991c48f559e59
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374902"
---
# <a name="open-source-library-guidance"></a><span data-ttu-id="b88be-103">オープン ソース ライブラリのガイダンス</span><span class="sxs-lookup"><span data-stu-id="b88be-103">Open-source library guidance</span></span>

<span data-ttu-id="b88be-104">このガイドでは、高品質の .NET ライブラリを作成するための開発者向け推奨事項を説明します。</span><span class="sxs-lookup"><span data-stu-id="b88be-104">This guidance provides recommendations for developers to create high-quality .NET libraries.</span></span> <span data-ttu-id="b88be-105">このドキュメントでは、.NET ライブラリを構築するときの、"*方法*" ではなく、"*内容*" と "*理由*" について説明します。</span><span class="sxs-lookup"><span data-stu-id="b88be-105">This documentation focuses on the *what* and the *why* when building a .NET library, not the *how*.</span></span>

<span data-ttu-id="b88be-106">高品質のオープン ソースの .NET ライブラリの特徴:</span><span class="sxs-lookup"><span data-stu-id="b88be-106">Aspects of high-quality open-source .NET libraries:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="b88be-107">**包括的である** - 多くのプラットフォームやアプリケーションをサポートするように、適切な .NET ライブラリで対応しています。</span><span class="sxs-lookup"><span data-stu-id="b88be-107">**Inclusive** - Good .NET libraries strive to support many platforms and applications.</span></span>
> * <span data-ttu-id="b88be-108">**安定している** - 適切な .NET ライブラリが .NET エコシステム内で共存しており、多くのライブラリを使用してビルドされたアプリケーション内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="b88be-108">**Stable** - Good .NET libraries coexist in the .NET ecosystem, running in applications built with many libraries.</span></span>
> * <span data-ttu-id="b88be-109">**進化するように設計されている** - .NET ライブラリは、既存のユーザーをサポートしながら、時間の経過と共に改善され進化します。</span><span class="sxs-lookup"><span data-stu-id="b88be-109">**Designed to evolve** - .NET libraries should improve and evolve over time, while supporting existing users.</span></span>
> * <span data-ttu-id="b88be-110">**デバッグできる** - .NET ライブラリでは、最新のツールを使用してユーザー向けの優れたデバッグ エクスペリエンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b88be-110">**Debuggable** - .NET libraries should use the latest tools to create a great debugging experience for users.</span></span>
> * <span data-ttu-id="b88be-111">**信頼されている** - .NET ライブラリは、セキュリティのベスト プラクティスを使用して NuGet に発行することにより、開発者から信頼されています。</span><span class="sxs-lookup"><span data-stu-id="b88be-111">**Trusted** - .NET libraries have developers' trust by publishing to NuGet using security best practices.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="b88be-112">開始するには</span><span class="sxs-lookup"><span data-stu-id="b88be-112">Get Started</span></span>](./get-started.md)

## <a name="recommendations"></a><span data-ttu-id="b88be-113">推奨事項</span><span class="sxs-lookup"><span data-stu-id="b88be-113">Recommendations</span></span>

<span data-ttu-id="b88be-114">各記事には、**実施**、**検討**、**回避**、**実施しない**という表現を使用して示した、ご利用の .NET ライブラリに対する推奨事項の一覧が記載されています。</span><span class="sxs-lookup"><span data-stu-id="b88be-114">With each article, there is a list of recommendations for your .NET library using **Do**, **Consider**, **Avoid**, and **Do not**.</span></span> <span data-ttu-id="b88be-115">各推奨事項の内容は、どの程度厳密に従う必要があるかを示します。</span><span class="sxs-lookup"><span data-stu-id="b88be-115">The wording of each recommendation indicates how strongly it should be followed.</span></span>

<span data-ttu-id="b88be-116">**実施**推奨事項は、ほとんどすべての場合に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b88be-116">A **Do** recommendation is one that should almost always be followed:</span></span>

<span data-ttu-id="b88be-117">NuGet パッケージを使用してご利用のライブラリの配布を **✔️ 実施**してください。</span><span class="sxs-lookup"><span data-stu-id="b88be-117">**✔️ DO** distribute your library using a NuGet package.</span></span>

<span data-ttu-id="b88be-118">その一方で、**検討**推奨事項は、一般に実施する必要がありますが、ルールには正当な例外があり、ガイダンスに従っていないことを気する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b88be-118">On the other hand, **Consider** recommendations should generally be followed, but there are legitimate exceptions to the rule and you shouldn't feel bad about not following the guidance:</span></span>

<span data-ttu-id="b88be-119">ご利用の NuGet パッケージのバージョンに [SemVer 2.0.0](https://semver.org/) を使用することを **✔️ 検討**してください。</span><span class="sxs-lookup"><span data-stu-id="b88be-119">**✔️ CONSIDER** using [SemVer 2.0.0](https://semver.org/) to version your NuGet package.</span></span>

<span data-ttu-id="b88be-120">**回避**推奨事項は一般には良いアイデアではありませんが、規則に違反することが効果的である場合があります。</span><span class="sxs-lookup"><span data-stu-id="b88be-120">**Avoid** recommendations are things that are generally not a good idea, but breaking the rule sometimes makes sense:</span></span>

<span data-ttu-id="b88be-121">正確なバージョンを要求する NuGet パッケージは **❌ 回避**してください。</span><span class="sxs-lookup"><span data-stu-id="b88be-121">**❌ AVOID** NuGet package references that demand an exact version.</span></span>

<span data-ttu-id="b88be-122">最後に、**実施しない**は、ほとんどやってはいけないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b88be-122">And finally, **do not** indicates something you should almost never do:</span></span>

<span data-ttu-id="b88be-123">ご利用のライブラリに関して厳密な名前が指定されたバージョンおよび厳密でない名前が指定されたバージョンの発行は **❌ 実施しない**でください。</span><span class="sxs-lookup"><span data-stu-id="b88be-123">**❌ DO NOT** publish strong-named and non-strong-named versions of your library.</span></span> <span data-ttu-id="b88be-124">たとえば、`Contoso.Api` と`Contoso.Api.StrongNamed` です。</span><span class="sxs-lookup"><span data-stu-id="b88be-124">For example, `Contoso.Api` and `Contoso.Api.StrongNamed`.</span></span>

>[!div class="step-by-step"]
[<span data-ttu-id="b88be-125">次へ</span><span class="sxs-lookup"><span data-stu-id="b88be-125">Next</span></span>](./get-started.md)
