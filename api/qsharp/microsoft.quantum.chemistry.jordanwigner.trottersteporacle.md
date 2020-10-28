---
uid: Microsoft.Quantum.Chemistry.JordanWigner.TrotterStepOracle
title: Trottersteporacle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: TrotterStepOracle
qsharp.summary: Returns Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: f7659616ea39d781137c26965cbf2005c5e634b2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703097"
---
# <a name="trottersteporacle-function"></a>Trottersteporacle-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


Gibt den Vorgang des trockschrittes und die für die Ausführung erforderlichen Parameter zurück.

```qsharp
function TrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a>Eingabe

### <a name="qsharpdata--jordanwignerencodingdata"></a>qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.


### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)

Schrittgröße des trotterintegrator.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge des trockintegrator.



## <a name="output--intdoublequbit--unit-adj--ctl"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL))

Ein Tupel, wobei: `Int` die Anzahl der zugeordneten Qubits ist, `Double` `1.0/trotterStepSize` und der Vorgang ist der trockschritt.