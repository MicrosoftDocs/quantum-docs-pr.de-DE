---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Rmencoding-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: f3c54d2e40511dacb21618b4eaf1eef9f4903f9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855344"
---
# <a name="rmencoding-function"></a>Rmencoding-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


{-1,1} Codieren eines booleschen Wahrheits Werts

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a>Eingabe

### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

Boolescher Wert



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

1, wenn `b` false ist, andernfalls-1.