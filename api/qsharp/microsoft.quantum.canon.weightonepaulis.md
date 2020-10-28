---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Gewickepaulis-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703709"
---
# <a name="weightonepaulis-function"></a>Gewickepaulis-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt ein Array aller Gewichtungs-1-Pauli-Operatoren für eine angegebene Anzahl von Qubits zurück.

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, für die die zurückgegebenen Pauli-Operatoren definiert sind.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Ein Array von multiqubit-Pauli-Operatoren, die jeweils als ein Array mit einer Länge dargestellt werden `nQubits` .