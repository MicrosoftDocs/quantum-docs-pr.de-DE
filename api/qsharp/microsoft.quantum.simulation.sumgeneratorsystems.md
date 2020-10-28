---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: Sumgeneratorsystems-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: b667a6af313b5bb8950a34a6d0406976bde49311
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706450"
---
# <a name="sumgeneratorsystems-function"></a>Sumgeneratorsystems-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Fügt mehrere `GeneratorSystem` s hinzu, um ein neues Generatorsystem zu erstellen.

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="generatorsystems--generatorsystem"></a>Generatorsystems: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]

Ein Array vom Typ `GeneratorSystem[]`.



## <a name="output--generatorsystem"></a>Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Ein `GeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme darstellt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)