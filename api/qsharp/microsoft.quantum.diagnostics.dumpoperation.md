---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Dumpoperation-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: b0e07173ddbeb8a96d4a85928258b6e30deb394d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202055"
---
# <a name="dumpoperation-operation"></a>Dumpoperation-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Zeigt bei einem Vorgang Diagnoseinformationen zu dem Vorgang an, der vom aktuellen Ausführungs Ziel verfügbar gemacht wird.

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, auf die der angegebene Vorgang angewendet wird.


### <a name="op--qubit--unit--is-adj"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Der Vorgang, der diagnostiziert werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Das Aufrufen dieses Vorgangs hat keine Observable-Auswirkung in Q #. Die genaue Diagnose, die ggf. angezeigt wird, hängt vom aktuellen Ausführungs Ziel und der Editor Umgebung ab.
Wenn z. b. für den vollständigen Quantum-Simulator verwendet wird, wird eine einheitliche Matrix, die zur Darstellung von verwendet wird, `op` angezeigt.

Beachten Sie, dass bei der Durchführung von Simulatoren, die eine globale Phasen Mehrdeutigkeit zulassen (z. b. der voll Zustands Simulator), die zurückgegebenen Darstellungen bis zu einer globalen Phase variieren können.

Ebenso kann die Reihenfolge der Zeilen-und Spalten Matrizen von den Konventionen abweichen, die von den einzelnen Simulatoren verwendet werden, die diesen Vorgang unterstützen.