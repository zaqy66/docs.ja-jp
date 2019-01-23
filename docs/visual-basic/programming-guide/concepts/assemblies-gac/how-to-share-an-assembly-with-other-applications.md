---
title: '方法: その他のアプリケーション (Visual Basic) とアセンブリを共有します。'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: d0e1dafc700b55a63342331b3280337d2c93cbd1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631829"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a><span data-ttu-id="0a510-102">方法: その他のアプリケーション (Visual Basic) とアセンブリを共有します。</span><span class="sxs-lookup"><span data-stu-id="0a510-102">How to: Share an Assembly with Other Applications (Visual Basic)</span></span>
<span data-ttu-id="0a510-103">アセンブリはプライベートまたは共有にすることができます。既定では、ほとんどの単純なプログラムは、他のアプリケーションによって使われることを意図されていないので、プライベート アセンブリで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0a510-103">Assemblies can be private or shared: by default, most simple programs consist of a private assembly because they are not intended to be used by other applications.</span></span>  
  
 <span data-ttu-id="0a510-104">他のアプリケーションとアセンブリを共有するには、[グローバル アセンブリ キャッシュ](../../../../framework/app-domains/gac.md) (GAC) にアセンブリを置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a510-104">In order to share an assembly with other applications, it must be placed in the [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span></span>  
  
### <a name="sharing-an-assembly"></a><span data-ttu-id="0a510-105">アセンブリの共有</span><span class="sxs-lookup"><span data-stu-id="0a510-105">Sharing an assembly</span></span>  
  
1.  <span data-ttu-id="0a510-106">アセンブリを作成します。</span><span class="sxs-lookup"><span data-stu-id="0a510-106">Create your assembly.</span></span> <span data-ttu-id="0a510-107">詳しくは、「[アセンブリの作成](../../../../framework/app-domains/create-assemblies.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0a510-107">For more information, see [Creating Assemblies](../../../../framework/app-domains/create-assemblies.md).</span></span>  
  
2.  <span data-ttu-id="0a510-108">アセンブリに厳密な名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0a510-108">Assign a strong name to your assembly.</span></span> <span data-ttu-id="0a510-109">詳細については、「[方法 :厳密な名前でアセンブリに署名する](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a510-109">For more information, see [How to: Sign an Assembly with a Strong Name](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span>  
  
3.  <span data-ttu-id="0a510-110">アセンブリにバージョン情報を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0a510-110">Assign version information to your assembly.</span></span> <span data-ttu-id="0a510-111">詳細については、「[アセンブリのバージョン管理](../../../../framework/app-domains/assembly-versioning.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a510-111">For more information, see [Assembly Versioning](../../../../framework/app-domains/assembly-versioning.md).</span></span>  
  
4.  <span data-ttu-id="0a510-112">グローバル アセンブリ キャッシュにアセンブリを追加します。</span><span class="sxs-lookup"><span data-stu-id="0a510-112">Add your assembly to the Global Assembly Cache.</span></span> <span data-ttu-id="0a510-113">詳細については、「[方法 :グローバル アセンブリ キャッシュにアセンブリをインストール](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md)します。</span><span class="sxs-lookup"><span data-stu-id="0a510-113">For more information, see [How to: Install an Assembly into the Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span></span>  
  
5.  <span data-ttu-id="0a510-114">他のアプリケーションからアセンブリに含まれる型にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0a510-114">Access the types contained in the assembly from the other applications.</span></span> <span data-ttu-id="0a510-115">詳細については、「[方法 :厳密な名前のアセンブリ参照](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md)します。</span><span class="sxs-lookup"><span data-stu-id="0a510-115">For more information, see [How to: Reference a Strong-Named Assembly](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a510-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a510-116">See also</span></span>

- [<span data-ttu-id="0a510-117">プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="0a510-117">Programming Concepts</span></span>](../../../../visual-basic/programming-guide/concepts/index.md)
- [<span data-ttu-id="0a510-118">アセンブリとグローバル アセンブリ キャッシュ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0a510-118">Assemblies and the Global Assembly Cache (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [<span data-ttu-id="0a510-119">アセンブリを使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="0a510-119">Programming with Assemblies</span></span>](../../../../framework/app-domains/programming-with-assemblies.md)
