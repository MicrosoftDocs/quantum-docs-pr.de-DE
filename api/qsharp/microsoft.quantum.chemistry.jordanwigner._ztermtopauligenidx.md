---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliGenIdx
title: _ZTermToPauliGenIdx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 1569ec742778549b8754cdca8b2d9872310e8976
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703271"
---
# <a name="_ztermtopauligenidx-function"></a>_ZTermToPauliGenIdx-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paketen [](https://nuget.org/packages/)


Konvertiert einen generatorindex, der einen Z-Begriff beschreibt, in den Ausdruck ' generatorindex [] ' in Bezug auf Paulis.

```qsharp
function _ZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a>Eingabe

### <a name="term--generatorindex"></a>Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` , der einen Z-Begriff darstellt.



## <a name="output--generatorindex"></a>Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]

' Generatorindex [] ' ausgedrückt: Z-Begriff als Pauli-Begriffe.