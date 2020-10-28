---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Paulistringfromgenidx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 33da4bc3d7e58b87aef75b453b6af09a51214923
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701712"
---
# <a name="paulistringfromgenidx-function"></a>Paulistringfromgenidx-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Extrahiert die Pauli-Zeichenfolge und ihre Qubit-Indizes eines von einem beschriebenen Pauli-Begriffs `GeneratorIndex` .

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a>Eingabe

### <a name="generatorindex--generatorindex"></a>generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` der Typ, der einen Pauli-Begriff codiert.



## <a name="output--pauliint"></a>Ausgabe: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])

Die Pauli-Zeichenfolge des von einem beschriebenen Begriffs `GeneratorIndex` und Indizes zu den Qubits, auf die Sie angewendet wird.