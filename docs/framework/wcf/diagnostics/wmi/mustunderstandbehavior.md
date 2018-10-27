---
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 0f3efc446104a1afff507f6e7d2cd8c01c4ed417
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452600"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="b043e-102">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="b043e-102">MustUnderstandBehavior</span></span>
<span data-ttu-id="b043e-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="b043e-103">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b043e-104">構文</span><span class="sxs-lookup"><span data-stu-id="b043e-104">Syntax</span></span>  
  
```csharp
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b043e-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="b043e-105">Methods</span></span>  
 <span data-ttu-id="b043e-106">MustUnderstandBehavior クラスで定義されるメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="b043e-106">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b043e-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b043e-107">Properties</span></span>  
 <span data-ttu-id="b043e-108">MustUnderstandBehavior クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="b043e-108">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="b043e-109">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="b043e-109">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="b043e-110">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="b043e-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="b043e-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b043e-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b043e-112">`true` の場合、未処理の `MustUnderstand` 属性を持つすべての SOAP ヘッダーは、動作が例外をスローする原因となります。</span><span class="sxs-lookup"><span data-stu-id="b043e-112">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b043e-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="b043e-113">Requirements</span></span>  
  
|<span data-ttu-id="b043e-114">MOF</span><span class="sxs-lookup"><span data-stu-id="b043e-114">MOF</span></span>|<span data-ttu-id="b043e-115">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="b043e-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b043e-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="b043e-116">Namespace</span></span>|<span data-ttu-id="b043e-117">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="b043e-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b043e-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b043e-118">See Also</span></span>  
 <xref:System.ServiceModel.Description.MustUnderstandBehavior>
