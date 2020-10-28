---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Htermstogenidx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 73324a48cc4b42de0d5d8618ad9e833d289125f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703560"
---
# <a name="htermstogenidx-function"></a>Htermstogenidx-Funktion

Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)

Paketen [](https://nuget.org/packages/)


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