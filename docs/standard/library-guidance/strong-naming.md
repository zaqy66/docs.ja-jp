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
# <a name="strong-naming"></a><span data-ttu-id="232c2-103">厳密な名前付け</span><span class="sxs-lookup"><span data-stu-id="232c2-103">Strong naming</span></span>

<span data-ttu-id="232c2-104">生成キーを持つアセンブリの署名とは厳密な名前付け、[アセンブリの厳密な名前](../../framework/app-domains/strong-named-assemblies.md)します。</span><span class="sxs-lookup"><span data-stu-id="232c2-104">Strong naming refers to signing an assembly with a key, producing a [strong-named assembly](../../framework/app-domains/strong-named-assemblies.md).</span></span> <span data-ttu-id="232c2-105">アセンブリは、厳密な名前が、名前とアセンブリのバージョン番号に基づく一意の id を作成し、アセンブリの競合を防止できます。</span><span class="sxs-lookup"><span data-stu-id="232c2-105">When an assembly is strong-named, it creates a unique identity based on the name and assembly version number, and it can help prevent assembly conflicts.</span></span>

<span data-ttu-id="232c2-106">厳密な名前付けの欠点は、Windows 上の .NET Framework により、アセンブリが厳密な名前とアセンブリの厳密な読み込みことです。</span><span class="sxs-lookup"><span data-stu-id="232c2-106">The downside to strong naming is that the .NET Framework on Windows enables strict loading of assemblies once an assembly is strong named.</span></span> <span data-ttu-id="232c2-107">厳密な名前付きのアセンブリの参照を強制的に開発者が、アセンブリによって参照されているバージョンと一致する必要があります[バインド リダイレクトを構成する](../../framework/configure-apps/redirect-assembly-versions.md)アセンブリを使用する場合。</span><span class="sxs-lookup"><span data-stu-id="232c2-107">A strong-named assembly reference must exactly match the version referenced by an assembly, forcing developers to [configure binding redirects](../../framework/configure-apps/redirect-assembly-versions.md) when using the assembly:</span></span>

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

<span data-ttu-id="232c2-108">.NET 開発者は、厳密な名前付けに関する警告を出したり、ときに、厳密なアセンブリの読み込みにはどのようないる通常気候について文句です。</span><span class="sxs-lookup"><span data-stu-id="232c2-108">When .NET developers complain about strong naming, what they're usually complaining about is strict assembly loading.</span></span> <span data-ttu-id="232c2-109">さいわい、この問題は、.NET Framework に分離されます。</span><span class="sxs-lookup"><span data-stu-id="232c2-109">Fortunately, this issue is isolated to the .NET Framework.</span></span> <span data-ttu-id="232c2-110">.NET core、Xamarin、UWP、およびその他のほとんどの .NET 実装は、厳密なアセンブリの読み込みに必要はありませんし、厳密な名前付けの主な欠点を削除します。</span><span class="sxs-lookup"><span data-stu-id="232c2-110">.NET Core, Xamarin, UWP, and most other .NET implementations don't have strict assembly loading and removes the main downside of strong naming.</span></span>

<span data-ttu-id="232c2-111">厳密な名前付けの 1 つの重要な側面はウイルスである: 強力なという名前のアセンブリが唯一の参照の他の厳密な名前付きアセンブリ。</span><span class="sxs-lookup"><span data-stu-id="232c2-111">One important aspect of strong naming is that it's viral: a strong named assembly can only reference other strong named assemblies.</span></span> <span data-ttu-id="232c2-112">ライブラリが厳密な名前付きしていない場合は、アプリケーションまたはそれを使用してから、厳密な名前付けが必要なライブラリを構築する開発者を除外います。</span><span class="sxs-lookup"><span data-stu-id="232c2-112">If your library isn't strong named, then you have excluded developers who are building an application or library that needs strong naming from using it.</span></span>

<span data-ttu-id="232c2-113">厳密な名前付けの利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="232c2-113">The benefits of strong naming are:</span></span>

1. <span data-ttu-id="232c2-114">アセンブリの参照し、その他の厳密な名前のアセンブリで使用されることができます。</span><span class="sxs-lookup"><span data-stu-id="232c2-114">The assembly can be referenced and used by other strong-named assemblies.</span></span>
2. <span data-ttu-id="232c2-115">アセンブリはグローバル アセンブリ キャッシュ (GAC) に格納できます。</span><span class="sxs-lookup"><span data-stu-id="232c2-115">The assembly can be stored in the Global Assembly Cache (GAC).</span></span>
3. <span data-ttu-id="232c2-116">アセンブリは、アセンブリの他のバージョンと並行読み込まれることができます。</span><span class="sxs-lookup"><span data-stu-id="232c2-116">The assembly can be loaded side by side with other versions of the assembly.</span></span> <span data-ttu-id="232c2-117">サイド バイ サイド アセンブリの読み込みは一般に、プラグイン アーキテクチャを持つアプリケーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="232c2-117">Side-by-side assembly loading is commonly required by applications with plug-in architectures.</span></span>

## <a name="create-strong-named-net-libraries"></a><span data-ttu-id="232c2-118">強力な .NET ライブラリをという名前の作成します。</span><span class="sxs-lookup"><span data-stu-id="232c2-118">Create strong named .NET libraries</span></span>

