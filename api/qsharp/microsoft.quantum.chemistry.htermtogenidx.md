---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Htermabgenidx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703553"
---
# <a name="htermtogenidx-function"></a>Htermabgenidx-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paketen [](https://nuget.org/packages/)


Konvertiert einen hamiltona-Begriff im `HTerm` Datenformat in einen generatorindex.

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Eingabe

### <a name="term--hterm"></a>Begriff: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)

Eingabedaten im- `HTerm` Format.


### <a name="termtype--int"></a>Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]

Zusätzliche Informationen, die generatorindex hinzugefügt werden.



## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `term` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .