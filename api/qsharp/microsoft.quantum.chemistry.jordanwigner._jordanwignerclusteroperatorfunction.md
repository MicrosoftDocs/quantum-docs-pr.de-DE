---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: _JordanWignerClusterOperatorFunction-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 58b0c7ad2216b1f58b9ea2765494b85fab4e1ff9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703476"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a>_JordanWignerClusterOperatorFunction-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in der jordanwigner-Basis dar.

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a>Eingabe

### <a name="generatorindex--generatorindex"></a>generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Ein Generator Index, der als einheitliche Evolution in der jordanwigner dargestellt werden soll.



## <a name="output--evolutionunitary"></a>Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)

Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.