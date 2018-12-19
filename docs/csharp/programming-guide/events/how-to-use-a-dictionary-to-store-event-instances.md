---
title: '方法: ディクショナリを使用してイベント インスタンスを格納する - C# プログラミング ガイド'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: 819c81aed3a6f09a20e51285058dcc77749dd33a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245143"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a>方法: ディクショナリを使用してイベント インスタンスを格納する (C# プログラミング ガイド)
多数のイベントを公開する場合に `accessor-declarations` を使用すると、各イベントにフィールドを割り当てる代わりにディクショナリを使用してイベント インスタンスを格納できます。 これが便利なのは、多数のイベントがあるものの、それらのほとんどが実装されそうもない場合だけです。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuideEvents#9](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-use-a-dictionary-to-store-event-instances_1.cs)]  
  
## <a name="see-also"></a>参照

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [イベント](../../../csharp/programming-guide/events/index.md)  
- [デリゲート](../../../csharp/programming-guide/delegates/index.md)
