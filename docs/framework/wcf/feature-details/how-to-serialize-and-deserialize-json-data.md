---
title: '方法: および JSON データを逆シリアル化'
ms.date: 03/30/2017
ms.assetid: 88abc1fb-8196-4ee3-a23b-c6934144d1dd
ms.openlocfilehash: 797b29fd7ddecd3e3ed85f8cb3a6df93044942ef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704343"
---
# <a name="how-to-serialize-and-deserialize-json-data"></a><span data-ttu-id="27c32-102">方法: および JSON データを逆シリアル化</span><span class="sxs-lookup"><span data-stu-id="27c32-102">How to: Serialize and Deserialize JSON Data</span></span>
<span data-ttu-id="27c32-103">JSON (JavaScript Object Notation) は、クライアント ブラウザーと AJAX 対応の Web サービスとの間で、少量のデータを高速に交換できる効率的なデータ エンコード形式です。</span><span class="sxs-lookup"><span data-stu-id="27c32-103">JSON (JavaScript Object Notation) is an efficient data encoding format that enables fast exchanges of small amounts of data between client browsers and AJAX-enabled Web services.</span></span>  
  
 <span data-ttu-id="27c32-104">ここでは、<xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> を使用して .NET 型のオブジェクトを JSON エンコードされたデータにシリアル化し、この JSON 形式のデータを .NET 型のインスタンスに戻すために逆シリアル化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="27c32-104">This topic demonstrates how to serialize .NET type objects into JSON-encoded data and then deserialize data in the JSON format back into instances of .NET types using the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span> <span data-ttu-id="27c32-105">この例では、ユーザー定義された `Person` 型のシリアル化と逆シリアル化を示すためにデータ コントラクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="27c32-105">This example uses a data contract to demonstrate serialization and deserialization of a user-defined `Person` type.</span></span>  
  
 <span data-ttu-id="27c32-106">通常、JSON のシリアル化および逆シリアル化が自動的に処理 Windows Communication Foundation (WCF) によって AJAX 対応エンドポイント経由で公開されているサービス操作でデータ コントラクト型を使用する場合。</span><span class="sxs-lookup"><span data-stu-id="27c32-106">Normally, JSON serialization and deserialization is handled automatically by Windows Communication Foundation (WCF) when you use data contract types in service operations that are exposed over AJAX-enabled endpoints.</span></span> <span data-ttu-id="27c32-107">ただし、特定の場合においては JSON データを直接処理する必要があります。このトピックでは、このようなシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="27c32-107">However, in some cases you may need to work with JSON data directly - this is the scenario that this topic demonstrates.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="27c32-108">サーバー上で送信応答のシリアル化中にエラーが発生した場合、または応答操作がなんらかの理由で例外をスローした場合、エラーにより応答がクライアントに戻らないことがあります。</span><span class="sxs-lookup"><span data-stu-id="27c32-108">If an error occurs during serialization of an outgoing reply on the server or the reply operation throws an exception for some other reason, it may not get returned to the client as a fault.</span></span>  
  
 <span data-ttu-id="27c32-109">このトピックではに基づいて、 [JSON のシリアル化](../../../../docs/framework/wcf/samples/json-serialization.md)サンプル。</span><span class="sxs-lookup"><span data-stu-id="27c32-109">This topic is based on the [JSON Serialization](../../../../docs/framework/wcf/samples/json-serialization.md) sample.</span></span>  
  
### <a name="to-define-the-data-contract-for-a-person"></a><span data-ttu-id="27c32-110">Person のデータ コントラクトを定義するには</span><span class="sxs-lookup"><span data-stu-id="27c32-110">To define the data contract for a Person</span></span>  
  
1.  <span data-ttu-id="27c32-111">クラスに `Person` をアタッチし、シリアル化するメンバーに <xref:System.Runtime.Serialization.DataContractAttribute> 属性をアタッチすることで、<xref:System.Runtime.Serialization.DataMemberAttribute> のデータ コントラクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="27c32-111">Define the data contract for `Person` by attaching the <xref:System.Runtime.Serialization.DataContractAttribute> to the class and <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to the members you want to serialize.</span></span> <span data-ttu-id="27c32-112">データ コントラクトの詳細については、次を参照してください。 [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md)します。</span><span class="sxs-lookup"><span data-stu-id="27c32-112">For more information about data contracts, see [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md).</span></span>  
  
    ```csharp  
    [DataContract]  
    internal class Person  
    {  
        [DataMember]  
        internal string name;  
  
        [DataMember]  
        internal int age;  
    }  
    ```  
  
### <a name="to-serialize-an-instance-of-type-person-to-json"></a><span data-ttu-id="27c32-113">Person 型のインスタンスを JSON にシリアル化するには</span><span class="sxs-lookup"><span data-stu-id="27c32-113">To serialize an instance of type Person to JSON</span></span>  
  
