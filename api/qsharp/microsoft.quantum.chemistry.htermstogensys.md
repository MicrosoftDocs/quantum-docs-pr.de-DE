---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Htermstogensys-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: b78ff393fa1e51c38028ef56bb3c61b8f1d5e478
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703554"
---
# <a name="htermstogensys-function"></a>Htermstogensys-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paketen [](https://nuget.org/packages/)


Konvertiert ein hamiltonan im `HTerm[]` Datenformat in ein Generatorsystem.

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="data--hterm"></a>Daten: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Eingabedaten im- `HTerm[]` Format.


### <a name="termtype--int"></a>Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]

Zusätzliche Informationen, die generatorindex hinzugefügt werden.



## <a name="output--generatorsystem"></a>Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Ein Generatorsystem, das eine von der Eingabe dargestellte hamiltona darstellt `data` .