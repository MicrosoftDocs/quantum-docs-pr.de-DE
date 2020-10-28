---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Multiplygeneratorsystem-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: 1d28de99dab3f7aca4bf3706fe98f5ef7c5286a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706687"
---
# <a name="multiplygeneratorsystem-function"></a>Multiplygeneratorsystem-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Multipliziert den Koeffizient aller Begriffe in einem `GeneratorSystem` .

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="multiplier--double"></a>Multiplikator: [Double](xref:microsoft.quantum.lang-ref.double)

Der Multiplikator des Koeffizienten.


### <a name="generatorsystem--generatorsystem"></a>Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Die zu multiplizierende `GeneratorSystem`.



## <a name="output--generatorsystem"></a>Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Ein, das `GeneratorSystem` ein System mit Koeffizienten darstellt, das `multiplier` größer ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)