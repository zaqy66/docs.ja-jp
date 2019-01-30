---
title: 既定プロパティ '<propertyname1>' は、'<propertyname2>' の既定プロパティ '<classname>' と競合しているため、'Shadows' と宣言できません。
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: bc75b01532ffb112622d7f9bc837490c627883b3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270392"
---
# <a name="default-property-propertyname1-conflicts-with-default-property-propertyname2-in-classname-and-so-should-be-declared-shadows"></a><span data-ttu-id="0d377-102">既定のプロパティ '\<propertyname1 >' 既定のプロパティと競合'\<propertyname2 >' で '\<classname >'、'Shadows' を宣言する必要があります</span><span class="sxs-lookup"><span data-stu-id="0d377-102">Default property '\<propertyname1>' conflicts with default property '\<propertyname2>' in '\<classname>' and so should be declared 'Shadows'</span></span>
<span data-ttu-id="0d377-103">プロパティは、基底クラスで定義されたプロパティと同じ名前で宣言します。</span><span class="sxs-lookup"><span data-stu-id="0d377-103">A property is declared with the same name as a property defined in the base class.</span></span> <span data-ttu-id="0d377-104">このような状況では、このクラスのプロパティは、基底クラスのプロパティをシャドウする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d377-104">In this situation, the property in this class should shadow the base class property.</span></span>  
  
 <span data-ttu-id="0d377-105">このメッセージは警告です。</span><span class="sxs-lookup"><span data-stu-id="0d377-105">This message is a warning.</span></span> <span data-ttu-id="0d377-106">`Shadows` は、既定で指定されていると見なされます。</span><span class="sxs-lookup"><span data-stu-id="0d377-106">`Shadows` is assumed by default.</span></span> <span data-ttu-id="0d377-107">警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0d377-107">For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="0d377-108">**エラー ID:** BC40007</span><span class="sxs-lookup"><span data-stu-id="0d377-108">**Error ID:** BC40007</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0d377-109">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="0d377-109">To correct this error</span></span>  
  
-   <span data-ttu-id="0d377-110">追加、`Shadows`プロパティの名前が宣言されているキーワードを宣言、または変更します。</span><span class="sxs-lookup"><span data-stu-id="0d377-110">Add the `Shadows` keyword to the declaration, or change the name of the property being declared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d377-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d377-111">See also</span></span>
- [<span data-ttu-id="0d377-112">Shadows</span><span class="sxs-lookup"><span data-stu-id="0d377-112">Shadows</span></span>](../../../visual-basic/language-reference/modifiers/shadows.md)
- [<span data-ttu-id="0d377-113">Visual Basic におけるシャドウ</span><span class="sxs-lookup"><span data-stu-id="0d377-113">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
