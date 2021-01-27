---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Preparepaulieigen State-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: 473bb2fa4429a14f69bcae4573354aad87dc37df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854353"
---
# <a name="preparepaulieigenstate-operation"></a>Preparepaulieigen State-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bereitet ein Qubit im positiven eigen Zustand eines angegebenen Pauli-Operators vor.
Wenn der Identity-Operator angegeben ist, wird das Qubit im Status "in maximalgemischter Form" vorbereitet.

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a>Beschreibung

Wenn sich das Qubit anfänglich im $ \ket {0} $-Zustand befunden hat, bereitet dieser Vorgang das Qubit im $ + $1-eigen Zustand eines angegebenen Pauli-Operators bzw `PauliI` . für im Status "maximisch Mixed" (siehe <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ) vor.

Wenn sich das Qubit in einem anderen Zustand als $ \ket {0} $ befunden hat, wendet dieser Vorgang die folgenden Gates an: $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` und <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI` .

## <a name="input"></a>Eingabe

### <a name="basis--pauli"></a>Basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Ein Pauli-Operator $P $.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, das vorbereitet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

So bereiten Sie ein Qubit im Zustand "$ \ket{+} $" vor:

```qsharp
using (q = Qubit()) {
    PreparePauliEigenstate(PauliX, qubit);
    // ...
}
```