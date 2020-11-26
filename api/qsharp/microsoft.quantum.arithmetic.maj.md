---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Maj-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 356689baa6d47b7b93a393f3672991bb589f6921
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222761"
---
# <a name="maj-operation"></a>Maj-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dadurch wird der Vorgang für die direkte Mehrheit auf 3 Qubits angewendet.

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Wenn wir den Zustand des Ziel-Qubit als $ \ket{z} $ und die Eingabe Zustände der Eingabe-Qubits als $ \ket{x} $ und $ \ket{y} $ bezeichnen, dieser Vorgang führt die folgende Transformation aus: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{Maj} (x, y, z)} $.

## <a name="input"></a>Eingabe

### <a name="input0--qubit"></a>input0: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das erste Eingabe-Qubit.


### <a name="input1--qubit"></a>eingabe1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das zweite Eingabe-Qubit.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, auf das die Mehrheits Funktion angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

