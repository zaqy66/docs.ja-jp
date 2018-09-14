---
title: アセンブリと DLL の名前
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], DLLs
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
- DLLs, names
ms.assetid: e800b610-31b4-4949-9c14-cb60e9f254be
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97bd152cff53fb1c2edb107b6d6b34bd91ca1c49
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45516225"
---
# <a name="names-of-assemblies-and-dlls"></a><span data-ttu-id="6fd3a-102">アセンブリと DLL の名前</span><span class="sxs-lookup"><span data-stu-id="6fd3a-102">Names of Assemblies and DLLs</span></span>
<span data-ttu-id="6fd3a-103">アセンブリは、展開およびマネージ コード アプリケーションの id の単位です。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-103">An assembly is the unit of deployment and identity for managed code programs.</span></span> <span data-ttu-id="6fd3a-104">アセンブリは、1 つまたは複数のファイルにまたがることができます、通常このアセンブリは DLL と 1 対 1 をマップします。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-104">Although assemblies can span one or more files, typically an assembly maps one-to-one with a DLL.</span></span> <span data-ttu-id="6fd3a-105">そのため、このセクションでは、のみ DLL の名前付け規則、アセンブリの名前付け規則にマップできますがについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-105">Therefore, this section describes only DLL naming conventions, which then can be mapped to assembly naming conventions.</span></span>  
  
 <span data-ttu-id="6fd3a-106">**✓ DO** アセンブリ System.Data などの機能の大きなチャンクを提案する Dll の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-106">**✓ DO** choose names for your assembly DLLs that suggest large chunks of functionality, such as System.Data.</span></span>  
  
 <span data-ttu-id="6fd3a-107">アセンブリと DLL の名前が名前空間の名前に対応する必要はありませんが、アセンブリの名前を付けるときは、名前空間の名前を次に適切です。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-107">Assembly and DLL names don’t have to correspond to namespace names, but it is reasonable to follow the namespace name when naming assemblies.</span></span> <span data-ttu-id="6fd3a-108">適切な経験則では、アセンブリに含まれている名前空間の共通のプレフィックスに基づいた DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-108">A good rule of thumb is to name the DLL based on the common prefix of the namespaces contained in the assembly.</span></span> <span data-ttu-id="6fd3a-109">たとえば、2 つの名前空間を持つアセンブリ`MyCompany.MyTechnology.FirstFeature`と`MyCompany.MyTechnology.SecondFeature`、呼び出すことができます`MyCompany.MyTechnology.dll`します。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-109">For example, an assembly with two namespaces, `MyCompany.MyTechnology.FirstFeature` and `MyCompany.MyTechnology.SecondFeature`, could be called `MyCompany.MyTechnology.dll`.</span></span>  
  
 <span data-ttu-id="6fd3a-110">**✓ CONSIDER** Dll を次のパターンに従って名前付け。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-110">**✓ CONSIDER** naming DLLs according to the following pattern:</span></span>  
  
 `<Company>.<Component>.dll`  
  
 <span data-ttu-id="6fd3a-111">場所`<Component>`ドットで区切られた 1 つ以上の句が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-111">where `<Component>` contains one or more dot-separated clauses.</span></span> <span data-ttu-id="6fd3a-112">例えば:</span><span class="sxs-lookup"><span data-stu-id="6fd3a-112">For example:</span></span>  
  
 <span data-ttu-id="6fd3a-113">`Litware.Controls.dll`。</span><span class="sxs-lookup"><span data-stu-id="6fd3a-113">`Litware.Controls.dll`.</span></span>  
  
 <span data-ttu-id="6fd3a-114">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="6fd3a-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="6fd3a-115">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="6fd3a-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fd3a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="6fd3a-116">See also</span></span>

- [<span data-ttu-id="6fd3a-117">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="6fd3a-117">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="6fd3a-118">名前付けのガイドライン</span><span class="sxs-lookup"><span data-stu-id="6fd3a-118">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
