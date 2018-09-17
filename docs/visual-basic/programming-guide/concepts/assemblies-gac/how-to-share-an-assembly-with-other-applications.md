---
title: '方法: アセンブリを他のアプリケーション (Visual Basic) と共有'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: 3d29a3558a64c02fc8c59035f2fee5c64c4a776f
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45746248"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a>方法: アセンブリを他のアプリケーション (Visual Basic) と共有
アセンブリはプライベートまたは共有にすることができます。既定では、ほとんどの単純なプログラムは、他のアプリケーションによって使われることを意図されていないので、プライベート アセンブリで構成されます。  
  
 他のアプリケーションとアセンブリを共有するには、[グローバル アセンブリ キャッシュ](../../../../framework/app-domains/gac.md) (GAC) にアセンブリを置く必要があります。  
  
### <a name="sharing-an-assembly"></a>アセンブリの共有  
  
1.  アセンブリを作成します。 詳しくは、「[アセンブリの作成](../../../../framework/app-domains/create-assemblies.md)」をご覧ください。  
  
2.  アセンブリに厳密な名前を割り当てます。 詳しくは、「[方法 : 厳密な名前でアセンブリに署名する](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)」をご覧ください。  
  
3.  アセンブリにバージョン情報を割り当てます。 詳細については、「[アセンブリのバージョン管理](../../../../framework/app-domains/assembly-versioning.md)」を参照してください。  
  
4.  グローバル アセンブリ キャッシュにアセンブリを追加します。 詳しくは、「[方法 : グローバル アセンブリ キャッシュにアセンブリをインストールする](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md)」をご覧ください。  
  
5.  他のアプリケーションからアセンブリに含まれる型にアクセスします。 詳しくは、「[方法 : 厳密な名前のアセンブリを参照する](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md)」をご覧ください。  
  
## <a name="see-also"></a>関連項目

- [プログラミングの概念](../../../../visual-basic/programming-guide/concepts/index.md)
- [アセンブリとグローバル アセンブリ キャッシュ (Visual Basic)](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
- [アセンブリを使用したプログラミング](../../../../framework/app-domains/programming-with-assemblies.md)
