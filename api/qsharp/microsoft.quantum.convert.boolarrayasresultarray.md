---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Boolarrayasresultarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: b30da07272ee1a6c19ae13afa618ba5deb7aaa2d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834192"
---
# <a name="boolarrayasresultarray-function"></a>Boolarrayasresultarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert einen `Bool[]` Typ in einen `Result[]` -Typ, wobei `true` zugeordnet ist `One` und `false` zugeordnet ist `Zero` .

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a>Eingabe

### <a name="input--bool"></a>Eingabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

`Bool[]` , das konvertiert werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__[]

Die `Result[]`, die das `input` darstellt.