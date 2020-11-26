---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Htermstogenidx-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: dbe0718fa3b5439a2987d455fdad73731c988678
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216012"
---
# <a name="htermstogenidx-function"></a>Htermstogenidx-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Konvertiert einen Index in einen hamiltona-Begriff im `HTerm[]` Datenformat in einen generatorindex.

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Eingabe

### <a name="data--hterm"></a>Daten: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]

Eingabedaten im- `HTerm[]` Format.


### <a name="termtype--int"></a>Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]

Zusätzliche Informationen, die generatorindex hinzugefügt werden.


### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Index für einen Begriff von hamiltonan



## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `data[idx]` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .