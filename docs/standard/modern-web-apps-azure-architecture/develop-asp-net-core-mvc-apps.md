---
title: ASP.NET Core MVC アプリの開発
description: ASP.NET Core および Azure での最新の Web アプリケーションの設計 | ASP.NET Core MVC アプリの開発
author: ardalis
ms.author: wiwagn
ms.date: 06/28/2018
ms.openlocfilehash: 2fd3eb1e123959130884b96ee9d2e59b83c41b0a
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404646"
---
# <a name="develop-aspnet-core-mvc-apps"></a><span data-ttu-id="3cd24-103">ASP.NET Core MVC アプリを開発する</span><span class="sxs-lookup"><span data-stu-id="3cd24-103">Develop ASP.NET Core MVC apps</span></span>

> <span data-ttu-id="3cd24-104">"最初から正しく理解する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-104">"It's not important to get it right the first time.</span></span> <span data-ttu-id="3cd24-105">しかし、最後に正しく理解していることは極めて重要です。"</span><span class="sxs-lookup"><span data-stu-id="3cd24-105">It's vitally important to get it right the last time."</span></span>  
> <span data-ttu-id="3cd24-106">_- Andrew Hunt、David Thomas_</span><span class="sxs-lookup"><span data-stu-id="3cd24-106">_- Andrew Hunt and David Thomas_</span></span>

<span data-ttu-id="3cd24-107">ASP.NET Core は、最新のクラウド向けに最適化された Web アプリケーションを構築するための、クロス プラットフォームのオープン ソース フレームワークです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-107">ASP.NET Core is a cross-platform, open-source framework for building modern cloud-optimized web applications.</span></span> <span data-ttu-id="3cd24-108">ASP.NET Core アプリは、軽量なモジュール形式であり、依存関係の挿入の組み込みサポートを備え、テストと保守の容易性を大幅に向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-108">ASP.NET Core apps are lightweight and modular, with built-in support for dependency injection, enabling greater testability and maintainability.</span></span> <span data-ttu-id="3cd24-109">ビュー ベースのアプリだけでなく最新の Web API の構築をサポートする MVC と組み合わせて、ASP.NET Core は、エンタープライズ Web アプリケーション構築のための強力なフレームワークになります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-109">Combined with MVC, which supports building modern web APIs in addition to view-based apps, ASP.NET Core is a powerful framework with which to build enterprise web applications.</span></span>

## <a name="mapping-requests-to-responses"></a><span data-ttu-id="3cd24-110">応答と要求のマッピング</span><span class="sxs-lookup"><span data-stu-id="3cd24-110">Mapping requests to responses</span></span>

<span data-ttu-id="3cd24-111">ASP.NET Core アプリの中心となる機能は、受信した要求を送信する応答にマップすることです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-111">At its heart, ASP.NET Core apps map incoming requests to outgoing responses.</span></span> <span data-ttu-id="3cd24-112">下位のレベルではこれはミドルウェアによって行われ、カスタム ミドルウェアのみで簡単な ASP.NET Core アプリとマイクロサービスを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-112">At a low level, this is done with middleware, and simple ASP.NET Core apps and microservices may be comprised solely of custom middleware.</span></span> <span data-ttu-id="3cd24-113">ASP.NET Core MVC を使うと、"_ルート_"、"_コントローラー_"、"_アクション_" など、さらに上位のレベルで操作することができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-113">When using ASP.NET Core MVC, you can work at a somewhat higher level, thinking in terms of _routes_, _controllers_, and _actions_.</span></span> <span data-ttu-id="3cd24-114">着信した各要求はアプリケーションのルーティング テーブルと比較され、一致するルートが見つかった場合、関連付けられている (コントローラーに属する) アクション メソッドが呼び出されて要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-114">Each incoming request is compared with the application's routing table, and if a matching route is found, the associated action method (belonging to a controller) is called to handle the request.</span></span> <span data-ttu-id="3cd24-115">一致するルートが見つからない場合は、エラー ハンドラーが呼び出されます (この場合、NotFound の結果を返します)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-115">If no matching route is found, an error handler (in this case, returning a NotFound result) is called.</span></span>

<span data-ttu-id="3cd24-116">ASP.NET Core MVC アプリは、規則ルートと属性ルートのどちらか一方または両方を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-116">ASP.NET Core MVC apps can use conventional routes, attribute routes, or both.</span></span> <span data-ttu-id="3cd24-117">規則ルートはコードで定義されており、次の例のような構文を使ってルーティングの "_規則_" を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-117">Conventional routes are defined in code, specifying routing _conventions_ using syntax like in the example below:</span></span>

```csharp
app.UseMvc(routes =>;
{
    routes.MapRoute("default","{controller=Home}/{action=Index}/{id?}");
});
```

<span data-ttu-id="3cd24-118">この例では、"default" という名前のルートがルーティング テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-118">In this example, a route named "default" has been added to the routing table.</span></span> <span data-ttu-id="3cd24-119">_controller_、_action_、_id_ のプレースホルダーでルート テンプレートを定義します。controller と action プレースホルダーには既定値が指定されており (それぞれ、"Home" と "Index")、id プレースホルダーは ("?" が適用されているので) 省略可能です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-119">It defines a route template with placeholders for _controller_, _action_, and _id_. The controller and action placeholders have default specified ("Home" and "Index", respectively), and the id placeholder is optional (by virtue of a "?" applied to it).</span></span> <span data-ttu-id="3cd24-120">ここで定義されている規則は、要求の最初の部分はコントローラーの名前に対応する必要があり、2 番目の部分はアクションに対応する必要があり、3 番目の部分は必要に応じて id パラメーターを表す、というものです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-120">The convention defined here states that the first part of a request should correspond to the name of the controller, the second part to the action, and then if necessary a third part will represent an id parameter.</span></span> <span data-ttu-id="3cd24-121">規則ルートは通常、Startup クラスの Configure メソッドなど、アプリケーションに対して 1 か所で定義されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-121">Conventional routes are typically defined in one place for the application, such as in the Configure method in the Startup class.</span></span>

<span data-ttu-id="3cd24-122">属性ルートは、グローバルに指定されるのではなく、コントローラーとアクションに直接適用されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-122">Attribute routes are applied to controllers and actions directly, rather than specified globally.</span></span> <span data-ttu-id="3cd24-123">この方法の場合、特定のメソッドを探しているときに検出しやすいという利点がありますが、ルーティング情報がアプリケーション内の 1 か所に保持されないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-123">This has the advantage of making them much more discoverable when you're looking at a particular method, but does mean that routing information is not kept in one place in the application.</span></span> <span data-ttu-id="3cd24-124">属性ルートでは、特定のアクションに対する複数ルートや、コントローラーとアクションの組み合わせルートを、簡単に指定できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-124">With attribute routes, you can easily specify multiple routes for a given action, as well as combine routes between controllers and actions.</span></span> <span data-ttu-id="3cd24-125">例:</span><span class="sxs-lookup"><span data-stu-id="3cd24-125">For example:</span></span>

```csharp
[Route("Home")]
public class HomeController : Controller
{
    [Route("")] // Combines to define the route template "Home"
    [Route("Index")] // Combines to define route template "Home/Index"
    [Route("/")] // Does not combine, defines the route template ""
    public IActionResult Index() {}
}
```

<span data-ttu-id="3cd24-126">ルートは [HttpGet] や同様の属性で指定することができ、[Route] 属性を別途追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-126">Routes can be specified on [HttpGet] and similar attributes, avoiding the need to add separate [Route] attributes.</span></span> <span data-ttu-id="3cd24-127">次に示すように、属性ルートではトークンを使って、コントローラーやアクションの名前を繰り返し指定する必要性を軽減することもできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-127">Attribute routes can also use tokens to reduce the need to repeat controller or action names, as shown below:</span></span>

```csharp
[Route("[controller\]")]
public class ProductsController : Controller
{
    [Route("")] // Matches 'Products'
    [Route("Index")] // Matches 'Products/Index'
    public IActionResult Index() {}
}
```

<span data-ttu-id="3cd24-128">特定の要求がルートと一致した後、アクション メソッドが呼び出される前に、ASP.NET Core MVC は要求に対して[モデル バインド](/aspnet/core/mvc/models/model-binding)と[モデル検証](/aspnet/core/mvc/models/validation)を実行します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-128">Once a given request has been matched to a route, but before the action method is called, ASP.NET Core MVC will perform [model binding](/aspnet/core/mvc/models/model-binding) and [model validation](/aspnet/core/mvc/models/validation) on the request.</span></span> <span data-ttu-id="3cd24-129">モデル バインドでは、着信した HTTP データが、呼び出されるアクション メソッドのパラメーターとして指定されている .NET 型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-129">Model binding is responsible for converting incoming HTTP data into the .NET types specified as parameters of the action method to be called.</span></span> <span data-ttu-id="3cd24-130">たとえば、アクション メソッドが int 型の ID パラメーターを必要としている場合、モデル バインドは要求の一部として指定された値からこのパラメーターを提供しようとします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-130">For example, if the action method expects an int id parameter, model binding will attempt to provide this parameter from a value provided as part of the request.</span></span> <span data-ttu-id="3cd24-131">そのために、モデル バインドは、ポストされたフォーム内、ルート自体、クエリ文字列で値を検索します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-131">To do so, model binding looks for values in a posted form, values in the route itself, and query string values.</span></span> <span data-ttu-id="3cd24-132">ID 値が見つかった場合は、整数に変換されてからアクション メソッドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-132">Assuming an id value is found, it will be converted to an integer before being passed into the action method.</span></span>

<span data-ttu-id="3cd24-133">モデルをバインドした後、アクション メソッドを呼び出す前に、モデルの検証が行われます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-133">After binding the model but before calling the action method, model validation occurs.</span></span> <span data-ttu-id="3cd24-134">モデルの検証では、モデルの種類に対するオプション属性が使われ、指定されたモデル オブジェクトが特定のデータ要件に準拠していることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-134">Model validation uses optional attributes on the model type, and can help ensure that the provided model object conforms to certain data requirements.</span></span> <span data-ttu-id="3cd24-135">特定の値を必須として指定したり、特定の長さや数値範囲に制限したりすることができます。検証属性が指定されていて、モデルがその要件に準拠していない場合は、ModelState.IsValid プロパティが false に設定され、準拠していない検証規則のセットを要求元のクライアントに送信できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-135">Certain values may be specified as required, or limited to a certain length or numeric range, etc. If validation attributes are specified but the model does not conform to their requirements, the property ModelState.IsValid will be false, and the set of failing validation rules will be available to send to the client making the request.</span></span>

