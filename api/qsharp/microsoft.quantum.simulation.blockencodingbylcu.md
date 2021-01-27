---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Blockencodingbylcu-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 1d7890e96513817c127ef768f49c0b915ea22fa1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858156"
---
# <a name="blockencodingbylcu-function"></a>Blockencodingbylcu-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codiert einen relevanten Operator in eine `BlockEncoding` .

Dadurch wird ein `BlockEncoding` einheitlicher $U = p\cdot v\cdot P ^ \dagger $ erstellt, der einen Operator $H = \ sum_ {j} | \ alpha_j codiert | U_j $ von Interesse, bei dem es sich um eine lineare Kombination von uniflüssen handelt. In der Regel ist $P $ eine einheitliche Zustands Vorbereitung, z. b. $P \ket {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ und $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="statepreparation--t--unit--is-adj--ctl"></a>statepreparation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher $P $, der einen bestimmten Ziel Status vorbereitet.


### <a name="selector--ts--unit--is-adj--ctl"></a>Selektor: ('t, es) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher $V $, der die Komponenten unierungen von $H $ codiert.



## <a name="output--ts--unit--is-adj--ctl"></a>Ausgabe: ('t, es) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher $U $, der gemeinsam für Register fungiert `a` und `s` $H $ codiert und $U ^ \dagger = U $ entspricht.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="s"></a>Spaniens



## <a name="remarks"></a>Bemerkungen

Diese `BlockEncoding` Implementierung gibt Ihnen die Eigenschaften eines `BlockEncodingReflection` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. Quantum. Simulation. blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)