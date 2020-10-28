---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Trotterstepsize-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: fabfbff74572b3c96c701de5443e4265a0468d78
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703721"
---
# <a name="trotterstepsize-function"></a>Trotterstepsize-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Berechnet die Schrittgröße des Trotters in der rekursiven Implementierung des trocksimulations Algorithmus.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>Eingabe

### <a name="order--int"></a>Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Hinweise

Bei diesem Vorgang wird eine andere Indizierungs Konvention verwendet als [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139). Dies entspricht insbesondere `DecomposedIntoTimeStepsCA(_, 4)` dem skalaren $p _2 (\lambda) $ in quant-ph/0508139.