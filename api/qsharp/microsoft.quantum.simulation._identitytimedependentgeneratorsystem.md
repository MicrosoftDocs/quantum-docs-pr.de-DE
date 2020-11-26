---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: _IdentityTimeDependentGeneratorSystem-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 7b93a6674bec974e61496696a3d8403225b16d80
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225600"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a>_IdentityTimeDependentGeneratorSystem-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein mit der hamiltonan konsistentes Generator System zurück `H(s) = 0` , wobei `s` ein Zeit Plan Parameter ist.

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="schedule--double"></a>Zeitplan: [Double](xref:microsoft.quantum.lang-ref.double)

Diese Eingabe wird ignoriert und wird aus Gründen der Konsistenz mit dem <xref:microsoft.quantum.canon.timedependentgeneratorsystem> benutzerdefinierten Typ definiert.



## <a name="output--generatorsystem"></a>Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Ein Generator System, das die Evolution unter den hamiltonan $H (s) = $0 für alle $s $ darstellt.