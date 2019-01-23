---
title: 埋め込まれた相互運用機能アセンブリへの参照が作成された&#39; &lt;assembly1&gt; &#39;アセンブリからそのアセンブリへの間接参照により&#39; &lt;assembly2&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc40059
- bc40059
helpviewer_keywords:
- VBC40059
- BC40059
ms.assetid: 520e39cb-8ab6-46f5-aa00-08afd51b4b7c
ms.openlocfilehash: fe04742e0a3be5e1d19ab4017e55f2293988a671
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560023"
---
# <a name="a-reference-was-created-to-embedded-interop-assembly-39ltassembly1gt39-because-of-an-indirect-reference-to-that-assembly-from-assembly-39ltassembly2gt39"></a>埋め込まれた相互運用機能アセンブリへの参照が作成された&#39; &lt;assembly1&gt; &#39;アセンブリからそのアセンブリへの間接参照により&#39; &lt;assembly2&gt;&#39;
埋め込まれた相互運用機能アセンブリ '\<assembly1>' への参照が作成されました。これは、そのアセンブリへの間接参照がアセンブリ '\<assembly2>' によって作成されたためです。 両方のアセンブリで '相互運用機能型の埋め込み' プロパティを変更することを検討してください。  
  
 `Embed Interop Types` プロパティが `True` に設定されたアセンブリ (assembly1) に参照を追加しました。 これにより、コンパイラは、このアセンブリから相互運用機能の型情報を埋め込むよう指示されます。 ただし、参照していた別のアセンブリ (assembly2) もこのアセンブリ (assembly1) を参照しており、また `Embed Interop Types` プロパティが `False` に設定されているため、コンパイラはこのアセンブリから相互運用機能の型情報を埋め込むことができません。  
  
> [!NOTE]
>  アセンブリ参照の `Embed Interop Types` プロパティを `True` に設定することは、コマンド ライン コンパイラの `/link` オプションを使用してアセンブリを参照することと同じです。  
  
 **エラー ID:** BC40059  
  
### <a name="to-address-this-warning"></a>この警告に対処するには  
  
-   両方のアセンブリに相互運用の型情報を埋め込むには、assembly1 へのすべての参照の `Embed Interop Types` プロパティを `True` に設定します。  
  
-   assembly1 の `Embed Interop Types` プロパティを `False` に設定すると警告を回避できます。 この場合は、相互運用機能型の情報は、プライマリ相互運用機能アセンブリ (PIA) によって提供されます。  
  
## <a name="see-also"></a>関連項目
- [/link (Visual Basic)](../../../visual-basic/reference/command-line-compiler/link.md)
- [アンマネージ コードとの相互運用](../../../framework/interop/index.md)
