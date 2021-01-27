---
uid: Microsoft.Quantum.Simulation.IdxToCoeff
title: Idxto coeff-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToCoeff
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: b6523c0d8f3e6d0ac4ec63234a7de342f8d6c065
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857903"
---
# <a name="idxtocoeff-function"></a>Idxto coeff-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wird in der Implementierung von `PauliBlockEncoding`

```qsharp
function IdxToCoeff (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToCoeff : (Microsoft.Quantum.Simulation.GeneratorIndex -> Double)) : Double
```


## <a name="input"></a>Eingabe

### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="genfun--int---generatorindex"></a>genfun: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="genidxtocoeff--generatorindex---double"></a>genidxto coeff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. pauliblockencoding](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)