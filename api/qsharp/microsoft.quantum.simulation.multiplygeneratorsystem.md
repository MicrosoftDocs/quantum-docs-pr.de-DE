---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Multiplygeneratorsystem-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: cebd08c86ad8a3793ba7d0e9ce241d7a1ef046ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858496"
---
# <a name="multiplygeneratorsystem-function"></a>Multiplygeneratorsystem-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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