---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Trotterstepsize-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840073"
---
# <a name="trotterstepsize-function"></a>Trotterstepsize-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet die Schrittgröße des Trotters in der rekursiven Implementierung des trocksimulations Algorithmus.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>Eingabe

### <a name="order--int"></a>Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Bemerkungen

Bei diesem Vorgang wird eine andere Indizierungs Konvention verwendet als [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139). Dies entspricht insbesondere `DecomposedIntoTimeStepsCA(_, 4)` dem skalaren $p _2 (\lambda) $ in quant-ph/0508139.