<span data-ttu-id="3cd24-136">モデルの検証を使う場合は常に、状態変更コマンドを実行する前にモデルが有効であることを確認し、無効なデータによってアプリが破損しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-136">If you're using model validation, you should be sure to always check that the model is valid before performing any state-altering commands, to ensure your app is not corrupted by invalid data.</span></span> <span data-ttu-id="3cd24-137">[フィルター](/aspnet/core/mvc/controllers/filters)を使って、すべてのアクションにそのためのコードを追加しなくて済むようにできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-137">You can use a [filter](/aspnet/core/mvc/controllers/filters) to avoid the need to add code for this in every action.</span></span> <span data-ttu-id="3cd24-138">ASP.NET Core MVC フィルターを使うと、要求のグループをインターセプトして、共通のポリシーや横断的な事柄を特定の対象にだけ適用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-138">ASP.NET Core MVC filters offer a way of intercepting groups of requests, so that common policies and cross-cutting concerns can be applied on a targeted basis.</span></span> <span data-ttu-id="3cd24-139">フィルターは、個々のアクション、コントローラー全体、またはアプリケーション全体に適用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-139">Filters can be applied to individual actions, whole controllers, or globally for an application.</span></span>

<span data-ttu-id="3cd24-140">Web API に対しては、ASP.NET Core MVC は[_コンテンツ ネゴシエーション_](/aspnet/core/mvc/models/formatting)をサポートしており、応答の書式設定方法を要求で指定することができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-140">For web APIs, ASP.NET Core MVC supports [_content negotiation_](/aspnet/core/mvc/models/formatting), allowing requests to specify how responses should be formatted.</span></span> <span data-ttu-id="3cd24-141">要求で指定されたヘッダーに基づき、データを返すアクションは、XML、JSON、または他のサポートされている形式で応答を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-141">Based on headers provided in the request, actions returning data will format the response in XML, JSON, or another supported format.</span></span> <span data-ttu-id="3cd24-142">この機能を使うと、同じ API を、データ形式要件が異なる複数のクライアントで使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-142">This feature enables the same API to be used by multiple clients with different data format requirements.</span></span>

> ### <a name="references--mapping-requests-to-responses"></a><span data-ttu-id="3cd24-143">参照 – 応答と要求のマッピング</span><span class="sxs-lookup"><span data-stu-id="3cd24-143">References – Mapping Requests to Responses</span></span>
>
> - <span data-ttu-id="3cd24-144">**コントローラー アクションへのルーティング**
> <https://docs.microsoft.com/aspnet/core/mvc/controllers/routing></span><span class="sxs-lookup"><span data-stu-id="3cd24-144">**Routing to Controller Actions**
<https://docs.microsoft.com/aspnet/core/mvc/controllers/routing></span></span>
> - <span data-ttu-id="3cd24-145">**モデル バインド**
> <https://docs.microsoft.com/aspnet/core/mvc/models/model-binding></span><span class="sxs-lookup"><span data-stu-id="3cd24-145">**Model Binding**
<https://docs.microsoft.com/aspnet/core/mvc/models/model-binding></span></span>
> - <span data-ttu-id="3cd24-146">**モデルの検証**
> <https://docs.microsoft.com/aspnet/core/mvc/models/validation></span><span class="sxs-lookup"><span data-stu-id="3cd24-146">**Model Validation**
<https://docs.microsoft.com/aspnet/core/mvc/models/validation></span></span>
> - <span data-ttu-id="3cd24-147">**フィルター**
> <https://docs.microsoft.com/aspnet/core/mvc/controllers/filters></span><span class="sxs-lookup"><span data-stu-id="3cd24-147">**Filters**
<https://docs.microsoft.com/aspnet/core/mvc/controllers/filters></span></span>

## <a name="working-with-dependencies"></a><span data-ttu-id="3cd24-148">依存関係の使用</span><span class="sxs-lookup"><span data-stu-id="3cd24-148">Working with dependencies</span></span>

