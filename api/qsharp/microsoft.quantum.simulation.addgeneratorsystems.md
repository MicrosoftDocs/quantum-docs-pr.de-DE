---
uid: Microsoft.Quantum.Simulation.AddGeneratorSystems
title: Addgeneratorsystems-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: 494037aa7635cccf25978bea9339ecc7aee75142
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701754"
---
# <a name="addgeneratorsystems-function"></a>Addgeneratorsystems-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Fügt zwei `GeneratorSystem` s hinzu, um einen neuen zu erstellen `GeneratorSystem` .

```qsharp
function AddGeneratorSystems (generatorSystemA : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemB : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="generatorsystema--generatorsystem"></a>generatorsystema: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Die erste `GeneratorSystem`.


### <a name="generatorsystemb--generatorsystem"></a>generatorsystemb: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Das zweite `GeneratorSystem`.



## <a name="output--generatorsystem"></a>Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Ein `GeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme darstellt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)