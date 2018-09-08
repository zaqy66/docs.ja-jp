---
title: 接続文字列を定義する方法
ms.date: 03/30/2017
ms.assetid: 6027335d-4e26-420d-9151-6523289b1989
ms.openlocfilehash: f40b8bc68eda1cb4b64b34d12b2922da69929203
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44210170"
---
# <a name="how-to-define-the-connection-string"></a><span data-ttu-id="86aef-102">接続文字列を定義する方法</span><span class="sxs-lookup"><span data-stu-id="86aef-102">How to: Define the Connection String</span></span>
<span data-ttu-id="86aef-103">このトピックでは、概念モデルに接続するための接続文字列を定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86aef-103">This topic shows how to define the connection string that is used when connecting to a conceptual model.</span></span> <span data-ttu-id="86aef-104">このトピックではに基づいて、 [AdventureWorks Sales](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832)概念モデル。</span><span class="sxs-lookup"><span data-stu-id="86aef-104">This topic is based on the [AdventureWorks Sales](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) conceptual model.</span></span> <span data-ttu-id="86aef-105">AdventureWorks Sales Model は、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] ドキュメントのタスク関連のトピック全般で使用されます。</span><span class="sxs-lookup"><span data-stu-id="86aef-105">The AdventureWorks Sales Model is used throughout the task-related topics in the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] documentation.</span></span> <span data-ttu-id="86aef-106">このトピックでは、既に構成されていることを想定しています、 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] AdventureWorks Sales Model が定義されているとします。</span><span class="sxs-lookup"><span data-stu-id="86aef-106">This topic assumes that you have already configured the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] and defined the AdventureWorks Sales Model.</span></span> <span data-ttu-id="86aef-107">詳細については、次を参照してください。[方法: モデル ファイルとマッピング ファイルを手動で定義](https://msdn.microsoft.com/library/d4fd6864-f2a1-48f0-aa32-1e318775a99a)します。</span><span class="sxs-lookup"><span data-stu-id="86aef-107">For more information, see [How to: Manually Define the Model and Mapping Files](https://msdn.microsoft.com/library/d4fd6864-f2a1-48f0-aa32-1e318775a99a).</span></span> <span data-ttu-id="86aef-108">このトピックの手順でに含まれるも[方法: Entity Framework プロジェクトを手動で構成](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)します。</span><span class="sxs-lookup"><span data-stu-id="86aef-108">The procedures in this topic are also included in [How to: Manually Configure an Entity Framework Project](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="86aef-109">使用する場合、[!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)]ウィザード、Visual Studio プロジェクトに自動的に .edmx ファイルを生成し、使用するプロジェクトを構成、、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="86aef-109">If you use the [!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)] Wizard in a Visual Studio project, it automatically generates an .edmx file and configures the project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="86aef-110">詳細については、次を参照してください[方法: Entity Data Model ウィザードを使用して、。](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)</span><span class="sxs-lookup"><span data-stu-id="86aef-110">For more information, see [How to: Use the Entity Data Model Wizard](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)</span></span>  
  
### <a name="to-define-the-entity-framework-connection-string"></a><span data-ttu-id="86aef-111">Entity Framework 接続文字列を定義するには</span><span class="sxs-lookup"><span data-stu-id="86aef-111">To define the Entity Framework connection string</span></span>  
  
-   <span data-ttu-id="86aef-112">プロジェクトのアプリケーション構成ファイル (app.config) を開き、次の接続文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="86aef-112">Open the project's application configuration file (app.config) and add the following connection string:</span></span>  
  
  
  
     <span data-ttu-id="86aef-113">プロジェクトがアプリケーション構成ファイルを持たない場合は、1 つを選択して、追加**新しい項目の追加**から、**プロジェクト** メニューを選択すると、**全般**カテゴリで、選択**アプリケーション構成ファイル**、 をクリックし、**追加**します。</span><span class="sxs-lookup"><span data-stu-id="86aef-113">If your project does not have an application configuration file, you can add one by selecting **Add New Item** from the **Project** menu, selecting the **General** category, selecting **Application Configuration File**, and then clicking **Add**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86aef-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="86aef-114">See Also</span></span>  
 [<span data-ttu-id="86aef-115">クイック スタート</span><span class="sxs-lookup"><span data-stu-id="86aef-115">Quickstart</span></span>](https://msdn.microsoft.com/library/0bc534be-789f-4819-b9f6-76e51d961675)  
 [<span data-ttu-id="86aef-116">方法: 新しい .edmx ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="86aef-116">How to: Create a New .edmx File</span></span>](https://msdn.microsoft.com/library/beb8189e-e51c-4051-839c-9902c224abf2)  
 [<span data-ttu-id="86aef-117">ADO.NET Entity Data Model ツール</span><span class="sxs-lookup"><span data-stu-id="86aef-117">ADO.NET Entity Data Model  Tools</span></span>](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)
