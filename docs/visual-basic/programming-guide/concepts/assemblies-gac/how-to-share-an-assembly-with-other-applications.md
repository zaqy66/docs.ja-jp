---
title: '方法: アセンブリを他のアプリケーション (Visual Basic) と共有'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: 3d29a3558a64c02fc8c59035f2fee5c64c4a776f
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44200143"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a><span data-ttu-id="d1cbb-102">方法: アセンブリを他のアプリケーション (Visual Basic) と共有</span><span class="sxs-lookup"><span data-stu-id="d1cbb-102">How to: Share an Assembly with Other Applications (Visual Basic)</span></span>
<span data-ttu-id="d1cbb-103">アセンブリはプライベートまたは共有にすることができます。既定では、ほとんどの単純なプログラムは、他のアプリケーションによって使われることを意図されていないので、プライベート アセンブリで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-103">Assemblies can be private or shared: by default, most simple programs consist of a private assembly because they are not intended to be used by other applications.</span></span>  
  
 <span data-ttu-id="d1cbb-104">他のアプリケーションとアセンブリを共有するには、[グローバル アセンブリ キャッシュ](../../../../framework/app-domains/gac.md) (GAC) にアセンブリを置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-104">In order to share an assembly with other applications, it must be placed in the [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span></span>  
  
### <a name="sharing-an-assembly"></a><span data-ttu-id="d1cbb-105">アセンブリの共有</span><span class="sxs-lookup"><span data-stu-id="d1cbb-105">Sharing an assembly</span></span>  
  
1.  <span data-ttu-id="d1cbb-106">アセンブリを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-106">Create your assembly.</span></span> <span data-ttu-id="d1cbb-107">詳しくは、「[アセンブリの作成](../../../../framework/app-domains/create-assemblies.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-107">For more information, see [Creating Assemblies](../../../../framework/app-domains/create-assemblies.md).</span></span>  
  
2.  <span data-ttu-id="d1cbb-108">アセンブリに厳密な名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-108">Assign a strong name to your assembly.</span></span> <span data-ttu-id="d1cbb-109">詳しくは、「[方法 : 厳密な名前でアセンブリに署名する](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-109">For more information, see [How to: Sign an Assembly with a Strong Name](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span>  
  
3.  <span data-ttu-id="d1cbb-110">アセンブリにバージョン情報を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-110">Assign version information to your assembly.</span></span> <span data-ttu-id="d1cbb-111">詳細については、「[アセンブリのバージョン管理](../../../../framework/app-domains/assembly-versioning.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-111">For more information, see [Assembly Versioning](../../../../framework/app-domains/assembly-versioning.md).</span></span>  
  
4.  <span data-ttu-id="d1cbb-112">グローバル アセンブリ キャッシュにアセンブリを追加します。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-112">Add your assembly to the Global Assembly Cache.</span></span> <span data-ttu-id="d1cbb-113">詳しくは、「[方法 : グローバル アセンブリ キャッシュにアセンブリをインストールする](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-113">For more information, see [How to: Install an Assembly into the Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span></span>  
  
5.  <span data-ttu-id="d1cbb-114">他のアプリケーションからアセンブリに含まれる型にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-114">Access the types contained in the assembly from the other applications.</span></span> <span data-ttu-id="d1cbb-115">詳しくは、「[方法 : 厳密な名前のアセンブリを参照する](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d1cbb-115">For more information, see [How to: Reference a Strong-Named Assembly](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1cbb-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1cbb-116">See also</span></span>

- [<span data-ttu-id="d1cbb-117">プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="d1cbb-117">Programming Concepts</span></span>](../../../../visual-basic/programming-guide/concepts/index.md)
- [<span data-ttu-id="d1cbb-118">アセンブリとグローバル アセンブリ キャッシュ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d1cbb-118">Assemblies and the Global Assembly Cache (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
- [<span data-ttu-id="d1cbb-119">アセンブリを使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="d1cbb-119">Programming with Assemblies</span></span>](../../../../framework/app-domains/programming-with-assemblies.md)
