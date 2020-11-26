---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Interpolategeneratorsystems-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230581"
---
# <a name="interpolategeneratorsystems-function"></a>Interpolategeneratorsystems-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen zurück, `TimeDependentGeneratorSystem` der die lineare interpolung zwischen zwei `GeneratorSystem` n darstellt.

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="generatorsystemstart--generatorsystem"></a>generatorsystemstart: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Der Start `GeneratorSystem` .


### <a name="generatorsystemend--generatorsystem"></a>generatorsystemend: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Das Ende `GeneratorSystem` .



## <a name="output--timedependentgeneratorsystem"></a>Ausgabe: [timedependentgeneratorsystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)

Ein `TimeDependentGeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme ist, mit der Gewichtung $ (1-s) $ on `generatorSystemStart` und Weight $s $ on `generatorSystemEnd` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [Microsoft. Quantum. Simulation. timedependentgeneratorsystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)