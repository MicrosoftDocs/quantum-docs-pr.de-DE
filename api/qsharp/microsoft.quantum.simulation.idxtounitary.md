---
uid: Microsoft.Quantum.Simulation.IdxToUnitary
title: Idx| einheitliche-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToUnitary
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: ceba7cdb02a2ed8bf280f1b300d881eec1323b38
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858112"
---
# <a name="idxtounitary-function"></a>Idx| einheitliche-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wird in der Implementierung von `PauliBlockEncoding`

```qsharp
function IdxToUnitary (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToUnitary : (Microsoft.Quantum.Simulation.GeneratorIndex -> (Qubit[] => Unit is Adj + Ctl))) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="genfun--int---generatorindex"></a>genfun: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="genidxtounitary--generatorindex---qubit--unit--is-adj--ctl"></a>genidxdeeinheitlicher: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) - -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL





## <a name="output--qubit--unit--is-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. pauliblockencoding](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)