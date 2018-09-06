---
title: Visual Basic における型変換
ms.date: 07/20/2015
helpviewer_keywords:
- conversions [Visual Basic], type
- data types [Visual Basic], changing
- variables [Visual Basic], changing data type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- changing data types [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 1cdacd21-ba31-4b62-b5be-395e41eeaa17
ms.openlocfilehash: 026b2a250abfac0782feb0946bc50a94f504f7ed
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "44037004"
---
# <a name="type-conversions-in-visual-basic"></a><span data-ttu-id="bf4e0-102">Visual Basic における型変換</span><span class="sxs-lookup"><span data-stu-id="bf4e0-102">Type Conversions in Visual Basic</span></span>
<span data-ttu-id="bf4e0-103">1 つのデータ型から別の型に値を変更するプロセスと呼ばれます*変換*します。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-103">The process of changing a value from one data type to another type is called *conversion*.</span></span> <span data-ttu-id="bf4e0-104">変換は、いずれかの*拡大*または*縮小*、関与する型のデータ容量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-104">Conversions are either *widening* or *narrowing*, depending on the data capacities of the types involved.</span></span> <span data-ttu-id="bf4e0-105">*暗黙的な*または*明示的な*、ソース コード内の構文によって異なります。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-105">They are also *implicit* or *explicit*, depending on the syntax in the source code.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="bf4e0-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="bf4e0-106">In This Section</span></span>  
 [<span data-ttu-id="bf4e0-107">拡大変換と縮小変換</span><span class="sxs-lookup"><span data-stu-id="bf4e0-107">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)  
 <span data-ttu-id="bf4e0-108">変換先の型がデータを保持するかどうかによって分類される変換について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-108">Explains conversions classified by whether the destination type can hold the data.</span></span>  
  
 [<span data-ttu-id="bf4e0-109">暗黙の型変換と明示的な型変換</span><span class="sxs-lookup"><span data-stu-id="bf4e0-109">Implicit and Explicit Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)  
 <span data-ttu-id="bf4e0-110">かどうか Visual Basic でに実行によって自動的に分類される変換をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-110">Discusses conversions classified by whether Visual Basic performs them automatically.</span></span>  
  
 [<span data-ttu-id="bf4e0-111">文字列とその他の型との変換</span><span class="sxs-lookup"><span data-stu-id="bf4e0-111">Conversions Between Strings and Other Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/conversions-between-strings-and-other-types.md)  
 <span data-ttu-id="bf4e0-112">文字列と数値、間の変換を示しています。 `Boolean`、または日付/時刻値。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-112">Illustrates converting between strings and numeric, `Boolean`, or date/time values.</span></span>  
  
 [<span data-ttu-id="bf4e0-113">方法: オブジェクトを Visual Basic で別の型に変換</span><span class="sxs-lookup"><span data-stu-id="bf4e0-113">How to: Convert an Object to Another Type in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-convert-an-object-to-another-type.md)  
 <span data-ttu-id="bf4e0-114">変換する方法を示しています、`Object`変数を他のデータ型にします。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-114">Shows how to convert an `Object` variable to any other data type.</span></span>  
  
 [<span data-ttu-id="bf4e0-115">配列変換</span><span class="sxs-lookup"><span data-stu-id="bf4e0-115">Array Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md)  
 <span data-ttu-id="bf4e0-116">手順について説明するさまざまなデータ型の配列間で変換するプロセス。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-116">Steps you through the process of converting between arrays of different data types.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="bf4e0-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf4e0-117">Related Sections</span></span>  
 [<span data-ttu-id="bf4e0-118">データの種類</span><span class="sxs-lookup"><span data-stu-id="bf4e0-118">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)  
 <span data-ttu-id="bf4e0-119">Visual Basic のデータ型を紹介し、それらを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-119">Introduces the Visual Basic data types and describes how to use them.</span></span>  
  
 [<span data-ttu-id="bf4e0-120">データの種類</span><span class="sxs-lookup"><span data-stu-id="bf4e0-120">Data Types</span></span>](../../../../visual-basic/language-reference/data-types/index.md)  
 <span data-ttu-id="bf4e0-121">Visual Basic によって提供される基本データ型を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-121">Lists the elementary data types supplied by Visual Basic.</span></span>  
  
 [<span data-ttu-id="bf4e0-122">トラブルシューティング (データ型)</span><span class="sxs-lookup"><span data-stu-id="bf4e0-122">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 <span data-ttu-id="bf4e0-123">データ型を使用する場合に生じる可能性のある一般的な問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf4e0-123">Discusses some common problems that can arise when working with data types.</span></span>
