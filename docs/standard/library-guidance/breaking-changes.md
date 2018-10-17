---
title: 重大な変更と .NET ライブラリ
description: .NET ライブラリを作成するときに重大な変更を移動するための推奨されるベスト プラクティスです。
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 83c01fdad7d836877bf692b87eeb0230219ded36
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370339"
---
# <a name="breaking-changes"></a><span data-ttu-id="9402b-103">重大な変更</span><span class="sxs-lookup"><span data-stu-id="9402b-103">Breaking changes</span></span>

<span data-ttu-id="9402b-104">既存のユーザーの安定性と今後のイノベーションの間のバランスを見つけるための .NET ライブラリの重要です。</span><span class="sxs-lookup"><span data-stu-id="9402b-104">It's important for a .NET library to find a balance between stability for existing users and innovation for the future.</span></span> <span data-ttu-id="9402b-105">ライブラリの作成者は、リファクタリングとコードについての再考完璧ですが、既存のユーザーの重大な低レベルのライブラリの特に、悪影響を及ぼしますまでに向かってリーンします。</span><span class="sxs-lookup"><span data-stu-id="9402b-105">Library authors lean towards refactoring and rethinking code until it's perfect, but breaking your existing users has a negative impact, especially for low-level libraries.</span></span>

## <a name="project-types-and-breaking-changes"></a><span data-ttu-id="9402b-106">プロジェクトの種類と重大な変更</span><span class="sxs-lookup"><span data-stu-id="9402b-106">Project types and breaking changes</span></span>

<span data-ttu-id="9402b-107">.NET コミュニティでライブラリを使用する方法は、エンドユーザー開発者に重大な変更の効果を変更します。</span><span class="sxs-lookup"><span data-stu-id="9402b-107">How a library is used by the .NET community changes the effect of breaking changes on end-user developers.</span></span>

* <span data-ttu-id="9402b-108">**低、中レベルのライブラリ**シリアライザー、HTML パーサー、データベースのオブジェクト リレーショナル マッパー、または web フレームワークのように、最も影響を受けるで重大な変更。</span><span class="sxs-lookup"><span data-stu-id="9402b-108">**Low and middle-level libraries** like a serializer, HTML parser, database object-relational mapper, or web framework are the most affected by breaking changes.</span></span>

  <span data-ttu-id="9402b-109">パッケージのビルド ブロックでは、エンドユーザー開発者は、アプリケーションを作成、およびその他のライブラリを NuGet の依存関係として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9402b-109">Building block packages are used by end-user developers to build applications, and by other libraries as NuGet dependencies.</span></span> <span data-ttu-id="9402b-110">たとえば、アプリケーションを構築し、web サービスを呼び出す、オープン ソースのクライアントを使用しています。</span><span class="sxs-lookup"><span data-stu-id="9402b-110">For example, you're building an application and are using an open-source client to call a web service.</span></span> <span data-ttu-id="9402b-111">クライアントを使用して依存関係に重大な更新プログラムを修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="9402b-111">A breaking update to a dependency the client uses isn't something you can fix.</span></span> <span data-ttu-id="9402b-112">変更する必要のあるオープン ソースのクライアントがあり、制御はありません。</span><span class="sxs-lookup"><span data-stu-id="9402b-112">It's the open-source client that needs to be changed and you have no control over it.</span></span> <span data-ttu-id="9402b-113">互換性のあるバージョンのライブラリを検索またはクライアント ライブラリへの修正の送信し、新しいバージョンを待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9402b-113">You have to find compatible versions of the libraries or submit a fix to the client library and wait for a new version.</span></span> <span data-ttu-id="9402b-114">最悪の状況では、3 番目のライブラリの互換性のないバージョンに依存する 2 つのライブラリを使用するかどうかです。</span><span class="sxs-lookup"><span data-stu-id="9402b-114">The worst-case situation is if you want to use two libraries that depend on mutually incompatible versions of a third library.</span></span>

