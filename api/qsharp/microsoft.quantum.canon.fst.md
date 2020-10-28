---
uid: Microsoft.Quantum.Canon.Fst
title: FST-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704178"
---
# <a name="fst-function"></a>FST-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt bei einem Paar das erste Element zurück.

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a>Eingabe

### <a name="pair--tu"></a>paar: ('t, ' U)

Ein Tupel mit zwei Elementen.



## <a name="output--t"></a>Ausgabe: 't

Das erste Element von `pair`.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Members des Paars.
### <a name="u"></a>"U

Der Typ des zweiten Members des Paars.