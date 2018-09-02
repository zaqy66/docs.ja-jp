---
title: EscapeQuotes が True に設定されている場合、二重引用符は有効な区切り記号でないため、区切り記号で分けられたフィールドを読み取れません
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_IllegalDelimiter
ms.assetid: ab8a0c3a-b89c-4617-9e31-7e81f5dca433
ms.openlocfilehash: faa42c2fec5851857496b321dbdb53c16c43e8c1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43389651"
---
# <a name="unable-to-read-delimited-fields-because-a-double-quote-is-not-a-legal-delimiter-when-escapequotes-is-set-to-true"></a><span data-ttu-id="05efa-102">EscapeQuotes が True に設定されている場合、二重引用符は有効な区切り記号でないため、区切り記号で分けられたフィールドを読み取れません</span><span class="sxs-lookup"><span data-stu-id="05efa-102">Unable to read delimited fields because a double quote is not a legal delimiter when EscapeQuotes is set to True</span></span>
<span data-ttu-id="05efa-103">引用符 (") が区切り文字として指定されており、 `TextFieldParser` が `EscapeQuotes` に設定されているため、 `True`はファイルからの読み取りができません。</span><span class="sxs-lookup"><span data-stu-id="05efa-103">The `TextFieldParser` cannot read from the file because a quotation mark (") has been supplied as the delimiter and `EscapeQuotes` is set to `True`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="05efa-104">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="05efa-104">To correct this error</span></span>  
  
-   <span data-ttu-id="05efa-105">`EscapeQuotes` を `False` に設定します。</span><span class="sxs-lookup"><span data-stu-id="05efa-105">Set `EscapeQuotes` to `False`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05efa-106">関連項目</span><span class="sxs-lookup"><span data-stu-id="05efa-106">See Also</span></span>  
 [<span data-ttu-id="05efa-107">TextFieldParser.SetDelimiters メソッド</span><span class="sxs-lookup"><span data-stu-id="05efa-107">TextFieldParser.SetDelimiters Method</span></span>](https://msdn.microsoft.com/library/21fa40ec-5866-4d0e-9fd9-c708a190dcc9)  
 [<span data-ttu-id="05efa-108">TextFieldParser.Delimiters プロパティ</span><span class="sxs-lookup"><span data-stu-id="05efa-108">TextFieldParser.Delimiters Property</span></span>](https://msdn.microsoft.com/library/4eb18f4d-3011-40a9-b668-be93eed0444f)  
 [<span data-ttu-id="05efa-109">方法: コンマ区切りのテキスト ファイルを読み取る</span><span class="sxs-lookup"><span data-stu-id="05efa-109">How to: Read From Comma-Delimited Text Files</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)  
 [<span data-ttu-id="05efa-110">TextFieldParser オブジェクト</span><span class="sxs-lookup"><span data-stu-id="05efa-110">TextFieldParser Object</span></span>](../../visual-basic/language-reference/objects/textfieldparser-object.md)
