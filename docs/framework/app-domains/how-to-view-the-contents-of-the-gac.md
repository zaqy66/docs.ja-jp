---
title: '方法 : グローバル アセンブリ キャッシュの内容を表示する'
ms.date: 03/30/2017
helpviewer_keywords:
- assemblies [.NET Framework], global assembly cache
- global assembly cache, viewing contents
- viewing assemblies in global assembly cache
- Gacutil.exe
- strong-named assemblies, global assembly cache
- GAC (global assembly cache), viewing contents
- list of assemblies in global assembly cache
- Global Assembly Cache tool
ms.assetid: c5f786a0-969b-4f14-9f02-e77c3384d9af
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3650de934cb3d2940d0e8e971d03aff856bddfd7
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43515480"
---
# <a name="how-to-view-the-contents-of-the-global-assembly-cache"></a><span data-ttu-id="1899e-102">方法 : グローバル アセンブリ キャッシュの内容を表示する</span><span class="sxs-lookup"><span data-stu-id="1899e-102">How to: View the Contents of the Global Assembly Cache</span></span>
<span data-ttu-id="1899e-103">[グローバル アセンブリ キャッシュ ツール (Gacutil.exe)](../../../docs/framework/tools/gacutil-exe-gac-tool.md) を使用すると、グローバル アセンブリ キャッシュの内容を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1899e-103">Use the [Global Assembly Cache tool (Gacutil.exe)](../../../docs/framework/tools/gacutil-exe-gac-tool.md) to view the contents of the global assembly cache.</span></span>  
  
### <a name="to-view-a-list-of-the-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="1899e-104">グローバル アセンブリ キャッシュ内のアセンブリの一覧を表示するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="1899e-104">To view a list of the assemblies in the global assembly cache</span></span>  
  
1.  <span data-ttu-id="1899e-105">[Visual Studio コマンド プロンプト](../../../docs/framework/tools/developer-command-prompt-for-vs.md)で次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="1899e-105">At the [Visual Studio command prompt](../../../docs/framework/tools/developer-command-prompt-for-vs.md), type the following command:</span></span>  
  
     <span data-ttu-id="1899e-106">**gacutil -l** </span><span class="sxs-lookup"><span data-stu-id="1899e-106">**gacutil -l** </span></span>  
     <span data-ttu-id="1899e-107">- または -</span><span class="sxs-lookup"><span data-stu-id="1899e-107">-or-</span></span>  
    <span data-ttu-id="1899e-108">**gacutil /l**</span><span class="sxs-lookup"><span data-stu-id="1899e-108">**gacutil /l**</span></span>  
  
 <span data-ttu-id="1899e-109">以前のバージョンの .NET Framework では、Windows のシェル拡張機能である [Shfusion.dll](https://msdn.microsoft.com/library/0d9464cf-ddba-4ca9-bbec-f678fb58f380) により、エクスプローラーでグローバル アセンブリ キャッシュを表示することができました。</span><span class="sxs-lookup"><span data-stu-id="1899e-109">In earlier versions of the .NET Framework, the [Shfusion.dll](https://msdn.microsoft.com/library/0d9464cf-ddba-4ca9-bbec-f678fb58f380) Windows shell extension enabled you to view the global assembly cache in File Explorer.</span></span> <span data-ttu-id="1899e-110">[!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] 以降では、Shfusion.dll は廃止されましたが、互換性のために残されています。</span><span class="sxs-lookup"><span data-stu-id="1899e-110">Beginning with the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], Shfusion.dll is obsolete.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1899e-111">参照</span><span class="sxs-lookup"><span data-stu-id="1899e-111">See Also</span></span>  
 [<span data-ttu-id="1899e-112">アセンブリとグローバル アセンブリ キャッシュの使用</span><span class="sxs-lookup"><span data-stu-id="1899e-112">Working with Assemblies and the Global Assembly Cache</span></span>](../../../docs/framework/app-domains/working-with-assemblies-and-the-gac.md)  
 [<span data-ttu-id="1899e-113">Gacutil.exe (グローバル アセンブリ キャッシュ ツール)</span><span class="sxs-lookup"><span data-stu-id="1899e-113">Gacutil.exe (Global Assembly Cache Tool)</span></span>](../../../docs/framework/tools/gacutil-exe-gac-tool.md)