* <span data-ttu-id="9402b-115">**高度なライブラリ**UI の一連のようなコントロールは、重大な変更を受けにくい。</span><span class="sxs-lookup"><span data-stu-id="9402b-115">**High-level libraries** like a suite of UI controls are less sensitive to breaking changes.</span></span>

  <span data-ttu-id="9402b-116">高度なライブラリは、エンド ユーザー アプリケーションで直接参照されます。</span><span class="sxs-lookup"><span data-stu-id="9402b-116">High-level libraries are directly referenced in an end-user application.</span></span> <span data-ttu-id="9402b-117">重大な変更が発生した場合、開発者は最新のバージョンに更新することができます。 または重大な変更を使用するには、そのアプリケーションを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="9402b-117">If breaking changes occur, the developer can choose to update to the latest version, or can modify their application to work with the breaking change.</span></span>

<span data-ttu-id="9402b-118">**✔️ は**ライブラリの使用方法について考えてみてください。</span><span class="sxs-lookup"><span data-stu-id="9402b-118">**✔️ DO** think about how your library will be used.</span></span> <span data-ttu-id="9402b-119">どのような効果のアプリケーションおよびそれを使用するライブラリで重大な変更がありますか。</span><span class="sxs-lookup"><span data-stu-id="9402b-119">What effect will breaking changes have on applications and libraries that use it?</span></span>

<span data-ttu-id="9402b-120">**✔️ は**低レベルの .NET ライブラリを開発する際に、重大な変更を最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="9402b-120">**✔️ DO** minimize breaking changes when developing a low-level .NET library.</span></span>

<span data-ttu-id="9402b-121">**✔️ をご検討ください**新しい NuGet パッケージとして、ライブラリの書き換え、大規模なを発行します。</span><span class="sxs-lookup"><span data-stu-id="9402b-121">**✔️ CONSIDER** publishing a major rewrite of a library as a new NuGet package.</span></span>

## <a name="types-of-breaking-changes"></a><span data-ttu-id="9402b-122">重大な変更の種類</span><span class="sxs-lookup"><span data-stu-id="9402b-122">Types of breaking changes</span></span>

<span data-ttu-id="9402b-123">重大な変更では、さまざまなカテゴリに分類されは均等にインパクトのあります。</span><span class="sxs-lookup"><span data-stu-id="9402b-123">Breaking changes fall into different categories and aren't equally impactful.</span></span>

### <a name="source-breaking-change"></a><span data-ttu-id="9402b-124">ソースの重大な変更</span><span class="sxs-lookup"><span data-stu-id="9402b-124">Source breaking change</span></span>

<span data-ttu-id="9402b-125">互換性に影響する変更のソースは、プログラムの実行には影響しませんが、次回、アプリケーションが再コンパイルされるコンパイル エラーが発生されます。</span><span class="sxs-lookup"><span data-stu-id="9402b-125">A source breaking change doesn't affect program execution but will cause compilation errors the next time the application is recompiled.</span></span> <span data-ttu-id="9402b-126">たとえば、新しいオーバー ロードは、以前は、あいまいなされたメソッドの呼び出しで、あいまいさを作成できます。 または名前が変更されたパラメーターの名前付きパラメーターを使用する呼び出し元が中断します。</span><span class="sxs-lookup"><span data-stu-id="9402b-126">For example, a new overload can create an ambiguity in method calls that were unambiguous previously, or a renamed parameter will break callers that use named parameters.</span></span>

```csharp
public class Task
{
    // Adding a type called Task could conflict with System.Threading.Tasks.Task at compilation
}
```

<span data-ttu-id="9402b-127">開発者が自分のアプリケーションを再コンパイル時に、互換性に影響する変更のソースは害を及ぼすだけであるため、最も無難な重大な変更になります。</span><span class="sxs-lookup"><span data-stu-id="9402b-127">Because a source breaking change is only harmful when developers recompile their applications, it's the least disruptive breaking change.</span></span> <span data-ttu-id="9402b-128">開発者は、独自の切断されたソース コードを簡単に修正できます。</span><span class="sxs-lookup"><span data-stu-id="9402b-128">Developers can fix their own broken source code easily.</span></span>

### <a name="behavior-breaking-change"></a><span data-ttu-id="9402b-129">動作の変更点</span><span class="sxs-lookup"><span data-stu-id="9402b-129">Behavior breaking change</span></span>

