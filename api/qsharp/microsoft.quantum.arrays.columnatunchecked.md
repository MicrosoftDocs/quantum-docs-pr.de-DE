---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Columnatdeaktiviert-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 17211c1ae1fe12fcadf34a9411f9b0cf0cdcab50
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706162"
---
# <a name="columnatunchecked-function"></a>Columnatdeaktiviert-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Diese Funktion prüft nicht die Form "Matrix".

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion kann in anderen mehrdimensionalen Funktionen verwendet werden, die die Eingabe Matrix bereits auf eine gültige rechteckige Form überprüft haben.

## <a name="input"></a>Eingabe

### <a name="column--int"></a>Spalte: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="matrix--t"></a>Matrix: 't [] []





## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF
