---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Präfixe-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 3501c11437534b1623bffba272a4517487e5634a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220387"
---
# <a name="prefixes-function"></a>Präfixe-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei Angabe eines Arrays alle zugehörigen Präfixe zurück.

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a>BESCHREIBUNG

Gibt ein Array aller Präfixe zurück, beginnend mit einem Array, das nur das erste Element bis zum vollständigen Array enthält.

## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen.



## <a name="output--t"></a>Ausgabe: 't [] []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.