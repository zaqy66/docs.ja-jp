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
型は、メソッド、プロパティ、イベント、コンストラクタ、フィールド といったメンバーで構成されます。以下のセクションでは、メンバーの命名ガイドラインについて説明します。
  
## <a name="names-of-methods"></a>メソッドの名前  
 メソッドは操作を実行する手段であるため、このガイドラインでは、メソッドは動詞または動詞句で命名することを規定します。このガイドラインに従うと、メソッド名を名詞や形容詞で命名されるプロパティや型と区別することもできます。
  
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
  
 **✓ 推奨** 肯定の語句でブール型プロパティの名前 (`CantSeek`の代わりに`CanSeek`)。 必要に応じて、ブールプロパティの先頭に "Is"、 "Can"、または "Has"を追加することもできますが、値を追加する場合に限定します。 
  
 **✓ 要検討** プロパティを、その型名と同じに命名することも検討しましょう。  
  
 例えば、次のプロパティはenum型の`Color`の値を読み書きするので、プロパティも`Color`と命名しています:  
  
```  
public enum Color {...}  
public class Control {  
    public Color Color { get {...} set {...} }  
}  
```  
  
## <a name="names-of-events"></a>イベントの名前  
 イベントは常に、これから発生する、または発生済みの、何らかのアクションを参照します。 したがって、メソッドの場合と同様に、イベントには動詞が付けられ、動詞の時制はイベントが発生したタイミングを表すために使われます。  
  
 **✓ 推奨** イベントは動詞または動詞句で命名しましょう。  
  
 例えば、 `Clicked`、 `Painting`、`DroppedDown`のようにします。  
  
 **✓ 推奨** 現在および過去時制を使用して、前後の概念でイベント名を提供します。  
  
 例えば、クローズイベントで、ウィンドウが閉じられる前に呼び出されるイベントを`Closing`、ウィンドウが閉じられた後に発生するイベントを`Closed`と命名すると良いでしょう。  
  
 **X 非推奨** プレイベントとポストイベントを示す "Before" または "After"を接頭や接尾に使用しないでください。 前述の通り、現在と過去の時制を使用します。
  
 **✓ 推奨** 次の例に示すように"EventHandler"サフィックスを持つイベント ハンドラー (デリゲートがイベントの種類として使用) の名前をつけます。 
  
 `public delegate void ClickedEventHandler(object sender, ClickedEventArgs e);`  
  
 **✓ 推奨** イベント ハンドラーにおいては`sender`と`e`という 2 つのパラメーターを使用します。 
  
 `sender`パラメーターは、イベントを発生させたオブジェクトを表します。 `sender`パラメーターは、具体的な型を採用することが可能な場合でも通常`object`型で宣言します。  
  
 **✓ 推奨** イベントハンドラーの2つ目の引数のクラスは"EventArgs"接尾辞を付けて命名しましょう。  
  
## <a name="names-of-fields"></a>フィールドの名前  
 このフィールド命名ガイドラインは、publicおよびprotectedのstaticフィールドに適用します。 internalおよびprivateフィールドは、ガイドラインの対象外で、publicまたはprotectedのインスタンスフィールドは[メンバー デザインのガイドライン](../../../docs/standard/design-guidelines/member.md)によって許可されていません。  
  
 **✓ 推奨** フィールドの名前に PascalCasing を使用します。   
  
 **✓ 推奨** 名詞、名詞句、または形容詞を使用してフィールドを命名しましょう。  
  
 **X 非推奨** 次の例のように、フィールド名に接頭辞を付けないようにしましょう。  
  
 例えば、"g_" や "s_" といった接頭辞をstaticフィールドである事を示すために使わないようにしましょう。
  
 *部分 © 2005、2009 Microsoft Corporation します。All rights reserved.*  
  
 *ピアソン教育, Inc. からのアクセス許可によって検出[Framework デザイン ガイドライン: 規則、表現方法、および再利用可能な .NET ライブラリを第 2 版パターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)は Cwalina と Brad Abrams、2008 年 10 月 22 日で発行されました。Microsoft Windows 開発シリーズの一部として、Addison-wesley Professional。*  
  
## <a name="see-also"></a>関連項目  
 [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
 [名前付けのガイドライン](../../../docs/standard/design-guidelines/naming-guidelines.md)
