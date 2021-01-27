---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: Blockencodingreflectionbylcu-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: ef92e517ae40e76c94aff1121c78ece9985109fc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857709"
---
# <a name="blockencodingreflectionbylcu-function"></a>Blockencodingreflectionbylcu-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codiert einen relevanten Operator in eine `BlockEncodingReflection` .

Dadurch wird ein `BlockEncodingReflection` einheitlicher $U = p\cdot v\cdot P ^ \dagger $ erstellt, der einen Operator $H = \ sum_ {j} | \ alpha_j codiert | U_j $ von Interesse, bei dem es sich um eine lineare Kombination von uniflüssen handelt. In der Regel ist $P $ eine einheitliche Zustands Vorbereitung, z {0} \_ . b. $P \ket a \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ und $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Eingabe

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a>statepreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher $P $, der einen bestimmten Ziel Status vorbereitet.


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a>Selector: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher $V $, der die Komponenten unierungen von $H $ codiert.



## <a name="output--blockencodingreflection"></a>Ausgabe: [blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Ein einheitlicher $U $, der gemeinsam für Register agiert `a` und `s` $H $ codiert und $U "^ {-1} = U $" erfüllt.

## <a name="remarks"></a>Bemerkungen

Diese `BlockEncoding` Implementierung gibt Ihnen die Eigenschaften eines `BlockEncodingReflection` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)