---
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 0f3efc446104a1afff507f6e7d2cd8c01c4ed417
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49371797"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="b4a2b-102">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="b4a2b-102">MustUnderstandBehavior</span></span>
<span data-ttu-id="b4a2b-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="b4a2b-103">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4a2b-104">構文</span><span class="sxs-lookup"><span data-stu-id="b4a2b-104">Syntax</span></span>  
  
```csharp
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b4a2b-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="b4a2b-105">Methods</span></span>  
 <span data-ttu-id="b4a2b-106">MustUnderstandBehavior クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-106">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b4a2b-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4a2b-107">Properties</span></span>  
 <span data-ttu-id="b4a2b-108">MustUnderstandBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-108">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="b4a2b-109">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="b4a2b-109">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="b4a2b-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="b4a2b-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="b4a2b-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b4a2b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b4a2b-112">`true` の場合、未処理の `MustUnderstand` 属性を持つすべての SOAP ヘッダーは、動作が例外をスローする原因となります。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-112">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4a2b-113">要件</span><span class="sxs-lookup"><span data-stu-id="b4a2b-113">Requirements</span></span>  
  
|<span data-ttu-id="b4a2b-114">MOF</span><span class="sxs-lookup"><span data-stu-id="b4a2b-114">MOF</span></span>|<span data-ttu-id="b4a2b-115">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b4a2b-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4a2b-116">Namespace</span></span>|<span data-ttu-id="b4a2b-117">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="b4a2b-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b4a2b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4a2b-118">See Also</span></span>  
 <xref:System.ServiceModel.Description.MustUnderstandBehavior>
