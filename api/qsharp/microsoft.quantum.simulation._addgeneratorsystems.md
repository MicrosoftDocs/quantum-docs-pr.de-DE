---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: _AddGeneratorSystems-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: e51addb38da99e508a71dffa757cd7fb19c89dcd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858005"
---
# <a name="_addgeneratorsystems-function"></a>_AddGeneratorSystems-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Fügt zwei `GeneratorSystem` s hinzu, um einen neuen zu erstellen `GeneratorSystem` .

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Eingabe

### <a name="idxterm--int"></a>idxterm: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="ntermsa--int"></a>ntermsa: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="ntermsb--int"></a>ntermsb: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="generatorindexfunctiona--int---generatorindex"></a>generatorindexfunctiona: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="generatorindexfunctionb--int---generatorindex"></a>generatorindexfunctionb: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)





## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)



## <a name="remarks"></a>Bemerkungen

Dies ist ein Zwischenschritt und sollte nicht aufgerufen werden.