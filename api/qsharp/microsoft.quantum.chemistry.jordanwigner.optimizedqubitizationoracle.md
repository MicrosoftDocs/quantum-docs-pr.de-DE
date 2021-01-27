---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle
title: Optimizedqubitizationoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedQubitizationOracle
qsharp.summary: Returns T-count optimized Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: da569e8ddad575b1ba1bbc2081a6a948cb675d48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837042"
---
# <a name="optimizedqubitizationoracle-function"></a>Optimizedqubitizationoracle-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Gibt einen optimierten qubisierungsvorgang mit T-Anzahl und die für die Ausführung erforderlichen Parameter zurück.

```qsharp
function OptimizedQubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, targetError : Double) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a>Eingabe

### <a name="qsharpdata--jordanwignerencodingdata"></a>qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.


### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Fehler bei der schrittweisen Vorbereitung des Zustands.



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL))

Ein Tupel, in dem: `Int` die Anzahl der zugeordneten Qubits ist, `Double` die One-Norm von hamiltona-Koeffizienten ist, und der Vorgang ist der durch die qubisierung erstellte Quantum Walk.