<span data-ttu-id="3cd24-149">ASP.NET Core は、[依存関係の挿入](/aspnet/core/fundamentals/dependency-injection)と呼ばれる手法の組み込みサポートを備えており、内部的に使用します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-149">ASP.NET Core has built-in support for and internally makes use of a technique known as [dependency injection](/aspnet/core/fundamentals/dependency-injection).</span></span> <span data-ttu-id="3cd24-150">依存関係の挿入は、アプリケーションの異なる部分間を疎結合できる手法です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-150">Dependency injection is a technique that enables loose coupling between different parts of an application.</span></span> <span data-ttu-id="3cd24-151">結合を緩くすることを、アプリケーションの各部分の分離が容易になり、部分ごとにテストや置換が可能になるため、望ましいことです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-151">Looser coupling is desirable because it makes it easier to isolate parts of the application, allowing for testing or replacement.</span></span> <span data-ttu-id="3cd24-152">また、アプリケーションの 1 つの部分に対する変更が、アプリケーションの別の場所に予期しない影響を与える可能性も低くなります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-152">It also makes it less likely that a change in one part of the application will have an unexpected impact somewhere else in the application.</span></span> <span data-ttu-id="3cd24-153">依存関係の挿入は、依存関係逆転 (Dependency Inversion) の原則に基づいており、多くの場合、開放/閉鎖 (Open/closed) の原則の実現に不可欠です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-153">Dependency injection is based on the dependency inversion principle, and is often key to achieving the open/closed principle.</span></span> <span data-ttu-id="3cd24-154">アプリケーションによる依存関係の処理方法を評価するときは、[静的な結び付き](https://deviq.com/static-cling/)を持つコードのにおいに注意し、"[new は接着剤である](https://ardalis.com/new-is-glue)" という格言を思い出してください。</span><span class="sxs-lookup"><span data-stu-id="3cd24-154">When evaluating how your application works with its dependencies, beware of the [static cling](https://deviq.com/static-cling/) code smell, and remember the aphorism "[new is glue](https://ardalis.com/new-is-glue)."</span></span>

<span data-ttu-id="3cd24-155">静的な結び付きは、クラスが静的メソッドを呼び出したとき、または静的プロパティにアクセスしたときに発生し、インフラストラクチャに対する副作用または依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-155">Static cling occurs when your classes make calls to static methods, or access static properties, which have side effects or dependencies on infrastructure.</span></span> <span data-ttu-id="3cd24-156">たとえば、あるメソッドが静的メソッドを呼び出し、その静的メソッドがデータベースに書き込む場合、元のメソッドはデータベースに密に結合されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-156">For example, if you have a method that calls a static method, which in turn writes to a database, your method is tightly coupled to the database.</span></span> <span data-ttu-id="3cd24-157">何かによってデータベース呼び出しが中断されると、メソッドも中断されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-157">Anything that breaks that database call will break your method.</span></span> <span data-ttu-id="3cd24-158">このようなメソッドのテストは、静的な呼び出しを模倣するために市販のモック ライブラリが必要になるか、またはテスト データベースを使ってしかテストできないため、非常に困難です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-158">Testing such methods is notoriously difficult, since such tests either require commercial mocking libraries to mock the static calls, or can only be tested with a test database in place.</span></span> <span data-ttu-id="3cd24-159">インフラストラクチャに対する依存関係のない静的呼び出しは (特に、完全にステートレスのもの)、問題なく呼び出すことができて、結合や (コードの結合だけでなく静的な呼び出し自体の) テスト可能性に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-159">Static calls that don't have any dependence on infrastructure, especially those that are completely stateless, are fine to call and have no impact on coupling or testability (beyond coupling code to the static call itself).</span></span>

<span data-ttu-id="3cd24-160">多くの開発者は、静的な結び付きとグローバルな状態のリスクを理解していますが、それでも直接的なインスタンス化によって特定の実装にコードを密接に結合します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-160">Many developers understand the risks of static cling and global state, but will still tightly couple their code to specific implementations through direct instantiation.</span></span> <span data-ttu-id="3cd24-161">"new は接着剤である" という格言は、この結合を喚起するものであり、new キーワードの使用を全般に非難しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-161">"New is glue" is meant to be a reminder of this coupling, and not a general condemnation of the use of the new keyword.</span></span> <span data-ttu-id="3cd24-162">静的メソッドの呼び出しと同様に、外部依存関係を持たない型の新しいインスタンスは通常、実装の詳細にコードを密接に結合したり、テストを困難にしたりすることはありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-162">Just as with static method calls, new instances of types that have no external dependencies typically do not tightly couple code to implementation details or make testing more difficult.</span></span> <span data-ttu-id="3cd24-163">ただし、クラスをインスタンス化するたびに、その特定のインスタンスをその特定の場所にハード コーディングすることに意味があるかどうか、またはそのインスタンスを依存関係として要求する方が優れた設計ではないかということを、少し検討してください。</span><span class="sxs-lookup"><span data-stu-id="3cd24-163">But each time a class is instantiated, take just a brief moment to consider whether it makes sense to hard-code that specific instance in that particular location, or if it would be a better design to request that instance as a dependency.</span></span>

### <a name="declare-your-dependencies"></a><span data-ttu-id="3cd24-164">依存関係の宣言</span><span class="sxs-lookup"><span data-stu-id="3cd24-164">Declare your dependencies</span></span>

<span data-ttu-id="3cd24-165">ASP.NET Core のメソッドとクラスは依存関係を宣言するようになっており、引数としてそれを要求します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-165">ASP.NET Core is built around having methods and classes declare their dependencies, requesting them as arguments.</span></span> <span data-ttu-id="3cd24-166">通常、ASP.NET アプリケーションは Startup クラスにおいてセットアップされ、Startup クラス自体が複数のポイントで依存関係の挿入をサポートするように構成されています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-166">ASP.NET applications are typically set up in a Startup class, which itself is configured to support dependency injection at several points.</span></span> <span data-ttu-id="3cd24-167">Startup クラスにコンストラクターがある場合は、次のように、コンストラクターで依存関係を要求できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-167">If your Startup class has a constructor, it can request dependencies through the constructor, like so:</span></span>

```csharp
public class Startup
{
    public Startup(IHostingEnvironment env)
    {
        var builder = new ConfigurationBuilder()
        .SetBasePath(env.ContentRootPath)
        .AddJsonFile("appsettings.json", optional: false, reloadOnChange: true)
        .AddJsonFile(\$"appsettings.{env.EnvironmentName}.json", optional: true);
    }
}
```

<span data-ttu-id="3cd24-168">Startup クラスの興味深い点は、明示的な型の要件がないことです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-168">The Startup class is interesting in that there are no explicit type requirements for it.</span></span> <span data-ttu-id="3cd24-169">特別な Startup 基底クラスを継承することなく、特定のインターフェイスも実装していません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-169">It doesn't inherit from a special Startup base class, nor does it implement any particular interface.</span></span> <span data-ttu-id="3cd24-170">コンストラクターを提供してもしなくてもよく、コンストラクターでは必要なだけいくつでもパラメーターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-170">You can give it a constructor, or not, and you can specify as many parameters on the constructor as you want.</span></span> <span data-ttu-id="3cd24-171">アプリケーション用に構成した Web ホストは、開始するとき、使うように指示された Startup クラスを呼び出し、依存関係の挿入を使って Startup クラスに必要なすべての依存関係を設定します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-171">When the web host you've configured for your application starts, it will call the Startup class you've told it to use, and will use dependency injection to populate any dependencies the Startup class requires.</span></span> <span data-ttu-id="3cd24-172">もちろん、ASP.NET Core によって使われるサービス コンテナーで構成されていないパラメーターを要求すると、例外が発生しますが、コンテナーが認識している依存関係を使っている限り、何でも自由に要求できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-172">Of course, if you request parameters that aren't configured in the services container used by ASP.NET Core, you'll get an exception, but as long as you stick to dependencies the container knows about, you can request anything you want.</span></span>

<span data-ttu-id="3cd24-173">依存関係の挿入は、最初に Startup インスタンスを作成したときから、ASP.NET Core アプリに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-173">Dependency injection is built into your ASP.NET Core apps right from the start, when you create the Startup instance.</span></span> <span data-ttu-id="3cd24-174">依存関係の挿入は Startup クラスだけの機能ではありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-174">It doesn't stop there for the Startup class.</span></span> <span data-ttu-id="3cd24-175">Configure メソッドで依存関係を要求することもできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-175">You can also request dependencies in the Configure method:</span></span>

```csharp
public void Configure(IApplicationBuilder app,
    IHostingEnvironment env,
    ILoggerFactory loggerFactory)
{

}
```

<span data-ttu-id="3cd24-176">ただし、ConfigureServices メソッドはこの動作の例外であり、IServiceCollection 型のパラメーターを 1 つだけ受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-176">The ConfigureServices method is the exception to this behavior; it must take just one parameter of type IServiceCollection.</span></span> <span data-ttu-id="3cd24-177">このメソッドは、サービス コンテナーにオブジェクトを追加する役割を持ち、IServiceCollection パラメーターを介して現在構成されているすべてのサービスにアクセスできるため、依存関係の挿入をサポートする必要はまったくありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-177">It doesn't really need to support dependency injection, since on the one hand it is responsible for adding objects to the services container, and on the other it has access to all currently configured services via the IServiceCollection parameter.</span></span> <span data-ttu-id="3cd24-178">したがって、必要なサービスをパラメーターとして要求するか、ConfigureServices で IServiceCollection を使うことにより、Startup クラスのすべての部分で、ASP.NET Core のサービス コレクションで定義されている依存関係を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-178">Thus, you can work with dependencies defined in the ASP.NET Core services collection in every part of the Startup class, either by requesting the needed service as a parameter or by working with the IServiceCollection in ConfigureServices.</span></span>

> [!NOTE]
> <span data-ttu-id="3cd24-179">特定のサービスを Startup クラスで確実に利用できるようにする必要がある場合は、WebHostBuilder とその ConfigureServices メソッドを使ってサービスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-179">If you need to ensure certain services are available to your Startup class, you can configure them using WebHostBuilder and its ConfigureServices method.</span></span>

<span data-ttu-id="3cd24-180">Startup クラスは、独自のサービスに対するコントローラーからミドルウェアやフィルターまで、ASP.NET Core アプリケーションの他の部分で必要な構成方法のモデルになります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-180">The Startup class is a model for how you should structure other parts of your ASP.NET Core application, from Controllers to Middleware to Filters to your own Services.</span></span> <span data-ttu-id="3cd24-181">いずれの場合も、[明示的な依存関係の原則](https://deviq.com/explicit-dependencies-principle/)に従い、依存関係を直接作成するのではなく要求し、アプリケーション全体で依存関係の挿入を利用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-181">In each case, you should follow the [Explicit Dependencies Principle](https://deviq.com/explicit-dependencies-principle/), requesting your dependencies rather than directly creating them, and leveraging dependency injection throughout your application.</span></span> <span data-ttu-id="3cd24-182">実装を直接インスタンス化する場所と方法に注意する必要があります (特に、インフラストラクチャを使用する、または副作用があるサービスとオブジェクトの場合)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-182">Be careful of where and how you directly instantiate implementations, especially services and objects that work with infrastructure or have side effects.</span></span> <span data-ttu-id="3cd24-183">特定の実装の種類に対する参照をハードコーディングするのではなく、抽象化をアプリケーション コアで定義し、引数として渡すようにします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-183">Prefer working with abstractions defined in your application core and passed in as arguments to hardcoding references to specific implementation types.</span></span>

## <a name="structuring-the-application"></a><span data-ttu-id="3cd24-184">アプリケーションの構成</span><span class="sxs-lookup"><span data-stu-id="3cd24-184">Structuring the application</span></span>

<span data-ttu-id="3cd24-185">通常、モノリシックなアプリケーションのエントリ ポイントは 1 つです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-185">Monolithic applications typically have a single entry point.</span></span> <span data-ttu-id="3cd24-186">ASP.NET Core Web アプリケーションの場合は、ASP.NET Core Web プロジェクトがエントリ ポイントになります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-186">In the case of an ASP.NET Core web application, the entry point will be the ASP.NET Core web project.</span></span> <span data-ttu-id="3cd24-187">ただし、これは、ソリューションは 1 つのプロジェクトだけで構成する必要があるという意味ではありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-187">However, that doesn't mean the solution should consist of just a single project.</span></span> <span data-ttu-id="3cd24-188">懸念事項の分離に従って、アプリケーションを複数の異なるレイヤーに分割するのは役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-188">It's useful to break up the application into different layers in order to follow separation of concerns.</span></span> <span data-ttu-id="3cd24-189">レイヤーに分割した後は、フォルダーだけでなくプロジェクトも分割して、カプセル化を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-189">Once broken up into layers, it's helpful to go beyond folders to separate projects, which can help achieve better encapsulation.</span></span> <span data-ttu-id="3cd24-190">ASP.NET Core アプリケーションでこれらの目標を実現するための最善の方法は、第 5 章で説明されているクリーン アーキテクチャのバリエーションです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-190">The best approach to achieve these goals with an ASP.NET Core application is a variation of the Clean Architecture discussed in chapter 5.</span></span> <span data-ttu-id="3cd24-191">この方法に従うと、アプリケーションのソリューションは、UI、Infrastructure、ApplicationCore に対する個別のライブラリで構成されるようになります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-191">Following this approach, the application's solution will be comprised of separate libraries for the UI, Infrastructure, and ApplicationCore.</span></span>

<span data-ttu-id="3cd24-192">これらのプロジェクトだけでなく、テスト プロジェクトも別に含まれます (テストについては 9 章で説明します)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-192">In addition to these projects, separate test projects are included as well (Testing is discussed in Chapter 9).</span></span>

<span data-ttu-id="3cd24-193">アプリケーションのオブジェクト モデルとインターフェイスは、ApplicationCore プロジェクトに置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-193">The application's object model and interfaces should be placed in the ApplicationCore project.</span></span> <span data-ttu-id="3cd24-194">このプロジェクトはできるだけ少ない依存関係を持つようにして、ソリューション内の他のプロジェクトはそれを参照します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-194">This project will have as few dependencies as possible, and the other projects in the solution will reference it.</span></span> <span data-ttu-id="3cd24-195">永続化する必要があるビジネス エンティティと、インフラストラクチャに直接依存していないサービスは、ApplicationCore プロジェクトで定義します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-195">Business entities that need to be persisted are defined in the ApplicationCore project, as are services that do not directly depend on infrastructure.</span></span>

<span data-ttu-id="3cd24-196">永続化を実行する方法や、ユーザーに通知を送信する方法など、実装の詳細は、Infrastructure プロジェクトで保持します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-196">Implementation details, such as how persistence is performed or how notifications might be sent to a user, are kept in the Infrastructure project.</span></span> <span data-ttu-id="3cd24-197">このプロジェクトは、Entity Framework Core などの実装固有のパッケージを参照しますが、これらの実装に関する詳細をプロジェクトの外部に公開しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-197">This project will reference implementation-specific packages such as Entity Framework Core, but should not expose details about these implementations outside of the project.</span></span> <span data-ttu-id="3cd24-198">インフラストラクチャ サービスとリポジトリは ApplicationCore プロジェクトで定義されているインターフェイスを実装する必要があり、このプロジェクトの永続化の実装が、ApplicationCore で定義されているエンティティの取得と格納を行います。</span><span class="sxs-lookup"><span data-stu-id="3cd24-198">Infrastructure services and repositories should implement interfaces that are defined in the ApplicationCore project, and its persistence implementations are responsible for retrieving and storing entities defined in ApplicationCore.</span></span>

<span data-ttu-id="3cd24-199">ASP.NET Core UI プロジェクトは、UI レベルの処理を行いますが、ビジネス ロジックまたはインフラストラクチャの詳細を含まないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-199">The ASP.NET Core UI project is responsible for any UI level concerns, but should not include business logic or infrastructure details.</span></span> <span data-ttu-id="3cd24-200">実際に、理想的なのは Infrastructure プロジェクトに対する依存関係さえ持つべきではなく、これにより 2 つのプロジェクト間に誤って依存関係が発生するのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-200">In fact, ideally it shouldn't even have a dependency on the Infrastructure project, which will help ensure no dependency between the two projects is introduced accidentally.</span></span> <span data-ttu-id="3cd24-201">これは、StructureMap などのサード パーティ製 DI コンテナーを使って実現でき、各プロジェクトの Registry クラスで DI 規則を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-201">This can be achieved using a third-party DI container like StructureMap, which allows you to define DI rules in Registry classes in each project.</span></span>

<span data-ttu-id="3cd24-202">実装の詳細からアプリケーションを分離するもう 1 つの方法は、通常は個別の Docker コンテナーで展開されているマイクロサービスをアプリケーションで呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-202">Another approach to decoupling the application from implementation details is to have the application call microservices, perhaps deployed in individual Docker containers.</span></span> <span data-ttu-id="3cd24-203">この方法を使うと、2 つのプロジェクト間に DI を利用する場合より、懸念事項の分離と分割はさらに大きくなりますが、複雑さは増大します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-203">This provides even greater separation of concerns and decoupling than leveraging DI between two projects, but has additional complexity.</span></span>

### <a name="feature-organization"></a><span data-ttu-id="3cd24-204">機能の編成</span><span class="sxs-lookup"><span data-stu-id="3cd24-204">Feature organization</span></span>

<span data-ttu-id="3cd24-205">既定では、ASP.NET Core アプリケーションは、コントローラーとビューさらに多くの場合は ViewModels を含むように、フォルダー構造を編成します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-205">By default, ASP.NET Core applications organize their folder structure to include Controllers and Views, and frequently ViewModels.</span></span> <span data-ttu-id="3cd24-206">通常、これらのサーバー側構造をサポートするためのクライアント側のコードは、wwwroot フォルダーに個別に格納されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-206">Client-side code to support these server-side structures is typically stored separately in the wwwroot folder.</span></span> <span data-ttu-id="3cd24-207">ただし、大規模なアプリケーションでは、特定の機能を使用するためにこれらのフォルダー間を移動する必要があるため、このような編成では問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-207">However, large applications may encounter problems with this organization, since working on any given feature often requires jumping between these folders.</span></span> <span data-ttu-id="3cd24-208">各フォルダー内のファイルとサブフォルダーの数が増えるとますます困難になり、ソリューション エクスプローラーのスクロール量が膨大になります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-208">This gets more and more difficult as the number of files and subfolders in each folder grows, resulting in a great deal of scrolling through Solution Explorer.</span></span> <span data-ttu-id="3cd24-209">この問題の 1 つの解決策は、アプリケーションのコードをファイルの種類別ではなく "_機能_" 別に整理することです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-209">One solution to this problem is to organize application code by _feature_ instead of by file type.</span></span> <span data-ttu-id="3cd24-210">この編成スタイルは、通常、機能フォルダーまたは機能スライスと呼ばれます ([垂直スライス](https://deviq.com/vertical-slices/)も参照してください)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-210">This organizational style is typically referred to as feature folders or feature slices (see also: [Vertical Slices](https://deviq.com/vertical-slices/)).</span></span>

<span data-ttu-id="3cd24-211">ASP.NET Core MVC では、この目的のために区分 (Area) がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-211">ASP.NET Core MVC supports Areas for this purpose.</span></span> <span data-ttu-id="3cd24-212">区分を使うと、各区分フォルダー内にコントローラー フォルダーとビュー フォルダー (および関連するすべてのモデル) のセットを個別に作成できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-212">Using areas, you can create separate sets of Controllers and Views folders (as well as any associated models) in each Area folder.</span></span> <span data-ttu-id="3cd24-213">図 7-1 は、区分を使用したフォルダー構造の例です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-213">Figure 7-1 shows an example folder structure, using Areas.</span></span>

![](./media/image7-1.png)

<span data-ttu-id="3cd24-214">図 7-1 区分編成の例</span><span class="sxs-lookup"><span data-stu-id="3cd24-214">Figure 7-1 Sample Area Organization</span></span>

<span data-ttu-id="3cd24-215">区分を使う場合は、属性を使って、コントローラーが属する区分の名前でコントローラーを装飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-215">When using Areas, you must use attributes to decorate your controllers with the name of the area to which they belong:</span></span>

```csharp
[Area("Catalog")]
public class HomeController
{}
```

<span data-ttu-id="3cd24-216">また、区分のサポートをルートに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-216">You also need to add area support to your routes:</span></span>

```csharp
app.UseMvc(routes =>
{
    // Areas support
    routes.MapRoute(
    name: "areaRoute",
    template: "{area:exists}/{controller=Home}/{action=Index}/{id?}");
    routes.MapRoute(
    name: "default",
    template: "{controller=Home}/{action=Index}/{id?}");
});
```

<span data-ttu-id="3cd24-217">区分の組み込みサポートに加えて、独自のフォルダー構造を作成し、属性とカスタム ルートの代わりの規則を使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-217">In addition to the built-in support for Areas, you can also use your own folder structure, and conventions in place of attributes and custom routes.</span></span> <span data-ttu-id="3cd24-218">このようにすると、機能フォルダーにビューやコントローラーなどのフォルダーが個別に含まれないようにして、フラットな階層を維持し、各機能について 1 つの場所ですべての関連ファイルを簡単に見ることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-218">This would allow you to have feature folders that didn't include separate folders for Views, Controllers, etc., keeping the hierarchy flatter and making it easier to see all related files in a single place for each feature.</span></span>

<span data-ttu-id="3cd24-219">ASP.NET Core は、組み込みの規則の種類を使って、その動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-219">ASP.NET Core uses built-in convention types to control its behavior.</span></span> <span data-ttu-id="3cd24-220">これらの規則は変更したり置き換えたりできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-220">You can modify or replace these conventions.</span></span> <span data-ttu-id="3cd24-221">たとえば、名前空間に基づいて特定のコントローラーの機能名を自動的に取得する規則を作成できます (これは通常、コントローラーが存在するフォルダーに関連付けられます)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-221">For example, you can create a convention that will automatically get the feature name for a given controller based on its namespace (which typically correlates to the folder in which the controller is located):</span></span>

```csharp
FeatureConvention : IControllerModelConvention
{
    public void Apply(ControllerModel controller)
    {
        controller.Properties.Add("feature",
        GetFeatureName(controller.ControllerType));
    }

    private string GetFeatureName(TypeInfo controllerType)
    {
        string[] tokens = controllerType.FullName.Split('.');
        if (!tokens.Any(t => t == "Features")) return "";
        string featureName = tokens
        .SkipWhile(t => !t.Equals("features",
        StringComparison.CurrentCultureIgnoreCase))
        .Skip(1)
        .Take(1)
        .FirstOrDefault();
        return featureName;
    }
}
```

<span data-ttu-id="3cd24-222">その後、ConfigureServices でアプリケーションに MVC のサポートを追加するときに、オプションとしてこの規則を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-222">You then specify this convention as an option when you add support for MVC to your application in ConfigureServices:</span></span>

```csharp
services.AddMvc(o => o.Conventions.Add(new FeatureConvention()));
```

<span data-ttu-id="3cd24-223">また、ASP.NET Core MVC はビューを配置する場合にも規則を使います。</span><span class="sxs-lookup"><span data-stu-id="3cd24-223">ASP.NET Core MVC also uses a convention to locate views.</span></span> <span data-ttu-id="3cd24-224">これをカスタム規則でオーバーライドして、ビューが独自の機能フォルダーに配置されるようにすることができます (上の FeatureConvention によって提供される機能名を使用)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-224">You can override it with a custom convention so that views will be located in your feature folders (using the feature name provided by the FeatureConvention, above).</span></span> <span data-ttu-id="3cd24-225">この方法について詳しくは、MSDN の記事「[ASP.NET Core MVC 向け機能スライス](https://msdn.microsoft.com/magazine/mt763233.aspx)」をご覧ください。実際に動くサンプルをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-225">You can learn more about this approach and download a working sample from the MSDN article, [Feature Slices for ASP.NET Core MVC](https://msdn.microsoft.com/magazine/mt763233.aspx).</span></span>

### <a name="cross-cutting-concerns"></a><span data-ttu-id="3cd24-226">横断的な問題</span><span class="sxs-lookup"><span data-stu-id="3cd24-226">Cross-cutting concerns</span></span>

<span data-ttu-id="3cd24-227">アプリケーションが大きくなるほど、横断的な事柄を抽出して、重複を排除し、整合性を維持することの重要性が増します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-227">As applications grow, it becomes increasingly important to factor out cross-cutting concerns to eliminate duplication and maintain consistency.</span></span> <span data-ttu-id="3cd24-228">ASP.NET Core アプリケーションでの横断的な事柄の例としては、認証、モデル検証規則、出力キャッシュ、エラー処理などがありますが、その他にも多くのことがあります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-228">Some examples of cross-cutting concerns in ASP.NET Core applications are authentication, model validation rules, output caching, and error handling, though there are many others.</span></span> <span data-ttu-id="3cd24-229">ASP.NET Core MVC で[フィルター](/aspnet/core/mvc/controllers/filters)を使うと、要求処理パイプラインの特定のステップの前または後にコードを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-229">ASP.NET Core MVC [filters](/aspnet/core/mvc/controllers/filters) allow you to run code before or after certain steps in the request processing pipeline.</span></span> <span data-ttu-id="3cd24-230">たとえば、フィルターは、モデル バインドの前後、アクションの前後、またはアクションの結果の前後に実行できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-230">For instance, a filter can run before and after model binding, before and after an action, or before and after an action's result.</span></span> <span data-ttu-id="3cd24-231">また、承認フィルターを使って、パイプラインの残りの部分へのアクセスを制御することができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-231">You can also use an authorization filter to control access to the rest of the pipeline.</span></span> <span data-ttu-id="3cd24-232">図 7-2 では、フィルターを構成した場合に要求の実行がそれをどのように通過するかを示します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-232">Figures 7-2 shows how request execution flows through filters, if configured.</span></span>

![要求は、承認フィルター、リソース フィルター、モデル バインド、アクション フィルター、アクションの実行とアクション結果の変換、例外フィルター、結果フィルター、結果の実行を介して処理されます。](./media/image7-2.png)

<span data-ttu-id="3cd24-235">図 7-2 フィルターと要求パイプラインを通過する要求実行の流れ。</span><span class="sxs-lookup"><span data-stu-id="3cd24-235">Figure 7-2 Request execution through filters and request pipeline.</span></span>

<span data-ttu-id="3cd24-236">通常、フィルターは属性として実装されるので、コントローラーまたはアクションにフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-236">Filters are usually implemented as attributes, so you can apply them controllers or actions.</span></span> <span data-ttu-id="3cd24-237">この方法で追加したフィルターをアクション レベルで指定すると、コントローラー レベルで指定されたフィルターをオーバーライドするか、その上に構築されて、それ自体がグローバル フィルターをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-237">When added in this fashion, filters specified at the action level override or build upon filters specified at the controller level, which themselves override global filters.</span></span> <span data-ttu-id="3cd24-238">たとえば、\[Route\] 属性を使って、コントローラーとアクションの間にルートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-238">For example, the \[Route\] attribute can be used to build up routes between controllers and actions.</span></span> <span data-ttu-id="3cd24-239">同様に、コントローラー レベルで承認を構成した後、次の例に示すように、個々のアクションでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-239">Likewise, authorization can be configured at the controller level, and then overridden by individual actions, as the following sample demonstrates:</span></span>

```csharp
[Authorize]
public class AccountController : Controller

{
    [AllowAnonymous]
    public async Task<IActionResult> Login() {}
    public async Task<IActionResult> ForgotPassword() {}
}
```

<span data-ttu-id="3cd24-240">最初の Login メソッドでは、AllowAnonymous フィルター (属性) を使って、コントローラー レベルで設定されている Authorize フィルターをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-240">The first method, Login, uses the AllowAnonymous filter (attribute) to override the Authorize filter set at the controller level.</span></span> <span data-ttu-id="3cd24-241">ForgotPassword アクション (および AllowAnonymous 属性を持たないクラスの他のすべてのアクション) では、認証された要求が必要です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-241">The ForgotPassword action (and any other action in the class that doesn't have an AllowAnonymous attribute) will require an authenticated request.</span></span>

<span data-ttu-id="3cd24-242">フィルターを使うと、API に対する共通エラー処理ポリシーの形式で、重複を除去できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-242">Filters can be used to eliminate duplication in the form of common error handling policies for APIs.</span></span> <span data-ttu-id="3cd24-243">たとえば、一般的な API ポリシーでは、存在しないキーを参照している要求に対しては NotFound 応答を返し、モデルの検証が失敗した場合は BadRequest 応答を返します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-243">For example, a typical API policy is to return a NotFound response to requests referencing keys that do not exist, and a BadRequest response if model validation fails.</span></span> <span data-ttu-id="3cd24-244">次の例では、アクションでのこれら 2 つのポリシーを示します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-244">The following example demonstrates these two policies in action:</span></span>

```csharp
[HttpPut("{id}")]
public async Task<IActionResult> Put(int id, [FromBody]Author author)
{
    if ((await _authorRepository.ListAsync()).All(a => a.Id != id))
    {
        return NotFound(id);
    }
    if (!ModelState.IsValid)
    {
        return BadRequest(ModelState);
    }
    author.Id = id;
    await _authorRepository.UpdateAsync(author);
    return Ok();
}
```

<span data-ttu-id="3cd24-245">このような条件付きコードで、アクション メソッドを乱雑にしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="3cd24-245">Don't allow your action methods to become cluttered with conditional code like this.</span></span> <span data-ttu-id="3cd24-246">代わりに、必要に応じて適用できるフィルターにポリシーを格納します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-246">Instead, pull the policies into filters that can be applied on an as-needed basis.</span></span> <span data-ttu-id="3cd24-247">この例では、コマンドが API に送られるたびに実行する必要があるモデルの検証チェックを、次の属性で置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-247">In this example, the model validation check, which should occur any time a command is sent to the API, can be replaced by the following attribute:</span></span>

```csharp
public class ValidateModelAttribute : ActionFilterAttribute
{
    public override void OnActionExecuting(ActionExecutingContext context)
    {
        if (!context.ModelState.IsValid)
        {
            context.Result = new BadRequestObjectResult(context.ModelState);
        }
    }
}
```

<span data-ttu-id="3cd24-248">同様に、フィルターを使ってレコードが存在するかどうかをチェックし、アクションが実行される前に 404 を返して、アクションでこれらのチェックを実行する必要がないようにできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-248">Likewise, a filter can be used to check if a record exists and return a 404 before the action is executed, eliminating the need to perform these checks in the action.</span></span> <span data-ttu-id="3cd24-249">共通の規則を抽出し、インフラストラクチャ コードとビジネス ロジックを UI から分離するようにソリューションを構成すると、MVC アクション メソッドは非常にスリムになるはずです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-249">Once you've pulled out common conventions and organized your solution to separate infrastructure code and business logic from your UI, your MVC action methods should be extremely thin:</span></span>

```csharp
[HttpPut("{id}")]
[ValidateAuthorExists]
public async Task<IActionResult> Put(int id, [FromBody]Author author)
{
    await _authorRepository.UpdateAsync(author);
    return Ok();
}
```

<span data-ttu-id="3cd24-250">フィルターの実装について詳しくは、MSDN の記事「[実際の ASP.NET Core MVC フィルター](https://msdn.microsoft.com/magazine/mt767699.aspx)」をご覧ください。動作するサンプルをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-250">You can read more about implementing filters and download a working sample from the MSDN article, [Real World ASP.NET Core MVC Filters](https://msdn.microsoft.com/magazine/mt767699.aspx).</span></span>

> ### <a name="references--structuring-applications"></a><span data-ttu-id="3cd24-251">参照 – アプリケーションの構成</span><span class="sxs-lookup"><span data-stu-id="3cd24-251">References – Structuring applications</span></span>
>
> - <span data-ttu-id="3cd24-252">**領域**</span><span class="sxs-lookup"><span data-stu-id="3cd24-252">**Areas**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/mvc/controllers/areas>
> - <span data-ttu-id="3cd24-253">**MSDN マガジン - ASP.NET Core MVC 向け機能スライス**</span><span class="sxs-lookup"><span data-stu-id="3cd24-253">**MSDN Magazine – Feature Slices for ASP.NET Core MVC**</span></span>  
 > <https://msdn.microsoft.com/magazine/mt763233.aspx>
> - <span data-ttu-id="3cd24-254">**フィルター**</span><span class="sxs-lookup"><span data-stu-id="3cd24-254">**Filters**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/mvc/controllers/filters>
> - <span data-ttu-id="3cd24-255">**MSDN – 実際の ASP.NET Core MVC フィルター**</span><span class="sxs-lookup"><span data-stu-id="3cd24-255">**MSDN – Real World ASP.NET Core MVC Filters**</span></span>  
>   <https://msdn.microsoft.com/magazine/mt767699.aspx>

## <a name="security"></a><span data-ttu-id="3cd24-256">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="3cd24-256">Security</span></span>

<span data-ttu-id="3cd24-257">Web アプリケーションのセキュリティ保護は大きなトピックであり、さまざまな考慮事項があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-257">Securing web applications is a large topic, with many considerations.</span></span> <span data-ttu-id="3cd24-258">最も基本的なレベルのセキュリティには、特定の要求を行ったユーザーを認識し、その要求が必要なリソースだけにアクセスできるようにすることが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-258">At its most basic level, security involves ensuring you know who a given request is coming from, and then ensuring that that request only has access to resources it should.</span></span> <span data-ttu-id="3cd24-259">認証は、要求で提供された資格情報を、信頼できるデータ ストア内の資格情報と比較して、要求を既知のエンティティから送信されたものとして扱う必要があるかどうかを確認するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-259">Authentication is the process of comparing credentials provided with a request to those in a trusted data store, to see if the request should be treated as coming from a known entity.</span></span> <span data-ttu-id="3cd24-260">承認は、ユーザーの ID に基づいて特定のリソースへのアクセスを制限するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-260">Authorization is the process of restricting access to certain resources based on user identity.</span></span> <span data-ttu-id="3cd24-261">セキュリティに関する 3 番目の考慮事項は、第三者による傍受から要求を保護することであり、少なくとも[アプリケーションが SSL を使っていることを確認する](/aspnet/core/security/enforcing-ssl)必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-261">A third security concern is protecting requests from eavesdropping by third parties, for which you should at least [ensure that SSL is used by your application](/aspnet/core/security/enforcing-ssl).</span></span>

### <a name="authentication"></a><span data-ttu-id="3cd24-262">認証</span><span class="sxs-lookup"><span data-stu-id="3cd24-262">Authentication</span></span>

<span data-ttu-id="3cd24-263">ASP.NET Core Identity は、アプリケーションのログイン機能をサポートするために使うことができるメンバーシップ システムです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-263">ASP.NET Core Identity is a membership system you can use to support login functionality for your application.</span></span> <span data-ttu-id="3cd24-264">ローカル ユーザー アカウントをサポートするだけでなく、Microsoft アカウント、Twitter、Facebook、Google などのプロバイダーからの外部ログイン プロバイダーもサポートします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-264">It has support for local user accounts as well as external login provider support from providers like Microsoft Account, Twitter, Facebook, Google, and more.</span></span> <span data-ttu-id="3cd24-265">ASP.NET Core Identity だけでなく、アプリケーションでは Windows 認証や、[Identity Server](https://github.com/IdentityServer/IdentityServer4) のようなサード パーティの ID プロバイダーを使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-265">In addition to ASP.NET Core Identity, your application can use windows authentication, or a third-party identity provider like [Identity Server](https://github.com/IdentityServer/IdentityServer4).</span></span>

<span data-ttu-id="3cd24-266">[個別のユーザー アカウント] オプションを選択した場合、新しいプロジェクト テンプレートには ASP.NET Core Identity が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-266">ASP.NET Core Identity is included in new project templates if the Individual User Accounts option is selected.</span></span> <span data-ttu-id="3cd24-267">このテンプレートには、登録、ログイン、外部ログイン、パスワードを忘れた場合、および追加機能のサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-267">This template includes support for registration, login, external logins, forgotten passwords, and additional functionality.</span></span>

![](./media/image7-3.png)

<span data-ttu-id="3cd24-268">図 7-3 [個別のユーザー アカウント] を選択して Identity を事前構成する。</span><span class="sxs-lookup"><span data-stu-id="3cd24-268">Figure 7-3 Select Individual User Accounts to have Identity preconfigured.</span></span>

<span data-ttu-id="3cd24-269">Identity のサポートは、Startup の ConfigureServices と Configure の両方で構成されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-269">Identity support is configured in Startup, both in ConfigureServices and Configure:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    // Add framework services.
    services.AddDbContext<ApplicationDbContext>(options =>
    options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
    services.AddIdentity<ApplicationUser, IdentityRole>()
    .AddEntityFrameworkStores<ApplicationDbContext>()
    .AddDefaultTokenProviders();
    services.AddMvc();
}

public void Configure(IApplicationBuilder app)
{
    app.UseStaticFiles();
    app.UseIdentity();
    app.UseMvc(routes =>
    {
        routes.MapRoute(
        name: "default",
        template: "{controller=Home}/{action=Index}/{id?}");
    });
}
```

<span data-ttu-id="3cd24-270">Configure メソッドで UseMvc の前に UseIdentity を指定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-270">It's important that UseIdentity appear before UseMvc in the Configure method.</span></span> <span data-ttu-id="3cd24-271">ConfigureServices で Identity を構成すると、AddDefaultTokenProviders の呼び出しがあることがわかります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-271">When configuring Identity in ConfigureServices, you'll notice a call to AddDefaultTokenProviders.</span></span> <span data-ttu-id="3cd24-272">これは、Web 通信をセキュリティ保護するために使われる場合があるトークンとは関係なく、ユーザーによる ID 確認のために SMS またはメールでユーザーに送信できるプロンプトを作成するプロバイダーを参照しています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-272">This has nothing to do with tokens that may be used to secure web communications, but instead refers to providers that create prompts that can be sent to users via SMS or email in order for them to confirm their identity.</span></span>

<span data-ttu-id="3cd24-273">詳しくは、ASP.NET Core の公式ドキュメントで [2 要素認証の構成](/aspnet/core/security/authentication/2fa)および[外部ログイン プロバイダーの有効化](/aspnet/core/security/authentication/social/)に関する記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3cd24-273">You can learn more about [configuring two-factor authentication](/aspnet/core/security/authentication/2fa) and [enabling external login providers](/aspnet/core/security/authentication/social/) from the official ASP.NET Core docs.</span></span>

### <a name="authorization"></a><span data-ttu-id="3cd24-274">承認</span><span class="sxs-lookup"><span data-stu-id="3cd24-274">Authorization</span></span>

<span data-ttu-id="3cd24-275">承認の最も単純な形式には、匿名ユーザーに対するアクセスの制限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-275">The simplest form of authorization involves restricting access to anonymous users.</span></span> <span data-ttu-id="3cd24-276">これは、特定のコントローラーまたはアクションに \[Authorize\] 属性を適用するだけで実現できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-276">This can be achieved by simply applying the \[Authorize\] attribute to certain controllers or actions.</span></span> <span data-ttu-id="3cd24-277">ロールを使っている場合は、次のように、特定のロールに属しているユーザーのアクセス制限まで、属性をさらに拡張できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-277">If roles are being used, the attribute can be further extended to restrict access to users who belong to certain roles, as shown:</span></span>

```csharp
[Authorize(Roles = "HRManager,Finance")]
public class SalaryController : Controller
{

}
```

<span data-ttu-id="3cd24-278">この例では、HRManager ロールと Finance ロールのどちらか一方または両方に属しているユーザーは、SalaryController にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-278">In this case, users belonging to either the HRManager or Finance roles (or both) would have access to the SalaryController.</span></span> <span data-ttu-id="3cd24-279">ユーザーが (複数のロールの 1 つだけでなく) 複数のロールに属していることを必要とするには、属性を複数回適用し、そのたびに必要なロールを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-279">To require that a user belong to multiple roles (not just one of several), you can apply the attribute multiple times, specifying a required role each time.</span></span>

<span data-ttu-id="3cd24-280">特定のロール セットを文字列として多くの異なるコントローラーやアクションで指定すると、望ましくない繰り返しにつながります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-280">Specifying certain sets of roles as strings in many different controllers and actions can lead to undesirable repetition.</span></span> <span data-ttu-id="3cd24-281">承認規則をカプセル化する承認ポリシーを構成し、\[Authorize\] 属性を適用するときに、個別のロールではなくポリシーを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-281">You can configure authorization policies, which encapsulate authorization rules, and then specify the policy instead of individual roles when applying the \[Authorize\] attribute:</span></span>

```csharp
[Authorize(Policy = "CanViewPrivateReport")]
public IActionResult ExecutiveSalaryReport()
{
    return View();
}
```

<span data-ttu-id="3cd24-282">この方法でポリシーを使うと、適用される特定のロールまたは規則から、制限されるアクションの種類を切り離すことができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-282">Using policies in this way, you can separate the kinds of actions being restricted from the specific roles or rules that apply to it.</span></span> <span data-ttu-id="3cd24-283">後で、特定のリソースへのアクセスを必要とする新しいロールを作成する場合は、ポリシーを更新するだけでよく、すべての \[Authorize\] 属性ですべてのロール リストを更新する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-283">Later, if you create a new role that needs to have access to certain resources, you can just update a policy, rather than updating every list of roles on every \[Authorize\] attribute.</span></span>

#### <a name="claims"></a><span data-ttu-id="3cd24-284">クレーム</span><span class="sxs-lookup"><span data-stu-id="3cd24-284">Claims</span></span>

<span data-ttu-id="3cd24-285">クレームは、認証済みユーザーのプロパティを表す名前と値のペアです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-285">Claims are name value pairs that represent properties of an authenticated user.</span></span> <span data-ttu-id="3cd24-286">たとえば、ユーザーの従業員番号をクレームとして格納できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-286">For example, you might store users' employee number as a claim.</span></span> <span data-ttu-id="3cd24-287">その後、承認ポリシーの一部としてクレームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-287">Claims can then be used as part of authorization policies.</span></span> <span data-ttu-id="3cd24-288">次の例では、"EmployeeNumber" という名前のクレームが存在する必要のある "EmployeeOnly" というポリシーを作成しています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-288">You could create a policy called "EmployeeOnly" that requires the existence of a claim called "EmployeeNumber", as shown in this example:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddMvc();
    services.AddAuthorization(options =>
    {
        options.AddPolicy("EmployeeOnly", policy => policy.RequireClaim("EmployeeNumber"));
    });
}
```

<span data-ttu-id="3cd24-289">その後、上記のように、このポリシーを \[Authorize\] 属性で使って、コントローラーやアクションを保護できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-289">This policy could then be used with the \[Authorize\] attribute to protect any controller and/or action, as described above.</span></span>

#### <a name="securing-web-apis"></a><span data-ttu-id="3cd24-290">Web API のセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="3cd24-290">Securing web APIs</span></span>

<span data-ttu-id="3cd24-291">ほとんどの Web API は、トークン ベースの認証システムを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-291">Most web APIs should implement a token-based authentication system.</span></span> <span data-ttu-id="3cd24-292">トークン認証はステートレスであり、拡張できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="3cd24-292">Token authentication is stateless and designed to be scalable.</span></span> <span data-ttu-id="3cd24-293">トークン ベースの認証システムでは、クライアントは最初に認証プロバイダーで認証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-293">In a token-based authentication system, the client must first authenticate with the authentication provider.</span></span> <span data-ttu-id="3cd24-294">それが成功した場合、クライアントはトークンを発行されます。トークンは、単に暗号化された意味のある文字列です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-294">If successful, the client is issued a token, which is simply a cryptographically meaningful string of characters.</span></span> <span data-ttu-id="3cd24-295">その後、クライアントが API に要求を発行する必要があるときは、このトークンを要求のヘッダーとして追加します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-295">When the client then needs to issue a request to an API, it adds this token as a header on the request.</span></span> <span data-ttu-id="3cd24-296">サーバーは、要求を完了する前に、要求ヘッダーに含まれるトークンを検証します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-296">The server then validates the token found in the request header before completing the request.</span></span> <span data-ttu-id="3cd24-297">図 7-4 はこのプロセスを示したものです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-297">Figure 7-4 demonstrates this process.</span></span>

![TokenAuth](./media/image7-4.png)

<span data-ttu-id="3cd24-299">**図 7-4.**</span><span class="sxs-lookup"><span data-stu-id="3cd24-299">**Figure 7-4.**</span></span> <span data-ttu-id="3cd24-300">Web API に対するトークン ベースの認証。</span><span class="sxs-lookup"><span data-stu-id="3cd24-300">Token-based authentication for Web APIs.</span></span>

> ### <a name="references--security"></a><span data-ttu-id="3cd24-301">参照 – セキュリティ</span><span class="sxs-lookup"><span data-stu-id="3cd24-301">References – Security</span></span>
>
> - <span data-ttu-id="3cd24-302">**セキュリティ ドキュメントの概要**</span><span class="sxs-lookup"><span data-stu-id="3cd24-302">**Security Docs Overview**</span></span>  
>   https://docs.microsoft.com/aspnet/core/security/
> - <span data-ttu-id="3cd24-303">**ASP.NET Core アプリで SSL を適用する**</span><span class="sxs-lookup"><span data-stu-id="3cd24-303">**Enforcing SSL in an ASP.NET Core App**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/security/enforcing-ssl>
> - <span data-ttu-id="3cd24-304">**Identity の概要**</span><span class="sxs-lookup"><span data-stu-id="3cd24-304">**Introduction to Identity**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/security/authentication/identity>
> - <span data-ttu-id="3cd24-305">**承認の概要**</span><span class="sxs-lookup"><span data-stu-id="3cd24-305">**Introduction to Authorization**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/security/authorization/introduction>
> - <span data-ttu-id="3cd24-306">**Azure App Service での API Apps に対する認証および承認**</span><span class="sxs-lookup"><span data-stu-id="3cd24-306">**Authentication and Authorization for API Apps in Azure App Service**</span></span>  
>   <https://docs.microsoft.com/azure/app-service-api/app-service-api-authentication>

## <a name="client-communication"></a><span data-ttu-id="3cd24-307">クライアントの通信</span><span class="sxs-lookup"><span data-stu-id="3cd24-307">Client communication</span></span>

<span data-ttu-id="3cd24-308">Web API によりページを提供してデータの要求に応答するだけでなく、ASP.NET Core アプリは接続されているクライアントと直接通信できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-308">In addition to serving pages and responding to requests for data via web APIs, ASP.NET Core apps can communicate directly with connected clients.</span></span> <span data-ttu-id="3cd24-309">この送信通信では、さまざまなトランスポート テクノロジを使うことができ、最も一般的なものは WebSocket です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-309">This outbound communication can use a variety of transport technologies, the most common being WebSockets.</span></span> <span data-ttu-id="3cd24-310">ASP.NET Core SignalR は、サーバーとクライアントの間のリアルタイム通信機能をアプリケーションに容易に追加できるようにするライブラリです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-310">ASP.NET Core SignalR is a library that makes it simple to add real-time server-to-client communication functionality to your applications.</span></span> <span data-ttu-id="3cd24-311">SignalR は、WebSocket などのさまざまなトランスポート テクノロジをサポートしており、多くの実装の詳細を開発者から抽象化します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-311">SignalR supports a variety of transport technologies, including WebSockets, and abstracts away many of the implementation details from the developer.</span></span>

<span data-ttu-id="3cd24-312">ASP.NET Core SignalR は ASP.NET Core 2.1 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-312">ASP.NET Core SignalR is available with ASP.NET Core 2.1.</span></span>

<span data-ttu-id="3cd24-313">WebSocket を直接使うか、他の技法を使うかに関係なく、リアルタイムのクライアント通信は、さまざまなアプリケーション シナリオで役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-313">Real-time client communication, whether using WebSockets directly or other techniques, are useful in a variety of application scenarios.</span></span> <span data-ttu-id="3cd24-314">次に、それらの例の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-314">Some examples include:</span></span>

- <span data-ttu-id="3cd24-315">ライブ チャット ルーム アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3cd24-315">Live chat room applications</span></span>

- <span data-ttu-id="3cd24-316">アプリケーションの監視</span><span class="sxs-lookup"><span data-stu-id="3cd24-316">Monitoring applications</span></span>

- <span data-ttu-id="3cd24-317">ジョブの進行状況の更新</span><span class="sxs-lookup"><span data-stu-id="3cd24-317">Job progress updates</span></span>

- <span data-ttu-id="3cd24-318">通知</span><span class="sxs-lookup"><span data-stu-id="3cd24-318">Notifications</span></span>

- <span data-ttu-id="3cd24-319">対話型のフォーム アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3cd24-319">Interactive forms applications</span></span>

<span data-ttu-id="3cd24-320">クライアント通信をアプリケーションに組み込むときは、通常、2 つのコンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-320">When building client communication into your applications, there are typically two components:</span></span>

- <span data-ttu-id="3cd24-321">サーバー側の接続マネージャー (SignalR Hub、WebSocketManager WebSocketHandler)</span><span class="sxs-lookup"><span data-stu-id="3cd24-321">Server-side connection manager (SignalR Hub, WebSocketManager WebSocketHandler)</span></span>

- <span data-ttu-id="3cd24-322">クライアント側のライブラリ</span><span class="sxs-lookup"><span data-stu-id="3cd24-322">Client-side library</span></span>

<span data-ttu-id="3cd24-323">クライアントはブラウザーに限定されず、モバイル アプリ、コンソール アプリ、他のネイティブ アプリも SignalR/WebSocket を使って通信できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-323">Clients aren't limited to browsers – mobile apps, console apps, and other native apps can also communicate using SignalR/WebSockets.</span></span> <span data-ttu-id="3cd24-324">次の簡単なプログラムは、WebSocketManager サンプル アプリケーションの一部として、チャット アプリケーションに送信されたすべての内容をコンソールにエコーします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-324">The following simple program echoes all content sent to a chat application to the console, as part of a WebSocketManager sample application:</span></span>

```csharp
public class Program
{
    private static Connection _connection;
    public static void Main(string[] args)
    {
        StartConnectionAsync();
        _connection.On("receiveMessage", (arguments) =>;
        {
            Console.WriteLine(\$"{arguments\[0\]} said: {arguments\[1\]}");
        });
        Console.ReadLine();
        StopConnectionAsync();
    }

    public static async Task StartConnectionAsync()
    {
        _connection = new Connection();
        await _connection.StartConnectionAsync("ws://localhost:65110/chat");
    }

    public static async Task StopConnectionAsync()
    {
        await _connection.StopConnectionAsync();
    }
}
```

<span data-ttu-id="3cd24-325">アプリケーションがクライアント アプリケーションと直接通信する方法を検討し、リアルタイム通信によってアプリのユーザー エクスペリエンスが向上するかどうかを検討します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-325">Consider ways in which your applications communicate directly with client applications, and consider whether real-time communication would improve your app's user experience.</span></span>

> ### <a name="references--client-communication"></a><span data-ttu-id="3cd24-326">参照 – クライアントの通信</span><span class="sxs-lookup"><span data-stu-id="3cd24-326">References – Client Communication</span></span>
>
> - <span data-ttu-id="3cd24-327">**ASP.NET Core SignalR**</span><span class="sxs-lookup"><span data-stu-id="3cd24-327">**ASP.NET Core SignalR**</span></span>  
>   <https://github.com/aspnet/SignalR>
> - <span data-ttu-id="3cd24-328">**WebSocket マネージャー**</span><span class="sxs-lookup"><span data-stu-id="3cd24-328">**WebSocket Manager**</span></span>  
>   https://github.com/radu-matei/websocket-manager

## <a name="domain-driven-design--should-you-apply-it"></a><span data-ttu-id="3cd24-329">ドメイン駆動設計 – 適用する必要があるか?</span><span class="sxs-lookup"><span data-stu-id="3cd24-329">Domain-driven design – Should you apply it?</span></span>

<span data-ttu-id="3cd24-330">ドメイン駆動設計 (DDD) は、"_ビジネス ドメイン_" に注目するソフトウェア構築のためのアジャイルな方法です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-330">Domain-Driven Design (DDD) is an agile approach to building software that emphasizes focusing on the _business domain_.</span></span> <span data-ttu-id="3cd24-331">実際のシステムのしくみについて開発者に関わることができるビジネス ドメインの専門家とのコミュニケーションと対話に重点が置かれます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-331">It places a heavy emphasis on communication and interaction with business domain expert(s) who can relate to the developers how the real-world system works.</span></span> <span data-ttu-id="3cd24-332">たとえば、株取引を処理するシステムを構築する場合のドメインの専門家は、経験豊富な株式ブローカーなどです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-332">For example, if you're building a system that handles stock trades, your domain expert might be an experienced stock broker.</span></span> <span data-ttu-id="3cd24-333">DDD は、大規模で複雑なビジネスの問題に対処するように設計されており、多くの場合、ドメインの理解とモデリングに対する投資に見合わないため、小さくて単純なアプリケーションには適しません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-333">DDD is designed to address large, complex business problems, and is often not appropriate for smaller, simpler applications, as the investment in understanding and modeling the domain is not worth it.</span></span>

<span data-ttu-id="3cd24-334">DDD 手法でソフトウェアを作成する場合、チーム (非技術的な利害関係者や貢献者を含む) は問題領域のための "_ユビキタス言語_" を開発する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-334">When building software following a DDD approach, your team (including non-technical stakeholders and contributors) should develop a _ubiquitous language_ for the problem space.</span></span> <span data-ttu-id="3cd24-335">つまり、モデル化される実際の概念、それに相当するソフトウェア、概念を保持するために存在する構造 (データベース テーブルなど) に、同じ用語を使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-335">That is, the same terminology should be used for the real-world concept being modeled, the software equivalent, and any structures that might exist to persist the concept (for example, database tables).</span></span> <span data-ttu-id="3cd24-336">したがって、ユビキタス言語で説明される概念は、"_ドメイン モデル_" の基礎を形成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-336">Thus, the concepts described in the ubiquitous language should form the basis for your _domain model_.</span></span>

<span data-ttu-id="3cd24-337">ドメイン モデルは、相互に対話してシステムの動作を表すオブジェクトで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-337">Your domain model is comprised of objects that interact with one another to represent the behavior of the system.</span></span> <span data-ttu-id="3cd24-338">これらのオブジェクトは以下のカテゴリに分けられます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-338">These objects may fall into the following categories:</span></span>

- <span data-ttu-id="3cd24-339">[エンティティ](https://deviq.com/entity/)は、ID のスレッドでオブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-339">[Entities](https://deviq.com/entity/), which represent objects with a thread of identity.</span></span> <span data-ttu-id="3cd24-340">エンティティは、通常、後で取得できるキーを使って永続的に格納されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-340">Entities are typically stored in persistence with a key by which they can later be retrieved.</span></span>

- <span data-ttu-id="3cd24-341">[集計](https://deviq.com/aggregate-pattern/)は、単位として永続化する必要のあるオブジェクトのグループを表します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-341">[Aggregates](https://deviq.com/aggregate-pattern/), which represent groups of objects that should be persisted as a unit.</span></span>

- <span data-ttu-id="3cd24-342">[値オブジェクト](https://deviq.com/value-object/)は、プロパティ値の合計に基づいて比較できる概念を表します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-342">[Value objects](https://deviq.com/value-object/), which represent concepts that can be compared on the basis of the sum of their property values.</span></span> <span data-ttu-id="3cd24-343">たとえば、開始日と終了日で構成される DateRange などです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-343">For example, DateRange consisting of a start and end date.</span></span>

- <span data-ttu-id="3cd24-344">[ドメイン イベント](https://martinfowler.com/eaaDev/DomainEvent.html)は、システムの他の部分にとって重要な、システム内で発生している出来事を表します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-344">[Domain events](https://martinfowler.com/eaaDev/DomainEvent.html), which represent things happening within the system that are of interest to other parts of the system.</span></span>

<span data-ttu-id="3cd24-345">DDD ドメイン モデルでは、モデル内に複雑な動作をカプセル化する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3cd24-345">Note that a DDD domain model should encapsulate complex behavior within the model.</span></span> <span data-ttu-id="3cd24-346">特にエンティティは、プロパティの単なるコレクションであってはなりません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-346">Entities, in particular, should not merely be collections of properties.</span></span> <span data-ttu-id="3cd24-347">ドメイン モデルに動作が欠如していて、システムの状態を表しているだけの場合は、[貧血症のモデル](https://deviq.com/anemic-model/)と呼ばれ、DDD では望ましくないことです。</span><span class="sxs-lookup"><span data-stu-id="3cd24-347">When the domain model lacks behavior and merely represents the state of the system, it is said to be an [anemic model](https://deviq.com/anemic-model/), which is undesirable in DDD.</span></span>

<span data-ttu-id="3cd24-348">これらのモデルの種類に加えて、通常、DDD ではさまざまなパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-348">In addition to these model types, DDD typically employs a variety of patterns:</span></span>

- <span data-ttu-id="3cd24-349">[リポジトリ](https://deviq.com/repository-pattern/)は、永続化の詳細を抽象化します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-349">[Repository](https://deviq.com/repository-pattern/), for abstracting persistence details.</span></span>

- <span data-ttu-id="3cd24-350">[ファクトリ](https://en.wikipedia.org/wiki/Factory_method_pattern)は、複雑なオブジェクトの作成をカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-350">[Factory](https://en.wikipedia.org/wiki/Factory_method_pattern), for encapsulating complex object creation.</span></span>

- <span data-ttu-id="3cd24-351">ドメイン イベントは、トリガーの動作から依存する動作を分離します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-351">Domain events, for decoupling dependent behavior from triggering behavior.</span></span>

- <span data-ttu-id="3cd24-352">[サービス](http://gorodinski.com/blog/2012/04/14/services-in-domain-driven-design-ddd/)は、複雑な動作やインフラストラクチャの実装の詳細をカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-352">[Services](http://gorodinski.com/blog/2012/04/14/services-in-domain-driven-design-ddd/), for encapsulating complex behavior and/or infrastructure implementation details.</span></span>

- <span data-ttu-id="3cd24-353">[コマンド](https://en.wikipedia.org/wiki/Command_pattern)は、コマンドの発行とコマンド自体の実行を切り離します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-353">[Command](https://en.wikipedia.org/wiki/Command_pattern), for decoupling issuing commands and executing the command itself.</span></span>

- <span data-ttu-id="3cd24-354">[仕様](https://deviq.com/specification-pattern/)は、クエリの詳細をカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-354">[Specification](https://deviq.com/specification-pattern/), for encapsulating query details.</span></span>

<span data-ttu-id="3cd24-355">また、DDD では、疎結合、カプセル化、単体テストを使って簡単に検証できるコードに対応するため、前に説明したクリーン アーキテクチャを使うことも推奨されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-355">DDD also recommends the use of the Clean Architecture discussed previously, allowing for loose coupling, encapsulation, and code that can easily be verified using unit tests.</span></span>

### <a name="when-should-you-apply-ddd"></a><span data-ttu-id="3cd24-356">DDD を適用する必要がある場合</span><span class="sxs-lookup"><span data-stu-id="3cd24-356">When should you apply DDD</span></span>

<span data-ttu-id="3cd24-357">DDD は、(技術的だけでなく) ビジネス的にも非常に複雑な大規模アプリケーションに最適です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-357">DDD is well-suited to large applications with significant business (not just technical) complexity.</span></span> <span data-ttu-id="3cd24-358">アプリケーションでは、ドメイン専門家の知識が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-358">The application should require the knowledge of domain experts.</span></span> <span data-ttu-id="3cd24-359">ドメイン モデル自体にも重要な動作が存在する必要があり、データ ストアからさまざまなレコードの現在の状態を単に取得するだけでなく、ビジネス ルールや相互作用を表します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-359">There should be significant behavior in the domain model itself, representing business rules and interactions beyond simply storing and retrieving the current state of various records from data stores.</span></span>

### <a name="when-shouldnt-you-apply-ddd"></a><span data-ttu-id="3cd24-360">DDD を適用してはならない場合</span><span class="sxs-lookup"><span data-stu-id="3cd24-360">When shouldn't you apply DDD</span></span>

<span data-ttu-id="3cd24-361">DDD では、モデリング、アーキテクチャ、コミュニケーションへの投資が伴い、小規模なアプリケーションや基本的に CRUD (作成/読み取り/更新/削除) だけのアプリケーションでは正当化されない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-361">DDD involves investments in modeling, architecture, and communication that may not be warranted for smaller applications or applications that are essentially just CRUD (create/read/update/delete).</span></span> <span data-ttu-id="3cd24-362">アプリケーション開発のアプローチに DDD を選んだ場合でも、ドメインに動作を持たない貧血症のモデルがあることがわかったときは、アプローチの再考が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-362">If you choose to approach your application following DDD, but find that your domain has an anemic model with no behavior, you may need to rethink your approach.</span></span> <span data-ttu-id="3cd24-363">アプリケーションで DDD を使う必要がないか、またはデータベースやユーザー インターフェイスではなくドメイン モデルにビジネス ロジックをカプセル化するためのアプリケーションのリファクタリングにサポートが必要な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-363">Either your application may not need DDD, or you may need assistance refactoring your application to encapsulate business logic in the domain model, rather than in your database or user interface.</span></span>

<span data-ttu-id="3cd24-364">ハイブリッド アプローチでは、アプリケーションのトランザクション部分やさらに複雑な部分にだけ DDD を使い、アプリケーションの簡単な CRUD 部分や読み取り専用の部分には使わないようにします。</span><span class="sxs-lookup"><span data-stu-id="3cd24-364">A hybrid approach would be to only use DDD for the transactional or more complex areas of the application, but not for simpler CRUD or read-only portions of the application.</span></span> <span data-ttu-id="3cd24-365">たとえば、レポートを表示したり、ダッシュボードにデータを視覚化したりするためにデータをクエリする場合、集計の制約を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-365">For instance, you needn't have the constraints of an Aggregate if you're querying data to display a report or to visualize data for a dashboard.</span></span> <span data-ttu-id="3cd24-366">このような要件に対しては、独立したシンプルな読み取りモデルでまったく問題ありません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-366">It's perfectly acceptable to have a separate, simpler read model for such requirements.</span></span>

> ### <a name="references--domain-driven-design"></a><span data-ttu-id="3cd24-367">参照 – ドメイン駆動設計</span><span class="sxs-lookup"><span data-stu-id="3cd24-367">References – Domain-Driven Design</span></span>
>
> - <span data-ttu-id="3cd24-368">**わかりやすい英語での DDD (StackOverflow の回答)**</span><span class="sxs-lookup"><span data-stu-id="3cd24-368">**DDD in Plain English (StackOverflow Answer)**</span></span>  
>   <https://stackoverflow.com/questions/1222392/can-someone-explain-domain-driven-design-ddd-in-plain-english-please/1222488#1222488>

## <a name="deployment"></a><span data-ttu-id="3cd24-369">配置</span><span class="sxs-lookup"><span data-stu-id="3cd24-369">Deployment</span></span>

<span data-ttu-id="3cd24-370">ホストされる場所に関係なく、ASP.NET Core アプリケーションを展開するプロセスには複数のステップがあります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-370">There are a few steps involved in the process of deploying your ASP.NET Core application, regardless of where it will be hosted.</span></span> <span data-ttu-id="3cd24-371">最初のステップであるアプリケーションの発行は、dotnet publish CLI コマンド使って行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-371">The first step is to publish the application, which can be done using the dotnet publish CLI command.</span></span> <span data-ttu-id="3cd24-372">アプリケーションがコンパイルされて、アプリケーションの実行に必要なすべてのファイルが指定したフォルダに配置されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-372">This will compile the application and place all of the files needed to run the application into a designated folder.</span></span> <span data-ttu-id="3cd24-373">Visual Studio から展開する場合、このステップは自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-373">When you deploy from Visual Studio, this step is performed for you automatically.</span></span> <span data-ttu-id="3cd24-374">publish フォルダーには、アプリケーションとその依存関係の .exe ファイルと .dll ファイルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-374">The publish folder contains .exe and .dll files for the application and its dependencies.</span></span> <span data-ttu-id="3cd24-375">自己充足型のアプリケーションには、.NET ランタイムのバージョンも含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-375">A self-contained application will also include a version of the .NET runtime.</span></span> <span data-ttu-id="3cd24-376">ASP.NET Core アプリケーションには、構成ファイル、静的クライアント資産、MVC ビューも含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-376">ASP.NET Core applications will also include configuration files, static client assets, and MVC views.</span></span>

<span data-ttu-id="3cd24-377">ASP.NET Core アプリケーションはコンソール アプリケーションであり、サーバーの起動時、およびアプリケーション (またはサーバー) がクラッシュした場合の再起動時に、起動される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-377">ASP.NET Core applications are console applications that must be started when the server boots and restarted if the application (or server) crashes.</span></span> <span data-ttu-id="3cd24-378">プロセス マネージャーを使って、このプロセスを自動化できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-378">A process manager can be used to automate this process.</span></span> <span data-ttu-id="3cd24-379">ASP.NET Core の最も一般的なプロセス マネージャーは、Linux の場合は Nginx と Apache、Windows の場合は IIS と Windows Service です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-379">The most common process managers for ASP.NET Core are Nginx and Apache on Linux and IIS or Windows Service on Windows.</span></span>

<span data-ttu-id="3cd24-380">Kestrel Web サーバーでホストされる ASP.NET Core アプリケーションの場合は、プロセス マネージャーだけでなく、リバース プロキシ サーバーも使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-380">In addition to a process manager, ASP.NET Core applications hosted in the Kestrel web server must use a reverse proxy server.</span></span> <span data-ttu-id="3cd24-381">リバース プロキシ サーバーはインターネットから HTTP 要求を受け取り、事前にいくつかの処理を行ってから Kestrel に転送します。</span><span class="sxs-lookup"><span data-stu-id="3cd24-381">A reverse proxy server receives HTTP requests from the internet and forwards them to Kestrel after some preliminary handling.</span></span> <span data-ttu-id="3cd24-382">リバース プロキシ サーバーは、アプリケーションにセキュリティのレイヤーを提供し、(インターネットからのトラフィックに対して公開される) エッジ展開に必要です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-382">Reverse proxy servers provide a layer of security for the application, and are required for edge deployments (exposed to traffic from the Internet).</span></span> <span data-ttu-id="3cd24-383">Kestrel は比較的新しく、ある種の攻撃に対する防御がまだ提供されていません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-383">Kestrel is relatively new and does not yet offer defenses against certain attacks.</span></span> <span data-ttu-id="3cd24-384">また、Kestrel は同じポートでの複数アプリケーションのホストもサポートしていないので、ホスト ヘッダーなどの手法を使って同じポートと IP アドレスで複数のアプリケーションをホストすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3cd24-384">Kestrel also doesn't support hosting multiple applications on the same port, so techniques like host headers cannot be used with it to enable hosting multiple applications on the same port and IP address.</span></span>

![インターネットに対する Kestrel](./media/image7-5.png)

<span data-ttu-id="3cd24-386">図 7-5 リバース プロキシ サーバーの背後の Kestrel でホストされている ASP.NET</span><span class="sxs-lookup"><span data-stu-id="3cd24-386">Figure 7-5 ASP.NET hosted in Kestrel behind a reverse proxy server</span></span>

<span data-ttu-id="3cd24-387">リバース プロキシが役に立つもう 1 つのシナリオは、SSL/HTTPS を使って複数のアプリケーションをセキュリティ保護する場合です。</span><span class="sxs-lookup"><span data-stu-id="3cd24-387">Another scenario in which a reverse proxy can be helpful is to secure multiple applications using SSL/HTTPS.</span></span> <span data-ttu-id="3cd24-388">この場合、リバース プロキシでは SSL だけを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd24-388">In this case, only the reverse proxy would need to have SSL configured.</span></span> <span data-ttu-id="3cd24-389">リバース プロキシ サーバーと Kestrel の間の通信は、HTTP で行われます (図 7-6 を参照)。</span><span class="sxs-lookup"><span data-stu-id="3cd24-389">Communication between the reverse proxy server and Kestrel could take place over HTTP, as shown in Figure 7-6.</span></span>

![](./media/image7-6.png)

<span data-ttu-id="3cd24-390">図 7-6 HTTPS で保護されたリバース プロキシ サーバーの背後でホストされている ASP.NET</span><span class="sxs-lookup"><span data-stu-id="3cd24-390">Figure 7-6 ASP.NET hosted behind an HTTPS-secured reverse proxy server</span></span>

<span data-ttu-id="3cd24-391">急速に普及しているアプローチは ASP.NET Core アプリケーションを Docker コンテナーでホストする方法で、ローカルにホストしたり、クラウド ベースのホスト用に Azure に展開したりできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-391">An increasingly popular approach is to host your ASP.NET Core application in a Docker container, which then can be hosted locally or deployed to Azure for cloud-based hosting.</span></span> <span data-ttu-id="3cd24-392">Docker コンテナーは、Kestrel で実行されるアプリケーションのコードを格納することができ、上記のように、リバース プロキシ サーバーの背後に展開されます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-392">The Docker container could contain your application code, running on Kestrel, and would be deployed behind a reverse proxy server, as shown above.</span></span>

<span data-ttu-id="3cd24-393">Azure でアプリケーションをホストしている場合は、専用の仮想アプライアンスとして Microsoft Azure Application Gateway を使って、複数のサービスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-393">If you're hosting your application on Azure, you can use Microsoft Azure Application Gateway as a dedicated virtual appliance to provide several services.</span></span> <span data-ttu-id="3cd24-394">個々のアプリケーションに対するリバース プロキシとして動作するだけでなく、Application Gateway は次の機能を提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="3cd24-394">In addition to acting as a reverse proxy for individual applications, Application Gateway can also offer the following features:</span></span>

- <span data-ttu-id="3cd24-395">HTTP の負荷分散</span><span class="sxs-lookup"><span data-stu-id="3cd24-395">HTTP load balancing</span></span>

- <span data-ttu-id="3cd24-396">SSL のオフロード (インターネットに対する SSL のみ)</span><span class="sxs-lookup"><span data-stu-id="3cd24-396">SSL offload (SSL only to Internet)</span></span>

- <span data-ttu-id="3cd24-397">エンド ツー エンドの SSL</span><span class="sxs-lookup"><span data-stu-id="3cd24-397">End to End SSL</span></span>

- <span data-ttu-id="3cd24-398">複数サイトのルーティング (最大 20 個のサイトを 1 つの Application Gateway に統合)</span><span class="sxs-lookup"><span data-stu-id="3cd24-398">Multi-site routing (consolidate up to 20 sites on a single Application Gateway)</span></span>

- <span data-ttu-id="3cd24-399">Web アプリケーション ファイアウォール</span><span class="sxs-lookup"><span data-stu-id="3cd24-399">Web application firewall</span></span>

- <span data-ttu-id="3cd24-400">WebSocket のサポート</span><span class="sxs-lookup"><span data-stu-id="3cd24-400">Websocket support</span></span>

- <span data-ttu-id="3cd24-401">高度な診断</span><span class="sxs-lookup"><span data-stu-id="3cd24-401">Advanced diagnostics</span></span>

<span data-ttu-id="3cd24-402">_Azure のデプロイ オプションについては、[10 章](development-process-for-azure.md)で説明します。_</span><span class="sxs-lookup"><span data-stu-id="3cd24-402">_Learn more about Azure deployment options in [Chapter 10](development-process-for-azure.md)._</span></span>

> ### <a name="references--deployment"></a><span data-ttu-id="3cd24-403">参照 – 展開</span><span class="sxs-lookup"><span data-stu-id="3cd24-403">References – Deployment</span></span>
>
> - <span data-ttu-id="3cd24-404">**ホスティングと展開の概要**</span><span class="sxs-lookup"><span data-stu-id="3cd24-404">**Hosting and Deployment Overview**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/publishing/>
> - <span data-ttu-id="3cd24-405">**Kestrel とリバース プロキシを使用するタイミング**</span><span class="sxs-lookup"><span data-stu-id="3cd24-405">**When to use Kestrel with a reverse proxy**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/fundamentals/servers/kestrel#when-to-use-kestrel-with-a-reverse-proxy>
> - <span data-ttu-id="3cd24-406">**Docker で ASP.NET Core アプリをホストする**</span><span class="sxs-lookup"><span data-stu-id="3cd24-406">**Host ASP.NET Core apps in Docker**</span></span>  
>   <https://docs.microsoft.com/aspnet/core/publishing/docker>
> - <span data-ttu-id="3cd24-407">**Azure Application Gateway の概要**</span><span class="sxs-lookup"><span data-stu-id="3cd24-407">**Introducing Azure Application Gateway**</span></span>  
>   <https://docs.microsoft.com/azure/application-gateway/application-gateway-introduction>

>[!div class="step-by-step"]
<span data-ttu-id="3cd24-408">[前へ](common-client-side-web-technologies.md)
[次へ](work-with-data-in-asp-net-core-apps.md)</span><span class="sxs-lookup"><span data-stu-id="3cd24-408">[Previous](common-client-side-web-technologies.md)
[Next](work-with-data-in-asp-net-core-apps.md)</span></span>
