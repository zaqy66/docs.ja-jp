---
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 334bab97a04ed464dce6944692b04a9ed1295296
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54613826"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="11836-102">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="11836-102">MustUnderstandBehavior</span></span>
<span data-ttu-id="11836-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="11836-103">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11836-104">構文</span><span class="sxs-lookup"><span data-stu-id="11836-104">Syntax</span></span>  
  
```csharp
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="11836-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="11836-105">Methods</span></span>  
 <span data-ttu-id="11836-106">MustUnderstandBehavior クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="11836-106">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="11836-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="11836-107">Properties</span></span>  
 <span data-ttu-id="11836-108">MustUnderstandBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="11836-108">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="11836-109">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="11836-109">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="11836-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="11836-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="11836-111">アクセスの種類:読み取り専用</span><span class="sxs-lookup"><span data-stu-id="11836-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="11836-112">`true` の場合、未処理の `MustUnderstand` 属性を持つすべての SOAP ヘッダーは、動作が例外をスローする原因となります。</span><span class="sxs-lookup"><span data-stu-id="11836-112">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11836-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="11836-113">Requirements</span></span>  
  
|<span data-ttu-id="11836-114">MOF</span><span class="sxs-lookup"><span data-stu-id="11836-114">MOF</span></span>|<span data-ttu-id="11836-115">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="11836-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="11836-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="11836-116">Namespace</span></span>|<span data-ttu-id="11836-117">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="11836-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="11836-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="11836-118">See also</span></span>
- <xref:System.ServiceModel.Description.MustUnderstandBehavior>
