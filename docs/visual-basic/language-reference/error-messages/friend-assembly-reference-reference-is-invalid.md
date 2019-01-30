---
title: フレンド アセンブリ参照 <reference> は無効です
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: ff2cdbebe13f6224209ef8da62600c99348c911b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286820"
---
# <a name="friend-assembly-reference-reference-is-invalid"></a>フレンド アセンブリ参照\<参照 > が無効です
フレンド アセンブリ参照\<参照 > が無効です。 厳密な名前の署名つきアセンブリはその InternalsVisibleTo 宣言内で公開キーを指定しなければなりません。  
  
 渡すアセンブリ名、<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>属性コンス トラクターは、厳密な名前のアセンブリを識別しますは含まれません、`PublicKey`属性。  
  
 **エラー ID:** BC31535  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  厳密な名前のフレンド アセンブリの公開キーを確認します。 渡されるアセンブリ名の一部として、公開キーを含めて、<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>属性のコンス トラクターを使用して、`PublicKey`属性。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Reflection.AssemblyName>
- [フレンド アセンブリ](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)


