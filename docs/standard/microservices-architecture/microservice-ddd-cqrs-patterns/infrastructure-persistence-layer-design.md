---
title: インフラストラクチャの永続レイヤーの設計
description: インフラストラクチャの永続レイヤーを設計する方法について説明します。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/28/2017
ms.openlocfilehash: a0fcaead363e41f0dd02ed1e2ddfc90afb8d0c57
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404474"
---
# <a name="designing-the-infrastructure-persistence-layer"></a><span data-ttu-id="b9192-103">インフラストラクチャの永続レイヤーの設計</span><span class="sxs-lookup"><span data-stu-id="b9192-103">Designing the infrastructure persistence layer</span></span>

<span data-ttu-id="b9192-104">データ永続化コンポーネントは、マイクロサービス (つまり、マイクロサービスのデータベース) の境界内でホストされているデータへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b9192-104">Data persistence components provide access to the data hosted within the boundaries of a microservice (that is, a microservice’s database).</span></span> <span data-ttu-id="b9192-105">内容としては、リポジトリや[作業単位](https://martinfowler.com/eaaCatalog/unitOfWork.html)クラス (カスタム Entity Framework (EF) <xref:Microsoft.EntityFrameworkCore.DbContext> など) などのコンポーネントの実際の実装が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9192-105">They contain the actual implementation of components such as repositories and [Unit of Work](https://martinfowler.com/eaaCatalog/unitOfWork.html) classes, like custom Entity Framework (EF) <xref:Microsoft.EntityFrameworkCore.DbContext> objects.</span></span>

## <a name="the-repository-pattern"></a><span data-ttu-id="b9192-106">リポジトリ パターン</span><span class="sxs-lookup"><span data-stu-id="b9192-106">The Repository pattern</span></span>

<span data-ttu-id="b9192-107">リポジトリは、データ ソースへのアクセスに必要なロジックをカプセル化するクラスまたはコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="b9192-107">Repositories are classes or components that encapsulate the logic required to access data sources.</span></span> <span data-ttu-id="b9192-108">リポジトリは一般的なデータ アクセス機能を一元管理して保守性を向上させ、ドメイン モデル レイヤーからデータベースにアクセスするためのインフラストラクチャやテクノロジを切り離します。</span><span class="sxs-lookup"><span data-stu-id="b9192-108">They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer.</span></span> <span data-ttu-id="b9192-109">Entity Framework などのオブジェクト リレーショナル マップ (ORM) を使用する場合、LINQ と厳密な型指定により、実装する必要があるコードが簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-109">If you use an object-relational mapping (ORM) like Entity Framework, the code that must be implemented is simplified, thanks to LINQ and strong typing.</span></span> <span data-ttu-id="b9192-110">これによりデータ アクセスの組み込みではなく、データ永続化ロジックに集中できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b9192-110">This lets you focus on the data persistence logic rather than on data access plumbing.</span></span>

<span data-ttu-id="b9192-111">リポジトリ パターンは、ドキュメントが整備されたデータ ソース操作方法です。</span><span class="sxs-lookup"><span data-stu-id="b9192-111">The Repository pattern is a well-documented way of working with a data source.</span></span> <span data-ttu-id="b9192-112">Martin Fowler は、著書『[エンタープライズ アプリケーション アーキテクチャ パターン](https://www.amazon.com/Patterns-Enterprise-Application-Architecture-Martin/dp/0321127420/)』の中でリポジトリのことを次のように述べています。</span><span class="sxs-lookup"><span data-stu-id="b9192-112">In the book [Patterns of Enterprise Application Architecture](https://www.amazon.com/Patterns-Enterprise-Application-Architecture-Martin/dp/0321127420/), Martin Fowler describes a repository as follows:</span></span>

> <span data-ttu-id="b9192-113">リポジトリは、ドメイン モデル レイヤーとデータ マッピングの間を媒介するタスクを実行し、メモリ内のドメイン オブジェクト セットに似たような動作をする。</span><span class="sxs-lookup"><span data-stu-id="b9192-113">A repository performs the tasks of an intermediary between the domain model layers and data mapping, acting in a similar way to a set of domain objects in memory.</span></span> <span data-ttu-id="b9192-114">クライアント オブジェクトは宣言によってクエリを構築し、リポジトリに送信して回答を得る。</span><span class="sxs-lookup"><span data-stu-id="b9192-114">Client objects declaratively build queries and send them to the repositories for answers.</span></span> <span data-ttu-id="b9192-115">概念上、リポジトリはデータベースに格納されている一連のオブジェクトとオブジェクト上で実行可能な操作をカプセル化し、永続レイヤーに近い方法を提供する。</span><span class="sxs-lookup"><span data-stu-id="b9192-115">Conceptually, a repository encapsulates a set of objects stored in the database and operations that can be performed on them, providing a way that is closer to the persistence layer.</span></span> <span data-ttu-id="b9192-116">また、リポジトリは、作業ドメインとデータの割り当て、すなわちマッピングとの依存関係を明確かつ一方向に切り離すという目的をサポートする。</span><span class="sxs-lookup"><span data-stu-id="b9192-116">Repositories, also, support the purpose of separating, clearly and in one direction, the dependency between the work domain and the data allocation or mapping.</span></span>

### <a name="define-one-repository-per-aggregate"></a><span data-ttu-id="b9192-117">集約ごとにリポジトリを定義する</span><span class="sxs-lookup"><span data-stu-id="b9192-117">Define one repository per aggregate</span></span>

<span data-ttu-id="b9192-118">各集約または集約ルートに1 つのリポジトリ クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9192-118">For each aggregate or aggregate root, you should create one repository class.</span></span> <span data-ttu-id="b9192-119">ドメイン駆動設計 (DDD) パターンに基づくマイクロサービスでは、リポジトリはデータベースの更新に使用する唯一のチャネルです。</span><span class="sxs-lookup"><span data-stu-id="b9192-119">In a microservice based on domain-driven design (DDD) patterns, the only channel you should use to update the database should be the repositories.</span></span> <span data-ttu-id="b9192-120">これは、リポジトリには集約ルートとの一対一の関係があるためで、これにより集約の不変性とトランザクションの一貫性が管理されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-120">This is because they have a one-to-one relationship with the aggregate root, which controls the aggregate’s invariants and transactional consistency.</span></span> <span data-ttu-id="b9192-121">データベースのクエリは他のチャネルで実行することもできますが (CQRS アプローチに従って実行することも可能)、それは、クエリではデータベースの状態が変更されないためです。</span><span class="sxs-lookup"><span data-stu-id="b9192-121">It's okay to query the database through other channels (as you can do following a CQRS approach), because queries don't change the state of the database.</span></span> <span data-ttu-id="b9192-122">ただし、トランザクション領域 (つまり、更新) は、常にリポジトリと集約ルートで制御する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9192-122">However, the transactional area (that is, the updates) must always be controlled by the repositories and the aggregate roots.</span></span>

<span data-ttu-id="b9192-123">基本的に、リポジトリでは、データベースから取得されたデータをドメイン エンティティの形式でメモリ内に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-123">Basically, a repository allows you to populate data in memory that comes from the database in the form of the domain entities.</span></span> <span data-ttu-id="b9192-124">メモリ内に設定されたエンティティは、トランザクションによって変更し、再度データベースに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-124">Once the entities are in memory, they can be changed and then persisted back to the database through transactions.</span></span>

<span data-ttu-id="b9192-125">前述したように、CQS/CQRS アーキテクチャ パターンを使用している場合、Dapper を使用した単純な SQL ステートメントによって実行されるドメイン モデルからの副クエリによって最初のクエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-125">As noted earlier, if you're using the CQS/CQRS architectural pattern, the initial queries are performed by side queries out of the domain model, performed by simple SQL statements using Dapper.</span></span> <span data-ttu-id="b9192-126">この方法は、必要な任意のテーブルを照会および結合可能で、クエリが集約からのルールによって制限されないため、リポジトリよりはるかに柔軟です。</span><span class="sxs-lookup"><span data-stu-id="b9192-126">This approach is much more flexible than repositories because you can query and join any tables you need, and these queries aren't restricted by rules from the aggregates.</span></span> <span data-ttu-id="b9192-127">その場合、データはプレゼンテーション レイヤーまたはクライアント アプリに移動します。</span><span class="sxs-lookup"><span data-stu-id="b9192-127">That data goes to the presentation layer or client app.</span></span>

<span data-ttu-id="b9192-128">ユーザーが変更を行うと、更新されるデータは、クライアント アプリまたはプレゼンテーション レイヤーからアプリケーションレイヤー (Web API サービスなど) に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9192-128">If the user makes changes, the data to be updated comes from the client app or presentation layer to the application layer (such as a Web API service).</span></span> <span data-ttu-id="b9192-129">コマンド ハンドラーでコマンドとデータを受信したら、リポジトリを使用して、更新するデータをデータベースから取得します。</span><span class="sxs-lookup"><span data-stu-id="b9192-129">When you receive a command with data in a command handler, you use repositories to get the data you want to update from the database.</span></span> <span data-ttu-id="b9192-130">メモリ内で、コマンドを使用して渡された情報を更新した後、トランザクションによりデータベース内のデータ (ドメイン エンティティ) を追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="b9192-130">You update it in memory with the information passed with the commands, and you then add or update the data (domain entities) in the database through a transaction.</span></span>

<span data-ttu-id="b9192-131">図 9-17 に示すように、各集約ルートに定義するリポジトリは 1 つだけであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9192-131">Remember that only one repository should be defined for each aggregate root, as shown in Figure 9-17.</span></span> <span data-ttu-id="b9192-132">集約内のすべてのオブジェクト間のトランザクションの一貫性を維持するという集約ルートの目標を達成するため、データベース内の各テーブルのリポジトリは作成しません。</span><span class="sxs-lookup"><span data-stu-id="b9192-132">To achieve the goal of the aggregate root to maintain transactional consistency between all the objects within the aggregate, you should never create a repository for each table in the database.</span></span>

![](./media/image18.png)

<span data-ttu-id="b9192-133">**図 9-17**。</span><span class="sxs-lookup"><span data-stu-id="b9192-133">**Figure 9-17**.</span></span> <span data-ttu-id="b9192-134">リポジトリ、集約、およびデータベース テーブル間のリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="b9192-134">The relationship between repositories, aggregates, and database tables</span></span>

### <a name="enforcing-one-aggregate-root-per-repository"></a><span data-ttu-id="b9192-135">リポジトリごとに 1 つの集約ルートを適用</span><span class="sxs-lookup"><span data-stu-id="b9192-135">Enforcing one aggregate root per repository</span></span>

<span data-ttu-id="b9192-136">リポジトリ設計を実装する際に、集約ルートのみにリポジトリを設定するというルールを適用することが重要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9192-136">It can be valuable to implement your repository design in such a way that it enforces the rule that only aggregate roots should have repositories.</span></span> <span data-ttu-id="b9192-137">操作するエンティティの型を制約するジェネリック型または基本型のリポジトリを作成し、`IAggregateRoot` マーカー インターフェイスを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-137">You can create a generic or base repository type that constrains the type of entities it works with to ensure they have the `IAggregateRoot` marker interface.</span></span>

<span data-ttu-id="b9192-138">このように、インフラストラクチャ レイヤーで実装されている各リポジトリ クラスに独自のコントラクトまたはインターフェイスが実装されます (次のコードを参照)。</span><span class="sxs-lookup"><span data-stu-id="b9192-138">Thus, each repository class implemented at the infrastructure layer implements its own contract or interface, as shown in the following code:</span></span>

```csharp
namespace Microsoft.eShopOnContainers.Services.Ordering.Infrastructure.Repositories
{
    public class OrderRepository : IOrderRepository
    {
      // ...
    }
}
```

<span data-ttu-id="b9192-139">リポジトリの各インターフェイスには、ジェネリック IRepository インターフェイスが実装されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-139">Each specific repository interface implements the generic IRepository interface:</span></span>

```csharp
public interface IOrderRepository : IRepository<Order>
{
    Order Add(Order order);
    // ...
}
```

<span data-ttu-id="b9192-140">しかし、各リポジトリが単一の集計に関連付けられる規則を適用するコードを用意するには、ジェネリック型のリポジトリを実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9192-140">However, a better way to have the code enforce the convention that each repository is related to a single aggregate is to implement a generic repository type.</span></span> <span data-ttu-id="b9192-141">そうすることで、特定の集約を対象とするリポジトリを使用していることが明確になります。</span><span class="sxs-lookup"><span data-stu-id="b9192-141">That way, it's explicit that you're using a repository to target a specific aggregate.</span></span> <span data-ttu-id="b9192-142">これは、次のコードのように、そのジェネリックの `IRepository` 基底インターフェイスを実装することで簡単に行えます。</span><span class="sxs-lookup"><span data-stu-id="b9192-142">That can be easily done by implementing a generic `IRepository` base interface, as in the following code:</span></span>

```csharp
public interface IRepository<T> where T : IAggregateRoot
{
    //....
}
```

### <a name="the-repository-pattern-makes-it-easier-to-test-your-application-logic"></a><span data-ttu-id="b9192-143">アプリケーション ロジックのテストを容易にするリポジトリ パターン</span><span class="sxs-lookup"><span data-stu-id="b9192-143">The Repository pattern makes it easier to test your application logic</span></span>

<span data-ttu-id="b9192-144">リポジトリ パターンを利用すると、単体テストでアプリケーションを簡単にテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-144">The Repository pattern allows you to easily test your application with unit tests.</span></span> <span data-ttu-id="b9192-145">単体テストの対象はインフラストラクチャではなく、コードのみであるため、リポジトリの抽象化により目的を達成しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="b9192-145">Remember that unit tests only test your code, not infrastructure, so the repository abstractions make it easier to achieve that goal.</span></span>

<span data-ttu-id="b9192-146">前のセクションで説明したように、リポジトリ インターフェイスをドメイン モデル レイヤーに定義および配置し、アプリケーション レイヤー (Web API マイクロサービスなど) が、実際のリポジトリ クラスを実装しているインフラストラクチャ レイヤーに直接依存しないようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9192-146">As noted in an earlier section, it's recommended that you define and place the repository interfaces in the domain model layer so the application layer, such as your Web API microservice, doesn't depend directly on the infrastructure layer where you've implemented the actual repository classes.</span></span> <span data-ttu-id="b9192-147">これにより、Web API のコント ローラーで依存関係の挿入を使用して、データベースのデータではなく疑似データを返すモック リポジトリを実装できます。</span><span class="sxs-lookup"><span data-stu-id="b9192-147">By doing this and using Dependency Injection in the controllers of your Web API, you can implement mock repositories that return fake data instead of data from the database.</span></span> <span data-ttu-id="b9192-148">このような分離アプローチでは、データベースへの接続を必要とせず、アプリケーションのロジックだけをテストする単体テストを作成し、実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-148">This decoupled approach allows you to create and run unit tests that can test just the logic of your application without requiring connectivity to the database.</span></span>

<span data-ttu-id="b9192-149">データベースに対して膨大なテストを実行することには、データベースへの接続が失敗する可能性があることに加え、さらに大きな 2 つの理由から問題があります。</span><span class="sxs-lookup"><span data-stu-id="b9192-149">Connections to databases can fail and, more importantly, running hundreds of tests against a database is bad for two reasons.</span></span> <span data-ttu-id="b9192-150">その 1 つは、テスト量の多さにより時間がかかる可能性があることです。</span><span class="sxs-lookup"><span data-stu-id="b9192-150">First, it can take a long time because of the large number of tests.</span></span> <span data-ttu-id="b9192-151">もう一つは、データベースのレコードが変更され、テスト結果に影響して、データの一貫性がなくなる可能性があるということです。</span><span class="sxs-lookup"><span data-stu-id="b9192-151">Second, the database records might change and impact the results of your tests, so that they might not be consistent.</span></span> <span data-ttu-id="b9192-152">データベースに対するテストは単体テストではなく、統合テストです。</span><span class="sxs-lookup"><span data-stu-id="b9192-152">Testing against the database isn't a unit test but an integration test.</span></span> <span data-ttu-id="b9192-153">多数の単体テストを高速で実行する必要がありますが、データベースに対する統合テストは大量に行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b9192-153">You should have many unit tests running fast, but fewer integration tests against the databases.</span></span>

<span data-ttu-id="b9192-154">単体テストの問題の分離という観点から、ロジックはメモリ内のドメイン エンティティで動作します。</span><span class="sxs-lookup"><span data-stu-id="b9192-154">In terms of separation of concerns for unit tests, your logic operates on domain entities in memory.</span></span> <span data-ttu-id="b9192-155">ドメイン エンティティはリポジトリ クラスで提供されるものと想定します。</span><span class="sxs-lookup"><span data-stu-id="b9192-155">It assumes the repository class has delivered those.</span></span> <span data-ttu-id="b9192-156">また、ロジックによって変更されたドメイン エンティティは、リポジトリ クラスに適切に保存されるものと想定します。</span><span class="sxs-lookup"><span data-stu-id="b9192-156">Once your logic modifies the domain entities, it assumes the repository class will store them correctly.</span></span> <span data-ttu-id="b9192-157">ここでの重要なポイントは、単体テストはドメイン モデルとそのドメイン ロジックに対して作成するということです。</span><span class="sxs-lookup"><span data-stu-id="b9192-157">The important point here is to create unit tests against your domain model and its domain logic.</span></span> <span data-ttu-id="b9192-158">集約ルートは DDD の主な整合性境界です。</span><span class="sxs-lookup"><span data-stu-id="b9192-158">Aggregate roots are the main consistency boundaries in DDD.</span></span>

### <a name="the-difference-between-the-repository-pattern-and-the-legacy-data-access-class-dal-class-pattern"></a><span data-ttu-id="b9192-159">リポジトリ パターンと、従来のデータ アクセス クラス (DAL クラス) パターンの違い</span><span class="sxs-lookup"><span data-stu-id="b9192-159">The difference between the Repository pattern and the legacy Data Access class (DAL class) pattern</span></span>

<span data-ttu-id="b9192-160">データ アクセス オブジェクトは、データ アクセスおよび永続化操作を記憶域に対して直接実行します。</span><span class="sxs-lookup"><span data-stu-id="b9192-160">A data access object directly performs data access and persistence operations against storage.</span></span> <span data-ttu-id="b9192-161">リポジトリでは、メモリ内の作業単位オブジェクトの操作対象データにマークを付けますが (例: <xref:Microsoft.EntityFrameworkCore.DbContext> クラスを使用する場合の EF)、更新はすぐには実行されません。</span><span class="sxs-lookup"><span data-stu-id="b9192-161">A repository marks the data with the operations you want to perform in the memory of a unit of work object (as in EF when using the <xref:Microsoft.EntityFrameworkCore.DbContext> class), but these updates aren't performed immediately.</span></span>

<span data-ttu-id="b9192-162">作業単位は複数の挿入、更新、または削除操作が関与する単一のトランザクションとして表されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-162">A unit of work is referred to as a single transaction that involves multiple insert, update, or delete operations.</span></span> <span data-ttu-id="b9192-163">つまり、特定のユーザー操作 (Web サイトへの登録など) に対して、すべての挿入、更新、および削除のトランザクションが単一のトランザクションとして処理されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b9192-163">In simple terms, it means that for a specific user action, such as a registration on a website, all the insert, update, and delete transactions are handled in a single transaction.</span></span> <span data-ttu-id="b9192-164">これは、複数のデータベース トランザクションを対話方法で処理するよりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="b9192-164">This is more efficient than handling multiple database transactions in a chattier way.</span></span>

<span data-ttu-id="b9192-165">これらの複数の永続化操作は、後でアプリケーション レイヤーのコードが命令を発行したときに、1 アクションで実行されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-165">These multiple persistence operations are performed later in a single action when your code from the application layer commands it.</span></span> <span data-ttu-id="b9192-166">実際のデータベース記憶域にメモリ内の変更を適用する決定は、通常、[作業単位パターン](https://martinfowler.com/eaaCatalog/unitOfWork.html)に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="b9192-166">The decision about applying the in-memory changes to the actual database storage is typically based on the [Unit of Work pattern](https://martinfowler.com/eaaCatalog/unitOfWork.html).</span></span> <span data-ttu-id="b9192-167">EF には、作業単位パターンは <xref:Microsoft.EntityFrameworkCore.DbContext> として実装されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-167">In EF, the Unit of Work pattern is implemented as the <xref:Microsoft.EntityFrameworkCore.DbContext>.</span></span>

<span data-ttu-id="b9192-168">多くの場合、このパターンまたは記憶域に対する操作の適用方法により、アプリケーションのパフォーマンスを向上させ、不整合の可能性を低減することができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-168">In many cases, this pattern or way of applying operations against the storage can increase application performance and reduce the possibility of inconsistencies.</span></span> <span data-ttu-id="b9192-169">また、意図したすべての操作が単一のトランザクションの一部としてコミットされるので、データベース テーブル内でブロックされるトランザクションも少なくなります。</span><span class="sxs-lookup"><span data-stu-id="b9192-169">It also reduces transaction blocking in the database tables, because all the intended operations are committed as part of one transaction.</span></span> <span data-ttu-id="b9192-170">これは、データベースに対して多数の単独の操作を実行する場合と比べて効率的です。</span><span class="sxs-lookup"><span data-stu-id="b9192-170">This is more efficient in comparison to executing many isolated operations against the database.</span></span> <span data-ttu-id="b9192-171">そのため、小規模な個別のトランザクションを多数実行するのではなく、同じトランザクション内で複数の更新操作をグループ化することにより、選択した ORM でデータベースに対する実行を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="b9192-171">Therefore, the selected ORM can optimize the execution against the database by grouping several update actions within the same transaction, as opposed to many small and separate transaction executions.</span></span>

### <a name="repositories-shouldnt-be-mandatory"></a><span data-ttu-id="b9192-172">リポジトリは必須ではない</span><span class="sxs-lookup"><span data-stu-id="b9192-172">Repositories shouldn't be mandatory</span></span>

<span data-ttu-id="b9192-173">カスタム リポジトリは、前述の理由により便利であり、eShopOnContainers の順序付けマイクロサービスで採用されているアプローチですが、</span><span class="sxs-lookup"><span data-stu-id="b9192-173">Custom repositories are useful for the reasons cited earlier, and that is the approach for the ordering microservice in eShopOnContainers.</span></span> <span data-ttu-id="b9192-174">DDD 設計の実装、または一般的な .NET 開発に不可欠なパターンではありません。</span><span class="sxs-lookup"><span data-stu-id="b9192-174">However, it isn't an essential pattern to implement in a DDD design or even in general .NET development.</span></span>

<span data-ttu-id="b9192-175">たとえば、このガイドに対するフィードバックを直接提供してくれた Jimmy Bogard は次のように述べています。</span><span class="sxs-lookup"><span data-stu-id="b9192-175">For instance, Jimmy Bogard, when providing direct feedback for this guide, said the following:</span></span>

> <span data-ttu-id="b9192-176">おそらく、これは私の最大のフィードバックになるでしょう。</span><span class="sxs-lookup"><span data-stu-id="b9192-176">This’ll probably be my biggest feedback.</span></span> <span data-ttu-id="b9192-177">私はリポジトリが好きではありません。その主な理由は、基本となる永続化メカニズムの重要な詳細が隠ぺいされていることです。</span><span class="sxs-lookup"><span data-stu-id="b9192-177">I’m really not a fan of repositories, mainly because they hide the important details of the underlying persistence mechanism.</span></span> <span data-ttu-id="b9192-178">私がコマンドに MediatR を採用する理由もそこにあります。</span><span class="sxs-lookup"><span data-stu-id="b9192-178">It’s why I go for MediatR for commands, too.</span></span> <span data-ttu-id="b9192-179">永続レイヤーの機能をフルに活用し、集約ルートにドメイン動作のすべてをプッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-179">I can use the full power of the persistence layer, and push all that domain behavior into my aggregate roots.</span></span> <span data-ttu-id="b9192-180">通常は、リポジトリでのシミュレーションを行いたくないので、実際のデータで統合テストを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9192-180">I don’t usually want to mock my repositories – I still need to have that integration test with the real thing.</span></span> <span data-ttu-id="b9192-181">CQRS を利用すれば、もうリポジトリは不要です。</span><span class="sxs-lookup"><span data-stu-id="b9192-181">Going CQRS meant that we didn’t really have a need for repositories any more.</span></span>

<span data-ttu-id="b9192-182">リポジトリは便利ですが、集約パターンやリッチ ドメイン モデルとは異なり、DDD においてリポジトリは不可欠ではありません。</span><span class="sxs-lookup"><span data-stu-id="b9192-182">Repositories are useful, but they aren't critical for your DDD, in the way that the Aggregate pattern and rich domain model are.</span></span> <span data-ttu-id="b9192-183">したがって、リポジトリ パターンは使用しても、しなくても、かまいません。</span><span class="sxs-lookup"><span data-stu-id="b9192-183">Therefore, use the Repository pattern or not, as you see fit.</span></span>

## <a name="the-specification-pattern"></a><span data-ttu-id="b9192-184">仕様パターン</span><span class="sxs-lookup"><span data-stu-id="b9192-184">The Specification pattern</span></span>

<span data-ttu-id="b9192-185">仕様パターン (正式名称はクエリ仕様パターン) は、並べ替え/ページング ロジックを指定可能なクエリ定義を配置する場所として設けられた DDD パターンです。</span><span class="sxs-lookup"><span data-stu-id="b9192-185">The specification pattern (its full name would be Query-specification pattern) is a DDD pattern designed as the place where you can put the definition of a query with optional sorting and paging logic.</span></span>

<span data-ttu-id="b9192-186">仕様パターンによって、オブジェクトのクエリが定義されます。</span><span class="sxs-lookup"><span data-stu-id="b9192-186">The specification pattern defines a query in an object.</span></span> <span data-ttu-id="b9192-187">たとえば、必要な入力パラメーター (`pageNumber`、`pageSize`、`filter` など) を受け取る `PagedProduct` 仕様を作成することで、製品を検索するページ指定クエリをカプセル化できます。その後、任意のリポジトリ メソッド (通常は List() オーバーロード) 内で、`ISpecification` を受け取り、その仕様に基づいて予想されるクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9192-187">For example, to encapsulate a paged query that searches for some products, you can create a `PagedProduct` specification that takes the necessary input parameters, such as `pageNumber`, `pageSize`, `filter`, etc. Then, within any Repository method (usually a List() overload), it'd accept an `ISpecification` and run the expected query based on that specification.</span></span>

<span data-ttu-id="b9192-188">このアプローチにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="b9192-188">There are several benefits to this approach:</span></span>

- <span data-ttu-id="b9192-189">仕様には議論の余地のある名前 (単なる一連の LINQ 式ではなく) が付いています。</span><span class="sxs-lookup"><span data-stu-id="b9192-189">The specification has a name (as opposed to just a bunch of LINQ expressions) that you can discuss about.</span></span>

- <span data-ttu-id="b9192-190">仕様は単独で単体テストを実行し、適切であることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b9192-190">The specification can be unit tested in isolation to ensure it's right.</span></span> <span data-ttu-id="b9192-191">同様の動作が必要な場合に、仕様を容易に再利用できます。</span><span class="sxs-lookup"><span data-stu-id="b9192-191">It can also easily be reused if you need similar behavior.</span></span> <span data-ttu-id="b9192-192">たとえば、MVC ビュー アクションと Web API アクション、およびさまざまなサービスで仕様を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="b9192-192">For example, on an MVC View action and a Web API action, as well as in various services.</span></span>

- <span data-ttu-id="b9192-193">仕様は、返されるデータの構造の記述にも使用できるため、クエリで必要なデータだけを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="b9192-193">A specification can also be used to describe the shape of the data to be returned, so that queries can return just the data they required.</span></span> <span data-ttu-id="b9192-194">これにより、Web アプリケーションの遅延読み込み (通常はお勧めできない操作) の必要がなくなり、リポジトリの実装にこうした繁雑な詳細を取り入れずに済みます。</span><span class="sxs-lookup"><span data-stu-id="b9192-194">This eliminates the need for lazy loading in web applications, which is usually not recommended, and helps keep repository implementations from becoming cluttered with these details.</span></span>

<span data-ttu-id="b9192-195">一般的な仕様インターフェイスの例として、[eShopOnWeb](https://github.com/dotnet-architecture/eShopOnWeb) から抜粋した次のコードをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b9192-195">An example of a generic specification interface is the following code from [eShopOnWeb](https://github.com/dotnet-architecture/eShopOnWeb).</span></span>

```csharp
// https://github.com/dotnet-architecture/eShopOnWeb
public interface ISpecification<T>
{
    Expression<Func<T, bool>> Criteria { get; }
    List<Expression<Func<T, object>>> Includes { get; }
    List<string> IncludeStrings { get; }
}
```

<span data-ttu-id="b9192-196">次のセクションでは、仕様パターンを EF Core 2.x で実装する方法と、任意のリポジトリ クラスから使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b9192-196">The upcoming sections explain how to implement the specification pattern with EF Core 2.x and how to use it from any Repository class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9192-197">仕様パターンは、次の「その他の技術情報」セクションに示されているように、さまざまな方法で実装できる古いパターンです。</span><span class="sxs-lookup"><span data-stu-id="b9192-197">The specification pattern is an old pattern that can be implemented in many different ways, as in the following additional resources.</span></span> <span data-ttu-id="b9192-198">パターンやアイデアとしては古いアプローチがわかりやすいかもしれませんが、Linq や式のような最新の言語機能を利用していない古い実装には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="b9192-198">As a pattern/idea, older approaches are good to know, but beware of older implementations that are not taking advantage of modern language capabilities like Linq and expressions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9192-199">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="b9192-199">Additional resources</span></span>

### <a name="the-repository-pattern"></a><span data-ttu-id="b9192-200">リポジトリ パターン</span><span class="sxs-lookup"><span data-stu-id="b9192-200">The Repository pattern</span></span>

- <span data-ttu-id="b9192-201">**リポジトリ パターン**
  [https://deviq.com/repository-pattern/](https://deviq.com/repository-pattern/)</span><span class="sxs-lookup"><span data-stu-id="b9192-201">**The Repository pattern**
[https://deviq.com/repository-pattern/](https://deviq.com/repository-pattern/)</span></span>

- <span data-ttu-id="b9192-202">**Edward Hieatt、Rob Mee。リポジトリ パターン。**
  [_https://martinfowler.com/eaaCatalog/repository.html_](https://martinfowler.com/eaaCatalog/repository.html)</span><span class="sxs-lookup"><span data-stu-id="b9192-202">**Edward Hieatt and Rob Mee. Repository pattern.**
[_https://martinfowler.com/eaaCatalog/repository.html_](https://martinfowler.com/eaaCatalog/repository.html)</span></span>

- <span data-ttu-id="b9192-203">**リポジトリ パターン**
  [_https://docs.microsoft.com/previous-versions/msp-n-p/ff649690(v=pandp.10)_](https://docs.microsoft.com/previous-versions/msp-n-p/ff649690(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="b9192-203">**The Repository pattern**
[_https://docs.microsoft.com/previous-versions/msp-n-p/ff649690(v=pandp.10)_](https://docs.microsoft.com/previous-versions/msp-n-p/ff649690(v=pandp.10))</span></span>

- <span data-ttu-id="b9192-204">**Eric Evans。Domain-Driven Design: Tackling Complexity in the Heart of Software (ドメイン駆動設計: ソフトウェア中心部の複雑さへの取り組み)。**</span><span class="sxs-lookup"><span data-stu-id="b9192-204">**Eric Evans. Domain-Driven Design: Tackling Complexity in the Heart of Software.**</span></span> <span data-ttu-id="b9192-205">(書籍: リポジトリ パターンに関する説明が含まれています) [_https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/_](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/)</span><span class="sxs-lookup"><span data-stu-id="b9192-205">(Book; includes a discussion of the Repository pattern) [_https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/_](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/)</span></span>

### <a name="unit-of-work-pattern"></a><span data-ttu-id="b9192-206">Unit of Work パターン</span><span class="sxs-lookup"><span data-stu-id="b9192-206">Unit of Work pattern</span></span>

- <span data-ttu-id="b9192-207">**Martin Fowler。Unit of Work パターン。**
  [_https://martinfowler.com/eaaCatalog/unitOfWork.html_](https://martinfowler.com/eaaCatalog/unitOfWork.html)</span><span class="sxs-lookup"><span data-stu-id="b9192-207">**Martin Fowler. Unit of Work pattern.**
[_https://martinfowler.com/eaaCatalog/unitOfWork.html_](https://martinfowler.com/eaaCatalog/unitOfWork.html)</span></span>

- <span data-ttu-id="b9192-208">**ASP.NET MVC アプリケーションでの Repository および Unit of Work パターンの実装**
  [_https://docs.microsoft.com/aspnet/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application_](https://docs.microsoft.com/aspnet/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)</span><span class="sxs-lookup"><span data-stu-id="b9192-208">**Implementing the Repository and Unit of Work Patterns in an ASP.NET MVC Application**
[_https://docs.microsoft.com/aspnet/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application_](https://docs.microsoft.com/aspnet/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)</span></span>

### <a name="the-specification-pattern"></a><span data-ttu-id="b9192-209">仕様パターン</span><span class="sxs-lookup"><span data-stu-id="b9192-209">The Specification pattern</span></span>

- <span data-ttu-id="b9192-210">**仕様パターン。**
  [_https://deviq.com/specification-pattern/_](https://deviq.com/specification-pattern/)</span><span class="sxs-lookup"><span data-stu-id="b9192-210">**The Specification pattern.**
[_https://deviq.com/specification-pattern/_](https://deviq.com/specification-pattern/)</span></span>

- <span data-ttu-id="b9192-211">**Evans, Eric (2004 年)。「Domain Driven Design」(ドメイン駆動設計)。Addison-Wesley. p. 224.**</span><span class="sxs-lookup"><span data-stu-id="b9192-211">**Evans, Eric (2004). Domain Driven Design. Addison-Wesley. p. 224.**</span></span>

- <span data-ttu-id="b9192-212">**「Specifications」(仕様)。Martin Fowler**
  [_https://www.martinfowler.com/apsupp/spec.pdf/_](https://www.martinfowler.com/apsupp/spec.pdf)</span><span class="sxs-lookup"><span data-stu-id="b9192-212">**Specifications. Martin Fowler**
[_https://www.martinfowler.com/apsupp/spec.pdf/_](https://www.martinfowler.com/apsupp/spec.pdf)</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="b9192-213">[前へ](domain-events-design-implementation.md)
[次へ](infrastructure-persistence-layer-implemenation-entity-framework-core.md)</span><span class="sxs-lookup"><span data-stu-id="b9192-213">[Previous](domain-events-design-implementation.md)
[Next](infrastructure-persistence-layer-implemenation-entity-framework-core.md)</span></span>
