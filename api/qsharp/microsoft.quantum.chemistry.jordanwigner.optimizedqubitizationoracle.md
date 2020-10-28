---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle
title: Optimizedqubitizationoracle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedQubitizationOracle
qsharp.summary: Returns T-count optimized Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: c67dc5890fe1444c1689eb803ed3d24b2dbe5ce2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703146"
---
# <a name="optimizedqubitizationoracle-function"></a>Optimizedqubitizationoracle-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


Gibt einen optimierten qubisierungsvorgang mit T-Anzahl und die für die Ausführung erforderlichen Parameter zurück.

```qsharp
function OptimizedQubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, targetError : Double) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a>Eingabe

### <a name="qsharpdata--jordanwignerencodingdata"></a>qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.


### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Fehler bei der schrittweisen Vorbereitung des Zustands.



## <a name="output--intdoublequbit--unit-adj--ctl"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL))

Ein Tupel, in dem: `Int` die Anzahl der zugeordneten Qubits ist, `Double` die One-Norm von hamiltona-Koeffizienten ist, und der Vorgang ist der durch die qubisierung erstellte Quantum Walk.