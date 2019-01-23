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
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a>方法: その他のアプリケーション (Visual Basic) とアセンブリを共有します。
アセンブリはプライベートまたは共有にすることができます。既定では、ほとんどの単純なプログラムは、他のアプリケーションによって使われることを意図されていないので、プライベート アセンブリで構成されます。  
  
 他のアプリケーションとアセンブリを共有するには、[グローバル アセンブリ キャッシュ](../../../../framework/app-domains/gac.md) (GAC) にアセンブリを置く必要があります。  
  
### <a name="sharing-an-assembly"></a>アセンブリの共有  
  
1.  アセンブリを作成します。 詳しくは、「[アセンブリの作成](../../../../framework/app-domains/create-assemblies.md)」をご覧ください。  
  
2.  アセンブリに厳密な名前を割り当てます。 詳細については、「[方法 :厳密な名前でアセンブリに署名する](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)」を参照してください。  
  
3.  アセンブリにバージョン情報を割り当てます。 詳細については、「[アセンブリのバージョン管理](../../../../framework/app-domains/assembly-versioning.md)」を参照してください。  
  
4.  グローバル アセンブリ キャッシュにアセンブリを追加します。 詳細については、「[方法 :グローバル アセンブリ キャッシュにアセンブリをインストール](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md)します。  
  
5.  他のアプリケーションからアセンブリに含まれる型にアクセスします。 詳細については、「[方法 :厳密な名前のアセンブリ参照](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md)します。  
  
## <a name="see-also"></a>関連項目

- [プログラミングの概念](../../../../visual-basic/programming-guide/concepts/index.md)
- [アセンブリとグローバル アセンブリ キャッシュ (Visual Basic)](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [アセンブリを使用したプログラミング](../../../../framework/app-domains/programming-with-assemblies.md)
