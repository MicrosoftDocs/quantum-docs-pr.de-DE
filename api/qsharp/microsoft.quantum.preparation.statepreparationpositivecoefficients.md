---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Statepreparationpositivekoefficients-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722892"
---
# <a name="statepreparationpositivecoefficients-function"></a>Statepreparationpositivekoefficients-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Gibt einen Vorgang zurück, der den gegebenen Quantum-Zustand vorbereitet.

Der zurückgegebene Vorgang $U $ bereitet einen beliebigen Quantum-Status $ \ket{\psi} $ mit positiven Koeffizienten $ \ alpha_j \ge $0 aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0...0} $ vor.

Die Aktion "U" für ein neu zugeordneter Register wird durch "$ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \bruchteil {" angegeben. \ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.
\end{align} $ $

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Array von bis zu $2 ^ n $ Koeffizienten $ \ alpha_j $. Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.



## <a name="output--littleendian--unit-adj--ctl"></a>Ausgabe: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Eine einheitliche Zustands Vorbereitungs Operation $U $.

## <a name="remarks"></a>Hinweise

Negative Eingabe Koeffizienten $ \ alpha_j < $0 werden als positiv mit dem Wert $ | \ alpha_j | $ behandelt. `coefficients` wird mit Elementen $ \ alpha_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.