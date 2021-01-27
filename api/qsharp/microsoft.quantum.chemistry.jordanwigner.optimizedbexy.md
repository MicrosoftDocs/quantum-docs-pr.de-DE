---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Optimizedbexy-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 28a7c7877a3d48fd5ba50384d7996017e7cdb14f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837246"
---
# <a name="optimizedbexy-operation"></a>Optimizedbexy-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Ein einheitlicher $U $, der die Pauli-Zeichenfolge auf $ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1} anwendet... Z_0 $ on Qubits $0.. p $, bedingt an einem Index $z \in \{ 0, 1 \} $ und $p $. Das heißt: $ $ \begin{align} u\ket {z} \ Ket {p} \ Ket {\ PSI} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 \ket{\psi} \end{align} $ $

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="paulibasis--qubit"></a>paulibasis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Wenn sich dieses Qubit im Status $ \ket {0} $ befindet, wird $X $ angewendet. Wenn Sie den Status $ \ket {1} $ aufweist, wird $Y $ angewendet.


### <a name="indexregister--littleendian"></a>Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Der Status $ \ket{p} $ dieses Registers bestimmt das Qubit, auf dem $X $ oder $Y $ angewendet wird.


### <a name="targetregister--qubit"></a>targetregiester: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Register der Qubits, auf die die Pauli-Operatoren angewendet werden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>References

- Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662