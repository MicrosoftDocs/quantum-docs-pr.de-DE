---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Drawcategorical-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: fdc5ae3a9341cb11e8fda129bdd030289b6c99c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706719"
---
# <a name="drawcategorical-operation"></a>Drawcategorical-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


Zeichnet eine zufällige Stichprobe aus einer kategorischen Verteilung, die durch eine Liste von Wahrscheinlichkeiten angegeben wird.

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a>BESCHREIBUNG

Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index.
Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben. Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.

## <a name="input"></a>Eingabe

### <a name="probs--double"></a>probs: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Gleit Komma Zahlen proportional zu der Wahrscheinlichkeit, dass die einzelnen Indizes ausgewählt werden.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl $i $ mit der Wahrscheinlichkeitswert $ \pr (i) = p_i/\ sum_i p_i $, wobei $p _I $ das $i $ th-Element von ist `probs` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Random. kategoricaldistribution](xref:Microsoft.Quantum.Random.CategoricalDistribution)