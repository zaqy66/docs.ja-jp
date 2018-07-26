---
title: 基になる型&lt;typename&gt;の列挙型は CLS 準拠
ms.date: 07/20/2015
f1_keywords:
- vbc40032
- bc40032
helpviewer_keywords:
- BC40032
ms.assetid: 32bf1949-fd73-456c-a323-bf1ffe1320ed
ms.openlocfilehash: 876a59d1441c1ba4c5057556d5ef2fb2ecb43af6
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/10/2018
ms.locfileid: "37959680"
---
# <a name="underlying-type-lttypenamegt-of-enum-is-not-cls-compliant"></a>基になる型&lt;typename&gt;の列挙型は CLS 準拠
この列挙体は、指定されたデータ型の一部、 [Language Independence and Language-independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS)。 これはないため、エラー、コンポーネント内で、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]と Visual Basic は、このデータ型をサポートします。 ただし、厳密に CLS 準拠コードで記述された別のコンポーネントでは、このデータ型がサポートしない可能性があります。 このようなコンポーネントはできないコンポーネントを正常にやり取りすることがあります。  
  
 次の Visual Basic データ型は CLS 準拠ではありません。  
  
-   [SByte データ型](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [UInteger データ型](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [ULong データ型](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [UShort データ型](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 既定では、このメッセージは警告です。 警告を非表示または警告をエラーとして扱う方法の詳細については、次を参照してください。 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)します。  
  
 **エラー ID:** BC40032  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   コンポーネント インターフェイスの他の場合[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]コンポーネント、またはその他のコンポーネントとやり取り、何も変更する必要はありません。  
  
-   書かれていないコンポーネントとやり取りするかどうか、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]のドキュメントのサポートかどうか、このデータ型や、リフレクションを判断できる場合があります。 その場合、何も変更する必要はありません。  
  
-   このデータ型をサポートしていないコンポーネントとやり取りする場合は、最も近い CLS 準拠型で置き換える必要があります。 たとえば、2,147,483,647 を超える値の範囲が不要な場合は、 `UInteger` の代わりに `Integer` を使用できます。 拡張範囲が必要な場合は、 `UInteger` の代わりに `Long`を使用できます。  
  
-   オートメーション オブジェクトや COM オブジェクトとやり取りする場合は、一部の型のデータ幅が [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] とは異なることに注意してください。 たとえば、他の多くの環境では `uint` は 16 ビットです。 このようなコンポーネントに 16 ビットの引数を渡す場合の宣言として`UShort`の代わりに`UInteger`管理対象の Visual Basic コードです。  
  
## <a name="see-also"></a>関連項目  
 [リフレクション (Visual Basic)](../../programming-guide/concepts/reflection.md)  
 [リフレクション](../../../framework/reflection-and-codedom/reflection.md)  
 
