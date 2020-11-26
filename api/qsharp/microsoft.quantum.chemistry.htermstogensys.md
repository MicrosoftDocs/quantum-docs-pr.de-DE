---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: Htermstogensys-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: 936e1bcc58b2f1af3bdb606884128c38d2f58867
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204112"
---
# <a name="htermstogensys-function"></a>Htermstogensys-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


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