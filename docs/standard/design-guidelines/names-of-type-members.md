---
title: 型のメンバーの名前
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- events [.NET Framework], names
- methods [.NET Framework], names
- type members
- properties [.NET Framework], names
- fields, names
- field names
- names [.NET Framework], type members
- members [.NET Framework], type
ms.assetid: af5a0903-36af-4c2a-b848-cf959affeaa5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 25fe93b63c518f54ee72300f26dfcb3f3ad21d76
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2018
ms.locfileid: "33575350"
---
# <a name="names-of-type-members"></a>型のメンバーの名前
メンバーの種類がされています: メソッド、プロパティ、イベント、コンス トラクター、およびフィールドです。 次のセクションでは、型のメンバーの名前付けのガイドラインについて説明します。  
  
## <a name="names-of-methods"></a>メソッドの名前  
 メソッドは操作を実行する手段であるため、デザインのガイドラインは、動詞または動詞句メソッド名にすることが必要です。 このガイドラインにも従うプロパティと型名を名詞または形容詞句からメソッド名を区別するために機能します。  
  
 **✓ 推奨** 動詞または動詞句を使ってメソッドを命名しましょう。
  
```  
public class String {  
    public int CompareTo(...);  
    public string[] Split(...);  
    public string Trim();  
}  
```  
  
## <a name="names-of-properties"></a>プロパティの名前  
 他のメンバーとは異なり名詞句または形容詞名に、プロパティを指定する必要があります。 プロパティが、データを参照し、プロパティの名前を反映するためです。 プロパティ名は、pascal 表記を使用が常に使用されます。  
  
 **✓ 推奨** 名詞、名詞句、または形容詞を使ってプロパティを命名しましょう。
  
 **X 非推奨** 次の例のように、"Get"メソッド名と一致するプロパティを持たないようにしましょう。 
  
 `public string TextWriter { get {...} set {...} }`  
 `public string GetTextWriter(int value) { ... }`  
  
 この場合、一般的には、このプロパティはメソッドとして宣言すべきでしょう。  
  
 **✓ 推奨** "List"または"Collection"など単数形の語句を接尾辞として使う代わりに、コレクションの内容を示す単語の複数形でプロパティを命名しましょう。  
  
 **✓ 推奨** bool型のプロパティは肯定的な語句で命名しましょう (`CantSeek`ではなく`CanSeek`)。 必要な場合だけ、bool型のプロパティに"Is," "Can," or "Has,"を追加するようにしましょう。  
  
 **✓ 要検討** プロパティを、その型名と同じに命名することも検討しましょう。  
  
 例えば、次のプロパティはenum型の`Color`の値を読み書きするので、プロパティも`Color`と命名しています:  
  
```  
public enum Color {...}  
public class Control {  
    public Color Color { get {...} set {...} }  
}  
```  
  
## <a name="names-of-events"></a>イベントの名前  
 イベントは、常に、何らかのアクションでは、いずれかの問題であるかが発生した 1 つを参照してください。 そのため、メソッド、イベント名前付けには、動詞と同様動詞の時制を使用するイベントが発生した時刻を指定します。  
  
 **✓ 推奨** イベントは動詞または動詞句で命名しましょう。  
  
 例えば、 `Clicked`、 `Painting`、`DroppedDown`のようにします。  
  
 **✓ 推奨** イベントの発生前後が分かるように、現在および過去の時制を使って命名しましょう。  
  
 例えば、クローズイベントで、ウィンドウが閉じられる前に呼び出されるイベントを`Closing`、ウィンドウが閉じられた後に発生するイベントを`Closed`と命名すると良いでしょう。  
  
 **X 非推奨** イベントの発生前後を"Before"または"After"の接頭辞や接尾辞で表すのは避けましょう。現在および過去の時制を使って命名しましょう。   
  
 **✓ 推奨** 次の例のように、イベントハンドラー (イベントの種類を表すデリゲート) は`EventHandler`接尾辞を付けて命名しましょう。 
  
 `public delegate void ClickedEventHandler(object sender, ClickedEventArgs e);`  
  
 **✓ 推奨** イベントハンドラーの2つの引数は`sender`と`e`と命名しましょう。  
  
 `sender`パラメーターは、イベントを発生させたオブジェクトを表します。 `sender`パラメーターは、具体的な型を採用することが可能な場合でも通常`object`型で宣言します。  
  
 **✓ 推奨** イベントハンドラーの2つ目の引数のクラスは"EventArgs"接尾辞を付けて命名しましょう。  
  
## <a name="names-of-fields"></a>フィールドの名前  
 このフィールドの命名ガイドラインは、publicおよびprotectedのstaticフィールドに適用します。 internalおよびprivateフィールドは、ガイドラインの対象外で、publicまたはprotectedのインスタンスフィールドは[メンバー デザインのガイドライン](../../../docs/standard/design-guidelines/member.md)によって許可されていません。  
  
 **✓ 推奨** フィールドは pascal 表記を使って命名しましょう。  
  
 **✓ 推奨** 名詞、名詞句、または形容詞を使用してフィールドを命名しましょう。  
  
 **X 非推奨** 次の例のように、フィールド名に接頭辞を付けないようにしましょう。  
  
 例えば、"g_" や "s_" といった接頭辞をstaticフィールドである事を示すために使わないようにしましょう。
  
 *部分 © 2005、2009 Microsoft Corporation します。All rights reserved.*  
  
 *ピアソン教育, Inc. からのアクセス許可によって検出[Framework デザイン ガイドライン: 規則、表現方法、および再利用可能な .NET ライブラリを第 2 版パターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)は Cwalina と Brad Abrams、2008 年 10 月 22 日で発行されました。Microsoft Windows 開発シリーズの一部として、Addison-wesley Professional。*  
  
## <a name="see-also"></a>関連項目  
 [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
 [名前付けのガイドライン](../../../docs/standard/design-guidelines/naming-guidelines.md)
