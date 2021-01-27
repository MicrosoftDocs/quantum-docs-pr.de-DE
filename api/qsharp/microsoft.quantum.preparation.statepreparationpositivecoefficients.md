---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Statepreparationpositivekoefficients-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855844"
---
# <a name="statepreparationpositivecoefficients-function"></a>Statepreparationpositivekoefficients-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Statepreparationpositivekoefficients ist veraltet. Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>.

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



## <a name="output--littleendian--unit--is-adj--ctl"></a>Ausgabe: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL.

Eine einheitliche Zustands Vorbereitungs Operation $U $.

## <a name="example"></a>Beispiel

Im folgenden Code Ausschnitt wird der Quantum-Status $ \ket{\psi} = \ sqrt {1/8} \ Ket {0} + \ sqrt {7/8} \ Ket {2} $ im Qubit-Register vorbereitet `qubitsLE` .

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a>Bemerkungen

Negative Eingabe Koeffizienten $ \ alpha_j < $0 werden als positiv mit dem Wert $ | \ alpha_j | $ behandelt. `coefficients` wird mit Elementen $ \ alpha_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.