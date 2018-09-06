---
title: カスタム型を使用した Switch アクティビティの使用
ms.date: 03/30/2017
ms.assetid: 482a48c4-eb83-40c3-a4e2-2f9a8af88b75
ms.openlocfilehash: b24a03573b31f3fb1c34d4aa6e03bc11f5b25455
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "44038875"
---
# <a name="usage-of-the-switch-activity-with-custom-types"></a>カスタム型を使用した Switch アクティビティの使用
このサンプルでは、<xref:System.Activities.Statements.Switch%601> アクティビティを有効にしてユーザー定義の複合型を実行時に評価する方法について説明します。 従来のほとんどの手続き型プログラミング言語での[切り替える](https://go.microsoft.com/fwlink/?LinkId=180521)ステートメントは、変数の条件の評価に基づいて実行ロジックを選択します。 従来、`switch` ステートメントは、静的に評価できる式を対象としています。 つまり、たとえば C# では、プリミティブ型 (<xref:System.Boolean>、<xref:System.Int32>、<xref:System.String>、列挙型など) のみがサポートされます。  
  
 カスタム クラスで切り替えを有効にするには、カスタム複合型の値を実行時に評価するロジックを実装する必要があります。 このサンプルでは、`Person` という名前のカスタム複合型で切り替えを有効にする方法を示します。  
  
-   カスタム クラス `Person` では、<xref:System.ComponentModel.TypeConverter> 属性がカスタム <xref:System.ComponentModel.TypeConverter> の名前で宣言されます。  
  
    ```  
    [TypeConverter(typeof(PersonConverter))]  
    public class Person  
    {  
       public string Name { get; set; }  
       public int Age { get; set; }  
    ...  
    ```  
  
-   カスタム クラス `Person` では、<xref:System.Object.Equals%2A> クラスと <xref:System.Object.GetHashCode%2A> クラスがオーバーライドされます。  
  
    ```  
    public override bool Equals(object obj)  
    {  
        Person person = obj as Person;  
  
        if (person != null)  
        {  
            return string.Equals(this.Name, person.Name);  
        }  
  
        return false;  
    }  
  
    public override int GetHashCode()  
    {  
        if (this.Name != null)  
        {  
            return this.Name.GetHashCode();  
        }  
  
        return 0;  
    }  
    ```  
  
-   カスタム クラスのインスタンスから文字列への変換、および文字列からカスタム クラスのインスタンスへの変換を行う、カスタム <xref:System.ComponentModel.TypeConverter> クラスが実装されます。  
  
    ```  
    public class PersonConverter : TypeConverter  
    {  
        public override bool CanConvertFrom(ITypeDescriptorContext context,  
           Type sourceType)  
        {  
            return (sourceType is string);  
        }  
  
        // Overrides the ConvertFrom method of TypeConverter.  
        public override object ConvertFrom(ITypeDescriptorContext context,  
           CultureInfo culture, object value)  
        {  
            if (value == null)  
            {  
                return null;  
            }  
  
            if (value is string)  
            {  
                return new Person  
                {  
                    Name = (string)value  
                };  
            }  
  
            return base.ConvertFrom(context, culture, value);  
        }  
  
        // Overrides the ConvertTo method of TypeConverter.  
        public override object ConvertTo(ITypeDescriptorContext context,  
           CultureInfo culture, object value, Type destinationType)  
        {  
            if (destinationType == typeof(string))  
            {  
                if (value != null)  
                {  
                    return ((Person) value).Name;  
                }  
                else  
                {  
                    return null;  
                }  
            }  
  
            return base.ConvertTo(context, culture, value, destinationType);  
        }  
    }  
    ```  
  
 このサンプルには、次のファイルが含まれています。  
  
-   **Person.cs**: 定義、`Person`クラス。  
  
-   **PersonConverter.cs**: の型コンバーター、`Person`クラス。  
  
-   **Sequence.xaml**: ワークフローを切り替え、`Person`型。  
  
-   **Program.cs**: ワークフローを実行する main 関数。  
  
#### <a name="to-use-this-sample"></a>このサンプルを使用するには  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] に Switch.sln を読み込みます。  
  
2.  Ctrl キーと Shift キーを押しながら B キーを押して、ソリューションをビルドします。  
  
3.  Ctrl キーを押しながら F5 キーを押してサンプルを実行します。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。 続行する前に、次の (既定の) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。 このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\Switch`  
  
## <a name="see-also"></a>関連項目  
 [ビルトイン アクティビティ ライブラリ](../../../../docs/framework/windows-workflow-foundation/net-framework-4-5-built-in-activity-library.md)
