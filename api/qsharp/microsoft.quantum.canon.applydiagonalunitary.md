---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Applydiagonaleinheitlicher-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 8f17c3cb222bef00ead5e7fea5d29d296b9a428a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218851"
---
# <a name="applydiagonalunitary-operation"></a>Applydiagonaleinheitlicher-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet ein Array komplexer Phasen auf numerische Basiszustände eines Register von Qubits an.

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Mit diesem Vorgang wird eine Diagonale einheitliche implementiert, die eine komplexe Phase $e ^ {i \ theta_j} $ auf dem $n $-Qubit-Zahlen Status $ \ket{j} $ anwendet.
Insbesondere kann dieser Vorgang durch die einheitliche

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.
\end{align} $ $

## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $. Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.

## <a name="references"></a>Referenzen

- Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. ungefähre atelyapplydiagonaleinheitlicher](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)