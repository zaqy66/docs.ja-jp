---
title: volatile (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
ms.openlocfilehash: be7e081b18702710c00b5b86a9bc152800f0cf3d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526220"
---
# <a name="volatile-c-reference"></a>volatile (C# リファレンス)
`volatile` キーワードは、同時に実行されている複数のスレッドによって、フィールドが変更される可能性があることを示します。 `volatile` と宣言されているフィールドは、シングル スレッドによるアクセスを前提とする、コンパイラの最適化の対象にはなりません。 これらの制限により、すべてのスレッドが、他のスレッドによって実行された volatile の書き込みを、実行された順序で観察することが保証されます。 volatile 書き込みの単一の全体的順序がすべての実行スレッドから認識される保証はありません。  
  
 `volatile` 修飾子は、通常、アクセスをシリアル化する [lock](../../../csharp/language-reference/keywords/lock-statement.md) ステートメントが使用されない場合に、複数のスレッドからアクセスされるフィールドに対して使用します。  
  
 `volatile` キーワードは次の型のフィールドに使用できます。  
  
-   参照型。  
  
-   ポインター型 (unsafe コンテキスト内)。 ポインター自体は volatile にできますが、ポインターが指しているオブジェクトは volatile にできません。 つまり、"volatile を指すポインター" は宣言できません。  
  
-   sbyte、byte、short、ushort、int、uint、char、float、bool などの型。  
  
-   基本データ型 byte、sbyte、short、ushort、int、または uint のいずれかが含まれる列挙型。  
  
-   参照型であることが判明しているジェネリック型パラメーター。  
  
-   <xref:System.IntPtr> および <xref:System.UIntPtr>。  
  
 volatile キーワードは、クラスまたは構造体のフィールドにのみ適用できます。 ローカル変数を `volatile` として宣言することはできません。  
  
## <a name="example"></a>例  
 次の例は、public のフィールド変数を `volatile` として宣言する方法を示しています。  
  
 [!code-csharp[csrefKeywordsModifiers#24](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_1.cs)]  
  
## <a name="example"></a>例  
 次の例は、補助スレッドつまりワーカー スレッドを作成および使用して、プライマリ スレッドとの並行処理を実行する方法を示しています。 マルチスレッドの背景情報については、「[マネージド スレッド処理](../../../standard/threading/index.md)」および「[スレッド処理 (C#)](../../programming-guide/concepts/threading/index.md)」をご覧ください。  
  
 [!code-csharp[csProgGuideThreading#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_2.cs)]  
  
## <a name="c-language-specification"></a>C# 言語仕様  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [C# のキーワード](../../../csharp/language-reference/keywords/index.md)  
- [修飾子](../../../csharp/language-reference/keywords/modifiers.md)
