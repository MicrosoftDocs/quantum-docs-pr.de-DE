---
uid: Microsoft.Quantum.Arrays.Prefixes
title: Präfixe-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: 1576e57e9dc64a605eb65cb841640e72a3b126ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705823"
---
# <a name="prefixes-function"></a>Präfixe-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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