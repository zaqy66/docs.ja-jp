---
title: '方法: ディクショナリを使用してイベント インスタンスを格納する - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: 8f0284c5637890f35642346880d035619bc0e1e5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560062"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a>方法: ディクショナリを使用してイベント インスタンスを格納する (C# プログラミング ガイド)
多数のイベントを公開する場合に `accessor-declarations` を使用すると、各イベントにフィールドを割り当てる代わりにディクショナリを使用してイベント インスタンスを格納できます。 これが便利なのは、多数のイベントがあるものの、それらのほとんどが実装されそうもない場合だけです。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideEvents#9](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-use-a-dictionary-to-store-event-instances_1.cs)]  
  
## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [イベント](../../../csharp/programming-guide/events/index.md)
- [デリゲート](../../../csharp/programming-guide/delegates/index.md)
