---
title: この最初のステートメント&#39;Sub New&#39;への呼び出しである必要があります&#39;MyBase.New&#39;または&#39;に対して&#39;(アクセス可能なコンス トラクター パラメーターのないありません)
ms.date: 07/20/2015
f1_keywords:
- bc30148
- vbc30148
helpviewer_keywords:
- BC30148
ms.assetid: 4426e8fc-cb39-4eb8-ba95-503cd32fcc89
ms.openlocfilehash: 75832ae88908094c1cb74ce04ad84c0d2ae91e68
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728896"
---
# <a name="first-statement-of-this-39sub-new39-must-be-a-call-to-39mybasenew39-or-39myclassnew39-no-accessible-constructor-without-parameters"></a>この最初のステートメント&#39;Sub New&#39;への呼び出しである必要があります&#39;MyBase.New&#39;または&#39;に対して&#39;(アクセス可能なコンス トラクター パラメーターのないありません)
この 'Sub New' の最初のステートメントは 'mybase.new' または 'myclass.new' への呼び出しをする必要がありますので、基本クラスの\<basename >' の'\<derivedname >' 引数なしで呼び出せるアクセス可能な ' Sub New' はありません。  
  
 派生クラスでは、すべてのコンス トラクターが基底クラスのコンス トラクターを呼び出す必要があります (`MyBase.New`)。 基底クラスが派生クラスでアクセス可能なパラメーターなしのコンス トラクターを持つ場合`MyBase.New`自動的に呼び出すことができます。 できない場合は、パラメーターを持つ基底クラスのコンス トラクターを呼び出す必要があり、自動的に実行できません。 この場合、すべての派生クラス コンス トラクターの最初のステートメントは、基本クラスをパラメーター化されたコンス トラクターを呼び出すか、呼び出す基底クラスのコンス トラクターを派生クラスで別のコンス トラクターを呼び出す必要があります。  
  
 **エラー ID:** BC30148  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   いずれかの呼び出し`MyBase.New`、必要なパラメーターを指定するか、ピア コンス トラクターが、このような呼び出しを行います。  
  
     たとえば、基底クラスとして宣言されているコンス トラクターがある`Public Sub New(ByVal index as Integer)`、最初のステートメントで、派生クラスのコンス トラクターがあります`MyBase.New(100)`します。  
  
## <a name="see-also"></a>関連項目
- [継承の基本](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
