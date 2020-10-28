---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Assertqubitisinstatewithintoleranz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: 5d34bdac53870326dacb5a11c27c857793c3f420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702738"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a>Assertqubitisinstatewithintoleranz-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass ein Qubit im erwarteten Zustand ist.

`expected` stellt einen komplexen Vektor dar, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.
Das erste Element der Tupel, das jede $a $ darstellt, $b $ der reelle Teil der komplexen Zahl ist, während das zweite Element der imaginäre Teil ist.
Das letzte Argument definiert die Toleranz, mit der die-Assertionen durchgeführt werden.

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Eingabe

### <a name="expected--complexcomplex"></a>erwartet: ([Komplex](xref:Microsoft.Quantum.Math.Complex),[Komplex](xref:Microsoft.Quantum.Math.Complex))

Es wurden komplexe Verstärkung für "$ \ket {0} $" bzw. "$ \ket $" erwartet {1} .


### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, dessen Zustand bestätigt werden soll. Beachten Sie, dass dieses Qubit von anderen zugeordneten Qubits getrennt werden und nicht entkoppelt ist.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Additiv Toleranz, mit der tatsächliche Verstärkung von der erwarteten Abweichung abweichen darf.
Weitere Informationen finden Sie weiter unten in den hinweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Der folgende Mathematica-Code kann verwendet werden, um Ausdrücke für Mi, MX, my, MZ zu überprüfen:

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

Die Toleranz ist die $L \_ {\infty} $ Distance zwischen 3 dimensionalem Real Vector (x, x ₃, x ₄) definiert durch $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ und Real Vector (Y. y ₃, y ₄) definiert durch p = Y ₁ I + y. x + y ₃ y + y ₄ Z WHERE p ist die Dichte Matrix, die dem Status des Registers entspricht.
Dies gilt nur unter der Annahme, dass TR (p) und TR (| ψ ⟩ ⟨ ψ |) gleich 1 sind (z. b. x ₁ = 1/2, y ₁ = 1/2).
Wenn dies nicht der Fall ist, wird durch die-Funktion bestätigt, dass der Abstand zwischen (x, x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) und (y, y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) kleiner ist als der Tolerance-Parameter.