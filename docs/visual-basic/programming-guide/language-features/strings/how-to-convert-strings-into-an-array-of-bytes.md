---
title: '方法: 文字列を Visual Basic でバイト配列に変換します。'
ms.date: 07/20/2015
helpviewer_keywords:
- string conversion [Visual Basic], arrays
- arrays [Visual Basic], converting strings to
- byte arrays
- examples [Visual Basic], string conversion
- arrays [Visual Basic], byte arrays
ms.assetid: f477d35c-a3fc-4a30-b1d4-cd0d353aae1d
ms.openlocfilehash: 83efc9e6b4d4433d5416f2f8b2612c76581586e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648483"
---
# <a name="how-to-convert-strings-into-an-array-of-bytes-in-visual-basic"></a><span data-ttu-id="b4298-102">方法: 文字列を Visual Basic でバイト配列に変換します。</span><span class="sxs-lookup"><span data-stu-id="b4298-102">How to: Convert Strings into an Array of Bytes in Visual Basic</span></span>
<span data-ttu-id="b4298-103">このトピックでは、文字列をバイト配列に変換する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b4298-103">This topic shows how to convert a string into an array of bytes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b4298-104">例</span><span class="sxs-lookup"><span data-stu-id="b4298-104">Example</span></span>  
 <span data-ttu-id="b4298-105">この例では、<xref:System.Text.Encoding.GetBytes%2A>のメソッド、<xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>エンコーディングのバイト配列に文字列に変換するクラス。</span><span class="sxs-lookup"><span data-stu-id="b4298-105">This example uses the <xref:System.Text.Encoding.GetBytes%2A> method of the <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType> encoding class to convert a string into an array of bytes.</span></span>  
  
 [!code-vb[VbVbalrStrings#74](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-strings-into-an-array-of-bytes_1.vb)]  
  
 <span data-ttu-id="b4298-106">バイト配列に文字列に変換するいくつかのエンコード オプションから選択できます。</span><span class="sxs-lookup"><span data-stu-id="b4298-106">You can choose from several encoding options to convert a string into a byte array:</span></span>  
  
-   <span data-ttu-id="b4298-107"><xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>:ASCII (7 ビット) 文字セットのエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-107"><xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>: Gets an encoding for the ASCII (7-bit) character set.</span></span>  
  
-   <span data-ttu-id="b4298-108"><xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=nameWithType>:ビッグ エンディアン バイト順を使用する utf-16 形式のエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-108"><xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-16 format using the big-endian byte order.</span></span>  
  
-   <span data-ttu-id="b4298-109"><xref:System.Text.Encoding.Default%2A?displayProperty=nameWithType>:システムの現在の ANSI コード ページのエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-109"><xref:System.Text.Encoding.Default%2A?displayProperty=nameWithType>: Gets an encoding for the system's current ANSI code page.</span></span>  
  
-   <span data-ttu-id="b4298-110"><xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>:リトル エンディアン バイト順を使用する utf-16 形式のエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-110"><xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-16 format using the little-endian byte order.</span></span>  
  
-   <span data-ttu-id="b4298-111"><xref:System.Text.Encoding.UTF32%2A?displayProperty=nameWithType>:リトル エンディアン バイト順を使用する utf-32 形式のエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-111"><xref:System.Text.Encoding.UTF32%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-32 format using the little-endian byte order.</span></span>  
  
-   <span data-ttu-id="b4298-112"><xref:System.Text.Encoding.UTF7%2A?displayProperty=nameWithType>:UTF-7 形式のエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-112"><xref:System.Text.Encoding.UTF7%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-7 format.</span></span>  
  
-   <span data-ttu-id="b4298-113"><xref:System.Text.Encoding.UTF8%2A?displayProperty=nameWithType>:UTF-8 形式のエンコーディングを取得します。</span><span class="sxs-lookup"><span data-stu-id="b4298-113"><xref:System.Text.Encoding.UTF8%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-8 format.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4298-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4298-114">See also</span></span>
- <xref:System.Text.Encoding?displayProperty=nameWithType>
- <xref:System.Text.Encoding.GetBytes%2A>
- [<span data-ttu-id="b4298-115">方法: Visual Basic で文字列のバイト配列に変換します。</span><span class="sxs-lookup"><span data-stu-id="b4298-115">How to: Convert an Array of Bytes into a String in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-an-array-of-bytes-into-a-string.md)
