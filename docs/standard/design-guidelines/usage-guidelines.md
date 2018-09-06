---
title: 利用ガイドライン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], usage guidelines
ms.assetid: 42215ffa-a099-4a26-b14e-fb2bdb6f95b7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 04e44a6b58fd334b6a23e113922b980f69de627b
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43869867"
---
# <a name="usage-guidelines"></a><span data-ttu-id="a1e4e-102">利用ガイドライン</span><span class="sxs-lookup"><span data-stu-id="a1e4e-102">Usage guidelines</span></span>

<span data-ttu-id="a1e4e-103">このセクションには、パブリックにアクセスできる Api で一般的な種類の使用に関するガイドラインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-103">This section contains guidelines for using common types in publicly accessible APIs.</span></span> <span data-ttu-id="a1e4e-104">組み込みフレームワーク型 (シリアル化属性など) および一般的な演算子のオーバー ロードの直接の使用状況を処理します。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-104">It deals with direct usage of built-in Framework types (e.g., serialization attributes) and overloading common operators.</span></span>
  
<span data-ttu-id="a1e4e-105"><xref:System.IDisposable?displayProperty=nameWithType>インターフェイスは、このセクションでは説明しませんが、については、 [Dispose パターン](../../../docs/standard/design-guidelines/dispose-pattern.md)セクション。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-105">The <xref:System.IDisposable?displayProperty=nameWithType> interface is not covered in this section, but is discussed in the [Dispose Pattern](../../../docs/standard/design-guidelines/dispose-pattern.md) section.</span></span>

> [!NOTE]
> <span data-ttu-id="a1e4e-106">組み込みの .NET Framework 型のガイドラインと他の一般的なに関する詳細についてには、次の参照トピックを参照してください: <xref:System.DateTime?displayProperty=nameWithType>、 <xref:System.DateTimeOffset?displayProperty=nameWithType>、 <xref:System.ICloneable?displayProperty=nameWithType>、 <xref:System.IComparable%601?displayProperty=nameWithType>、 <xref:System.IEquatable%601?displayProperty=nameWithType>、 <xref:System.Nullable%601?displayProperty=nameWithType>、 <xref:System.Object?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-106">For guidelines and additional information about about other common, built-in .NET Framework types, see the reference topics for the following: <xref:System.DateTime?displayProperty=nameWithType>, <xref:System.DateTimeOffset?displayProperty=nameWithType>, <xref:System.ICloneable?displayProperty=nameWithType>, <xref:System.IComparable%601?displayProperty=nameWithType>, <xref:System.IEquatable%601?displayProperty=nameWithType>, <xref:System.Nullable%601?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a1e4e-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="a1e4e-107">In this section</span></span>

[<span data-ttu-id="a1e4e-108">配列</span><span class="sxs-lookup"><span data-stu-id="a1e4e-108">Arrays</span></span>](arrays.md)  
[<span data-ttu-id="a1e4e-109">属性</span><span class="sxs-lookup"><span data-stu-id="a1e4e-109">Attributes</span></span>](attributes.md)  
[<span data-ttu-id="a1e4e-110">コレクション</span><span class="sxs-lookup"><span data-stu-id="a1e4e-110">Collections</span></span>](guidelines-for-collections.md)  
[<span data-ttu-id="a1e4e-111">シリアル化</span><span class="sxs-lookup"><span data-stu-id="a1e4e-111">Serialization</span></span>](serialization.md)  
[<span data-ttu-id="a1e4e-112">System.Xml の使用法</span><span class="sxs-lookup"><span data-stu-id="a1e4e-112">System.Xml Usage</span></span>](system-xml-usage.md)  
[<span data-ttu-id="a1e4e-113">等値演算子</span><span class="sxs-lookup"><span data-stu-id="a1e4e-113">Equality Operators</span></span>](equality-operators.md)  

<span data-ttu-id="a1e4e-114">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="a1e4e-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

<span data-ttu-id="a1e4e-115">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="a1e4e-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1e4e-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1e4e-116">See also</span></span>

- [<span data-ttu-id="a1e4e-117">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="a1e4e-117">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
