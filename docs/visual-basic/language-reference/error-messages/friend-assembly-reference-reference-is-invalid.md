---
title: フレンド アセンブリ参照&lt;参照&gt;が無効です
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: cdedcc18aa82f6efd8c52cdca5d915d7d78e269f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611931"
---
# <a name="friend-assembly-reference-ltreferencegt-is-invalid"></a>フレンド アセンブリ参照&lt;参照&gt;が無効です
フレンド アセンブリ参照\<参照 > が無効です。 厳密な名前の署名つきアセンブリはその InternalsVisibleTo 宣言内で公開キーを指定しなければなりません。  
  
 渡すアセンブリ名、<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>属性コンス トラクターは、厳密な名前のアセンブリを識別しますは含まれません、`PublicKey`属性。  
  
 **エラー ID:** BC31535  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  厳密な名前のフレンド アセンブリの公開キーを確認します。 渡されるアセンブリ名の一部として、公開キーを含めて、<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>属性のコンス トラクターを使用して、`PublicKey`属性。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Reflection.AssemblyName>
- [フレンド アセンブリ](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)


