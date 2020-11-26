---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Gewickepaulis-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 904c606393131d51eaa44d464ad52bec509eaf72
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204537"
---
# <a name="weightonepaulis-function"></a>Gewickepaulis-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein Array aller Gewichtungs-1-Pauli-Operatoren für eine angegebene Anzahl von Qubits zurück.

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, für die die zurückgegebenen Pauli-Operatoren definiert sind.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Ein Array von multiqubit-Pauli-Operatoren, die jeweils als ein Array mit einer Länge dargestellt werden `nQubits` .