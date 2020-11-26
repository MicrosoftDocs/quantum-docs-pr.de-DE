---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: Composedoutput-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 7e361a62679ab93e9a0ebc04fa52be193805c78d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207461"
---
# <a name="composedoutput-function"></a>Composedoutput-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die Ausgabe der Komposition von `inner` und `outer` für eine angegebene Eingabe zurück.

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a>Eingabe

### <a name="outer--u---v"></a>Outer: "U->" V




### <a name="inner--t---u"></a>innere: 't-> ' U




### <a name="target--t"></a>Ziel: 't





## <a name="output--v"></a>Ausgabe: "V



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U


### <a name="v"></a>"V

