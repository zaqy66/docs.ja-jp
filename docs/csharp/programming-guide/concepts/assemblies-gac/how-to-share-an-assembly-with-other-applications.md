---
title: '方法 : アセンブリを他のアプリケーションと共有する (C#)'
ms.date: 07/20/2015
ms.assetid: c30e972b-1693-4e05-b115-c31831fdf9f2
ms.openlocfilehash: a5b20061c759fd914193f24aa123317f13d31dce
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44266470"
---
# <a name="how-to-share-an-assembly-with-other-applications-c"></a>方法 : アセンブリを他のアプリケーションと共有する (C#)
アセンブリはプライベートまたは共有にすることができます。既定では、ほとんどの単純なプログラムは、他のアプリケーションによって使われることを意図されていないので、プライベート アセンブリで構成されます。  
  
 他のアプリケーションとアセンブリを共有するには、[グローバル アセンブリ キャッシュ](../../../../framework/app-domains/gac.md) (GAC) にアセンブリを置く必要があります。  
  
### <a name="sharing-an-assembly"></a>アセンブリの共有  
  
1.  アセンブリを作成します。 詳しくは、「[アセンブリの作成](../../../../framework/app-domains/create-assemblies.md)」をご覧ください。  
  
2.  アセンブリに厳密な名前を割り当てます。 詳しくは、「[方法 : 厳密な名前でアセンブリに署名する](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)」をご覧ください。  
  
3.  アセンブリにバージョン情報を割り当てます。 詳細については、「[アセンブリのバージョン管理](../../../../../docs/framework/app-domains/assembly-versioning.md)」を参照してください。  
  
4.  グローバル アセンブリ キャッシュにアセンブリを追加します。 詳しくは、「[方法 : グローバル アセンブリ キャッシュにアセンブリをインストールする](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md)」をご覧ください。  
  
5.  他のアプリケーションからアセンブリに含まれる型にアクセスします。 詳しくは、「[方法 : 厳密な名前のアセンブリを参照する](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md)」をご覧ください。  
  
## <a name="see-also"></a>参照

- [C# プログラミング ガイド](../../../../csharp/programming-guide/index.md)  
- [アセンブリを使用したプログラミング](../../../../framework/app-domains/programming-with-assemblies.md)
