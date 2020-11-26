---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: Sumgeneratorsystems-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 7cb18e161dce3a52d7c9a0bf6a45d4818db2b849
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192467"
---
# <a name="sumgeneratorsystems-function"></a>Sumgeneratorsystems-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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