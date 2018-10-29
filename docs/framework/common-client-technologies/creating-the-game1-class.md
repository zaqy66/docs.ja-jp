---
title: Game1 クラスの作成
ms.date: 03/30/2017
ms.assetid: 47932ce3-2ba5-476f-a26b-3ddfd5226f27
ms.openlocfilehash: c96fa846d11947af03faec26dd6de99e0aeec052
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452798"
---
# <a name="creating-the-game1-class"></a>Game1 クラスの作成
すべての Microsoft XNA プロジェクトと同様、Game1 クラスは [Microsoft.Xna.Framework.Game](https://docs.microsoft.com/previous-versions/windows/xna/bb197040%28v%3dxnagamestudio.41%29) クラスから派生しています。このクラスでは、XNA ゲーム用に、基本的なグラフィックス デバイスの初期化、ゲーム ロジックの提供、およびコードのレンダリングを行います。 ほとんどの作業は GamePiece クラスと GamePieceCollection クラスで実行されるため、Game1 クラスは非常に簡潔になっています。  
  
## <a name="creating-the-code"></a>コードの作成  
 クラスのプライベート メンバーはゲーム ピースを格納する **GamePieceCollection** オブジェクト、[GraphicsDeviceManager](https://docs.microsoft.com/previous-versions/windows/xna/bb197317%28v%3dxnagamestudio.41%29) オブジェクト、ゲーム ピースのレンダリングに使用される [SpriteBatch](https://docs.microsoft.com/previous-versions/windows/xna/bb199034%28v%3dxnagamestudio.41%29) オブジェクトで構成されます。  
  
 [!code-csharp[ManipulationXNA#_Game1_PrivateMembers](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_privatemembers)]  
  
 ゲームの初期化中にこれらのオブジェクトはインスタンス化されます。  
  
 [!code-csharp[ManipulationXNA#_Game1_ConstructorInitialize](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_constructorinitialize)]  
  
 [LoadContent](https://docs.microsoft.com/previous-versions/windows/xna/bb975766%28v%3dxnagamestudio.41%29) メソッドが呼び出されると、ゲーム ピースが作成され、**GamePieceCollection** オブジェクトに割り当てられます。 ゲーム ピースには、次の 2 種類があります。 ピースのスケール ファクターは、小さいピースや大きいピースが存在するようにわずかに変更されます。  
  
 [!code-csharp[ManipulationXNA#_Game1_LoadContent](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_loadcontent)]  
  
 [Update](https://docs.microsoft.com/previous-versions/windows/xna/bb199616%28v%3dxnagamestudio.41%29) メソッドは、ゲームの実行中に XNA フレームワークによって繰り返し呼び出されます。 [Update](https://docs.microsoft.com/previous-versions/windows/xna/bb199616%28v%3dxnagamestudio.41%29) メソッドは、ゲーム ピースのコレクションで **ProcessInertia** メソッドと **UpdateFromMouse** メソッドを呼び出します。 これらのメソッドの説明は、「[GamePieceCollection クラスの作成](../../../docs/framework/common-client-technologies/creating-the-gamepiececollection-class.md)」にあります。  
  
 [!code-csharp[ManipulationXNA#_Game1_UpdateGame](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_updategame)]  
  
 [Draw](https://docs.microsoft.com/previous-versions/windows/xna/bb196422%28v%3dxnagamestudio.41%29) メソッドも、ゲームの実行中に XNA フレームワークによって繰り返し呼び出されます。 [Draw](https://docs.microsoft.com/previous-versions/windows/xna/bb196422%28v%3dxnagamestudio.41%29) メソッドは、**GamePieceCollection** オブジェクトの **Draw** メソッドを呼び出すことで、ゲーム ピースのレンダリングを実行します。 これらのメソッドの説明は、「[GamePieceCollection クラスの作成](../../../docs/framework/common-client-technologies/creating-the-gamepiececollection-class.md)」にあります。  
  
 [!code-csharp[ManipulationXNA#_Game1_DrawGame](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_drawgame)]  
  
## <a name="see-also"></a>参照  
 [操作と慣性](../../../docs/framework/common-client-technologies/manipulations-and-inertia.md)  
 [XNA アプリケーションでの操作と慣性の使用](../../../docs/framework/common-client-technologies/use-manipulations-and-inertia-in-an-xna-application.md)  
 [GamePiece クラスの作成](../../../docs/framework/common-client-technologies/creating-the-gamepiece-class.md)  
 [GamePieceCollection クラスの作成](../../../docs/framework/common-client-technologies/creating-the-gamepiececollection-class.md)  
 [完全なコードの一覧](../../../docs/framework/common-client-technologies/full-code-listings.md)
