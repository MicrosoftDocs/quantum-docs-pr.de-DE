---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Targetstatuereflectionoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191107"
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