<span data-ttu-id="232c2-119">オープン ソース .NET ライブラリは、厳密な名前必要があります。</span><span class="sxs-lookup"><span data-stu-id="232c2-119">You should strong name your open-source .NET libraries.</span></span> <span data-ttu-id="232c2-120">厳密なアセンブリの名前を付けにより、ほとんどの人がそれを使用し、厳密なアセンブリの読み込みのみが、.NET Framework に影響します。</span><span class="sxs-lookup"><span data-stu-id="232c2-120">Strong naming an assembly ensures the most people can use it, and strict assembly loading only affects the .NET Framework.</span></span>

> [!NOTE]
> <span data-ttu-id="232c2-121">このガイダンスは、.NET ライブラリは、NuGet.org に公開など、公開されている分散型の .NET ライブラリに固有です。厳密な名前付けと、ほとんどの .NET アプリケーションでは必要ありません、されません既定で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="232c2-121">This guidance is specific to publicly distributed .NET libraries, such as .NET libraries published on NuGet.org. Strong naming is not required by most .NET applications and should not be done by default.</span></span>

<span data-ttu-id="232c2-122">**✔️ をご検討ください**ライブラリのアセンブリの名前付け強力な。</span><span class="sxs-lookup"><span data-stu-id="232c2-122">**✔️ CONSIDER** strong naming your library's assemblies.</span></span>

<span data-ttu-id="232c2-123">**✔️ をご検討ください**でソース管理システムに厳密な名前に使用するキーを確認します。</span><span class="sxs-lookup"><span data-stu-id="232c2-123">**✔️ CONSIDER** checking in the key used to strong name into your source control system.</span></span>

> <span data-ttu-id="232c2-124">公開キーには、開発者は変更し、同じキーを持つライブラリのソース コードを再コンパイルができます。</span><span class="sxs-lookup"><span data-stu-id="232c2-124">A publicly available key lets developers modify and recompile your library source code with the same key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="232c2-125">暗号化、id が必要なときに[Authenticode](/windows-hardware/drivers/install/authenticode)と[NuGet パッケージに署名](/nuget/create-packages/sign-a-package)はお勧めします。</span><span class="sxs-lookup"><span data-stu-id="232c2-125">When a cryptographic identity is desired, [Authenticode](/windows-hardware/drivers/install/authenticode) and [NuGet Package Signing](/nuget/create-packages/sign-a-package) are recommended.</span></span> <span data-ttu-id="232c2-126">セキュリティに関する考慮事項厳密な名前付けを使用しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="232c2-126">Strong naming should not be used for security considerations.</span></span>

<span data-ttu-id="232c2-127">**✔️ をご検討ください**バインディングのリダイレクト、および更新される頻度を減らすユーザーを支援する唯一のメジャー バージョンの変更でアセンブリのバージョンをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="232c2-127">**✔️ CONSIDER** incrementing the assembly version on only major version changes to help users reduce binding redirects, and how often they're updated.</span></span>

> <span data-ttu-id="232c2-128">詳細をご覧ください[バージョン管理とアセンブリのバージョン](./versioning.md#assembly-version)します。</span><span class="sxs-lookup"><span data-stu-id="232c2-128">Read more about [versioning and the assembly version](./versioning.md#assembly-version).</span></span>

<span data-ttu-id="232c2-129">**❌ しない**を追加、削除、または厳密な名前付けのキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="232c2-129">**❌ DO NOT** add, remove, or change the strong naming key.</span></span>

> <span data-ttu-id="232c2-130">アセンブリの厳密な名前付けキーの変更では、アセンブリの id を変更し、それを使用するコンパイル済みコードを中断します。</span><span class="sxs-lookup"><span data-stu-id="232c2-130">Modifying an assembly's strong naming key changes the assembly's identity and breaks compiled code that uses it.</span></span> <span data-ttu-id="232c2-131">詳細については、次を参照してください。[バイナリの互換性に影響する変更](./breaking-changes.md#binary-breaking-change)します。</span><span class="sxs-lookup"><span data-stu-id="232c2-131">For more information, see [binary breaking changes](./breaking-changes.md#binary-breaking-change).</span></span>

<span data-ttu-id="232c2-132">**❌ しない**ライブラリの厳密な名前し、厳密な名前を持たないバージョンを発行します。</span><span class="sxs-lookup"><span data-stu-id="232c2-132">**❌ DO NOT** publish strong-named and non-strong-named versions of your library.</span></span> <span data-ttu-id="232c2-133">たとえば、`Contoso.Api` と`Contoso.Api.StrongNamed` です。</span><span class="sxs-lookup"><span data-stu-id="232c2-133">For example, `Contoso.Api` and `Contoso.Api.StrongNamed`.</span></span>

> <span data-ttu-id="232c2-134">開発者の環境のシステム パッケージの 2 つの分岐を発行します。</span><span class="sxs-lookup"><span data-stu-id="232c2-134">Publishing two packages forks your developer eco-system.</span></span> <span data-ttu-id="232c2-135">また、両方のパッケージによって最終的に、アプリケーションの場合、開発者には型名の競合が発生する可能性です。</span><span class="sxs-lookup"><span data-stu-id="232c2-135">Also, if an application ends up depending on both packages the developer can encounter type name conflicts.</span></span> <span data-ttu-id="232c2-136">.NET のに関してはさまざまなアセンブリ内のさまざまな種類です。</span><span class="sxs-lookup"><span data-stu-id="232c2-136">As far as .NET is concerned they are different types in different assemblies.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="232c2-137">[前へ](./cross-platform-targeting.md)
[次へ](./nuget.md)</span><span class="sxs-lookup"><span data-stu-id="232c2-137">[Previous](./cross-platform-targeting.md)
[Next](./nuget.md)</span></span>
