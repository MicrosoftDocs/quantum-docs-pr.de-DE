---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: Composedoutput-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 4da66616692055a7d60abbf1fac6e6799806675d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704351"
---
# <a name="composedoutput-function"></a>Composedoutput-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


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

