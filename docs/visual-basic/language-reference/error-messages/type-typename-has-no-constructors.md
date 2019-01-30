---
title: 型 '<typename>' にはコンストラクターがありません。
ms.date: 07/20/2015
f1_keywords:
- bc30251
- vbc30251
helpviewer_keywords:
- BC30251
ms.assetid: aff3e1df-abe6-4bc0-9abc-a1e70514c561
ms.openlocfilehash: 6a12bc35aeaa6e9e21835ce0a091ee89ea4c326d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260369"
---
# <a name="type-typename-has-no-constructors"></a>型 '\<typename >' のコンス トラクターがありません
型が `Sub New()` の呼び出しをサポートしません。 コンパイラまたはバイナリ ファイルが破損していることが原因の 1 つとして考えられます。  
  
 **エラー ID:** BC30251  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  型が別のプロジェクトまたは参照ファイル内にある場合は、プロジェクトまたはファイルを再インストールします。  
  
2.  型が同じプロジェクト内にある場合は、型を含むアセンブリを再コンパイルします。  
  
3.  エラーが再発する場合は、Visual Basic コンパイラを再インストールします。  
  
4.  エラーが続く場合は、状況に関する情報を収集し、マイクロソフト プロダクト サポート サービスに通知してください。  
  
## <a name="see-also"></a>関連項目
- [クラスとオブジェクト](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [ご意見](/visualstudio/ide/talk-to-us)
