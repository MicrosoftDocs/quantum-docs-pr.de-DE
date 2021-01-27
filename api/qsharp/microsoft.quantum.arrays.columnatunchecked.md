---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Columnatdeaktiviert-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 4f4631bb49f769816a3df772f7b2f346c8ccfc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842860"
---
# <a name="columnatunchecked-function"></a>Columnatdeaktiviert-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Diese Funktion prüft nicht die Form "Matrix".

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Beschreibung

Diese Funktion kann in anderen mehrdimensionalen Funktionen verwendet werden, die die Eingabe Matrix bereits auf eine gültige rechteckige Form überprüft haben.

## <a name="input"></a>Eingabe

### <a name="column--int"></a>Spalte: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="matrix--t"></a>Matrix: 't [] []





## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

