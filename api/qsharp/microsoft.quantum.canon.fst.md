---
uid: Microsoft.Quantum.Canon.Fst
title: FST-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840518"
---
# <a name="fst-function"></a>FST-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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