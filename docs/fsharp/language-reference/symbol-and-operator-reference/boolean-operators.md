---
title: ブール演算子 (F#)
description: F# プログラミング言語で使用可能なブール演算子について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: faa181090efa7c4064a30b42d83afa4888e98b82
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2018
ms.locfileid: "45638481"
---
# <a name="boolean-operators"></a>ブール演算子

このトピックでは、f# 言語でブール演算子のサポートについて説明します。

## <a name="summary-of-boolean-operators"></a>ブール演算子の概要

次の表では、f# 言語で使用可能なブール演算子をまとめたものです。 これらの演算子でサポートされている唯一の種類は、`bool`型。

|演算子|説明|
|--------|-----------|
|`not`|否定のブール型|
|<code>&#124;&#124;</code>|ブール型 OR|
|`&&`|ブール型 AND|

ブール型 AND および OR 演算子を実行*ショート サーキット評価*演算子の右辺の式を評価、式の全体的な結果を確認する必要がある場合にのみ、します。 2 番目の式、`&&`に最初の式が評価された場合にのみ、演算子が評価される`true`; の 2 番目の式、`||`に最初の式が評価された場合にのみ、演算子が評価される`false`します。

## <a name="see-also"></a>関連項目

- [ビット処理演算子](bitwise-operators.md)
- [算術演算子](arithmetic-operators.md)
- [シンボルと演算子のリファレンス](index.md)
