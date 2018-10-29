---
title: GamePieceCollection クラスの作成
ms.date: 03/30/2017
ms.assetid: e4b037ee-1201-4a55-b198-0d6532ed6f35
ms.openlocfilehash: 0a39ca479e9b370b027fcec4bcf76996e6191296
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50190581"
---
# <a name="creating-the-gamepiececollection-class"></a>GamePieceCollection クラスの作成
**GamePieceCollection** クラスは、汎用の List クラスから派生し、複数の **GamePiece** オブジェクトをより簡単に管理するメソッドを導入します。  
  
## <a name="creating-the-code"></a>コードの作成  
 **GamePieceCollection** クラスのコンストラクターは、プライベート メンバー *capturedIndex* を初期化します。 このフィールドは、現在どのゲーム ピースにマウス キャプチャがあるかを追跡するために使用します。  
  
 [!code-csharp[ManipulationXNA#_GamePieceCollection_PrivateMembersAndConstructor](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/gamepiececollection.cs#_gamepiececollection_privatemembersandconstructor)]  
  
 **ProcessInertia** メソッドと **Draw** メソッドは、コレクションのすべてのゲーム ピースを列挙し、各 **GamePiece** オブジェクトのそれぞれのメソッドで呼び出すことで、ゲームの [Game.Update](https://docs.microsoft.com/previous-versions/windows/xna/bb199616%28v%3dxnagamestudio.41%29) メソッドと [Game.Draw](https://docs.microsoft.com/previous-versions/windows/xna/bb196422%28v%3dxnagamestudio.41%29) メソッドに必要なコードを簡素化します。  
  
 [!code-csharp[ManipulationXNA#_GamePieceCollection_ProcessInertiaAndDraw](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/gamepiececollection.cs#_gamepiececollection_processinertiaanddraw)]  
  
 **UpdateFromMouse** メソッドもゲームの更新中に呼び出されます。 最初に現在のキャプチャ (もしあれば) が有効なままであるかどうかを確認すると、1 つのゲーム ピースのみがマウス キャプチャするようになります。 有効の場合、他のピースはキャプチャの確認ができません。  
  
 キャプチャがあるピースがない場合、**UpdateFromMouse** メソッドが最後から最初へとゲーム ピースを列挙し、対象のピースがマウス キャプチャを報告するかどうかを確認します。 報告する場合、対象のピースは現在キャプチャされているピースになり、後続の処理は実行されません。 **UpdateFromMouse** メソッドは、先にコレクションの最後の項目を確認します。そうすることで、2 つのピースが重なっている場合、Z オーダーが高いピースがキャプチャを取得します。 Z オーダーは明示的ではなく、変更もできません。Z オーダーは、ゲーム ピースがコレクションに追加された順序で管理されます。  
  
 [!code-csharp[ManipulationXNA#_GamePieceCollection_UpdateFromMouse](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/gamepiececollection.cs#_gamepiececollection_updatefrommouse)]  
  
## <a name="see-also"></a>参照  
 [操作と慣性](../../../docs/framework/common-client-technologies/manipulations-and-inertia.md)  
 [XNA アプリケーションでの操作と慣性の使用](../../../docs/framework/common-client-technologies/use-manipulations-and-inertia-in-an-xna-application.md)  
 [GamePiece クラスの作成](../../../docs/framework/common-client-technologies/creating-the-gamepiece-class.md)  
 [Game1 クラスの作成](../../../docs/framework/common-client-technologies/creating-the-game1-class.md)  
 [完全なコードの一覧](../../../docs/framework/common-client-technologies/full-code-listings.md)
