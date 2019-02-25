---
title: オブジェクト指向プログラミング (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 49794de4-64c3-473c-b8ed-fe98835df69c
ms.openlocfilehash: 058d8b932e50f784d4a5cefa9fadfb31953687f0
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153927"
---
# <a name="object-oriented-programming-visual-basic"></a>オブジェクト指向プログラミング (Visual Basic)

Visual Basic は、カプセル化、継承、ポリモーフィズムなどを完全にサポートしたオブジェクト指向プログラミングを提供します。

 "*カプセル化*" とは、関連するプロパティ、メソッド、およびその他のメンバーのグループが 1 つの単位またはオブジェクトとして扱われることを意味します。

 "*継承*" は、既存のクラスに基づいて新しいクラスを作成する機能です。

 "*ポリモーフィズム*" とは、同じプロパティまたはメソッドを異なる方法で実装している複数のクラスを、交換して使用できることです。

 このセクションでは、次の概念について説明します。

- [クラスとオブジェクト](#classes-and-objects)
  - [クラス メンバー](#class-members)
    - [プロパティとフィールド](#properties-and-fields)
    - [メソッド](#methods)
    - [コンストラクター](#constructors)
    - [デストラクター](#destructors)
    - [イベント](#events)
    - [入れ子になったクラス](#nested-classes)
  - [アクセス修飾子とアクセス レベル](#access-modifiers-and-access-levels)
    - [クラスをインスタンス化します。](#instantiating-classes)
    - [共有クラスとメンバー](#shared-classes-and-members)
    - [匿名型](#anonymous-types)
- [継承](#inheritance)
  - [メンバーをオーバーライドします。](#overriding-members)
- [インターフェイス](#interfaces)
- [ジェネリック](#generics)
- [デリゲート](#delegates)

## <a name="classes-and-objects"></a>クラスとオブジェクト

"*クラス*" という用語と "*オブジェクト*" という用語は同じ意味で使われる場合がありますが、実際には、クラスはオブジェクトの "*型*" を表すのに対し、オブジェクトはクラスの使用可能な "*インスタンス*" です。 そのため、オブジェクトを作成する操作は "*インスタンス化*" と呼ばれます。 設計図との対比を使って説明すると、クラスは設計図であり、オブジェクトはその設計図を基にした建築物です。

クラスを定義するコード例を次に示します。

```vb
Class SampleClass
End Class
```

Visual Basic は、クラスと呼ばれる軽量バージョンも用意されています。*構造*オブジェクトの大きな配列を作成し、実行する必要がある場合に便利なが過度のメモリを使用しません。

構造体を定義するコード例を次に示します。

```vb
Structure SampleStructure
End Structure
```

詳細については次を参照してください:

- [Class ステートメント](../../../visual-basic/language-reference/statements/class-statement.md)
- [Structure ステートメント](../../../visual-basic/language-reference/statements/structure-statement.md)

### <a name="class-members"></a>クラス メンバー

各クラスには、さまざまな "*クラス メンバー*" を含めることができます。クラス メンバーには、クラスのデータを記述するプロパティ、クラスの動作を定義するメソッド、異なるクラスやオブジェクト間で通信するためのイベントが含まれます。

#### <a name="properties-and-fields"></a>プロパティとフィールド

フィールドとプロパティは、オブジェクトに格納されている情報を表します。 フィールドは、直接読み取ったり設定したりできるので変数と似ています。

フィールドを定義するコード例を次に示します。

```vb
Class SampleClass
    Public SampleField As String
End Class
```

プロパティには get プロシージャと set プロシージャがあり、これらを使用することで値の設定方法や戻り値をより細かく制御できます。

Visual Basic ではプロパティ値を格納するプライベート フィールドを作成するか、背後で自動的に作成され、プロパティ プロシージャの基本的なロジックを提供するいわゆる自動実装プロパティを使用することができます。

自動実装プロパティを定義するコード例を次に示します。

```vb
Class SampleClass
    Public Property SampleProperty as String
End Class
```

プロパティ値の読み取りと書き込みのために追加の操作を実行する必要がある場合は、プロパティ値を格納するフィールドを定義し、値を格納および取得する基本的なロジックを実装します。

```vb
Class SampleClass
    Private m_Sample As String
    Public Property Sample() As String
        Get
            ' Return the value stored in the field.
            Return m_Sample
        End Get
        Set(ByVal Value As String)
            ' Store the value in the field.
            m_Sample = Value
        End Set
    End Property
End Class
```

ほとんどのプロパティには、プロパティ値の設定と取得を行うための両方のメソッドまたはプロシージャがあります。 ただし、読み取り専用または書き込み専用のプロパティを作成して、プロパティの変更や読み取りを制限することもできます。 そのためには、Visual Basic では `ReadOnly` キーワードと `WriteOnly` キーワードを使用します。 ただし、自動実装プロパティを読み取り専用または書き込み専用にすることはできません。

詳細については次を参照してください:

- [Property ステートメント](../../../visual-basic/language-reference/statements/property-statement.md)
- [Get ステートメント](../../../visual-basic/language-reference/statements/get-statement.md)
- [Set ステートメント](../../../visual-basic/language-reference/statements/set-statement.md)
- [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)
- [WriteOnly](../../../visual-basic/language-reference/modifiers/writeonly.md)

#### <a name="methods"></a>メソッド

 "*メソッド*" は、オブジェクトが実行できる処理です。

> [!NOTE]
> Visual Basic には、メソッドを作成する方法が 2 つあります。メソッドが値を返さない場合は `Sub` ステートメントを使用し、メソッドが値を返す場合は `Function` ステートメントを使用します。

クラスのメソッドを定義するコード例を次に示します。

```vb
Class SampleClass
    Public Function SampleFunc(ByVal SampleParam As String)
        ' Add code here
    End Function
End Class
```

クラスには、同じメソッドに対して、パラメーターの数やパラメーターの型が異なる複数の実装 ("*オーバーロード*") を含めることができます。

メソッドをオーバーロードするコード例を次に示します。

```vb
Overloads Sub Display(ByVal theChar As Char)
    ' Add code that displays Char data.
End Sub
Overloads Sub Display(ByVal theInteger As Integer)
    ' Add code that displays Integer data.
End Sub
```

ほとんどの場合、メソッドはクラス定義内で宣言します。 ただし、Visual Basic もサポートしています*拡張メソッド*クラスの実際の定義の外側の既存のクラスにメソッドを追加することができます。

詳細については次を参照してください:

- [Function ステートメント](../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub ステートメント](../../../visual-basic/language-reference/statements/sub-statement.md)
- [オーバーロード](../../../visual-basic/language-reference/modifiers/overloads.md)
- [拡張メソッド](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)

#### <a name="constructors"></a>コンストラクター

コンストラクターは、特定の型のオブジェクトを作成するときに自動的に実行されるクラス メソッドです。 コンストラクターは、通常、新しいオブジェクトのデータ メンバーを初期化します。 コンストラクターは、クラスの作成時に 1 回だけ実行できます。 また、コンストラクター内のコードは常に、クラス内の他のすべてのコードより先に実行されます。 他のメソッドと同じように、コンストラクターにも複数のオーバーロードを作成できます。

クラスのコンストラクターを定義するコード例を次に示します。

```vb
Class SampleClass
    Sub New(ByVal s As String)
        // Add code here.
    End Sub
End Class
```

詳細については次を参照してください:[オブジェクトの有効期間:オブジェクトの作成し、破棄方法](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)します。

#### <a name="destructors"></a>デストラクター

デストラクターは、クラスのインスタンスを消滅させるために使用します。 .NET Framework では、アプリケーション内のマネージド オブジェクトのメモリの割り当てと解放は、ガベージ コレクターによって自動的に管理されます。 ただし、アプリケーションで作成されるアンマネージ リソースを適切にクリーンアップするために、デストラクターも必要になることがあります。 1 つのクラスに定義できるデストラクターは 1 つだけです。

.NET Framework のデストラクターおよびガベージ コレクションの詳細については、「[ガベージ コレクション](../../../standard/garbage-collection/index.md)」をご覧ください。

#### <a name="events"></a>イベント

クラスやオブジェクトは、何か重要なことが起こった場合に、イベントを使用して他のクラスまたはオブジェクトに通知を送ります。 イベントを送信する (発生させる) クラスは "*パブリッシャー*" と呼ばれ、イベントを受信する (処理する) クラスは "*サブスクライバー*" と呼ばれます。 イベント、およびイベントの発生と処理の詳細については、「[イベント](../../../standard/events/index.md)」をご覧ください。

- イベントを宣言するには、使用、 [Event ステートメント](../../../visual-basic/language-reference/statements/event-statement.md)します。

- イベントを発生させるには、使用、 [RaiseEvent ステートメント](../../../visual-basic/language-reference/statements/raiseevent-statement.md)します。

- 宣言型の方法を使用してイベント ハンドラーを指定するには、使用、 [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)ステートメントおよび[処理](../../../visual-basic/language-reference/statements/handles-clause.md)句。

- 動的に追加、削除、およびイベントに関連付けられているイベント ハンドラーを変更するのには、使用、 [AddHandler ステートメント](../../../visual-basic/language-reference/statements/addhandler-statement.md)と[RemoveHandler ステートメント](../../../visual-basic/language-reference/statements/removehandler-statement.md)と共に、 [AddressOf演算子](../../../visual-basic/language-reference/operators/addressof-operator.md)します。

#### <a name="nested-classes"></a>入れ子になったクラス

別のクラス内で定義されているクラスを "*入れ子になったクラス*" と呼びます。 既定では、入れ子になったクラスはプライベートです。

```vb
Class Container
    Class Nested
    ' Add code here.
    End Class
End Class
```

入れ子になったクラスのインスタンスを作成するには、コンテナー クラスの名前に続けて、ドットと入れ子になったクラスの名前を指定します。

```vb
Dim nestedInstance As Container.Nested = New Container.Nested()
```

### <a name="access-modifiers-and-access-levels"></a>アクセス修飾子とアクセス レベル

すべてのクラスおよびクラス メンバーでは、"*アクセス修飾子*" を使って、他のクラスに提供するアクセス レベルを指定できます。

次のアクセス修飾子を使用できます。

|Visual Basic の修飾子|定義|
|---------------------------|----------------|
|[Public](../../../visual-basic/language-reference/modifiers/public.md)|この型またはメンバーには、同じアセンブリ内の他のコードや、そのアセンブリを参照する別のアセンブリ内の任意のコードからアクセスできます。|
|[Private](../../../visual-basic/language-reference/modifiers/private.md)|この型またはメンバーには、同じクラスのコードのみがアクセスできます。|
|[Protected](../../../visual-basic/language-reference/modifiers/protected.md)|この型またはメンバーには、同じクラスまたは派生クラスのコードのみがアクセスできます。|
|[Friend](../../../visual-basic/language-reference/modifiers/friend.md)|この型またはメンバーには、同じアセンブリ内の任意のコードからアクセスできますが、別のアセンブリからはアクセスできません。|
|`Protected Friend`|この型またはメンバーには、同じアセンブリ内の任意のコード、または別のアセンブリ内の任意の派生クラスからアクセスできます。|

詳細については、次を参照してください。[アクセス レベルを Visual Basic で](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)します。

### <a name="instantiating-classes"></a>クラスをインスタンス化します。

オブジェクトを作成するには、クラスをインスタンス化する (クラスのインスタンスを作成する) 必要があります。

```vb
Dim sampleObject as New SampleClass()
```

クラスをインスタンス化した後は、インスタンスのプロパティやフィールドに値を割り当てたり、クラスのメソッドを呼び出したりできます。

```vb
' Set a property value.
sampleObject.SampleProperty = "Sample String"
' Call a method.
sampleObject.SampleMethod()
```

クラスのインスタンス化のプロセスでプロパティに値を割り当てるには、オブジェクト初期化子を使用します。

```vb
Dim sampleObject = New SampleClass With
    {.FirstProperty = "A", .SecondProperty = "B"}
```

詳細については次を参照してください:

- [New 演算子](../../../visual-basic/language-reference/operators/new-operator.md)
- [オブジェクト初期化子:名前付きの匿名型](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)

### <a name="shared-classes-and-members"></a>共有クラスとメンバー

 クラスの共有メンバーは、プロパティ、プロシージャ、またはクラスのすべてのインスタンスによって共有されているフィールドです。

 共有メンバーを定義します。

```vb
Class SampleClass
    Public Shared SampleString As String = "Sample String"
End Class
```

 共有メンバーにアクセスするには、このクラスのオブジェクトを作成せず、クラスの名前を使用します。

```vb
MsgBox(SampleClass.SampleString)
```

 Visual Basic での共有モジュールは、メンバーのみを共有しており、インスタンス化することはできません。 非共有のプロパティ、フィールドやメソッドに、共有メンバーもアクセスできません。

 詳細については次を参照してください:

- [Shared](../../../visual-basic/language-reference/modifiers/shared.md)
- [Module ステートメント](../../../visual-basic/language-reference/statements/module-statement.md)

### <a name="anonymous-types"></a>匿名型

匿名型を使用すると、データ型のクラス定義を記述せずにオブジェクトを作成できます。 クラスは、コンパイラによって生成されます。 このクラスには使用可能な名前がなく、オブジェクトの宣言時に指定したプロパティが格納されます。

匿名型のインスタンスを作成するコード例を次に示します。

```vb
' sampleObject is an instance of a simple anonymous type.
Dim sampleObject =
    New With {Key .FirstProperty = "A", .SecondProperty = "B"}
```

詳細については次を参照してください:[匿名型](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)します。

## <a name="inheritance"></a>継承

継承を使用すると、他のクラスで定義されている動作を再利用、拡張、および変更する新しいクラスを作成できます。 メンバーが継承される側のクラスを "*基底クラス*" と呼び、メンバーを継承する側のクラスを "*派生クラス*" と呼びます。 ただし、Visual Basic のすべてのクラスが暗黙的の継承、<xref:System.Object>クラスを .NET クラスの階層構造をサポートし、すべてのクラスに下位レベルのサービスを提供します。

> [!NOTE]
> Visual Basic では、多重継承をサポートしていません。 つまり、派生クラスに対して指定できる基底クラスは 1 つだけです。

基底クラスを継承するコード例を次に示します。

```vb
Class DerivedClass
    Inherits BaseClass
End Class
```

既定では、すべてのクラスが継承可能になります。 ただし、クラスを基底クラスとして使用できないように指定したり、基底クラスとしてのみ使用できるクラスを作成したりできます。

クラスを基底クラスとして使用できないように指定する方法を次に示します。

```vb
NotInheritable Class SampleClass
End Class
```

クラスが基底クラスとしてのみ使用され、インスタンス化できないように指定する方法を次に示します。

```vb
MustInherit Class BaseClass
End Class
```

詳細については次を参照してください:

- [Inherits ステートメント](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [NotInheritable](../../../visual-basic/language-reference/modifiers/notinheritable.md)
- [MustInherit](../../../visual-basic/language-reference/modifiers/mustinherit.md)

### <a name="overriding-members"></a>メンバーをオーバーライドします。

既定では、派生クラスは基底クラスのすべてのメンバーを継承します。 継承したメンバーの動作を変更する場合は、そのメンバーをオーバーライドする必要があります。 つまり、派生クラスに、メソッド、プロパティ、またはイベントの新しい実装を定義できます。

プロパティやメソッドのオーバーライド方法を制御するには、次の修飾子を使用します。

|Visual Basic の修飾子|定義|
|---------------------------|----------------|
|[Overridable](../../../visual-basic/language-reference/modifiers/overridable.md)|派生クラスでのクラス メンバーのオーバーライドを許可します。|
|[Overrides](../../../visual-basic/language-reference/modifiers/overrides.md)|基底クラスで定義されている仮想メンバー (オーバーライドできるメンバー) をオーバーライドします。|
|[NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md)|継承するクラスでのメンバーのオーバーライドを禁止します。|
|[MustOverride](../../../visual-basic/language-reference/modifiers/mustoverride.md)|派生クラスでのクラス メンバーのオーバーライドを必須にします。|
|[Shadows](../../../visual-basic/language-reference/modifiers/shadows.md)|基底クラスから継承されたメンバーを隠ぺいします。|

## <a name="interfaces"></a>インターフェイス

インターフェイスは、クラスと同様にプロパティ、メソッド、およびイベントのセットを定義します。 ただし、クラスとは異なり、インターフェイスは実装を提供しません。 インターフェイスはクラスによって実装され、クラスとは別のエンティティとして定義されます。 インターフェイスを実装するクラスは、そのインターフェイスのあらゆる機能を定義に従って厳密に実装する必要があります。この点で、インターフェイスはコントラクトを表しています。

インターフェイスを定義するコード例を次に示します。

```vb
Public Interface ISampleInterface
    Sub DoSomething()
End Interface
```

クラスにインターフェイスを実装するコード例を次に示します。

```vb
Class SampleClass
    Implements ISampleInterface
    Sub DoSomething
        ' Method implementation.
    End Sub
End Class
```

詳細については次を参照してください:

- [インターフェイス](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
- [Interface ステートメント](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Implements ステートメント](../../../visual-basic/language-reference/statements/implements-statement.md)

## <a name="generics"></a>ジェネリック

クラス、構造体、インターフェイスおよび .NET のメソッドを含めることができます*パラメーター入力*格納または使用できるオブジェクトの種類を定義します。 ジェネリックの最も一般的な例として、コレクションがあります。コレクションには、その中に格納されるオブジェクトの型を指定できます。

ジェネリック クラスを定義するコード例を次に示します。

```vb
Class SampleGeneric(Of T)
    Public Field As T
End Class
```

ジェネリック クラスのインスタンスを作成するコード例を次に示します。

```vb
Dim sampleObject As New SampleGeneric(Of String)
sampleObject.Field = "Sample string"
```

詳細については次を参照してください:

- [ジェネリック](../../../standard/generics/index.md)
- [Generic Types in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)

## <a name="delegates"></a>デリゲート

 "*デリゲート*" は、メソッド シグネチャを定義する型であり、互換性のあるシグネチャを持つ任意のメソッドへの参照を提供できます。 メソッドは、デリゲートを使用して起動する (呼び出す) ことができます。 デリゲートは、他のメソッドへの引数としてメソッドを渡すために使用されます。

> [!NOTE]
> イベント ハンドラーは、デリゲートを介して呼び出されるメソッドにすぎません。 デリゲートを使用したイベント処理について詳しくは、「[イベント](../../../standard/events/index.md)」をご覧ください。

デリゲートを作成するコード例を次に示します。

```vb
Delegate Sub SampleDelegate(ByVal str As String)
```

デリゲートで指定されたシグネチャに一致するメソッドへの参照を作成するコード例を次に示します。

```vb
Class SampleClass
    ' Method that matches the SampleDelegate signature.
    Sub SampleSub(ByVal str As String)
        ' Add code here.
    End Sub
    ' Method that instantiates the delegate.
    Sub SampleDelegateSub()
        Dim sd As SampleDelegate = AddressOf SampleSub
        sd("Sample string")
    End Sub
End Class
```

詳細については次を参照してください:

- [デリゲート](../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [Delegate ステートメント](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [AddressOf 演算子](../../../visual-basic/language-reference/operators/addressof-operator.md)

## <a name="see-also"></a>関連項目

- [Visual Basic プログラミング ガイド](../../../visual-basic/programming-guide/index.md)
