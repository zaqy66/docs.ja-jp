---
title: 型の値&#39; &lt;typename1&gt; &#39;に変換できない&#39; &lt;typename2&gt; &#39; (複数ファイル参照)
ms.date: 07/20/2015
f1_keywords:
- vbc30961
- bc30961
helpviewer_keywords:
- BC30961
ms.assetid: 8be5aa0d-d236-4ac3-aa9c-5044f9f6562b
ms.openlocfilehash: 943b9612a9217b90c19f34285e812c4e1cccf81a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691374"
---
# <a name="value-of-type-39lttypename1gt39-cannot-be-converted-to-39lttypename2gt39-multiple-file-references"></a>型の値&#39; &lt;typename1&gt; &#39;に変換できない&#39; &lt;typename2&gt; &#39; (複数ファイル参照)
型の値 '\<typename1 >' に変換できません。'\<typename2 >'。 型の不一致がへの参照をファイルの混合によって生じた可能性があります '\<filepath1 >' プロジェクトで'\<projectname1 >' への参照をファイルに '\<filepath2 >' プロジェクトで'\<projectname2 >'。 両方のアセンブリが同一である場合は、これらの参照を同じ場所から参照するように置き換えてください。  
  
 プロジェクト アセンブリへの 1 つ以上のファイル参照は、場所の状況で、コンパイラは別に 1 つの型を変換できることを保証することはできません。  
  
 それぞれのファイル参照は、ファイルのパスとプロジェクト (通常は DLL ファイル) の出力ファイルの名前を指定します。 コンパイラは、出力ファイルが、同じソースから取得することや、同じアセンブリの同じバージョンを表すことが保証できません。 そのため、別の参照の型は、同じ型でまたは他にも、あるを変換できることを保証ができません。  
  
 参照されたアセンブリが同じアセンブリ id を持つことがわかっている場合は、1 つのファイルの参照を使用できます。 *アセンブリ ID* には、アセンブリの名前、バージョン、公開キー (存在する場合)、およびカルチャが含まれます。 この情報はアセンブリを一意に識別します。  
  
 **エラー ID:** BC30961  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   参照先アセンブリのアセンブリ id が同じ場合は、削除するか置き換えるファイルの参照のいずれか 1 つのファイル参照のみがあります。  
  
-   参照されたアセンブリは、同じアセンブリ id を持っていない場合、それ以外の型を 1 つの型を変換しませんようにコードを変更します。  
  
## <a name="see-also"></a>関連項目
- [Visual Basic における型変換](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [プロジェクト内の参照の管理](/visualstudio/ide/managing-references-in-a-project)