<span data-ttu-id="9402b-130">動作の変更は互換性に影響する変更の最も一般的な種類: 動作のほぼすべての変更では、だれかが中断します。</span><span class="sxs-lookup"><span data-stu-id="9402b-130">Behavior changes are the most common type of breaking change: almost any change in behavior could break someone.</span></span> <span data-ttu-id="9402b-131">例外がスローまたは入力または出力メソッドのシグネチャなど、ライブラリに変更をデータ形式の場合は、すべて悪影響を及ぼす可能性、ライブラリのコンシューマーです。</span><span class="sxs-lookup"><span data-stu-id="9402b-131">Changes to your library, such as method signatures, exceptions thrown or input or output data formats, could all negatively impact your library consumers.</span></span> <span data-ttu-id="9402b-132">ユーザーが既に中断されている動作に依存している場合、重大な変更として、バグ修正もが参加できます。</span><span class="sxs-lookup"><span data-stu-id="9402b-132">Even a bug fix can qualify as a breaking change if users relied on the previously broken behavior.</span></span>

<span data-ttu-id="9402b-133">機能の追加と、不適切な動作の向上は、良いことですが、不注意ために使用する既存のユーザーをアップグレードするは非常に困難です。</span><span class="sxs-lookup"><span data-stu-id="9402b-133">Adding features and improving bad behaviors is a good thing, but without care it can make it very hard for existing users to upgrade.</span></span> <span data-ttu-id="9402b-134">開発者は、重大な変更の動作を扱う方法の 1 つの設定の背後にある非表示にすることです。</span><span class="sxs-lookup"><span data-stu-id="9402b-134">One approach to helping developers deal with behavior breaking changes is to hide them behind settings.</span></span> <span data-ttu-id="9402b-135">設定は、開発者が同時にオプトインまたは重大な変更をオプトアウトすることを選択しながら、ライブラリの最新バージョンに更新を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9402b-135">Settings let developers update to the latest version of your library while at the same time choosing to opt in or opt out of breaking changes.</span></span> <span data-ttu-id="9402b-136">この戦略では、開発者は最新に保たれますながら、使用側コードが時間の経過と共に調整ができます。</span><span class="sxs-lookup"><span data-stu-id="9402b-136">This strategy lets developers stay up to date while letting their consuming code adapt over time.</span></span>

<span data-ttu-id="9402b-137">たとえば、ASP.NET Core MVC にはの概念、[互換性バージョン](/aspnet/core/mvc/compatibility-version)有効、無効になって機能を変更する`MvcOptions`します。</span><span class="sxs-lookup"><span data-stu-id="9402b-137">For example, ASP.NET Core MVC has the concept of a [compatibility version](/aspnet/core/mvc/compatibility-version) that modifies the features enabled and disabled on `MvcOptions`.</span></span>

<span data-ttu-id="9402b-138">**✔️ をご検討ください**開発者設定が機能することを選択できるように、既存のユーザーに影響を与える場合は、既定では、の新機能を終了します。</span><span class="sxs-lookup"><span data-stu-id="9402b-138">**✔️ CONSIDER** leaving new features off by default, if they affect existing users, and let developers opt in to the feature with a setting.</span></span>

### <a name="binary-breaking-change"></a><span data-ttu-id="9402b-139">バイナリの重大な変更</span><span class="sxs-lookup"><span data-stu-id="9402b-139">Binary breaking change</span></span>

<span data-ttu-id="9402b-140">変更の重大なバイナリの場合は、ライブラリのパブリック API を変更するために対してコンパイルされたアセンブリ、ライブラリの以前のバージョンで、不要になった API を呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="9402b-140">A binary breaking change happens when you change the public API of your library, so assemblies compiled against older versions of your library are no longer able to call the API.</span></span> <span data-ttu-id="9402b-141">たとえば、新しいパラメーターを追加することで、メソッドのシグネチャを変更すると、ライブラリの以前のバージョンに対してコンパイルされたアセンブリでスローする、<xref:System.MissingMethodException>します。</span><span class="sxs-lookup"><span data-stu-id="9402b-141">For example, changing a method's signature by adding a new parameter will cause assemblies compiled against the older version of the library to throw a <xref:System.MissingMethodException>.</span></span>

