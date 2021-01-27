---
uid: Microsoft.Quantum.Logical.Xor
title: XOR-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: 4a4af7f628ca64170e046584d9caffe7ceee3d56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848451"
---
# <a name="xor-function"></a>XOR-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die boolesche exklusive Disjunktion von zwei Werten zurück.

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

Der erste zu berücksichtigende Wert.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

Der zweite zu berücksichtigende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` nur dann, wenn genau eines von `a` und `b` ist `true` .