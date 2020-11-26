---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: Rmencoding-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202939"
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