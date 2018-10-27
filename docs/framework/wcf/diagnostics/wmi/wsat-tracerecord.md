---
title: WSAT_TraceRecord
ms.date: 03/30/2017
ms.assetid: 99bc7f66-1335-40d8-aa68-e754d569dc0d
ms.openlocfilehash: 907e764cf032e595c7aba455fd4808a640f68016
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50046280"
---
# <a name="wsattracerecord"></a><span data-ttu-id="3df5b-102">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="3df5b-102">WSAT_TraceRecord</span></span>
<span data-ttu-id="3df5b-103">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="3df5b-103">WSAT_TraceRecord</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3df5b-104">構文</span><span class="sxs-lookup"><span data-stu-id="3df5b-104">Syntax</span></span>  
  
```csharp
class WSAT_TraceRecord : WSAT_TraceEvent  
{  
  object ActivityID;  
  sint32 EventID;  
  string TraceRecord;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3df5b-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df5b-105">Methods</span></span>  
 <span data-ttu-id="3df5b-106">WSAT_TraceRecord クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="3df5b-106">The WSAT_TraceRecord class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3df5b-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3df5b-107">Properties</span></span>  
 <span data-ttu-id="3df5b-108">WSAT_TraceRecord クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3df5b-108">The WSAT_TraceRecord class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="3df5b-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="3df5b-109">ActivityID</span></span>  
 <span data-ttu-id="3df5b-110">データ型: object</span><span class="sxs-lookup"><span data-stu-id="3df5b-110">Data type: object</span></span>  
<span data-ttu-id="3df5b-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3df5b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3df5b-112">トレース レコードのアクティビティ ID です。</span><span class="sxs-lookup"><span data-stu-id="3df5b-112">The activity ID of the trace record.</span></span>  
  
### <a name="eventid"></a><span data-ttu-id="3df5b-113">EventID</span><span class="sxs-lookup"><span data-stu-id="3df5b-113">EventID</span></span>  
 <span data-ttu-id="3df5b-114">データ型 : sint32</span><span class="sxs-lookup"><span data-stu-id="3df5b-114">Data type: sint32</span></span>  
<span data-ttu-id="3df5b-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3df5b-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3df5b-116">トレース レコードのイベント ID です。</span><span class="sxs-lookup"><span data-stu-id="3df5b-116">The event ID of the trace record.</span></span>  
  
### <a name="tracerecord"></a><span data-ttu-id="3df5b-117">TraceRecord</span><span class="sxs-lookup"><span data-stu-id="3df5b-117">TraceRecord</span></span>  
 <span data-ttu-id="3df5b-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="3df5b-118">Data type: string</span></span>  
<span data-ttu-id="3df5b-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3df5b-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3df5b-120">トレース レコード</span><span class="sxs-lookup"><span data-stu-id="3df5b-120">Trace Record</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3df5b-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="3df5b-121">Requirements</span></span>  
  
|<span data-ttu-id="3df5b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="3df5b-122">MOF</span></span>|<span data-ttu-id="3df5b-123">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="3df5b-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3df5b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3df5b-124">Namespace</span></span>|<span data-ttu-id="3df5b-125">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="3df5b-125">Defined in root\ServiceModel</span></span>|