<span data-ttu-id="9402b-142">変更の重大なバイナリでも改ページは、**アセンブリ全体**します。</span><span class="sxs-lookup"><span data-stu-id="9402b-142">A binary breaking change can also break an **entire assembly**.</span></span> <span data-ttu-id="9402b-143">アセンブリの名前を変更する`AssemblyName`の追加、削除、またはアセンブリの厳密な名前付けのキーを変更するには、アセンブリの id を変更します。</span><span class="sxs-lookup"><span data-stu-id="9402b-143">Renaming an assembly with `AssemblyName` will change the assembly's identity, as will adding, removing, or changing the assembly's strong naming key.</span></span> <span data-ttu-id="9402b-144">アセンブリの id の変更は、それを使用するすべてのコンパイル済みコードで中断されます。</span><span class="sxs-lookup"><span data-stu-id="9402b-144">A change of an assembly's identity will break all compiled code that uses it.</span></span>

<span data-ttu-id="9402b-145">**❌ しない**アセンブリ名を変更します。</span><span class="sxs-lookup"><span data-stu-id="9402b-145">**❌ DO NOT** change an assembly name.</span></span>

<span data-ttu-id="9402b-146">**❌ しない**を追加、削除、または厳密な名前付けのキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="9402b-146">**❌ DO NOT** add, remove, or change the strong naming key.</span></span>

<span data-ttu-id="9402b-147">**✔️ をご検討ください**インターフェイスではなく抽象基本クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="9402b-147">**✔️ CONSIDER** using abstract base classes instead of interfaces.</span></span>

> <span data-ttu-id="9402b-148">インターフェイスに何も追加すると、失敗するそれを実装する既存の型。</span><span class="sxs-lookup"><span data-stu-id="9402b-148">Adding anything to an interface will cause existing types that implement it to fail.</span></span> <span data-ttu-id="9402b-149">抽象基本クラスを使用すると、既定の仮想実装を追加できます。</span><span class="sxs-lookup"><span data-stu-id="9402b-149">An abstract base class allows you to add a default virtual implementation.</span></span>

<span data-ttu-id="9402b-150">**✔️ をご検討ください**を配置すること、<xref:System.ObsoleteAttribute>の型とメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9402b-150">**✔️ CONSIDER** placing the <xref:System.ObsoleteAttribute> on types and members that you intend to remove.</span></span> <span data-ttu-id="9402b-151">属性、廃止された API を使用しないコードを更新するための手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="9402b-151">The attribute should have instructions for updating code to no longer use the obsolete API.</span></span>

> <span data-ttu-id="9402b-152">型およびメソッドを呼び出すコードを<xref:System.ObsoleteAttribute>属性に指定されたメッセージでビルド警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="9402b-152">Code that calls types and methods with the <xref:System.ObsoleteAttribute> will generate a build warning with the message supplied to the attribute.</span></span> <span data-ttu-id="9402b-153">移行のほとんどが不要になったは廃止された API が削除されるようにする古い API サーフェスの時間を使用する警告できるようにユーザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="9402b-153">The warnings give people who use the obsolete API surface time to migrate so that when the obsolete API is removed, most are no longer using it.</span></span>

```csharp
public class Document
{
    [Obsolete("LoadDocument(string) is obsolete. Use LoadDocument(Uri) instead.")]
    public static Document LoadDocument(string uri)
    {
        return LoadDocument(new Uri(uri));
    }

    public static Document LoadDocument(Uri uri)
    {
        // Load the document
    }
}
```

## <a name="see-also"></a><span data-ttu-id="9402b-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="9402b-154">See also</span></span>

* [<span data-ttu-id="9402b-155">C# 開発者向けのバージョンと更新プログラムに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="9402b-155">Version and update considerations for C# developers</span></span>](../../csharp/whats-new/version-update-considerations.md)
* [<span data-ttu-id="9402b-156">.NET での API に重大な変更に説明するもの</span><span class="sxs-lookup"><span data-stu-id="9402b-156">A definitive guide to API-breaking changes in .NET</span></span>](https://stackoverflow.com/questions/1456785/a-definitive-guide-to-api-breaking-changes-in-net)
* [<span data-ttu-id="9402b-157">CoreFX 互換性に影響する変更ルール</span><span class="sxs-lookup"><span data-stu-id="9402b-157">CoreFX Breaking Change Rules</span></span>](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/breaking-change-rules.md)

>[!div class="step-by-step"]
[<span data-ttu-id="9402b-158">前へ</span><span class="sxs-lookup"><span data-stu-id="9402b-158">Previous</span></span>](./versioning.md)