1.  <span data-ttu-id="27c32-114">`Person` 型のインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="27c32-114">Create an instance of the `Person` type.</span></span>  
  
    ```csharp  
    Person p = new Person();  
    p.name = "John";  
    p.age = 42;  
    ```  
  
2.  <span data-ttu-id="27c32-115">`Person` を使用して、<xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> オブジェクトをメモリ ストリームにシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="27c32-115">Serialize the `Person` object to a memory stream using the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span>  
  
    ```csharp  
    MemoryStream stream1 = new MemoryStream();  
    DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(Person));  
    ```  
  
3.  <span data-ttu-id="27c32-116">JSON データをストリームに書き込むには、<xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A> メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="27c32-116">Use the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A> method to write JSON data to the stream.</span></span>  
  
    ```csharp  
    ser.WriteObject(stream1, p);  
    ```  
  
4.  <span data-ttu-id="27c32-117">JSON の出力を表示します。</span><span class="sxs-lookup"><span data-stu-id="27c32-117">Show the JSON output.</span></span>  
  
    ```csharp  
    stream1.Position = 0;  
    StreamReader sr = new StreamReader(stream1);  
    Console.Write("JSON form of Person object: ");  
    Console.WriteLine(sr.ReadToEnd());  
    ```  
  
### <a name="to-deserialize-an-instance-of-type-person-from-json"></a><span data-ttu-id="27c32-118">JSON から Person 型のインスタンスに逆シリアル化するには</span><span class="sxs-lookup"><span data-stu-id="27c32-118">To deserialize an instance of type Person from JSON</span></span>  
  
1.  <span data-ttu-id="27c32-119">`Person` の <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.ReadObject%2A> メソッドを使用して、JSON エンコードされたデータを <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> の新しいインスタンスに逆シリアル化します。</span><span class="sxs-lookup"><span data-stu-id="27c32-119">Deserialize the JSON-encoded data into a new instance of `Person` by using the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.ReadObject%2A> method of the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span>  
  
    ```csharp  
    stream1.Position = 0;  
    Person p2 = (Person)ser.ReadObject(stream1);  
    ```  
  
2.  <span data-ttu-id="27c32-120">結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="27c32-120">Show the results.</span></span>  
  
    ```csharp  
    Console.WriteLine($"Deserialized back, got name={p2.name}, age={p2.age}");  
    ```  
  
## <a name="example"></a><span data-ttu-id="27c32-121">例</span><span class="sxs-lookup"><span data-stu-id="27c32-121">Example</span></span>  
  
```csharp  
// Create a User object and serialize it to a JSON stream.  
public static string WriteFromObject()  
{  
    //Create User object.  
    User user = new User("Bob", 42);  
  
    //Create a stream to serialize the object to.  
    MemoryStream ms = new MemoryStream();  
  
    // Serializer the User object to the stream.  
    DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(User));  
    ser.WriteObject(ms, user);  
    byte[] json = ms.ToArray();  
    ms.Close();  
    return Encoding.UTF8.GetString(json, 0, json.Length);  
}  
  
// Deserialize a JSON stream to a User object.  
public static User ReadToObject(string json)  
{  
    User deserializedUser = new User();  
    MemoryStream ms = new MemoryStream(Encoding.UTF8.GetBytes(json));  
    DataContractJsonSerializer ser = new DataContractJsonSerializer(deserializedUser.GetType());  
    deserializedUser = ser.ReadObject(ms) as User;  
    ms.Close();  
    return deserializedUser;  
}  
```  
  
> [!NOTE]
>  <span data-ttu-id="27c32-122">JSON シリアライザーは、次のサンプル コードに示すように、データ コントラクターの複数のメンバーが同じ名前である場合、シリアル化例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="27c32-122">The JSON serializer throws a serialization exception for data contracts that have multiple members with the same name, as shown in the following sample code.</span></span>  
  
```csharp  
[DataContract]  
public class TestDuplicateDataBase  
{  
    [DataMember]  
    public int field1 = 123;  
}

[DataContract]  
public class TestDuplicateDataDerived : TestDuplicateDataBase  
{  
    [DataMember]  
    public new int field1 = 999;  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="27c32-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="27c32-123">See also</span></span>
- [<span data-ttu-id="27c32-124">スタンドアロン JSON のシリアル化</span><span class="sxs-lookup"><span data-stu-id="27c32-124">Stand-Alone JSON Serialization</span></span>](../../../../docs/framework/wcf/feature-details/stand-alone-json-serialization.md)
- [<span data-ttu-id="27c32-125">JSON などのデータ転送形式のサポート</span><span class="sxs-lookup"><span data-stu-id="27c32-125">Support for JSON and Other Data Transfer Formats</span></span>](../../../../docs/framework/wcf/feature-details/support-for-json-and-other-data-transfer-formats.md)
