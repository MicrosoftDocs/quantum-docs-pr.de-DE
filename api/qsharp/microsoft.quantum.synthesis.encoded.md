---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Codierte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855493"
---
# <a name="encoded-function"></a>Codierte Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wahrheitstabelle beim {1,-1} Codieren codieren

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="table--bool"></a>Tabelle: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Wahrheitstabelle als Array von Wahrheits Werten



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Wahrheitstabelle als {1,-1} Array von ganzen Zahlen

## <a name="example"></a>Beispiel

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```