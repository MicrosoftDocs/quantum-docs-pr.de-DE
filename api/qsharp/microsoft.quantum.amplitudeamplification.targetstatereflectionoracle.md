---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Targetstatuereflectionoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 4169ccf3e210e27f779311553b845ea04f2c7dc6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843906"
---
# <a name="targetstatereflectionoracle-function"></a>Targetstatuereflectionoracle-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt eine `ReflectionOracle` über den Zielzustand, der durch das Flag-Qubit eindeutig gekennzeichnet ist.

Der Ziel Status verfügt über ein einzelnes Qubit, das auf 1 festgelegt ist, und alle anderen 0: $ \ket {1} _F $.

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a>Eingabe

### <a name="idxflagqubit--int"></a>idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)

Index zum Markieren von Qubit-$f $ of Oracle.



## <a name="output--reflectionoracle"></a>Ausgabe: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Ein `ReflectionOracle` , der den durch $ \ket _F $ markierten Zustand wieder gibt {1} .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. reflectionoracle](xref:Microsoft.Quantum.Canon.ReflectionOracle)