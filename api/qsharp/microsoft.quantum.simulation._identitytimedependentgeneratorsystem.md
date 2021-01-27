---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: _IdentityTimeDependentGeneratorSystem-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 960842f50353c01362f90eb38d979fb7c4f15d9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857982"
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