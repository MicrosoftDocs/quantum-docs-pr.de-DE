---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Dumpoperation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: cde188806506c586c4c77a7f9b2b43ad0e10ef1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829274"
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



## <a name="example"></a>Beispiel

Wenn der folgende Code Ausschnitt auf dem Quantum-simulatorziel ausgeführt wird, wird die Matrix $ $ \begin{aligned} \left ausgegeben (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \end{Matrix}\right) \end{aligned}.
$$

```qsharp
operation DumpCnot() : Unit {
    DumpOperation(2, ApplyToFirstTwoQubitsCA(CNOT, _));
}
```

## <a name="remarks"></a>Bemerkungen

Das Aufrufen dieses Vorgangs hat keine Observable-Auswirkung in Q #. Die genaue Diagnose, die ggf. angezeigt wird, hängt vom aktuellen Ausführungs Ziel und der Editor Umgebung ab.
Wenn z. b. für den vollständigen Quantum-Simulator verwendet wird, wird eine einheitliche Matrix, die zur Darstellung von verwendet wird, `op` angezeigt.

Beachten Sie, dass bei der Durchführung von Simulatoren, die eine globale Phasen Mehrdeutigkeit zulassen (z. b. der voll Zustands Simulator), die zurückgegebenen Darstellungen bis zu einer globalen Phase variieren können.

Ebenso kann die Reihenfolge der Zeilen-und Spalten Matrizen von den Konventionen abweichen, die von den einzelnen Simulatoren verwendet werden, die diesen Vorgang unterstützen.