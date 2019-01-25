---
title: ServiceBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 5faa266f-587f-4e03-828d-1c7dd5acfe65
ms.openlocfilehash: 420686ebda7f23a5d883deece251b034147fafa4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654582"
---
# <a name="servicebehaviorattribute"></a><span data-ttu-id="6bc95-102">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="6bc95-102">ServiceBehaviorAttribute</span></span>
<span data-ttu-id="6bc95-103">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="6bc95-103">ServiceBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bc95-104">構文</span><span class="sxs-lookup"><span data-stu-id="6bc95-104">Syntax</span></span>  
  
```csharp
class ServiceBehaviorAttribute : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  string ConfigurationName;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  string InstanceContextMode;  
  sint32 MaxItemsInObjectGraph;  
  string Name;  
  string Namespace;  
  boolean ReleaseServiceInstanceOnTransactionComplete;  
  boolean TransactionAutoCompleteOnSessionClose;  
  string TransactionIsolationLevel;  
  datetime TransactionTimeout;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6bc95-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="6bc95-105">Methods</span></span>  
 <span data-ttu-id="6bc95-106">ServiceBehaviorAttribute クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="6bc95-106">The ServiceBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6bc95-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="6bc95-107">Properties</span></span>  
 <span data-ttu-id="6bc95-108">ServiceBehaviorAttribute クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="6bc95-108">The ServiceBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="6bc95-109">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="6bc95-109">AutomaticSessionShutdown</span></span>  
 <span data-ttu-id="6bc95-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-112">クライアントが出力セッションを閉じるときにセッションを自動的に閉じるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-112">Indicates whether to automatically close a session when a client closes an output session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="6bc95-113">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="6bc95-113">ConcurrencyMode</span></span>  
 <span data-ttu-id="6bc95-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="6bc95-114">Data type: string</span></span>  
<span data-ttu-id="6bc95-115">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-116">サービスで、1 つのスレッド、複数のスレッド、または再入呼び出しをサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-116">Indicates whether a service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="configurationname"></a><span data-ttu-id="6bc95-117">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6bc95-117">ConfigurationName</span></span>  
 <span data-ttu-id="6bc95-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="6bc95-118">Data type: string</span></span>  
  
 <span data-ttu-id="6bc95-119">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-120">サービス構成の名前。</span><span class="sxs-lookup"><span data-stu-id="6bc95-120">The name of the service configuration.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="6bc95-121">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="6bc95-121">IgnoreExtensionDataObject</span></span>  
 <span data-ttu-id="6bc95-122">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-123">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-124">不明なシリアル化データをネットワークで送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-124">Specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="6bc95-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="6bc95-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="6bc95-126">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-127">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-128">デバッグの目的でクライアントに返される SOAP エラーの詳細に、マネージド例外情報を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
### <a name="instancecontextmode"></a><span data-ttu-id="6bc95-129">InstanceContextMode</span><span class="sxs-lookup"><span data-stu-id="6bc95-129">InstanceContextMode</span></span>  
 <span data-ttu-id="6bc95-130">データ型: string</span><span class="sxs-lookup"><span data-stu-id="6bc95-130">Data type: string</span></span>  
  
 <span data-ttu-id="6bc95-131">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-132">新しいサービス オブジェクトを作成するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-132">Specifies when a new service object is created.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="6bc95-133">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="6bc95-133">MaxItemsInObjectGraph</span></span>  
 <span data-ttu-id="6bc95-134">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="6bc95-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="6bc95-135">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-136">1 つのシリアル化されたオブジェクトで許可される項目の最大数。</span><span class="sxs-lookup"><span data-stu-id="6bc95-136">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="name"></a><span data-ttu-id="6bc95-137">名前</span><span class="sxs-lookup"><span data-stu-id="6bc95-137">Name</span></span>  
 <span data-ttu-id="6bc95-138">データ型: string</span><span class="sxs-lookup"><span data-stu-id="6bc95-138">Data type: string</span></span>  
  
 <span data-ttu-id="6bc95-139">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-140">WSDL でのサービスの名前属性。</span><span class="sxs-lookup"><span data-stu-id="6bc95-140">The name attribute of the service in WSDL.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="6bc95-141">名前空間</span><span class="sxs-lookup"><span data-stu-id="6bc95-141">Namespace</span></span>  
 <span data-ttu-id="6bc95-142">データ型: string</span><span class="sxs-lookup"><span data-stu-id="6bc95-142">Data type: string</span></span>  
  
 <span data-ttu-id="6bc95-143">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-144">WSDL でのサービスのターゲット名前空間。</span><span class="sxs-lookup"><span data-stu-id="6bc95-144">The target namespace of the service in WSDL.</span></span>  
  
### <a name="releaseserviceinstanceontransactioncomplete"></a><span data-ttu-id="6bc95-145">ReleaseServiceInstanceOnTransactionComplete</span><span class="sxs-lookup"><span data-stu-id="6bc95-145">ReleaseServiceInstanceOnTransactionComplete</span></span>  
 <span data-ttu-id="6bc95-146">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-146">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-147">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-148">現在のトランザクションの完了時に、サービス オブジェクトをリサイクルするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-148">Specifies whether the service object is recycled when the current transaction completes.</span></span>  
  
### <a name="transactionautocompleteonsessionclose"></a><span data-ttu-id="6bc95-149">TransactionAutoCompleteOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="6bc95-149">TransactionAutoCompleteOnSessionClose</span></span>  
 <span data-ttu-id="6bc95-150">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-150">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-151">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-152">現在のセッションの終了時に、保留中のトランザクションを完了するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-152">Specifies whether pending transactions are completed when the current session closes.</span></span>  
  
### <a name="transactionisolationlevel"></a><span data-ttu-id="6bc95-153">TransactionIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6bc95-153">TransactionIsolationLevel</span></span>  
 <span data-ttu-id="6bc95-154">データ型: string</span><span class="sxs-lookup"><span data-stu-id="6bc95-154">Data type: string</span></span>  
  
 <span data-ttu-id="6bc95-155">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-156">トランザクションの分離レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-156">Specifies the transaction isolation level.</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="6bc95-157">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="6bc95-157">TransactionTimeout</span></span>  
 <span data-ttu-id="6bc95-158">データ型 : datetime</span><span class="sxs-lookup"><span data-stu-id="6bc95-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="6bc95-159">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-160">トランザクションを完了しなければならない期間。</span><span class="sxs-lookup"><span data-stu-id="6bc95-160">The period within which a transaction must complete.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="6bc95-161">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="6bc95-161">UseSynchronizationContext</span></span>  
 <span data-ttu-id="6bc95-162">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-162">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-163">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-164">現在の同期コンテキストを使用してスレッドの実行を選択するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-164">Specifies whether to use the current synchronization context to choose the thread execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="6bc95-165">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="6bc95-165">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="6bc95-166">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="6bc95-166">Data type: boolean</span></span>  
  
 <span data-ttu-id="6bc95-167">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6bc95-167">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6bc95-168">システムまたはアプリケーションで SOAP MustUnderstand ヘッダー処理を強制的に行うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bc95-168">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bc95-169">必要条件</span><span class="sxs-lookup"><span data-stu-id="6bc95-169">Requirements</span></span>  
  
|<span data-ttu-id="6bc95-170">MOF</span><span class="sxs-lookup"><span data-stu-id="6bc95-170">MOF</span></span>|<span data-ttu-id="6bc95-171">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="6bc95-171">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6bc95-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="6bc95-172">Namespace</span></span>|<span data-ttu-id="6bc95-173">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="6bc95-173">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6bc95-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="6bc95-174">See also</span></span>
- <xref:System.ServiceModel.ServiceBehaviorAttribute>
