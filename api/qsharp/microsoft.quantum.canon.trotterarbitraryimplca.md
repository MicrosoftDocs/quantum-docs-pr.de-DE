---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: Vorgang "trotterarbiaryimplca"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1c094d09ac8bdd71a59ef57d8715a6f90f18efc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703746"
---
# <a name="trotterarbitraryimplca-operation"></a>Vorgang "trotterarbiaryimplca"

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Rekursive Implementierung des Trotters der geraden Ordnung – Suzuki Integrator.

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a>Eingabe

### <a name="order--int"></a>Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge von Trotter-Suzuki Integrator.


### <a name="nsteps--int"></a>nsteps: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.


### <a name="op--intdoublet--unit-adj--ctl"></a>OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ) `Double` und ein Quantum-Register (Typ `'T` ) für die Zerlegung akzeptiert werden.


### <a name="stepsize--double"></a>stepSize: [Double](xref:microsoft.quantum.lang-ref.double)

Multiplikator für die Größe der einzelnen Schritte der Simulation.


### <a name="target--t"></a>Ziel: 't

Ein Quantum-Register, für das der Vorgang ausgeführt wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .